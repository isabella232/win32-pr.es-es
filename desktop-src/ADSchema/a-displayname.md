---
title: Display-Name atributo)
description: Nombre para mostrar de un objeto.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Display-Name
- atributo displayName esquema de AD
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4fe662ccbdf2157c7ed51a311739cf7d16273b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804345"
---
# <a name="display-name-attribute"></a>Display-Name atributo)

Nombre para mostrar de un objeto. Suele ser la combinación de los nombres de usuario, inicial y apellido.



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| Nombre para mostrar de LDAP | DisplayName                                                                  |
| Tamaño              | \-                                                                           |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                       |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cuando es necesario cambiar el nombre para mostrar. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-ID-GUID    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                             |
| Está indexado             | True                                                                                                                                                                                                                                                                                                                                             |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Dirección: plantilla**](c-addresstemplate.md)<br/> [**PKI-Certificate-template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Dirección: plantilla**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Tiene un único valor       | True                            |
| Está indexado             | True                            |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Dirección: plantilla**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Dirección: plantilla**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Dirección: plantilla**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Dirección: plantilla**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



 

 





