---
title: Cómo funcionan las notificaciones
description: Cómo funcionan las notificaciones
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421477"
---
# <a name="how-notifications-work"></a>Cómo funcionan las notificaciones

Las notificaciones se originan en la aplicación de objetos y fluyen al contenedor mediante el controlador de objetos. Si el objeto es un objeto vinculado, el objeto vinculado intercepta las notificaciones desde el controlador de objetos y notifica al contenedor directamente.

Una aplicación de objeto debe administrar las solicitudes de registro, realizando un seguimiento del lugar en el que se enviarán las notificaciones y el envío de las notificaciones cuando sea necesario. OLE proporciona dos objetos de componente para simplificar esta tarea: OleAdviseHolder para las notificaciones de documentos compuestos y DataAdviseHolder para las notificaciones de datos.

Las aplicaciones de objeto determinan las condiciones que solicitan el envío de cada notificación específica y la frecuencia con la que debe enviarse cada notificación. Cuando es adecuado para enviar varias notificaciones, no importa qué notificación se envía en primer lugar; se pueden enviar en cualquier orden.

Los intervalos de las notificaciones afectan al rendimiento y la coordinación entre una aplicación de objeto y sus contenedores. Mientras que las notificaciones enviadas con demasiada frecuencia se ralentizan el procesamiento, las notificaciones se envían con poca frecuencia en un contenedor fuera de sincronización. La frecuencia de notificación puede compararse con la velocidad a la que se repinta una aplicación. Por lo tanto, es aconsejable utilizar una lógica similar para el control de tiempo de las notificaciones (como se usa para la repintado).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> </dl>

 

 