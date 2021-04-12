---
description: Enumera las enumeraciones usadas por las funciones de administración de directivas de LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumeraciones de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276999"
---
# <a name="security-management-enumerations"></a>Enumeraciones de administración de seguridad

Las enumeraciones de administración de seguridad son las siguientes:

-   [Enumeraciones de directivas de LSA](#lsa-policy-enumerations)
-   [Enumeraciones más seguras](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Enumeraciones de directivas de LSA

Las funciones de administración de directivas de LSA usan los siguientes tipos de enumeración.



| Enumeración                                                                               | Descripción                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ evento de auditoría de directiva \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Define los tipos de eventos que el sistema puede auditar.                                                                                     |
| [**\_clase de información de directiva \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Define los tipos de información que se pueden establecer o consultar para un objeto de [**Directiva**](policy-object.md) .                             |
| [**DIRECTIVA \_ LSA \_ ( \_ rol de servidor)**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indicar el rol de un servidor LSA.                                                                                                   |
| [**\_clase de \_ información de notificación de directiva \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Define los tipos de información de directivas e información de dominio de directivas para los que la aplicación puede solicitar notificación de cambios. |
| [**\_Estado de \_ habilitación del servidor de directivas \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Representa el estado del servidor LSA, es decir, si está habilitado o deshabilitado.                                                   |
| [**\_clase de información de confianza \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Define los tipos de información que se pueden establecer o consultar para un dominio de confianza.                                                     |



 

## <a name="safer-enumerations"></a>Enumeraciones más seguras

[Safe](safer.md) usa los siguientes tipos enumerados.



| Nombre                                                               | Descripción                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipos de identificación más seguros \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Tipo de enumeración que define los tipos posibles de estructuras de reglas de identificación que se pueden identificar mediante la estructura de [**\_ \_ encabezado de identificación más segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) . |
| [**\_clase de \_ información de objeto más segura \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Tipo de enumeración que define el tipo de información solicitada sobre un objeto más seguro.                                                                                                            |
| [**\_clase de \_ información de directiva más segura \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Tipo de enumeración que define las maneras en las que se puede consultar una directiva.                                                                                                                         |



 

 

 



