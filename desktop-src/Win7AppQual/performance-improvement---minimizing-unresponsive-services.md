---
description: Procedimientos recomendados para minimizar los servicios que no responde
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedimientos recomendados para minimizar los servicios que no responde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088003"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Procedimientos recomendados para minimizar los servicios que no responde

## <a name="affected-platform"></a>Plataforma afectada

 **Clientes:** Windows Vista \| Windows 7  

## <a name="description"></a>Descripción

Los servicios que no responden pueden dar lugar a tiempos de espera, sesiones terminadas e incluso pérdida de datos. El empleo de procedimientos recomendados puede reducir considerablemente la aparición de servicios que no responden.

## <a name="best-practices"></a>Prácticas recomendadas

Asegúrese de que las aplicaciones y todos sus servicios y controladores dependientes responden a las notificaciones de encendido y apagado del sistema.

-   Todas las aplicaciones deben responder de forma rápida y adecuada a los mensajes de apagado, como WM \_ QUERYENDSESSION y WM ENDSESSION, que indican que hay un apagado \_ en curso.
-   Todos los servicios deben responder rápidamente a las notificaciones de cierre de SCM. Si no lo hacen, la máquina los trata como no responde e inicia un tiempo de espera de 20 segundos y los detiene, lo que abre la posibilidad de que se pierdan datos. Esto también agrega 20 segundos al tiempo de apagado de una máquina.
-   Todos los servicios que tienen dependencias del controlador de dispositivo kernel deben responder de forma rápida y adecuada a la notificación \_ IRP MJ SHUTDOWN en \_ sus rutinas DispatchShutdown.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Kit de herramientas de rendimiento de Windows](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



