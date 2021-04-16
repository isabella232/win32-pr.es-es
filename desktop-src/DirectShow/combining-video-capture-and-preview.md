---
description: Combinación de captura de vídeo y vista previa
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinación de captura de vídeo y vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494633"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="256dc-103">Combinación de captura de vídeo y vista previa</span><span class="sxs-lookup"><span data-stu-id="256dc-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="256dc-104">En las secciones anteriores se describe cómo capturar vídeo en varios formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="256dc-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="256dc-105">En la sección de vista previa del [vídeo](previewing-video.md) se describe cómo crear un gráfico de vista previa dinámica.</span><span class="sxs-lookup"><span data-stu-id="256dc-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="256dc-106">Sin embargo, muchas aplicaciones deben hacerlo a la vez.</span><span class="sxs-lookup"><span data-stu-id="256dc-106">However, many applications must do both at once.</span></span> <span data-ttu-id="256dc-107">Para compilar una vista previa combinada y un gráfico de escritura de archivos, solo tiene que hacer dos llamadas a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span><span class="sxs-lookup"><span data-stu-id="256dc-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="256dc-108">En este código, el generador de gráficos de captura oculta algunos detalles:</span><span class="sxs-lookup"><span data-stu-id="256dc-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="256dc-109">Si el filtro de captura tiene un PIN de vista previa o un puerto de vídeo, además de un PIN de captura, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) simplemente representa ambos PIN, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="256dc-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![gráfico de captura y vista previa](images/vidcap04.png)

-   <span data-ttu-id="256dc-111">Si el filtro solo tiene un PIN de captura, el generador de gráficos de captura usa el filtro de [Smart Tee](smart-tee-filter.md) para dividir el flujo de captura.</span><span class="sxs-lookup"><span data-stu-id="256dc-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="256dc-112">En la ilustración siguiente se muestra el gráfico con un inteligente tee.</span><span class="sxs-lookup"><span data-stu-id="256dc-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![capturar y obtener una vista previa de un gráfico con filtro Smart Tee](images/vidcap05.png)

<span data-ttu-id="256dc-114">El filtro Smart Tee tiene un PIN de captura y un PIN de vista previa.</span><span class="sxs-lookup"><span data-stu-id="256dc-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="256dc-115">Toma un solo flujo de vídeo del filtro de captura y lo divide en dos flujos, uno para la captura y otro para la vista previa.</span><span class="sxs-lookup"><span data-stu-id="256dc-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="256dc-116">Para mantener el rendimiento en el PIN de captura, el PIN de vista previa quita los fotogramas según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="256dc-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="256dc-117">También quita las marcas de tiempo de cada muestra antes de entregarlas, por las razones descritas en el tema [filtros de captura de vídeo de DirectShow](directshow-video-capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="256dc-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="256dc-118">Aunque Smart Tee divide el flujo, no duplica físicamente los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="256dc-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="256dc-119">En su lugar, utiliza objetos de ejemplo multimedia personalizados que comparten los búferes.</span><span class="sxs-lookup"><span data-stu-id="256dc-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="256dc-120">Los ejemplos están marcados como "de solo lectura" para asegurarse de que los filtros de nivel inferior no escriben en los datos.</span><span class="sxs-lookup"><span data-stu-id="256dc-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="256dc-121">Si el gráfico de capturas tiene una ventana de vista previa, hay varias cosas que pueden hacer que Filter Graph Manager detenga todo el gráfico, incluida la secuencia de captura:</span><span class="sxs-lookup"><span data-stu-id="256dc-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="256dc-122">Bloquear el equipo.</span><span class="sxs-lookup"><span data-stu-id="256dc-122">Locking the computer.</span></span>
-   <span data-ttu-id="256dc-123">Presione CTRL + ALT + SUPR en un equipo que sea miembro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="256dc-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="256dc-124">Ejecutar una aplicación de Direct3D de pantalla completa, como un juego o un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="256dc-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="256dc-125">Cambiar monitores o cambiar la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="256dc-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="256dc-126">Ejecutar un programa que hace que Windows muestre un cuadro de diálogo de control de cuentas de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="256dc-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="256dc-127">(Windows Vista o posterior).</span><span class="sxs-lookup"><span data-stu-id="256dc-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="256dc-128">Ejecutar una ventana de DOS de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="256dc-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="256dc-129">Cualquiera de estos eventos puede interrumpir la sesión de captura, lo que podría provocar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="256dc-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="256dc-130">(Esto es lo que sucede internamente: el representador de vídeo pierde los recursos de Direct3D o DirectDraw que necesita.</span><span class="sxs-lookup"><span data-stu-id="256dc-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="256dc-131">En el proceso de recuperación de esos recursos, el representador de vídeo debe volver a conectarse con el filtro de nivel superior, lo que hace que el administrador de gráficos de filtro detenga el gráfico).</span><span class="sxs-lookup"><span data-stu-id="256dc-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="256dc-132">Dos posibles soluciones a este problema son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="256dc-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="256dc-133">No incluya una secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="256dc-133">Do not include a preview stream.</span></span> <span data-ttu-id="256dc-134">Sin embargo, tenga en cuenta que el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) agrega automáticamente una ventana de vista previa cuando el dispositivo de captura tiene un PIN de puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="256dc-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="256dc-135">Consulte [PIN del puerto de vídeo en la captura de archivos](video-port-pins-in-file-capture.md).</span><span class="sxs-lookup"><span data-stu-id="256dc-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="256dc-136">Use el motor de búfer de secuencia para enviar la secuencia de vista previa a un gráfico en otro proceso.</span><span class="sxs-lookup"><span data-stu-id="256dc-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="256dc-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="256dc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="256dc-138">Capturar vídeo en un archivo</span><span class="sxs-lookup"><span data-stu-id="256dc-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



