---
description: 'Más información sobre: eventos de seguimiento de la administración de memoria'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventos de seguimiento de administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669934"
---
# <a name="memory-management-tracing-events"></a>Eventos de seguimiento de administración de memoria

En esta sección se describe información detallada sobre los detalles del evento de seguimiento de administración de memoria específico.

El seguimiento de la administración de memoria es una característica de solución de problemas que se puede habilitar en los archivos binarios comerciales para realizar un seguimiento de determinados eventos de administración de memoria con una sobrecarga mínima. Esta característica permite mejorar las capacidades de diagnóstico de los desarrolladores y del soporte técnico. El seguimiento de eventos de administración de memoria admite operaciones de asignación, reasignación y liberación del montón de seguimiento.

El seguimiento de eventos de administración de memoria utiliza el seguimiento de eventos para Windows (ETW), un servicio de seguimiento de uso general y de alta velocidad proporcionado por el sistema operativo. ETW proporciona un mecanismo de seguimiento para los eventos generados por las aplicaciones de modo de usuario y los controladores de dispositivos de modo kernel. ETW puede habilitar y deshabilitar el registro de forma dinámica, lo que facilita la realización de seguimientos detallados en entornos de producción sin necesidad de reinicios o reinicios de aplicaciones. El seguimiento de eventos de administración de memoria con ETW es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores. Para obtener información general sobre ETW, vea [mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

La lista siguiente proporciona información detallada para cada evento de seguimiento de administración de memoria. Para obtener información adicional sobre cualquier evento, haga clic en el nombre del evento.



| Nombre del evento                                                  | Descripción                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_asignación de \_ eventos del montón ETW \_**](etw-heap-event-alloc.md)     | Evento de seguimiento de administración de memoria para una operación de asignación de montón.    |
| [**\_evento de montón ETW \_ \_ Free**](etw-heap-event-free.md)       | Evento de traza de administración de memoria para una operación libre del montón.          |
| [**\_evento de montón ETW \_ \_ REALLOC**](etw-heap-event-realloc.md) | Evento de traza de administración de memoria para una operación de reasignación del montón. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
