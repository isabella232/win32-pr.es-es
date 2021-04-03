---
title: atributo MS-DS-out-Claims-Transformation-Policy
description: Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de salida (las notificaciones que abandonan este bosque) al dominio de confianza.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- MS-DS-out-Claims-Transformation-esquema de AD de atributo de Directiva
- Esquema de AD de atributo msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997440"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>atributo MS-DS-out-Claims-Transformation-Policy

Este es un vínculo a un objeto de directiva de transformación de notificaciones para las notificaciones de salida (las notificaciones que abandonan este bosque) al dominio de confianza. Esto solo es aplicable a una confianza entre bosques entrantes o bidireccionales. Cuando este vínculo no está presente, todas las notificaciones pueden salir tal cual.



| Entrada | Value |
|-------------------|-------------------------------------------|
| CN                | MS-DS-out-Claims-Transformation-Policy |
| Nombre para mostrar de LDAP | msDS-EgressClaimsTransformationPolicy     |
| Tamaño              | \-                                        |
| Actualizar privilegio  | \-                                        |
| Frecuencia de actualización  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-ID-GUID    | c137427e-9a73-b040-9190-1b095bb43288      |
| Sintaxis            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | 2192                                                 |
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



 

 





