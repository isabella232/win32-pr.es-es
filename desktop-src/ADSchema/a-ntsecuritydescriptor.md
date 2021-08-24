---
title: Atributo NT-Security-Descriptor
description: Descriptor Windows de seguridad NT para el objeto de esquema. Un descriptor de seguridad es una estructura de datos que contiene información de seguridad sobre un objeto, como la propiedad y los permisos del objeto.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo NT-Security-Descriptor
- nTSecurityDescriptor attribute AD Schema
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33b5753429b63638f1f1c9a3103aa8d78bd8590b77ceebec4fff05b82e10dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703015"
---
# <a name="nt-security-descriptor-attribute"></a>Atributo NT-Security-Descriptor

Descriptor Windows de seguridad NT para el objeto de esquema. Un descriptor de seguridad es una estructura de datos que contiene información de seguridad sobre un objeto, como la propiedad y los permisos del objeto.

Para obtener información sobre el formato de este valor, vea Formato de cadena del descriptor de [seguridad (Windows).](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx)



| Entrada | Valor |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-Descriptor                              |
| Ldap-Display-Name | nTSecurityDescriptor                                |
| Size              | \-                                                  |
| Actualizar privilegios  | \-                                                  |
| Frecuencia de actualización  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-Id-Guid    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                               |
| Está indexado             | Falso                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                               |
| Está indexado             | Falso                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | Falso                                                                                        |
| Es de un solo valor       | Verdadero                                                                                         |
| Está indexado             | Falso                                                                                        |
| En el catálogo global      | Verdadero                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                               |
| Está indexado             | Falso                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                               |
| Está indexado             | Falso                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                               |
| Está indexado             | Falso                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                               |
| Está indexado             | Falso                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Arriba**](c-top.md)<br/> |



 

 





