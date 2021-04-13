---
title: 'Entry: atributo TTL'
description: Este atributo operativo es mantenido por el servidor y parece estar presente en cada entrada dinámica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Entry-TTL atributo AD Schema
- entryTTL esquema de AD de atributos
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493534"
---
# <a name="entry-ttl-attribute"></a>Entry: atributo TTL

Este atributo operativo es mantenido por el servidor y parece estar presente en cada entrada dinámica. El atributo no está presente cuando la entrada no contiene la clase de objeto dynamicObject. El valor de este atributo es el tiempo, en segundos, que la entrada seguirá existiendo antes de que se desaparezca del directorio. En ausencia de operaciones de "actualización" intermedias, se garantiza que los valores devueltos al leer el atributo en dos búsquedas sucesivas no están en aumento. El valor mínimo permitido es 0, lo que indica que la entrada puede desaparecer sin ninguna advertencia. El atributo está marcado como NO MODIFICAble por el usuario porque solo se puede cambiar mediante la operación de actualización.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Entrada: TTL                                   |
| Nombre para mostrar de LDAP | entryTTL                                    |
| Tamaño              | 4 bytes. Máximo = 1 año, valor predeterminado = 1 día. |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-ID-GUID    | d213decc-d81a-4384-AAC2-dcfcfd631cf8        |
| Sintaxis            | [**Enumeración**](s-enumeration.md)        |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Objeto dinámico**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Objeto dinámico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Objeto dinámico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Objeto dinámico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Objeto dinámico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Objeto dinámico**](c-dynamicobject.md)<br/> |



 

 





