---
title: Atributo ms-DS-Allowed-To-Delegate-To
description: Se trata de un atributo en objetos de cuenta de servicio (cuenta de usuario o equipo).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo ms-DS-Allowed-To-Delegate-To
- Esquema de AD del atributo msDS-AllowedToDelegateTo
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3a91abc375e67806387170ee6bda450c6f2bf167a3971f9808cd04e4c24d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704935"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>Atributo ms-DS-Allowed-To-Delegate-To

Se trata de un atributo en objetos de cuenta de servicio (cuenta de usuario o equipo). Contiene una lista de nombres de entidad de seguridad de servicio (SPN). Este atributo se usa para configurar un servicio de modo que pueda obtener vales de servicio que se pueden usar para la delegación restringida.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Allowed-To-Delegate-To                |
| Ldap-Display-Name | msDS-AllowedToDelegateTo                    |
| Size              | De 0 a 64 000                                    |
| Privilegio actualizar  | \-                                          |
| Frecuencia de actualización  | Infrecuentemente                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| System-Id-Guid    | 800d94d7-b7a1-42a1-b14d-7cae1423d07f        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Falso                                                              |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Falso                                                              |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Falso                                                              |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Falso                                                              |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Falso                                                              |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





