---
description: Enumera y describe los tipos de acceso del objeto de directiva.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Derechos de acceso a objetos de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666398"
---
# <a name="policy-object-access-rights"></a>Derechos de acceso a objetos de Directiva

El objeto de [**Directiva**](policy-object.md) tiene los siguientes tipos de acceso específicos del objeto:



| Tipo de acceso                         | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ información local de la vista de directiva \_    | Este tipo de acceso es necesario para leer la información de la Directiva de seguridad diversa del sistema de destino. Esto incluye la cuota predeterminada, la auditoría, el estado del servidor y la información de rol, y la información de confianza. Este tipo de acceso también es necesario para enumerar los dominios, las cuentas y los [*privilegios*](/windows/desktop/SecGloss/p-gly)de confianza. |
| DIRECTIVA \_ obtener \_ \_ información privada   | Este tipo de acceso es necesario para ver información confidencial, como los nombres de las cuentas establecidas para las relaciones de dominio de confianza.                                                                                                                                                                                                                              |
| \_Administrador de confianza de directiva \_                | Este tipo de acceso es necesario para cambiar la información del dominio de la cuenta o del dominio principal.                                                                                                                                                                                                                                                                             |
| \_límites de \_ cuota predeterminados de directiva establecida \_ \_ | Establezca las cuotas del sistema predeterminadas que se aplican a las cuentas de usuario.                                                                                                                                                                                                                                                                                                   |
| \_secreto de creación de directiva \_              | Este tipo de acceso es necesario para crear un nuevo objeto de datos privado.                                                                                                                                                                                                                                                                                                    |
| creación de una cuenta de directiva \_ \_             | Este tipo de acceso es necesario para crear un nuevo objeto de [**cuenta**](account-object.md) .                                                                                                                                                                                                                                                                               |
| \_requisitos de \_ Auditoría de conjunto de directivas \_    | Este tipo de acceso es necesario para actualizar los requisitos de auditoría del sistema.                                                                                                                                                                                                                                                                                      |
| \_Administrador de \_ registro de auditoría de directiva \_           | Este tipo de acceso es necesario para cambiar las características de la traza de auditoría, como su tamaño máximo o el período de retención de los registros de auditoría, o para borrar el registro.                                                                                                                                                                                               |
| \_información de \_ Auditoría de vista de directiva \_    | Este tipo de acceso es necesario para ver la información de los requisitos de auditoría o la pista de auditoría.                                                                                                                                                                                                                                                                                  |
| \_Administrador del servidor de directivas \_               | Este tipo de acceso es necesario para modificar el estado del servidor o la información del rol (maestro o réplica). También es necesario cambiar la información del origen de la réplica y del nombre de la cuenta.                                                                                                                                                                                           |
| \_nombres de búsqueda de directivas \_               | Este tipo de acceso es necesario para traducir entre nombres y SID.                                                                                                                                                                                                                                                                                                    |
| \_privilegio de creación de directiva \_           | Todavía no se admite.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genéricas

El objeto de [**Directiva**](policy-object.md) publica las siguientes asignaciones de tipos de acceso genéricos en tipos de acceso específicos:

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

Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:

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

 

 
