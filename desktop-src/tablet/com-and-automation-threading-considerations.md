---
description: Las siguientes consideraciones de subprocesos de Tablet PC son específicas de cuando se usan el modelo de objetos componentes (COM) y la automatización.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Consideraciones sobre el subproceso de automatización y COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705445"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="142cd-103">Consideraciones sobre el subproceso de automatización y COM</span><span class="sxs-lookup"><span data-stu-id="142cd-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="142cd-104">Las siguientes consideraciones de subprocesos de Tablet PC son específicas de cuando se usan el modelo de objetos componentes (COM) y la automatización.</span><span class="sxs-lookup"><span data-stu-id="142cd-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="142cd-105">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="142cd-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="142cd-106">Aplicaciones STA y MTA</span><span class="sxs-lookup"><span data-stu-id="142cd-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="142cd-107">InkCollector y InkOverlay</span><span class="sxs-lookup"><span data-stu-id="142cd-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="142cd-108">Receptores de eventos</span><span class="sxs-lookup"><span data-stu-id="142cd-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="142cd-109">Excepciones dentro de los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="142cd-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="142cd-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="142cd-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="142cd-111">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="142cd-111">Thread Safety</span></span>

<span data-ttu-id="142cd-112">A excepción de los controles [InkPicture](inkpicture-control.md) y [InkEdit](inkedit-control.md) , los objetos de Tablet PC son seguros para subprocesos y se marcan como ambos.</span><span class="sxs-lookup"><span data-stu-id="142cd-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="142cd-113">Al marcarse como Both, se pueden ejecutar en un contenedor uniproceso (STA) o en un contenedor multiproceso (MTA).</span><span class="sxs-lookup"><span data-stu-id="142cd-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="142cd-114">Windows Forms usa el modelo STA porque Windows Forms se basa en ventanas nativas de Win32 que son subprocesos de Apartamento inherentemente.</span><span class="sxs-lookup"><span data-stu-id="142cd-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="142cd-115">Aplicaciones STA y MTA</span><span class="sxs-lookup"><span data-stu-id="142cd-115">STA and MTA Applications</span></span>

<span data-ttu-id="142cd-116">Si la aplicación se ejecuta en un MTA o usa el contador de referencias de subprocesamiento libre (FTM), debe escribir código seguro para subprocesos; sin embargo, si lo hace, puede mejorar determinados problemas de rendimiento de control de eventos.</span><span class="sxs-lookup"><span data-stu-id="142cd-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="142cd-117">InkCollector y InkOverlay</span><span class="sxs-lookup"><span data-stu-id="142cd-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="142cd-118">La aplicación no debe liberar su referencia final a [**InkCollector**](inkcollector-class.md) o el objeto [**InkOverlay**](inkoverlay-class.md) , de modo que se destruya el objeto directamente del subproceso de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="142cd-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="142cd-119">En su lugar, la aplicación debe liberar el objeto **InkCollector** o **InkOverlay** de un subproceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="142cd-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="142cd-120">**PRECAUCIÓN:** Una aplicación marcada como MTA o usa el FTM, que permite llamadas directas desde el subproceso de entrada manuscrita al apartamento de la aplicación, puede liberar su referencia final al objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) directamente desde el subproceso de entrada manuscrita; sin embargo, esto provoca un error irrecuperable en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="142cd-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="142cd-121">Receptores de eventos</span><span class="sxs-lookup"><span data-stu-id="142cd-121">Event Sinks</span></span>

<span data-ttu-id="142cd-122">Si la aplicación no usa el FTM y un objeto y su receptor de eventos se crean en distintos apartamentos, el evento se ejecuta en el subproceso que atiende al receptor de eventos.</span><span class="sxs-lookup"><span data-stu-id="142cd-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="142cd-123">Excepciones dentro de los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="142cd-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="142cd-124">Las excepciones que se inician desde los controladores de eventos de Tablet PC se consumen y no son visibles para el resto o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="142cd-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="142cd-125">Del mismo modo, los valores HRESULT no se propagan desde los controladores de eventos de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="142cd-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="142cd-126">Si una aplicación que utiliza el nivel COM inicia una excepción, el subproceso en segundo plano finaliza y se pierde la excepción.</span><span class="sxs-lookup"><span data-stu-id="142cd-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="142cd-127">No se llamará a ningún controlador de eventos adicional.</span><span class="sxs-lookup"><span data-stu-id="142cd-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="142cd-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="142cd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="142cd-129">Ejemplo de receptores de eventos de C++</span><span class="sxs-lookup"><span data-stu-id="142cd-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="142cd-130">Consideraciones generales de subprocesos</span><span class="sxs-lookup"><span data-stu-id="142cd-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="142cd-131">Consideraciones sobre los subprocesos de biblioteca administrada</span><span class="sxs-lookup"><span data-stu-id="142cd-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 



