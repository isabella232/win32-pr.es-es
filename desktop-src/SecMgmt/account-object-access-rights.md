---
description: El tipo de derechos de acceso del objeto de cuenta tiene los siguientes tipos de acceso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Derechos de acceso a objetos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546222"
---
# <a name="account-object-access-rights"></a>Derechos de acceso a objetos de cuenta

El tipo de derechos de acceso del objeto de cuenta tiene los siguientes tipos de acceso.



| Tipo de acceso                     | Descripción                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| vista de cuentas \_                   | Este tipo de acceso es necesario para leer la información de la cuenta. Esto incluye los [*privilegios*](/windows/desktop/SecGloss/p-gly) asignados a la cuenta, las cuotas de memoria asignadas y los tipos de acceso especiales que se conceden. |
| \_privilegios de ajuste de cuenta \_     | Este tipo de acceso es necesario para asignar o quitar privilegios de una cuenta.                                                                                                                                                            |
| \_cuotas de ajuste de cuenta \_         | Este tipo de acceso es necesario para cambiar las cuotas del sistema asignadas a una cuenta.                                                                                                                                                                      |
| \_ajustar cuenta \_ \_ acceso al sistema | Este tipo de acceso es necesario para actualizar las marcas de acceso del sistema de la cuenta.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genéricas

El objeto [**account**](account-object.md) publica las siguientes asignaciones de tipos de acceso genéricos en tipos de acceso específicos.

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

Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es la siguiente.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
