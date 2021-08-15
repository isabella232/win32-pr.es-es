---
title: Atributo ms-DS-Ingress-Claims-Transformation-Policy
description: Se trata de un vínculo a un objeto de directiva de transformación notificaciones para las notificaciones de entrada (notificaciones que entran en este bosque) desde el dominio de confianza.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- ms-DS-Ingress-Claims-Transformation-Policy attribute AD Schema
- msDS-IngressClaimsTransformationPolicy attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d631e2f342302f8089a43a329ac3982cf7874b46ab0f60d3e4399855f573e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960754"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>Atributo ms-DS-Ingress-Claims-Transformation-Policy

Se trata de un vínculo a un objeto de directiva de transformación notificaciones para las notificaciones de entrada (notificaciones que entran en este bosque) desde el dominio de confianza. Esto solo es aplicable a una relación de confianza entre bosques saliente o bidireccional. Si este vínculo no está presente, se descartan todas las notificaciones de entrada.



| Entrada | Valor |
|-------------------|--------------------------------------------|
| CN                | ms-DS-Ingress-Claims-Transformation-Policy |
| Ldap-Display-Name | msDS-IngressClaimsTransformationPolicy     |
| Size              | \-                                         |
| Actualizar privilegios  | \-                                         |
| Frecuencia de actualización  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| System-Id-Guid    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | 2190                                                 |
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



 

 





