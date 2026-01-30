erDiagram
    USER ||--o{ COMPLAINT : raises
    LOCATION ||--o{ COMPLAINT : occurs_at
    TECHNICIAN ||--o{ COMPLAINT : resolves

    USER {
        int user_id PK
        string name
        string role
        string department
        string phone
        string email
    }

    LOCATION {
        int location_id PK
        string building
        int floor
        string room
        string network_type
    }

    COMPLAINT {
        int complaint_id PK
        string complaint_type
        string description
        string status
        string priority
        date complaint_date
        int user_id FK
        int location_id FK
        int technician_id FK
    }

    TECHNICIAN {
        int technician_id PK
        string name
        string phone
        string email
    }
