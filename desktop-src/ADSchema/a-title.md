---
title: Atributo title
description: Contiene el puesto de trabajo del usuario. Esta propiedad se utiliza normalmente para indicar el puesto de trabajo formal, como Programador Senior, en lugar de la clase ocupacional, como programador. Normalmente no se utiliza para los títulos de sufijo como Esq. o DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Atributo de título esquema de AD
- atributo de título esquema de AD
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbb4dae862db9fc363b22647bd5e56a98e9e60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906098"
---
# <a name="title-attribute-ad-schema"></a>Title (atributo) (esquema de AD)

Contiene el puesto de trabajo del usuario. Esta propiedad se utiliza normalmente para indicar el puesto de trabajo formal, como Programador Senior, en lugar de la clase ocupacional, como programador. Normalmente no se utiliza para los títulos de sufijo como Esq. o DDS.



| Entrada | Value |
|-------------------|---------------------------------------------------------------------------|
| CN                | Title                                                                     |
| Nombre para mostrar de LDAP | title                                                                     |
| Tamaño              | \-                                                                        |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                    |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar el título. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-ID-GUID    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Tiene un único valor       | True                                                                                                                            |
| Está indexado             | False                                                                                                                           |
| En el catálogo global      | False                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Tiene un único valor       | True                                                                                                                            |
| Está indexado             | False                                                                                                                           |
| En el catálogo global      | False                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Tiene un único valor       | True                                                                                                                            |
| Está indexado             | False                                                                                                                           |
| En el catálogo global      | False                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Tiene un único valor       | True                                                                                                                            |
| Está indexado             | False                                                                                                                           |
| En el catálogo global      | False                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Tiene un único valor       | True                                                                                                                            |
| Está indexado             | False                                                                                                                           |
| En el catálogo global      | False                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Tiene un único valor       | True                                                                                                                            |
| Está indexado             | False                                                                                                                           |
| En el catálogo global      | False                                                                                                                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



 

 





