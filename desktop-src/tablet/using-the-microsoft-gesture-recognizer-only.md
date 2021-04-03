---
description: 'Puede usar un recolector de tinta (InkCollector, InkOverlay o InkPicture) para tener acceso directamente al reconocedor de gestos de Microsoft predeterminado. Para usar un recolector de tinta para tener acceso al reconocedor de gestos: establezca la propiedad si CollectionMode es del recopilador de tinta en modo InkAndGesture o GestureOnly. inkOverlay. Si CollectionMode es = si CollectionMode es. GestureOnly; Elija el gesto que desea admitir. inkOverlay. SetGestureStatus (ApplicationGesture. AllGestures, true); implemente un controlador de eventos que reciba notificaciones de gestos. En el controlador de eventos, debe implementar la acción correspondiente a cada evento recibido. Nota el modo mixto solo admite gestos de un solo trazo. El modo de gestos admite varios gestos de trazo. inkOverlay. gesto + = nuevo InkCollectorGestureEventHandler ( \_ gesto de inkOverlay); en el modo InkAndGesture, cada trazo individual se envía al reconocedor de gestos de Microsoft. Si se reconoce como un gesto que se ha habilitado, se envía una notificación de eventos. Si la aplicación acepta la notificación de eventos, el trazo se borra. Si la aplicación no acepta la notificación o si no se reconoce que el trazo es un gesto, el trazo se almacena en el objeto de entrada manuscrita. En el modo GestureOnly, los trazos se delimitan mediante tiempos de espera antes y después de los trazos. Los trazos recopilados en el tiempo de espera se envían al reconocedor. Si los trazos se reconocen como un gesto que se ha habilitado, se envía una notificación de eventos. La aplicación puede aceptar o rechazar el evento, lo que afecta a la acción correspondiente. En el modo de solo gesto, los trazos nunca se guardan en el objeto de entrada manuscrita.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Usar el reconocedor de gestos de Microsoft únicamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907911"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Usar el reconocedor de gestos de Microsoft únicamente

Puede usar un recolector de tinta ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)o [InkPicture](inkpicture-control-reference.md)) para tener acceso directamente al reconocedor de gestos de Microsoft predeterminado.

Para usar un recolector de tinta para tener acceso al reconocedor de gestos:

-   Establezca la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) del recopilador de tinta en modo **InkAndGesture** o en modo **GestureOnly** .

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Elija el gesto que desee admitir.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implemente un controlador de eventos que reciba notificaciones de gestos. En el controlador de eventos, debe implementar la acción correspondiente a cada evento recibido.
    > [!Note]  
    > El modo mixto solo admite gestos de un solo trazo. El modo de gestos admite varios gestos de trazo.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

En el modo **InkAndGesture** , cada trazo individual se envía al reconocedor de gestos de Microsoft. Si se reconoce como un gesto que se ha habilitado, se envía una notificación de eventos. Si la aplicación acepta la notificación de eventos, el trazo se borra. Si la aplicación no acepta la notificación o si no se reconoce que el trazo es un gesto, el trazo se almacena en el objeto de [**entrada manuscrita**](inkdisp-class.md) .

En el modo **GestureOnly** , los trazos se delimitan mediante tiempos de espera antes y después de los trazos. Los trazos recopilados en el tiempo de espera se envían al reconocedor. Si los trazos se reconocen como un gesto que se ha habilitado, se envía una notificación de eventos. La aplicación puede aceptar o rechazar el evento, lo que afecta a la acción correspondiente. En el modo de solo gesto, los trazos nunca se guardan en el objeto de [**entrada manuscrita**](inkdisp-class.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink. InkCollector. Si CollectionMode es](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. Si CollectionMode es](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. Si CollectionMode es](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
