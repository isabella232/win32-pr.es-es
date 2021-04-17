---
description: Para enviar solicitudes de control a un servicio en ejecución, un programa de control de servicios utiliza la función ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Solicitudes de control de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666446"
---
# <a name="service-control-requests"></a>Solicitudes de control de servicio

Para enviar solicitudes de control a un servicio en ejecución, un programa de control de servicios utiliza la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Esta función especifica un valor de control que se pasa a la función [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) del servicio especificado. Este valor de control puede ser un código definido por el usuario o puede ser uno de los códigos estándar que permiten al programa de llamada realizar las siguientes acciones:

-   Detener un servicio ( \_ detención del control de servicio \_ ).
-   Pausar un servicio ( \_ pausar el control de servicio \_ ).
-   Reanuda la ejecución de un servicio en pausa ( \_ continuación de control de servicio \_ ).
-   Recuperar información de estado actualizada de un servicio ( \_ interrogar de control de servicio \_ ).

Cada servicio especifica los valores de control que aceptará y procesará. Para determinar cuál de los valores de control estándar es aceptado por un servicio, utilice la función [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) o especifique el \_ \_ valor del control interrogate del control de servicios en una llamada a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . El miembro **dwControlsAccepted** de la estructura de [**\_ Estado de servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) que devuelven estas funciones indica si el servicio se puede detener, pausar o reanudar. Todos los servicios aceptan el \_ \_ valor de control interrogate del control de servicios.

La función [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) notifica el estado más reciente de un servicio especificado, pero no obtiene un estado actualizado del propio servicio. El uso del \_ \_ valor de control interrogate del control de servicios en una llamada a [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garantiza que la información de estado devuelta es actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlar un servicio mediante SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



