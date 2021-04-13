---
title: Schema-Info atributo)
description: Un valor binario interno que se usa para detectar los cambios de esquema entre controladores de archivos y forzar un ciclo de replicación de NC de esquema antes de replicar cualquier otro NC. Se utiliza para resolver los lazos cuando se asumi el esquema FSMO y se realiza un cambio en más de un controlador de dominio.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Schema-Info
- schemaInfo esquema de AD de atributos
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536166"
---
# <a name="schema-info-attribute"></a>Schema-Info atributo)

Un valor binario interno que se usa para detectar los cambios de esquema entre controladores de archivos y forzar un ciclo de replicación de NC de esquema antes de replicar cualquier otro NC. Se utiliza para resolver los lazos cuando se asumi el esquema FSMO y se realiza un cambio en más de un controlador de dominio.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| Nombre para mostrar de LDAP | schemaInfo                                            |
| Tamaño              | \-                                                    |
| Actualizar privilegio  | El sistema establece este valor.                      |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-ID-GUID    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**DMD**](c-dmd.md)<br/> |



 

 





