---
title: Cómo funcionan las notificaciones
description: Cómo funcionan las notificaciones
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973624"
---
# <a name="how-notifications-work"></a>Cómo funcionan las notificaciones

Las notificaciones se originan en la aplicación de objeto y fluyen al contenedor mediante el controlador de objetos. Si el objeto es un objeto vinculado, el objeto vinculado intercepta las notificaciones del controlador de objetos y notifica al contenedor directamente.

Una aplicación de objeto debe administrar las solicitudes de registro, realizar un seguimiento de dónde enviar las notificaciones y enviarlas cuando sea necesario. OLE proporciona dos objetos de componente para simplificar esta tarea: OleAdviseHolder para notificaciones de documentos compuestos y DataAdviseHolder para notificaciones de datos.

Las aplicaciones de objetos determinan las condiciones que solicitan el envío de cada notificación específica y la frecuencia con la que se debe enviar cada notificación. Cuando es adecuado enviar varias notificaciones, no importa qué notificación se envíe primero. se pueden enviar en cualquier orden.

El tiempo de las notificaciones afecta al rendimiento y la coordinación entre una aplicación de objeto y sus contenedores. Mientras que las notificaciones enviadas con demasiada frecuencia ralentizan el procesamiento, las notificaciones enviadas con demasiada poca frecuencia tienen como resultado un contenedor no sincronizado. La frecuencia de notificación se puede comparar con la velocidad a la que se vuelve a dibujar una aplicación. Por lo tanto, es aconsejable usar una lógica similar para el tiempo de las notificaciones (como se usa para volver a dibujar).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> </dl>

 

 