---
title: ms-DS-Egress-Claims-Transformation-Policy
description: Se trata de un vínculo a un objeto de directiva de transformación notificaciones para las notificaciones de salida (notificaciones que salen de este bosque) al dominio de confianza.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- ms-DS-Egress-Claims-Transformation-Policy attribute AD Schema
- msDS-EgressClaimsTransformationPolicy attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ec71308c0ebc17942b3400d8ddd9e87ff88ea29d4f21e93047c3aa80f77128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118014658"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>ms-DS-Egress-Claims-Transformation-Policy

Se trata de un vínculo a un objeto de directiva de transformación notificaciones para las notificaciones de salida (notificaciones que salen de este bosque) al dominio de confianza. Esto solo es aplicable a una relación de confianza entre bosques entrante o bidireccional. Cuando este vínculo no está presente, todas las notificaciones pueden salir tal como están.



| Entrada | Valor |
|-------------------|-------------------------------------------|
| CN                | ms-DS-Egress-Claims-Transformation-Policy |
| Ldap-Display-Name | msDS-EgressClaimsTransformationPolicy     |
| Size              | \-                                        |
| Actualizar privilegios  | \-                                        |
| Frecuencia de actualización  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-Id-Guid    | c137427e-9a73-b040-9190-1b095bb43288      |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | 2192                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





