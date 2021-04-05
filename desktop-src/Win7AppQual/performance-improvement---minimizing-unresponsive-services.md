---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Prácticas recomendadas para minimizar los servicios que no responden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913213"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Prácticas recomendadas para minimizar los servicios que no responden

## <a name="affected-platform"></a>Plataforma afectada

 **Clientes** : Windows Vista Windows \| 7  

## <a name="description"></a>Descripción

Los servicios que no responden pueden dar lugar a tiempos de espera, sesiones terminadas e incluso pérdida de datos. La utilización de prácticas recomendadas puede reducir en gran medida la aparición de servicios que no responden.

## <a name="best-practices"></a>Prácticas recomendadas

Asegúrese de que las aplicaciones y todos sus servicios y controladores dependientes responden a las notificaciones de encendido y apagado del sistema.

-   Todas las aplicaciones deben responder rápidamente y adecuadamente para cerrar mensajes como WM \_ QUERYENDSESSION y WM \_ ENDSESSION que indican que hay un apagado en curso.
-   Todos los servicios deben responder rápidamente a las notificaciones de apagado de SCM. Si no lo hacen, el equipo los trata como si no respondiera e inicia un tiempo de espera de 20 segundos y los detiene, lo que abre la posibilidad de pérdida de datos. Esto también agrega 20 segundos a la hora de cierre de un apagado del equipo.
-   Todos los servicios que tienen dependencias de controlador de dispositivo de kernel deben responder rápidamente y adecuadamente \_ a \_ la notificación de cierre de IRP MJ en sus rutinas de DispatchShutdown.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Kit de herramientas de rendimiento de Windows](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



