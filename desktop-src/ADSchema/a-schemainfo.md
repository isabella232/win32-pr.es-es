---
title: Schema-Info atributo
description: Valor binario interno que se usa para detectar cambios de esquema entre los DCs y forzar un ciclo de replicación de NC de esquema antes de replicar cualquier otra NC. Se usa para resolver los lazos cuando se toma el esquema FSMO y se realiza un cambio en más de un controlador de dominio.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schema-Info esquema de AD de atributo
- Esquema de AD del atributo schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa0d55dd29f207b84b0951ee448ba988d128fabfd126f38b2a4692d7cd3e0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646536"
---
# <a name="schema-info-attribute"></a>Schema-Info atributo

Valor binario interno que se usa para detectar cambios de esquema entre los DCs y forzar un ciclo de replicación de NC de esquema antes de replicar cualquier otra NC. Se usa para resolver los lazos cuando se toma el esquema FSMO y se realiza un cambio en más de un controlador de dominio.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| Ldap-Display-Name | schemaInfo                                            |
| Size              | \-                                                    |
| Actualizar privilegios  | El sistema establece este valor.                      |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-Id-Guid    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Dmd**](c-dmd.md)<br/> |



 

 





