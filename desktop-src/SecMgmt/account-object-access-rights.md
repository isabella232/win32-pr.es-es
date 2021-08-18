---
description: El tipo derechos de acceso de objeto de cuenta tiene los siguientes tipos de acceso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Derechos de acceso a objetos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1251eecfd32bc574307cbc4f0f1327e4f96eb7fa7051d1dd638beb59e7ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895112"
---
# <a name="account-object-access-rights"></a>Derechos de acceso a objetos de cuenta

El tipo derechos de acceso de objeto de cuenta tiene los siguientes tipos de acceso.



| Tipo de acceso                     | Descripción                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VISTA \_ DE CUENTA                   | Este tipo de acceso es necesario para leer la información de la cuenta. Esto incluye los [*privilegios asignados*](/windows/desktop/SecGloss/p-gly) a la cuenta, las cuotas de memoria asignadas y los tipos de acceso especiales concedidos. |
| PRIVILEGIOS \_ DE \_ AJUSTE DE CUENTA     | Este tipo de acceso es necesario para asignar o quitar privilegios de una cuenta.                                                                                                                                                            |
| AJUSTE \_ DE LAS CUOTAS DE LA \_ CUENTA         | Este tipo de acceso es necesario para cambiar las cuotas del sistema asignadas a una cuenta.                                                                                                                                                                      |
| AJUSTE DE \_ LA CUENTA DEL ACCESO DEL \_ \_ SISTEMA | Este tipo de acceso es necesario para actualizar las marcas de acceso del sistema para la cuenta.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genérico

El [**objeto Account**](account-object.md) publica las siguientes asignaciones de tipos de acceso genéricos a tipos de acceso específicos.

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Tipos de acceso estándar

Este objeto no admite el tipo de acceso estándar SYNCHRONIZE (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es la siguiente.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
