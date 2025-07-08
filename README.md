# Design Patterns - Proyecto de Gestión de Automóviles

Este proyecto es una aplicación web basada en Razor Pages (.NET 8) que ejemplifica la aplicación de patrones de diseño en el desarrollo de software, específicamente en la gestión de vehículos para la empresa "Codificando Con Patrones Cía. Ltda.".

## Descripción General

El objetivo principal es construir una solución flexible y extensible que permita gestionar diferentes modelos de automóviles, facilitando la incorporación de nuevos requerimientos y modelos en el futuro. Para ello, se han implementado varios patrones de diseño reconocidos en la industria.

---

## Estado de los Requisitos

### 1. **Agregar vehículos (Mustang y Explorer) en el Home Page**
- **Estado:** - Implementado
- **Detalle:**  
  Se han implementado métodos y enlaces en la página principal que permiten agregar vehículos de los modelos Mustang y Explorer. Los usuarios pueden agregar estos vehículos directamente desde la interfaz principal, y la lógica correspondiente está conectada al repositorio de vehículos.

### 2. **Repositorio en memoria (sin base de datos)**
- **Estado:** - Implementado
- **Detalle:**  
  Dado que el esquema de la base de datos aún no está listo, se utiliza un repositorio en memoria (`MyVehiclesRepository`). Esto permite probar y validar toda la funcionalidad de la aplicación sin depender de una base de datos real, facilitando el desarrollo y las pruebas.

### 3. **Propiedades por defecto y año actual con patrón de diseño**
- **Estado:** - Implementado
- **Detalle:**  
  Se utiliza el patrón **Builder** para la creación de vehículos, lo que permite inicializarlos con propiedades por defecto, incluyendo el año actual. Este patrón facilita la extensión futura para agregar más propiedades sin modificar el código existente, cumpliendo así con la solicitud del equipo de negocio.

### 4. **Factory Method para nuevos modelos (ejemplo: Escape)**
- **Estado:** - Implementado
- **Detalle:**  
  Se implementó el patrón **Factory Method** para la creación de vehículos. Existen fábricas concretas para los modelos Mustang, Explorer y Escape (por ejemplo, `FordEscapeFactory`). Esto permite agregar fácilmente nuevos modelos en el futuro, siguiendo el principio de abierto/cerrado.

### 5. **Agregar 20 propiedades adicionales por defecto**
- **Estado:** - Implementado
- **Detalle:**  
  El patrón Builder ya está preparado para facilitar la adición de 20 propiedades adicionales por defecto en los vehículos, tal como lo requiere el negocio para el siguiente sprint. La estructura del código permite incorporar estas propiedades de manera sencilla y sin afectar la lógica existente.

---

## Resumen de Patrones de Diseño Utilizados

- **Repository Pattern:** Abstrae el acceso a los datos de los vehículos, permitiendo cambiar la fuente de datos (memoria o base de datos) sin afectar la lógica de negocio.
- **Builder Pattern:** Facilita la creación de objetos complejos (vehículos) con propiedades por defecto y futuras extensiones.
- **Factory Method Pattern:** Permite la creación de diferentes modelos de vehículos de manera flexible y escalable.

---

## Consideraciones Finales

La solución está diseñada para ser fácilmente extensible y mantenible, permitiendo la incorporación de nuevos modelos y propiedades sin grandes refactorizaciones. El uso de patrones de diseño asegura que el código sea robusto, limpio y preparado para cambios futuros.

---
