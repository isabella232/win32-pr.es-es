---
title: Atributo SD-Rights-Effective
description: Este atributo construido devuelve un único valor DWORD que puede tener hasta tres bits establecido OWNER \_ SECURITY \_ INFORMATIONDACL \_ SECURITY \_ INFORMATIONSACL SECURITY INFORMATION Si \_ se \_ establece un bit, el usuario tiene acceso de escritura a la parte correspondiente del descriptor de seguridad. Propietario significa propietario y grupo.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo SD-Rights-Effective
- Esquema de AD del atributo sDRightsEffective
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d65591c935955133ca004c066249e9c6ec4a2effa102ad8b0e2650e6e5155749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923225"
---
# <a name="sd-rights-effective-attribute"></a>Atributo SD-Rights-Effective

Este atributo construido devuelve un único **valor DWORD** que puede tener hasta tres bits establecidos:

-   INFORMACIÓN DE \_ SEGURIDAD DEL \_ PROPIETARIO
-   INFORMACIÓN DE SEGURIDAD DE DACL \_ \_
-   INFORMACIÓN DE \_ SEGURIDAD DE \_ SACL

Si se establece un bit, el usuario tiene acceso de escritura a la parte correspondiente del descriptor de seguridad. Propietario significa propietario y grupo.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | SD-Rights-Effective                  |
| Ldap-Display-Name | sDRightsEffective                    |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1304              |
| System-Id-Guid    | c3dbafa6-33df-11d2-98b2-0000f87a57d4 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





