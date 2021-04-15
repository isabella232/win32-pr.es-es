---
title: Atributo Well-Known-Objects
description: Este atributo contiene una lista de contenedores de objetos conocidos por GUID y nombre distintivo.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Well-know-Attributes Schema AD Schema
- wellKnownObjects esquema de AD de atributos
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493900"
---
# <a name="well-known-objects-attribute"></a>Atributo Well-Known-Objects

Este atributo contiene una lista de contenedores de objetos conocidos por GUID y nombre distintivo. Los objetos conocidos son contenedores del sistema. Esta información se usa para recuperar un objeto una vez que se ha colocado usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente la parte del nombre distintivo de los valores de objetos conocidos que hacía referencia al objeto. El archivo ntdsapi. h contiene las siguientes definiciones, que se pueden usar para recuperar un objeto (los GUID que están asociados a estos objetos están contenidos en ntdsapi. h):

-   contenedor de usuarios de GUID \_ \_ \_ W
-   \_contenedor de calculadores GUID \_ \_ W
-   \_contenedor de sistemas GUID \_ \_ W
-   \_contenedor de controladores de dominio GUID \_ \_ \_ W
-   \_contenedor de infraestructura GUID \_ \_ W
-   \_contenedor de objetos eliminados de GUID \_ \_ \_ W
-   contenedor de GUID \_ LOSTANDFOUND \_ \_ W
-   GUID \_ FOREIGNSECURITYPRINCIPALS \_ contenedor \_ W
-   \_contenedor de datos de programa GUID \_ \_ \_ W
-   GUID de \_ Microsoft \_ Program \_ Data \_ Container \_ W
-   \_contenedor de cuotas de NTDS GUID \_ \_ \_ W



| Entrada | Value |
|-------------------|-------------------------------------------------|
| CN                | Well-Known-Objects                              |
| Nombre para mostrar de LDAP | wellKnownObjects                                |
| Tamaño              | \-                                              |
| Actualizar privilegio  | El sistema establece este valor.                |
| Frecuencia de actualización  | Siempre que se mueva uno de los contenedores del sistema. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-ID-GUID    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Sintaxis            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





