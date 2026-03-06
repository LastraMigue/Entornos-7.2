# Entornos-7.2 - CASOS DE USO

## Ej 1: El Sistema de Iluminación Inteligente
**Contexto:** Queremos modelar una aplicación móvil sencilla para controlar las luces de una casa.

* **Actores:** Un **Usuario**.
* **Funcionalidades:** El usuario debe poder "Encender luces" y "Apagar luces".
* **Reto:** Representar la interacción básica actor-sistema.

```mermaid
graph LR

%% Actores
Usuario((Usuario))

%% Límite del Sistema
subgraph "El Sistema de Iluminación"
   
    CU1([Encender luces])
    CU2([Apagar luces])
end

%% Relaciones actor-casos de uso
Usuario --- CU1
Usuario --- CU2
```

---

## Ej 2: Gestión de Tienda Online
**Contexto:** Un sistema de comercio electrónico donde interactúan diferentes perfiles.

* **Actores: Cliente** y **Administrador**.
* **Funcionalidades:**
   * El **Cliente** puede "Comprar Producto".
   * El **Administrador** puede "Gestionar Stock".
* **Relaciones Especiales:** Al "Comprar Producto", el sistema permite de forma opcional "Aplicar Cupón Descuento" (si el cliente tiene uno).
* **Reto:** Aplicar correctamente la relación de extensión (<<extend>>).

```mermaid
graph LR

%% Actores
Cliente((Cliente))
Admin((Administrador))

%% Casos de Uso
subgraph "Gestión de Tienda Online"
CU1([Comprar Producto])
CU2([Aplicar Cupón Descuento])
CU3([Gestionar Stock])

%% Relación de Extensión
CU2 -.->|&lt;&lt;extend&gt;&gt;| CU1
end

%% Relaciones de los Actores
Cliente --- CU1
Admin --- CU3
```

---

