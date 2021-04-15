---
title: Atributo NT-Security-Descriptor
description: Descriptor de seguridad de Windows NT para el objeto de esquema. Un descriptor de seguridad es una estructura de datos que contiene información de seguridad sobre un objeto, como la propiedad y los permisos del objeto.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo NT-Security-Descriptor
- atributo nTSecurityDescriptor esquema de AD
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e951e28ce97b04380609774baf57e4c6bf8c545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535932"
---
# <a name="nt-security-descriptor-attribute"></a>Atributo NT-Security-Descriptor

Descriptor de seguridad de Windows NT para el objeto de esquema. Un descriptor de seguridad es una estructura de datos que contiene información de seguridad sobre un objeto, como la propiedad y los permisos del objeto.

Para obtener información sobre el formato de este valor, vea [formato de cadena de descriptor de seguridad (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Entrada | Value |
|-------------------|-----------------------------------------------------|
| CN                | Descriptor de NT-Security-                              |
| Nombre para mostrar de LDAP | nTSecurityDescriptor                                |
| Tamaño              | \-                                                  |
| Actualizar privilegio  | \-                                                  |
| Frecuencia de actualización  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-ID-GUID    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Sintaxis            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                               |
| Está indexado             | False                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                               |
| Está indexado             | False                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | False                                                                                        |
| Tiene un único valor       | True                                                                                         |
| Está indexado             | False                                                                                        |
| En el catálogo global      | True                                                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                               |
| Está indexado             | False                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                               |
| Está indexado             | False                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                               |
| Está indexado             | False                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                               |
| Está indexado             | False                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



 

 





