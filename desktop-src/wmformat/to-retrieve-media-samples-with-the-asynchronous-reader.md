---
title: Para recuperar ejemplos de medios con el lector asincrónico
description: Para recuperar ejemplos de medios con el lector asincrónico
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Advanced Systems Format (ASF), recuperar ejemplos de medios
- ASF (formato de sistemas avanzados), recuperar ejemplos de medios
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, recuperar ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077301"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>Para recuperar ejemplos de medios con el lector asincrónico

Después de recibir el mensaje de \_ estado abierto de WMT en la implementación de [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)en el estado, puede empezar a recibir ejemplos llamando a [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start). El lector asincrónico proporciona ejemplos a su implementación de [**IWMReaderCallback:: websample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Los ejemplos se entregan en el orden de presentación.

**Start** es una llamada asincrónica. Se devolverá casi inmediatamente y continuará ejecutándose en subprocesos independientes. El lector asincrónico usa varios subprocesos al descodificar el contenido y entregar ejemplos. Cuando se alcanza el final del archivo, el lector envía un mensaje de \_ Estado de EOF de WMT a su implementación de la devolución de llamada de **Estado** . Cuando \_ se envía el EOF para WMT, el lector detiene su propio procesamiento; no es necesario responder al \_ EOF de WMT con una llamada a [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Para implementar mensajes de lector en la devolución de llamada de estado**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**Para implementar la devolución de llamada de ejemplo**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




