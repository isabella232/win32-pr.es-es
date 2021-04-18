---
title: atributo MS-DS-Ingress-Claims-Transformation-Policy
description: Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de entrada (notificaciones que entran en este bosque) desde el dominio de confianza.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- MS-DS-Ingress-Claims-Transformation-esquema de AD de atributo de Directiva
- Esquema de AD de atributo msDS-IngressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536039"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>atributo MS-DS-Ingress-Claims-Transformation-Policy

Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de entrada (notificaciones que entran en este bosque) desde el dominio de confianza. Esto solo es aplicable a una confianza entre bosques de salida o bidireccional. Si este vínculo está ausente, se quitan todas las notificaciones de entrada.



| Entrada | Value |
|-------------------|--------------------------------------------|
| CN                | MS-DS-Ingress-Claims-Transformation-Policy |
| Nombre para mostrar de LDAP | msDS-IngressClaimsTransformationPolicy     |
| Tamaño              | \-                                         |
| Actualizar privilegio  | \-                                         |
| Frecuencia de actualización  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| System-ID-GUID    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Sintaxis            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | 2190                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | False                                                |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





