---
title: Para recuperar ejemplos de medios con el lector asincrónico
description: Para recuperar ejemplos de medios con el lector asincrónico
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Formato de sistemas avanzados (ASF), recuperación de ejemplos multimedia
- ASF (formato de sistemas avanzados), recuperación de ejemplos multimedia
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- lectores asincrónicos, recuperación de ejemplos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360198"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>Para recuperar ejemplos de medios con el lector asincrónico

Después de recibir el mensaje de estado WMT OPENED en la implementación de \_ [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), puede empezar a recibir ejemplos llamando a [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start). El lector asincrónico entrega ejemplos a la implementación de [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Los ejemplos se entregan en tiempo de presentación.

**Start** es una llamada asincrónica. Se devolverá casi inmediatamente y continuará en ejecución en subprocesos independientes. El lector asincrónico usa varios subprocesos al decodificar contenido y entregar ejemplos. Cuando se alcanza el final del archivo, el lector envía un mensaje de estado EOF de WMT a la implementación de la devolución de \_ **llamada OnStatus.** Cuando se envía WMT EOF, el lector detiene su propio procesamiento; no es necesario responder a WMT EOF con una llamada \_ \_ a [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Para implementar mensajes de lector en la devolución de llamada OnStatus**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**Para implementar la devolución de llamada OnSample**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




