---
title: Cómo funcionan las notificaciones
description: Cómo funcionan las notificaciones
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e90dfeb6e1df6de50ddaa3264a8c5475d280f30a72ad2d8c6acfffd39d60fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756375"
---
# <a name="how-notifications-work"></a>Cómo funcionan las notificaciones

Las notificaciones se originan en la aplicación de objeto y fluyen al contenedor mediante el controlador de objetos. Si el objeto es un objeto vinculado, el objeto vinculado intercepta las notificaciones del controlador de objetos y notifica al contenedor directamente.

Una aplicación de objeto debe administrar las solicitudes de registro, realizar un seguimiento de dónde enviar las notificaciones y enviarlas cuando corresponda. OLE proporciona dos objetos de componente para simplificar esta tarea: OleAdviseHolder para las notificaciones de documentos compuestos y DataAdviseHolder para las notificaciones de datos.

Las aplicaciones de objeto determinan las condiciones que solicitan el envío de cada notificación específica y la frecuencia con la que se debe enviar cada notificación. Cuando es adecuado enviar varias notificaciones, no importa qué notificación se envíe primero. se pueden enviar en cualquier orden.

El tiempo de las notificaciones afecta al rendimiento y la coordinación entre una aplicación de objeto y sus contenedores. Mientras que las notificaciones enviadas con demasiada frecuencia tardan en procesarse, las notificaciones enviadas con demasiada poca frecuencia tienen como resultado un contenedor no sincronizado. La frecuencia de notificación se puede comparar con la velocidad a la que se vuelve a dibujar una aplicación. Por lo tanto, es aconsejable usar una lógica similar para el tiempo de las notificaciones (como se usa para volver a dibujar).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> </dl>

 

 