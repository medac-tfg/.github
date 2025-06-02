# 🛒 CartX - Sistema de Checkout Automático con RFID

<div align="center">

![CartX Logo](/cartx.png)

**Trabajo de Fin de Grado - DAM (Desarrollo de Aplicaciones Multiplataforma)**  
**MEDAC Davante Elche | Curso 2023-2025**

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactnative.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Electron](https://img.shields.io/badge/Electron-191970?style=for-the-badge&logo=Electron&logoColor=white)](https://www.electronjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)

</div>

---

## 🚀 Introducción

CartX es un **sistema revolucionario de checkout automático** que sustituye las tradicionales cajas de autoservicio por un innovador portón inteligente equipado con tecnología RFID. Los clientes simplemente pasan con su carrito a través del sistema y todos los productos son detectados automáticamente, eliminando la necesidad de escanear manualmente cada artículo.

> **⚠️ Estado del Proyecto:** Work in Progress (WIP)  
> MEDAC priorizó el enfoque del TFG en el proyecto de empresa y no en el desarrollo del software (una pena...), por lo que el código nunca se llegó a terminar.

Este proyecto ha sido creado por [Cristian Olivares (visibait)](visibait.com), Alberto Rodríguez, Carlos Cremades y Fernando Luján.

## 🎯 Características Principales

<div style="width: 100%">

<table style="width: 100%;">
<tr>
<td style="width: 50%; vertical-align: top;">

### 🔍 **Detección Automática RFID**

- Identificación instantánea de productos
- Sin necesidad de escaneo manual
- Tecnología de vanguardia en retail

### 💳 **Procesamiento de Pagos**

- Integración con múltiples métodos de pago
- Transacciones seguras y rápidas
- Interfaz intuitiva para el cliente

</td>
<td style="width: 50%; vertical-align: top;">

### 📱 **Gestión de Inventario**

- App móvil para reponedores
- Vinculación códigos de barras - RFID
- Métricas en tiempo real

### 🖥️ **Sistema Dual-Screen**

- Interfaz para cliente y operador
- Experiencia de usuario optimizada
- Soporte multi-idioma

</td>
</tr>
</table>

</div>

---

## 🏗️ Arquitectura del Sistema

```mermaid
graph TB
    A[🛒 Cliente con Carrito] --> B[🚪 Portón RFID CartXUI]
    B --> C[☁️ CartXCloud Backend]
    C --> D[📱 CartXStockerApp]
    C --> E[💾 MongoDB Database]

    B --> F[💳 Sistema de Pagos]
    B --> G[🖥️ Pantalla Dual]

    D --> H[📦 Gestión Inventario]
    D --> I[📊 Métricas Tienda]

    style A fill:#e1f5fe
    style B fill:#f3e5f5
    style C fill:#e8f5e8
    style D fill:#fff3e0
```

---

## 📦 Repositorios del Proyecto

<div align="center">

| Repositorio                                                         | Descripción                              | Tecnologías                             | Estado |
| ------------------------------------------------------------------- | ---------------------------------------- | --------------------------------------- | ------ |
| **[CartXCloud](https://github.com/medac-tfg/CartXCloud)**           | 🌐 Backend principal del sistema         | Node.js, TypeScript, MongoDB, Socket.IO | 🟡 WIP |
| **[CartXUI](https://github.com/medac-tfg/CartXUI)**                 | 🖥️ Sistema del portón con doble pantalla | Electron, React, TypeScript, TensorFlow | 🟡 WIP |
| **[CartXStockerApp](https://github.com/medac-tfg/CartXStockerApp)** | 📱 App móvil para reponedores            | React Native, Expo, TypeScript          | 🟡 WIP |

</div>

---

## 🛠️ Stack Tecnológico

<div align="center">

### Backend & Database

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white)

### Frontend & Mobile

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Electron](https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)

### AI & Hardware

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![RFID](https://img.shields.io/badge/RFID-FF6B35?style=flat-square&logo=nfc&logoColor=white)

</div>

---

## 🎬 Demo del Sistema

<div align="center">

_Aquí próximamente aparecerá un video conceptual del sistema CartX en funcionamiento_

</div>

### 🔄 Flujo de Usuario

1. **🚶‍♂️ Entrada:** El cliente se acerca al portón con su carrito/cesta o con los productos en la mano
2. **🔍 Detección:** Los sensores RFID identifican automáticamente todos los productos
3. **📊 Procesamiento:** El sistema calcula el total y muestra los artículos en pantalla
4. **💳 Pago:** El cliente selecciona su método de pago preferido
5. **✅ Salida:** Transacción completada, el cliente puede marcharse

---

## 📈 Características Técnicas Destacadas

<div align="center">

| Característica              | Descripción                                 | Beneficio                                  |
| --------------------------- | ------------------------------------------- | ------------------------------------------ |
| **🔄 Real-time Updates**    | Socket.IO para actualizaciones instantáneas | Sincronización perfecta entre dispositivos |
| **🎯 Multi-tenant**         | Soporte para múltiples tiendas              | Escalabilidad empresarial                  |
| **🔒 Precisión Financiera** | Biblioteca big.js para cálculos exactos     | Eliminación de errores de redondeo         |
| **🌐 Multi-idioma**         | Soporte para 6 idiomas                      | Accesibilidad global                       |
| **🤖 IA Integrada**         | TensorFlow para detección de presencia      | Experiencia de usuario inteligente         |

</div>

---

## 🎓 Contexto Académico

<div align="center">

### 📚 **Trabajo de Fin de Grado**

**Grado Superior en Desarrollo de Aplicaciones Multiplataforma (DAM)**

🏫 **Centro:** MEDAC Davante Elche  
📅 **Período:** 2023-2025  
🎯 **Objetivo:** Desarrollar un sistema completo de retail automatizado

</div>

---

## 📄 Licencia

Este proyecto no se puede redistribuir ni modificar bajo ningún concepto. Los derechos del código pertenecen única y exclusivamente a [Cristian Olivares Canales (visibait)](visibait.com).

---

<div align="center">

**⭐ Si te gusta este proyecto, ¡dale una estrella! ⭐**

</div>
