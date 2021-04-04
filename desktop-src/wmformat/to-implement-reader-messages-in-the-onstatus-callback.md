---
title: Para implementar mensajes de lector en la devolución de llamada de estado
description: Para implementar mensajes de lector en la devolución de llamada de estado
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Advanced Systems Format (ASF), implementar mensajes de lector
- ASF (formato de sistemas avanzados), implementación de mensajes de lector
- Advanced Systems Format (ASF), alstatus callback
- ASF (formato de sistemas avanzados), devolución de llamada en estado
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, implementar mensajes de lector
- Método de devolución de llamada de estado, implementar mensajes de lector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077304"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>Para implementar mensajes de lector en la devolución de llamada de estado

Para usar el lector asincrónico para ofrecer contenido desde un archivo ASF, debe implementar un mínimo de dos métodos de devolución de llamada, [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) y [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). En esta sección se describe cómo implementar **IWMStatusCallback::** en el estado para recibir y responder a los mensajes de estado enviados por el lector. Los demás objetos del SDK de Windows Media Format usan el **Estado** . Para obtener información general sobre el **Estado**, consulte [usar la devolución de llamada de estado](using-the-onstatus-callback.md).

Al usar el lector asincrónico, debe interceptar los mensajes siguientes en **IWMStatusCallback:: en status**.



| Mensaje de estado | Descripción                                     |
|----------------|-------------------------------------------------|
| WMT \_ abierto    | Se envía cuando se completan las operaciones de apertura de archivos. |
| WMT \_ cerrado    | Se envía cuando se completan las operaciones de cierre de archivos. |



 

Debe usar los mensajes de estado enumerados anteriormente para controlar la ejecución de la aplicación de lectura. Por ejemplo, debe esperar hasta recibir el mensaje **de \_ Open WMT** para iniciar el lector o llamar a otros métodos que requieran que el lector tenga un archivo listo. Con frecuencia, las aplicaciones compiladas con el lector asincrónico usan un evento para indicar la finalización de las llamadas asincrónicas y continuar con el procesamiento. Para obtener más información sobre el uso de eventos para indicar la finalización de las operaciones, vea [uso de eventos con llamadas asincrónicas](using-events-with-asynchronous-calls.md).

El objeto de lectura envía muchos otros mensajes al **Estado** para permitir que la aplicación responda al estado de las operaciones de lectura. Los valores posibles de los mensajes de estado se definen en el tipo de enumeración [**\_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMStatusCallback:: en el estado**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usar la devolución de llamada en estado**](using-the-onstatus-callback.md)
</dt> </dl>

 

 




