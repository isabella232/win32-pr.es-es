---
description: La interfaz IDirect3DDevice9 admite el procesamiento de vértices en software y hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Procesar datos de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906753"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="5cb63-103">Procesar datos de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5cb63-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="5cb63-104">La interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) admite el procesamiento de vértices en software y hardware.</span><span class="sxs-lookup"><span data-stu-id="5cb63-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="5cb63-105">En general, las capacidades del dispositivo para el procesamiento de vértices de software y hardware no son idénticas.</span><span class="sxs-lookup"><span data-stu-id="5cb63-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="5cb63-106">Las capacidades de hardware son variables, dependiendo del adaptador de pantalla y del controlador, mientras que las capacidades de software son fijas.</span><span class="sxs-lookup"><span data-stu-id="5cb63-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="5cb63-107">Las marcas siguientes controlan el comportamiento del procesamiento de vértices para la capa de abstracción de hardware (HAL) y los dispositivos de referencia.</span><span class="sxs-lookup"><span data-stu-id="5cb63-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="5cb63-108">D3DCREATE \_ software \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="5cb63-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="5cb63-109">\_VERTEXPROCESSING de hardware D3DCREATE \_</span><span class="sxs-lookup"><span data-stu-id="5cb63-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="5cb63-110">D3DCREATE \_ Mixed \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="5cb63-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="5cb63-111">Especifique una de las marcas de comportamiento de procesamiento de vértices al llamar a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="5cb63-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="5cb63-112">La marca de modo mixto permite que el dispositivo realice el procesamiento de vértices de software y hardware.</span><span class="sxs-lookup"><span data-stu-id="5cb63-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="5cb63-113">Solo se puede establecer una marca de procesamiento de vértices para un dispositivo en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="5cb63-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="5cb63-114">Tenga en cuenta que \_ se debe establecer la marca D3DCREATE de hardware \_ VERTEXPROCESSING al crear un dispositivo puro (D3DCREATE \_ PUREDEVICE).</span><span class="sxs-lookup"><span data-stu-id="5cb63-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="5cb63-115">Para evitar las capacidades de procesamiento de vértices duales en un único dispositivo, solo se pueden consultar en tiempo de ejecución las capacidades de procesamiento de vértices de hardware.</span><span class="sxs-lookup"><span data-stu-id="5cb63-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="5cb63-116">Las capacidades de procesamiento de vértices de software son fijas y no se pueden consultar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5cb63-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="5cb63-117">El miembro VertexProcessingCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina las capacidades de procesamiento de vértices de hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5cb63-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="5cb63-118">Para el procesamiento de vértices de software, se admiten las siguientes funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="5cb63-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="5cb63-119">el \_ miembro D3DVTXPCAPS DIRECTIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="5cb63-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="5cb63-120">el \_ miembro D3DVTXPCAPS LOCALVIEWER de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="5cb63-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="5cb63-121">el \_ miembro D3DVTXPCAPS MATERIALSOURCE7 de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="5cb63-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="5cb63-122">el \_ miembro D3DVTXPCAPS POSITIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="5cb63-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="5cb63-123">el \_ miembro D3DVTXPCAPS TEXGEN de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="5cb63-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="5cb63-124">\_miembro de intercalación D3DVTXPCAPS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="5cb63-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="5cb63-125">Además, en la tabla siguiente se enumeran los valores que se establecen para los miembros de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para un dispositivo en el modo de procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="5cb63-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="5cb63-126">Miembro</span><span class="sxs-lookup"><span data-stu-id="5cb63-126">Member</span></span>                 | <span data-ttu-id="5cb63-127">Capacidades de procesamiento de vértices de software</span><span class="sxs-lookup"><span data-stu-id="5cb63-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="5cb63-128">MaxActiveLights</span><span class="sxs-lookup"><span data-stu-id="5cb63-128">MaxActiveLights</span></span>        | <span data-ttu-id="5cb63-129">Sin límite</span><span class="sxs-lookup"><span data-stu-id="5cb63-129">Unlimited</span></span>                               |
| <span data-ttu-id="5cb63-130">MaxUserClipPlanes</span><span class="sxs-lookup"><span data-stu-id="5cb63-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="5cb63-131">6</span><span class="sxs-lookup"><span data-stu-id="5cb63-131">6</span></span>                                       |
| <span data-ttu-id="5cb63-132">MaxVertexBlendMatrices</span><span class="sxs-lookup"><span data-stu-id="5cb63-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="5cb63-133">4</span><span class="sxs-lookup"><span data-stu-id="5cb63-133">4</span></span>                                       |
| <span data-ttu-id="5cb63-134">MaxStreams</span><span class="sxs-lookup"><span data-stu-id="5cb63-134">MaxStreams</span></span>             | <span data-ttu-id="5cb63-135">16</span><span class="sxs-lookup"><span data-stu-id="5cb63-135">16</span></span>                                      |
| <span data-ttu-id="5cb63-136">MaxVertexIndex</span><span class="sxs-lookup"><span data-stu-id="5cb63-136">MaxVertexIndex</span></span>         | <span data-ttu-id="5cb63-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5cb63-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="5cb63-138">En general, cualquier aplicación enlazada al procesamiento de vértices debe usar un dispositivo HAL.</span><span class="sxs-lookup"><span data-stu-id="5cb63-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="5cb63-139">El procesamiento de vértices de software proporciona un conjunto garantizado de funcionalidades de procesamiento de vértices, incluido un número ilimitado de luces y compatibilidad total con los sombreadores de vértices programables.</span><span class="sxs-lookup"><span data-stu-id="5cb63-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="5cb63-140">Puede alternar entre el procesamiento de vértices de software y hardware en cualquier momento cuando se usa el dispositivo HAL (que es el único tipo de dispositivo que admite el procesamiento de vértices de hardware y software).</span><span class="sxs-lookup"><span data-stu-id="5cb63-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="5cb63-141">El único requisito es que los búferes de vértices usados para el procesamiento de vértices de software deben asignarse en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="5cb63-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cb63-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5cb63-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cb63-143">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="5cb63-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
