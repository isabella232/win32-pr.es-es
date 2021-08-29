---
title: Para implementar mensajes de lector en la devolución de llamada OnStatus
description: Para implementar mensajes de lector en la devolución de llamada OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Formato de sistemas avanzados (ASF), implementar mensajes de lector
- ASF (formato de sistemas avanzados), implementar mensajes de lector
- Formato de sistemas avanzados (ASF), devolución de llamada de OnStatus
- ASF (formato de sistemas avanzados), devolución de llamada de OnStatus
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, implementar mensajes de lector
- Método de devolución de llamada OnStatus, implementar mensajes del lector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05865d07c94f34807b35e46c625a2c82d943aaca37da77b90a6d94b3d1cace84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084072"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>Para implementar mensajes de lector en la devolución de llamada OnStatus

Para usar el lector asincrónico para entregar contenido desde un archivo ASF, debe implementar un mínimo de dos métodos de devolución de llamada, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) e [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). En esta sección se describe cómo implementar **IWMStatusCallback::OnStatus** para recibir y responder a los mensajes de estado enviados por el lector. Otros objetos del SDK de formato multimedia de Windows usan **OnStatus.** Para obtener información general sobre **OnStatus**, vea [Using the OnStatus Callback](using-the-onstatus-callback.md).

Al usar el lector asincrónico, debe capturar los mensajes siguientes en **IWMStatusCallback::OnStatus**.



| Mensaje de estado | Descripción                                     |
|----------------|-------------------------------------------------|
| WMT \_ ABIERTO    | Se envía cuando se completan las operaciones de apertura de archivos. |
| WMT \_ CLOSED    | Se envía cuando se completan las operaciones de cierre de archivos. |



 

Debe usar los mensajes de estado enumerados anteriormente para controlar la ejecución de la aplicación de lectura. Por ejemplo, debe esperar hasta recibir el mensaje **WMT \_ OPENED** para iniciar el lector o llamar a otros métodos que requieren que el lector tenga un archivo listo. Con frecuencia, las aplicaciones creadas con el lector asincrónico usan un evento para indicar la finalización de llamadas asincrónicas y continuar con el procesamiento. Para obtener más información sobre el uso de eventos para señalizar la finalización de operaciones, vea [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).

El objeto lector envía muchos otros mensajes a **OnStatus** para permitir que la aplicación responda al estado de las operaciones de lectura. Los valores posibles del mensaje de estado se definen en el tipo [**de \_ enumeración STATUS de WMT.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Uso de la devolución de llamada OnStatus**](using-the-onstatus-callback.md)
</dt> </dl>

 

 




