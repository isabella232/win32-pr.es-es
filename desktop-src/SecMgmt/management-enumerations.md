---
description: Enumera las enumeraciones utilizadas por las funciones de administración de directivas LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumeraciones de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf87e6c41cb3e687a8927c294fe3bc1433a294aaf48991310b1c230f4741f299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894461"
---
# <a name="security-management-enumerations"></a>Enumeraciones de administración de seguridad

Las enumeraciones de administración de seguridad incluyen lo siguiente:

-   [Enumeraciones de directivas LSA](#lsa-policy-enumerations)
-   [Enumeraciones más seguras](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Enumeraciones de directivas LSA

Las funciones de administración de directivas LSA usan los siguientes tipos de enumeración.



| Enumeración                                                                               | Descripción                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ DE EVENTO POLICY AUDIT \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Define los tipos de eventos que el sistema puede auditar.                                                                                     |
| [**CLASE \_ DE INFORMACIÓN DE \_ DIRECTIVA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Define los tipos de información que se pueden establecer o consultar para un [**objeto Policy.**](policy-object.md)                             |
| [**ROL \_ DE SERVIDOR LSA \_ DE \_ DIRECTIVA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indique el rol de un servidor LSA.                                                                                                   |
| [**CLASE DE \_ INFORMACIÓN DE NOTIFICACIÓN DE \_ \_ DIRECTIVA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Define los tipos de información de directiva e información de dominio de directiva para los que la aplicación puede solicitar la notificación de cambios. |
| [**ESTADO DE \_ HABILITACIÓN \_ DEL SERVIDOR DE \_ DIRECTIVAS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Representa el estado del servidor LSA, es decir, si está habilitado o deshabilitado.                                                   |
| [**CLASE \_ DE INFORMACIÓN DE \_ CONFIANZA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Define los tipos de información que se pueden establecer o consultar para un dominio de confianza.                                                     |



 

## <a name="safer-enumerations"></a>Enumeraciones más seguras

[Más](safer.md) seguro usa los siguientes tipos enumerados.



| Nombre                                                               | Descripción                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPOS \_ DE IDENTIFICACIÓN MÁS \_ SEGUROS**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Tipo de enumeración que define los posibles tipos de estructuras de reglas de identificación que se pueden identificar mediante la [**estructura SAFER \_ IDENTIFICATION \_ HEADER.**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) |
| [**SAFER \_ OBJECT \_ INFO \_ (CLASE)**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Tipo de enumeración que define el tipo de información solicitada sobre un objeto Más seguro.                                                                                                            |
| [**CLASE \_ DE INFORMACIÓN DE DIRECTIVA MÁS \_ \_ SEGURA**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Tipo de enumeración que define las formas en que se puede consultar una directiva.                                                                                                                         |



 

 

 



