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
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="5dbcc-113">Usar el reconocedor de gestos de Microsoft únicamente</span><span class="sxs-lookup"><span data-stu-id="5dbcc-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="5dbcc-114">Puede usar un recolector de tinta ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)o [InkPicture](inkpicture-control-reference.md)) para tener acceso directamente al reconocedor de gestos de Microsoft predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="5dbcc-115">Para usar un recolector de tinta para tener acceso al reconocedor de gestos:</span><span class="sxs-lookup"><span data-stu-id="5dbcc-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="5dbcc-116">Establezca la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) del recopilador de tinta en modo **InkAndGesture** o en modo **GestureOnly** .</span><span class="sxs-lookup"><span data-stu-id="5dbcc-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="5dbcc-117">Elija el gesto que desee admitir.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="5dbcc-118">Implemente un controlador de eventos que reciba notificaciones de gestos.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="5dbcc-119">En el controlador de eventos, debe implementar la acción correspondiente a cada evento recibido.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="5dbcc-120">El modo mixto solo admite gestos de un solo trazo.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="5dbcc-121">El modo de gestos admite varios gestos de trazo.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="5dbcc-122">En el modo **InkAndGesture** , cada trazo individual se envía al reconocedor de gestos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="5dbcc-123">Si se reconoce como un gesto que se ha habilitado, se envía una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="5dbcc-124">Si la aplicación acepta la notificación de eventos, el trazo se borra.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="5dbcc-125">Si la aplicación no acepta la notificación o si no se reconoce que el trazo es un gesto, el trazo se almacena en el objeto de [**entrada manuscrita**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbcc-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="5dbcc-126">En el modo **GestureOnly** , los trazos se delimitan mediante tiempos de espera antes y después de los trazos.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="5dbcc-127">Los trazos recopilados en el tiempo de espera se envían al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="5dbcc-128">Si los trazos se reconocen como un gesto que se ha habilitado, se envía una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="5dbcc-129">La aplicación puede aceptar o rechazar el evento, lo que afecta a la acción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5dbcc-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="5dbcc-130">En el modo de solo gesto, los trazos nunca se guardan en el objeto de [**entrada manuscrita**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbcc-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dbcc-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbcc-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5dbcc-132">[Microsoft. Ink. InkCollector. Si CollectionMode es](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5dbcc-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="5dbcc-133">[Microsoft. Ink. InkOverlay. Si CollectionMode es](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5dbcc-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="5dbcc-134">[Microsoft. Ink. InkPicture. Si CollectionMode es](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="5dbcc-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
