---
title: Trust-Attributes atributo)
description: Este atributo almacena los atributos de confianza de un dominio de confianza.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Trust-Attributes
- trustAttributes esquema de AD de atributos
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804813"
---
# <a name="trust-attributes-attribute"></a>Trust-Attributes atributo)

Este atributo almacena los atributos de confianza de un dominio de confianza. Los posibles valores de atributo son los siguientes:

-   \_Atributo de \_ confianza \_ deshabilitar transitividad.
-   \_ \_ La confianza principal del árbol de atributos de confianza \_ está establecida en el árbol primario de la organización.
-   Confianza \_ \_ \_ raíz del árbol de atributos de confianza establecida en otra raíz de árbol del bosque.
-   \_Nivel de atributo de confianza \_ \_ : solo un vínculo de confianza válido solo para el cliente de nivel superior.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| Nombre para mostrar de LDAP | trustAttributes                      |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-ID-GUID    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





