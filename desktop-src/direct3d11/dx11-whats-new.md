---
title: Novedades del SDK de Windows 7/Direct3D 11 de agosto de 2009
description: Esta versión de Windows 7/Direct3D 11 se incluye como parte del SDK de DirectX y contiene nuevas características, herramientas y documentación.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794818"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a><span data-ttu-id="4a3c0-103">Novedades del SDK de Windows 7/Direct3D 11 de agosto de 2009</span><span class="sxs-lookup"><span data-stu-id="4a3c0-103">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>

<span data-ttu-id="4a3c0-104">Esta versión de Windows 7/Direct3D 11 se incluye como parte del SDK de DirectX y contiene nuevas características, herramientas y documentación.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-104">This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a3c0-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a3c0-105">Item</span></span></th>
<th><span data-ttu-id="4a3c0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a3c0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4a3c0-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span><span class="sxs-lookup"><span data-stu-id="4a3c0-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span></span><br/></td>
<td><span data-ttu-id="4a3c0-108">Direct2D es una API de gráficos 2D y con aceleración de hardware, que ofrece un alto rendimiento y una representación de alta calidad para geometría 2D, mapas de bits y texto.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-108">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="4a3c0-109">La API de Direct2D está diseñada para interoperar bien con Direct3D y GDI.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-109">The Direct2D API is designed to interoperate well with Direct3D and GDI.</span></span> <span data-ttu-id="4a3c0-110">Este SDK permite a los desarrolladores evaluar la API y escribir aplicaciones sencillas, con algunas de las funciones más avanzadas posibles en máquinas correctamente configuradas.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-110">This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines.</span></span> <br/> <span data-ttu-id="4a3c0-111">La <a href="/windows/win32/direct2d/direct2d-portal">documentación</a> y los <a href="/previous-versions//dd372354(v=vs.85)">ejemplos</a> de Direct2D están disponibles actualmente en MSDN.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-111"><a href="/windows/win32/direct2d/direct2d-portal">Documentation</a> and <a href="/previous-versions//dd372354(v=vs.85)">samples</a> for Direct2D are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a3c0-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span><span class="sxs-lookup"><span data-stu-id="4a3c0-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span></span><br/></td>
<td><span data-ttu-id="4a3c0-113">DirectWrite proporciona compatibilidad para la representación de texto de alta calidad, fuentes de esquema independientes de la resolución, compatibilidad con el diseño y texto Unicode completo, y mucho, mucho más:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-113">DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:</span></span><br/>
<ul>
<li><span data-ttu-id="4a3c0-114">Sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-114">A device-independent text layout system that improves text readability in documents and in UI.</span></span><br/></li>
<li><span data-ttu-id="4a3c0-115">Representación de texto de alta calidad, subpíxel y ClearType que puede usar la tecnología de representación de GDI Direct3D, Direct2D o específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-115">High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.</span></span><br/></li>
<li><span data-ttu-id="4a3c0-116">Compatibilidad con texto con varios formatos.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-116">Support for multi-format text.</span></span> <br/></li>
<li><span data-ttu-id="4a3c0-117">Compatibilidad con las características tipográficas avanzadas de las fuentes OpenType.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-117">Support for the advanced typography features of OpenType fonts.</span></span><br/></li>
<li><span data-ttu-id="4a3c0-118">Compatibilidad con el diseño y la representación de texto en todos los lenguajes compatibles con Windows.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-118">Support for the layout and rendering of text in all languages supported by Windows.</span></span><br/></li>
</ul>
<span data-ttu-id="4a3c0-119">Este SDK permite a los desarrolladores evaluar la API y escribir aplicaciones básicas solo con fines de demostración.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-119">This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.</span></span><br/> <span data-ttu-id="4a3c0-120">La <a href="/windows/win32/directwrite/direct-write-portal">documentación</a> y los <a href="/windows/win32/directwrite/samples">ejemplos</a> de DirectWrite están disponibles actualmente en MSDN.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentation</a> and <a href="/windows/win32/directwrite/samples">samples</a> for DirectWrite are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a3c0-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="4a3c0-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1</span></span><br/></td>
<td><span data-ttu-id="4a3c0-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">Dxgi 1,1</a> se basa en dxgi 1,0 y estará disponible en Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7.</span></span> <span data-ttu-id="4a3c0-123">DXGI 1,1 agrega varias características nuevas:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-123">DXGI 1.1 adds several new features:</span></span><br/>
<ul>
<li><span data-ttu-id="4a3c0-124">Compatibilidad con superficies compartidas sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-124">Synchronized Shared Surfaces Support.</span></span> <span data-ttu-id="4a3c0-125">Esto permite compartir de forma eficaz la superficie de lectura y escritura entre varios D3D (puede estar entre los dispositivos D3D10 y D3D11).</span><span class="sxs-lookup"><span data-stu-id="4a3c0-125">This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.</span></span><br/></li>
<li><span data-ttu-id="4a3c0-126">Compatibilidad con el formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-126">BGRA format support.</span></span> <span data-ttu-id="4a3c0-127">Esto permite que GDI se represente en la misma superficie de DXGI de destino de un dispositivo Direct2D, Direct3D 10,1 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-127">This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device.</span></span> <br/></li>
<li><span data-ttu-id="4a3c0-128">Latencia máxima de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-128">Maximum Frame Latency.</span></span> <span data-ttu-id="4a3c0-129">Con <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: SetMaximumFrameLatency</strong></a> y <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: GetMaximumFrameLatency</strong></a>, los títulos pueden controlar el número de fotogramas que se pueden almacenar en una cola, antes de enviarlos para su representación.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-129">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering.</span></span> <span data-ttu-id="4a3c0-130">La latencia se usa a menudo para controlar el modo en que la CPU elige entre responder a los datos proporcionados por el usuario y a los fotogramas que se encuentran en la cola de representación.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-130">Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.</span></span><br/></li>
<li><span data-ttu-id="4a3c0-131">Enumeración de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-131">Adapter Enumeration.</span></span> <span data-ttu-id="4a3c0-132">Con <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>, titles puede enumerar los adaptadores locales sin monitores ni salidas adjuntos, así como adaptadores con salidas adjuntas.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-132">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a3c0-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Ejemplos actualizados</span><span class="sxs-lookup"><span data-stu-id="4a3c0-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples</span></span><br/></td>
<td><span data-ttu-id="4a3c0-134">Esta versión tiene varios ejemplos nuevos y actualizados.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-134">This release has several new and updated samples.</span></span><br/>
<ul>
<li><span data-ttu-id="4a3c0-135">El nuevo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> es una ilustración de técnicas de procesamiento de sombreador de cálculo más avanzadas que se pueden ejecutar en una GPU D3D10 o D3D11.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-135">The new <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</span></span></li>
<li><span data-ttu-id="4a3c0-136">El <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">ejemplo HDRToneMappingCS11</a> se ha expandido para implementar efectos de desenfoque y floración (además de la asignación de tono) mediante el sombreador de cálculo, así como para proporcionar implementaciones del sombreador de píxeles para la comparación.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-136">The <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 sample</a> has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</span></span></li>
<li><span data-ttu-id="4a3c0-137">El <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">ejemplo MultithreadedRendering11</a> se ha actualizado significativamente, con recursos de arte más complejos y un procesamiento por subprocesos más intensivo.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-137">The <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 sample</a> has been significantly updated, with more complex art assets and more intensive per-thread processing.</span></span></li>
<li><span data-ttu-id="4a3c0-138">El <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">ejemplo SubD11</a> se ha actualizado con un nuevo modelo facial y el ejemplo ahora aprovecha la característica de cálculo de adyacencias del exportador de contenido de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-138">The <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 sample</a> has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4a3c0-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a3c0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3c0-140">Características introducidas en versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="4a3c0-140">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

