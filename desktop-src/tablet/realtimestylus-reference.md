---
description: Proporciona acceso a los eventos del lápiz óptico que proceden de los digitalizadores táctiles o de lápiz.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Referencia de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277779"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="05dcd-103">Referencia de RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="05dcd-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="05dcd-104">Proporciona acceso a los eventos del lápiz óptico que proceden de los digitalizadores táctiles o de lápiz.</span><span class="sxs-lookup"><span data-stu-id="05dcd-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="05dcd-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="05dcd-105">In This Section</span></span>

-   [<span data-ttu-id="05dcd-106">Clases e interfaces de RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="05dcd-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="05dcd-107">Enumeraciones de RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="05dcd-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="05dcd-108">Estructuras RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="05dcd-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="05dcd-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05dcd-109">Remarks</span></span>

<span data-ttu-id="05dcd-110">Este objeto implementa la interfaz com [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="05dcd-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="05dcd-111">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="05dcd-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="05dcd-112">Puede controlar por completo, representar, modificar e incluso eliminar datos de la secuencia de paquetes en los complementos sincrónicos y asincrónicos del objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="05dcd-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="05dcd-113">El lápiz en tiempo real proporciona una manera de crear un objeto **InkCollecting** que es de un solo subproceso y que reside en el subproceso de la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="05dcd-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="05dcd-114">Este objeto **InkCollecting** obtiene acceso a los datos del lápiz en tiempo real desde la cola.</span><span class="sxs-lookup"><span data-stu-id="05dcd-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="05dcd-115">Un objeto **InkCollecting** junto con el lápiz en tiempo real permite la edición de selección en tiempo real y la edición en tiempo real de los datos de tinta recopilados.</span><span class="sxs-lookup"><span data-stu-id="05dcd-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="05dcd-116">Para obtener más información, consulte [acceso y manipulación de entradas del lápiz óptico](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="05dcd-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="05dcd-117">Use el objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) para interactuar directamente con el flujo de datos de Tablet Stylus o para bloquear la entrada manuscrita en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="05dcd-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="05dcd-118">Use el objeto de [**clase InkCollector**](inkcollector-class.md) , el objeto de [**clase InkOverlay**](inkoverlay-class.md) , el control de [control InkPicture](inkpicture-control-reference.md) o el control de [control InkEdit](inkedit-control-reference.md) cuando el comportamiento predeterminado de estos objetos proporciona el comportamiento que necesita.</span><span class="sxs-lookup"><span data-stu-id="05dcd-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="05dcd-119">Los eventos del lápiz en tiempo real se encuentran en un identificador de ventana específico dentro de un rectángulo de entrada de la ventana específico.</span><span class="sxs-lookup"><span data-stu-id="05dcd-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="05dcd-120">RealTimeStylusService puede enviar datos del lápiz óptico a varios objetos de la [**clase RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="05dcd-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="05dcd-121">Cada objeto de **clase RealTimeStylus** recibe datos de lápiz óptico para una sección específica de una ventana basada en la [**propiedad IRealTimeStylus:: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definida para ese objeto de la **clase RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="05dcd-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="05dcd-122">El objeto de la **clase RealTimeStylus** obtiene los datos del lápiz y, a continuación, los procesa a través de una lista de complementos sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="05dcd-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="05dcd-123">La diferencia entre los complementos sincrónicos y los complementos asincrónicos se encuentra en el subproceso en el que se ejecutan y en la secuencia de llamada.</span><span class="sxs-lookup"><span data-stu-id="05dcd-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="05dcd-124">El subproceso en el que se ejecuta el objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) llama a los complementos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="05dcd-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="05dcd-125">Cada vez que se crea una instancia del objeto de la **clase RealTimeStylus** , se crea una instancia de un subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="05dcd-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="05dcd-126">Los complementos sincrónicos se ejecutan en este nuevo subproceso con instancias creadas para la instancia del objeto de la **clase RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="05dcd-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="05dcd-127">Se llama a los complementos asincrónicos a través de la interfaz de usuario o el subproceso de la aplicación después de que los complementos sincrónicos hayan procesado la secuencia de paquetes y estén almacenadas en la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="05dcd-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05dcd-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05dcd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05dcd-129">**Interfaz IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="05dcd-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="05dcd-130">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="05dcd-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="05dcd-131">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="05dcd-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="05dcd-132">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="05dcd-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
