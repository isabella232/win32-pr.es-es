---
description: Tablet PC incluye tecnología para interactuar con los datos del lápiz de Tablet PC a medida que se recopilan.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Acceso y manipulación de la entrada del lápiz óptico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666204"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="e4f75-103">Acceso y manipulación de la entrada del lápiz óptico</span><span class="sxs-lookup"><span data-stu-id="e4f75-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="e4f75-104">Tablet PC incluye tecnología para interactuar con los datos del lápiz de Tablet PC a medida que se recopilan.</span><span class="sxs-lookup"><span data-stu-id="e4f75-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="e4f75-105">La clase [**RealTimeStylus**](realtimestylus-class.md) forma parte de las interfaces de programación de aplicaciones (API) de StylusInput, que proporcionan acceso al flujo de datos del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e4f75-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="e4f75-106">Estas API permiten capturar, interrumpir y modificar la secuencia de forma independiente de la representación y la recopilación de entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="e4f75-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="e4f75-107">Las API de StylusInput están diseñadas para:</span><span class="sxs-lookup"><span data-stu-id="e4f75-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="e4f75-108">Proporcionar acceso en tiempo real al flujo de datos del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e4f75-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="e4f75-109">Impedir que el subproceso de la interfaz de usuario (UI) bloquee la representación dinámica de la tinta al poner en cola los datos del paquete en el subproceso de la interfaz de usuario y hacer que la colección de tintas sea de</span><span class="sxs-lookup"><span data-stu-id="e4f75-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="e4f75-110">Aumente el rendimiento y reduzca el uso general de subprocesos con el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) , el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) para recopilar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="e4f75-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="e4f75-111">Las API de StylusInput no están diseñadas para funcionar con el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) , el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f75-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="e4f75-112">Si necesita interactuar directamente con el flujo de datos del lápiz de Tablet PC o si la aplicación puede bloquear la entrada manuscrita en tiempo real, use el objeto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f75-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="e4f75-113">Use el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) , el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) cuando el comportamiento predeterminado de estos objetos proporcione el comportamiento que necesita.</span><span class="sxs-lookup"><span data-stu-id="e4f75-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e4f75-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e4f75-114">In This Section</span></span>

<span data-ttu-id="e4f75-115">En las secciones siguientes se describen los elementos de las API de StylusInput:</span><span class="sxs-lookup"><span data-stu-id="e4f75-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="e4f75-116">Arquitectura de las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="e4f75-117">Trabajar con las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="e4f75-118">Trabajar con la clase RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e4f75-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="e4f75-119">Complementos y la clase RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e4f75-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="e4f75-120">Datos de complementos y clase RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e4f75-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="e4f75-121">Notas de implementación para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="e4f75-122">Complementos de recopilación de tintas</span><span class="sxs-lookup"><span data-stu-id="e4f75-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="e4f75-123">Complementos de representador dinámico</span><span class="sxs-lookup"><span data-stu-id="e4f75-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="e4f75-124">Complementos de reconocedor</span><span class="sxs-lookup"><span data-stu-id="e4f75-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="e4f75-125">Consideraciones al usar las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="e4f75-126">Consideraciones de diseño para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="e4f75-127">Consideraciones sobre los subprocesos para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="e4f75-128">El modelo RealTimeStylus en cascada</span><span class="sxs-lookup"><span data-stu-id="e4f75-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="e4f75-129">Consideraciones sobre el control de errores para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="e4f75-130">Consideraciones de rendimiento para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="e4f75-131">Consideraciones de confianza parcial para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="e4f75-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="e4f75-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4f75-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f75-133">Ejemplo de complemento RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e4f75-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="e4f75-134">Ejemplo de colección de tintas RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e4f75-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



