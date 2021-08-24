---
title: Atributo Well-Known-Objects
description: Este atributo contiene una lista de contenedores de objetos conocidos por GUID y nombre distintivo.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Well-Known-Objects
- Esquema de AD del atributo wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5417b35ef821b1d84377c39eb4408eea57cf0dcc901ae0728a50ba48b88d6779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702415"
---
# <a name="well-known-objects-attribute"></a>Atributo Well-Known-Objects

Este atributo contiene una lista de contenedores de objetos conocidos por GUID y nombre distintivo. Los objetos conocidos son contenedores del sistema. Esta información se usa para recuperar un objeto después de que se haya movido usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente la parte Nombre distintivo de los valores Well-Known-Objects que hacían referencia al objeto. El archivo Ntdsapi.h contiene las definiciones siguientes, que se pueden usar para recuperar un objeto (los GUID asociados a estos objetos se encuentran en Ntdsapi.h):

-   CONTENEDOR DE \_ USUARIOS \_ GUID \_ W
-   CONTENEDOR \_ DE COMPUTRS \_ GUID \_ W
-   CONTENEDOR DE \_ SISTEMAS \_ GUID \_ W
-   CONTENEDOR DE \_ CONTROLADORES DE DOMINIO GUID \_ \_ \_ W
-   CONTENEDOR DE \_ INFRAESTRUCTURA \_ DE GUID \_ W
-   CONTENEDOR DE \_ OBJETOS \_ \_ ELIMINADOS \_ GUID W
-   GUID \_ LOSTANDFOUND \_ CONTAINER \_ W
-   GUID \_ FOREIGNSECURITYPRINCIPALS \_ CONTAINER \_ W
-   CONTENEDOR DE \_ DATOS DEL PROGRAMA GUID \_ \_ \_ W
-   GUID \_ DEL CONTENEDOR DE DATOS DEL PROGRAMA DE MICROSOFT \_ \_ \_ \_ W
-   GUID \_ NTDS \_ QUOTAS \_ CONTAINER \_ W



| Entrada | Valor |
|-------------------|-------------------------------------------------|
| CN                | Objetos conocidos                              |
| Ldap-Display-Name | wellKnownObjects                                |
| Size              | \-                                              |
| Actualizar privilegios  | El sistema establece este valor.                |
| Frecuencia de actualización  | Siempre que se mueve uno de los contenedores del sistema. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-Id-Guid    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





