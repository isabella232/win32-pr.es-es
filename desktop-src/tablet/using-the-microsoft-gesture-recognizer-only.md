---
description: 'Puede usar un recopilador de lápiz (InkCollector, InkOverlay o InkPicture) para acceder directamente al reconocedor de gestos de Microsoft predeterminado. Para usar un recopilador de entrada de lápiz para acceder al reconocedor de gestos: establezca la propiedad CollectionMode del recopilador de lápiz en el modo InkAndGesture o en GestureOnly mode.inkOverlay.CollectionMode = CollectionMode.GestureOnly; Elija el gesto que desea admitir.inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);Implemente un controlador de eventos que reciba notificaciones de gestos. En el controlador de eventos, debe implementar la acción correspondiente a cada evento recibido. Nota El modo mixto solo admite gestos de un solo trazo. El modo gesto admite varios gestos de trazo. inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay Gesture);In InkAndGesture mode, cada trazo individual se envía al reconocedor de \_ gestos de Microsoft. Si se reconoce como un gesto que ha habilitado, se envía una notificación de eventos. Si la aplicación acepta la notificación de eventos, se borra el trazo. Si la aplicación no acepta la notificación o si no se reconoce que el trazo es un gesto, el trazo se almacena en el objeto Ink. En el modo GestureOnly, los trazos se delimitan por tiempos de espera antes y después de los trazos. Los trazos recopilados dentro del tiempo de espera se envían al reconocedor. Si los trazos se reconocen como un gesto que ha habilitado, se envía una notificación de eventos. La aplicación puede aceptar o rechazar el evento, lo que afecta o no a la acción correspondiente. En el modo de solo gesto, los trazos nunca se guardan en el objeto Ink.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Usar solo El reconocedor de gestos de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d7b27ae30e0bba98ee2c9db57cc0da2d6491932d0137cc5cd4d2b6f86420ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715182"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Usar solo El reconocedor de gestos de Microsoft

Puede usar un recopilador de lápiz [**(InkCollector,**](inkcollector-class.md) [**InkOverlay**](inkoverlay-class.md)o [InkPicture)](inkpicture-control-reference.md)para acceder directamente al reconocedor de gestos de Microsoft predeterminado.

Para usar un recopilador de lápiz para acceder al reconocedor de gestos:

-   Establezca la [**propiedad CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) del recopilador de lápiz en el modo **InkAndGesture** o **en el modo GestureOnly.**

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Elija el gesto que desea admitir.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implemente un controlador de eventos que reciba notificaciones de gestos. En el controlador de eventos, debe implementar la acción correspondiente a cada evento recibido.
    > [!Note]  
    > El modo mixto solo admite gestos de trazo único. El modo gesto admite varios gestos de trazo.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

En **el modo InkAndGesture,** cada trazo individual se envía al reconocedor de gestos de Microsoft. Si se reconoce como un gesto que ha habilitado, se envía una notificación de eventos. Si la aplicación acepta la notificación de eventos, se borra el trazo. Si la aplicación no acepta la notificación o si no se reconoce que el trazo es un gesto, el trazo se almacena en el [**objeto Ink.**](inkdisp-class.md)

En **el modo GestureOnly,** los trazos se delimitan por tiempos de espera antes y después de los trazos. Los trazos recopilados dentro del tiempo de espera se envían al reconocedor. Si los trazos se reconocen como un gesto que ha habilitado, se envía una notificación de eventos. La aplicación puede aceptar o rechazar el evento, lo que afecta o no a la acción correspondiente. En el modo de solo gesto, los trazos nunca se guardan en el [**objeto Ink.**](inkdisp-class.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
