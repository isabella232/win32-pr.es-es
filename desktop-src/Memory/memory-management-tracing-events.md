---
description: 'Más información sobre: Eventos de seguimiento de administración de memoria'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventos de seguimiento de administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb395082d46ddd668cbb91ee396f211a4055472f49682ab75efc90cedca7ad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809012"
---
# <a name="memory-management-tracing-events"></a>Eventos de seguimiento de administración de memoria

En esta sección se describe información detallada sobre detalles específicos de eventos de seguimiento de administración de memoria.

El seguimiento de la administración de memoria es una característica de solución de problemas que se puede habilitar en los archivos binarios comerciales para realizar un seguimiento de determinados eventos de administración de memoria con una sobrecarga mínima. Esta característica permite mejores funcionalidades de diagnóstico para desarrolladores y soporte técnico de productos. El seguimiento de eventos de administración de memoria admite la asignación del montón de seguimiento, la reasignación y las operaciones gratuitas.

El seguimiento de eventos de administración de memoria usa el seguimiento de eventos para Windows (ETW), una instalación de seguimiento de alta velocidad de uso general proporcionada por el sistema operativo. ETW proporciona un mecanismo de seguimiento para los eventos producidos por las aplicaciones en modo de usuario y los controladores de dispositivo en modo kernel. ETW puede habilitar y deshabilitar el registro dinámicamente, lo que facilita la realización de un seguimiento detallado en entornos de producción sin necesidad de reiniciar o reiniciar la aplicación. El seguimiento de eventos de administración de memoria mediante ETW se admite en Windows 7 , Windows Server 2008 R2 y versiones posteriores. Para obtener información general sobre ETW, vea [Mejorar la depuración y el ajuste del rendimiento con ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

En la lista siguiente se proporciona información detallada para cada evento de seguimiento de administración de memoria. Para obtener información adicional sobre cualquier evento, haga clic en el nombre del evento.



| Nombre del evento                                                  | Descripción                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**ALLOC \_ DE EVENTOS DE MONTÓN \_ \_ ETW**](etw-heap-event-alloc.md)     | Evento de seguimiento de administración de memoria para una operación de asignación de montón.    |
| [**ETW \_ HEAP \_ EVENT \_ FREE**](etw-heap-event-free.md)       | Evento de seguimiento de administración de memoria para una operación sin montón.          |
| [**REALLOC \_ DE EVENTOS DE MONTÓN \_ ETW \_**](etw-heap-event-realloc.md) | Evento de seguimiento de administración de memoria para una operación de nueva asignación del montón. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
