# test-curso
```mermaid
classDiagram
    class Persona {
        -String nombre
        -String comuna
        -double latitud
        -double longitud
        +getNombre() String
        +getComuna() String
        +getLatitud() double
        +getLongitud() double
        +toString() String
    }

    class LocalVotacion {
        -String nombre
        -String comuna
        -double latitud
        -double longitud
        +getNombre() String
        +getComuna() String
        +getLatitud() double
        +getLongitud() double
        +toString() String
    }

    class AsignadorLocales {
        -List~LocalVotacion~ locales
        -List~Persona~ personas
        +calcularDistanciaHaversine(lat1, lon1, lat2, lon2) double
        +asignarLocalesMasCercanos()
        +mostrarAsignaciones()
    }

    Persona ||--o{ AsignadorLocales : usa
    LocalVotacion ||--o{ AsignadorLocales : procesa
```
