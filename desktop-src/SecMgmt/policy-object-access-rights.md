---
description: Enumera y describe los tipos de acceso del objeto Policy.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Derechos de acceso a objetos de directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae22db51c28e76e7122a1f7baf781671d9cc445e253fb6df7d63f87e3f7e921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005103"
---
# <a name="policy-object-access-rights"></a>Derechos de acceso a objetos de directiva

El [**objeto Policy**](policy-object.md) tiene los siguientes tipos de acceso específicos del objeto:



| Tipo de acceso                         | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INFORMACIÓN \_ LOCAL DE LA VISTA DE \_ \_ DIRECTIVA    | Este tipo de acceso es necesario para leer la información de directiva de seguridad miscelánea del sistema de destino. Esto incluye la cuota predeterminada, la auditoría, la información de estado y rol del servidor y la información de confianza. Este tipo de acceso también es necesario para enumerar dominios, cuentas y [*privilegios de confianza.*](/windows/desktop/SecGloss/p-gly) |
| POLICY \_ GET \_ PRIVATE \_ INFORMATION   | Este tipo de acceso es necesario para ver información confidencial, como los nombres de las cuentas establecidas para las relaciones de dominio de confianza.                                                                                                                                                                                                                              |
| ADMINISTRADOR DE \_ CONFIANZA \_ DE DIRECTIVAS                | Este tipo de acceso es necesario para cambiar la información del dominio de la cuenta o del dominio principal.                                                                                                                                                                                                                                                                             |
| LÍMITES \_ DE CUOTA PREDETERMINADOS DEL CONJUNTO DE \_ \_ \_ DIRECTIVAS | Establezca las cuotas predeterminadas del sistema que se aplican a las cuentas de usuario.                                                                                                                                                                                                                                                                                                   |
| POLICY \_ CREATE \_ SECRET              | Este tipo de acceso es necesario para crear un nuevo objeto Private Data.                                                                                                                                                                                                                                                                                                    |
| POLICY \_ CREATE \_ ACCOUNT             | Este tipo de acceso es necesario para crear un nuevo [**objeto Account.**](account-object.md)                                                                                                                                                                                                                                                                               |
| REQUISITOS DE \_ AUDITORÍA DEL CONJUNTO DE \_ \_ DIRECTIVAS    | Este tipo de acceso es necesario para actualizar los requisitos de auditoría del sistema.                                                                                                                                                                                                                                                                                      |
| ADMINISTRADOR DE \_ REGISTROS DE AUDITORÍA DE \_ \_ DIRECTIVAS           | Este tipo de acceso es necesario para cambiar las características de la pista de auditoría, como su tamaño máximo o el período de retención de los registros de auditoría, o para borrar el registro.                                                                                                                                                                                               |
| INFORMACIÓN DE \_ AUDITORÍA DE VISTA DE \_ \_ DIRECTIVA    | Este tipo de acceso es necesario para ver la información de los requisitos de auditoría o el registro de auditoría.                                                                                                                                                                                                                                                                                  |
| ADMINISTRADOR \_ DEL SERVIDOR DE \_ DIRECTIVAS               | Este tipo de acceso es necesario para modificar la información del rol o el estado del servidor (maestro o réplica). También es necesario cambiar la información de origen y nombre de cuenta de la réplica.                                                                                                                                                                                           |
| NOMBRES DE \_ BÚSQUEDA DE \_ DIRECTIVAS               | Este tipo de acceso es necesario para traducir entre nombres y SID.                                                                                                                                                                                                                                                                                                    |
| PRIVILEGIO DE \_ CREACIÓN \_ DE DIRECTIVA           | Todavía no se admite.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genérico

El [**objeto Policy**](policy-object.md) publica las siguientes asignaciones de tipos de acceso genéricos a tipos de acceso específicos:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a>Tipos de acceso estándar

Este objeto no admite el tipo de acceso estándar SYNCHRONIZE (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
