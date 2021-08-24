---
title: Atributo ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
description: Este atributo se usa para las comprobaciones de acceso a fin de determinar si un solicitante tiene permiso para actuar en nombre de otras identidades para los servicios que se ejecutan como esta cuenta.
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
- msDS-AllowedToActOnBehalfOfOtherIdentity attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3ea9795dd89777d390235193ff2663e5b514125cdf539c34dfc85ad1664bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552845"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a>Atributo ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity

Este atributo se usa para las comprobaciones de acceso a fin de determinar si un solicitante tiene permiso para actuar en nombre de otras identidades para los servicios que se ejecutan como esta cuenta.



| Entrada | Valor |
|-------------------|-----------------------------------------------------|
| CN                | ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity    |
| Ldap-Display-Name | msDS-AllowedToActOnBehalfOfOtherIdentity            |
| Size              | \-                                                  |
| Privilegio actualizar  | \-                                                  |
| Frecuencia de actualización  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.4.2182                             |
| System-Id-Guid    | 3f78c3e5-f79a-46bd-a0b8-9d18116ddc79                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Verdadero                                                               |
| Es de un solo valor       | Verdadero                                                               |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | 0                                                                  |
| Range-Upper            | 132096                                                             |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





