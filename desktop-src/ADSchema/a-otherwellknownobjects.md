---
title: Otro atributo de objetos conocidos
description: Contiene una lista de contenedores por GUID y nombre distintivo. Esto permite recuperar un objeto una vez que se ha desusado usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente el nombre distintivo.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- 'Otro: esquema de AD de atributos de objetos conocidos'
- otherWellKnownObjects esquema de AD de atributos
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493954"
---
# <a name="other-well-known-objects-attribute"></a>Otro atributo de objetos conocidos

Contiene una lista de contenedores por GUID y nombre distintivo. Esto permite recuperar un objeto una vez que se ha desusado usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente el nombre distintivo.



| Entrada | Value |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Otros objetos conocidos                                                                                                                                                                                      |
| Nombre para mostrar de LDAP | otherWellKnownObjects                                                                                                                                                                                         |
| Tamaño              | Ejemplo para recuperar el contenedor de usuarios en el dominio de Microsoft: LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com). Nota: los corchetes angulares se sustituyen por paréntesis para evitar conflictos XML. |
| Actualizar privilegio  | Administrador de esquema                                                                                                                                                                                          |
| Frecuencia de actualización  | Cada vez que se mueve el objeto.                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| System-ID-GUID    | 1ea64e5d-ac0f-11d2-90df-00c04fd91ab1                                                                                                                                                                          |
| Sintaxis            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                               |



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
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





