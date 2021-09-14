---
description: Para enviar solicitudes de control a un servicio en ejecución, un programa de control de servicio usa la función ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Solicitudes de control de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168886"
---
# <a name="service-control-requests"></a>Solicitudes de control de servicio

Para enviar solicitudes de control a un servicio en ejecución, un programa de control de servicio usa la [**función ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) Esta función especifica un valor de control que se pasa a la [**función HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) del servicio especificado. Este valor de control puede ser un código definido por el usuario o puede ser uno de los códigos estándar que permiten al programa de llamada realizar las siguientes acciones:

-   Detener un servicio (SERVICE \_ CONTROL \_ STOP).
-   Pausar un servicio (SERVICE \_ CONTROL \_ PAUSE).
-   Reanudar la ejecución de un servicio en pausa (SERVICE \_ CONTROL \_ CONTINUE).
-   Recuperar información de estado actualizada de un servicio (SERVICE \_ CONTROL \_ INTERROGATE).

Cada servicio especifica los valores de control que aceptará y procesará. Para determinar cuáles de los valores de control estándar son aceptados por un servicio, use la función [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) o especifique el valor del control SERVICE CONTROL INTERROGATE en una llamada a la \_ \_ función [**ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) El **miembro dwControlsAccepted** de la estructura [**SERVICE \_ STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) devuelta por estas funciones indica si el servicio se puede detener, pausar o reanudar. Todos los servicios aceptan el \_ valor del control SERVICE CONTROL \_ INTERROGATE.

La [**función QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) notifica el estado más reciente de un servicio especificado, pero no obtiene un estado actualizado del propio servicio. El uso del valor del control SERVICE CONTROL INTERROGATE en una llamada a ControlService garantiza que \_ la información de estado devuelta es \_ actual. [](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlar un servicio mediante SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



