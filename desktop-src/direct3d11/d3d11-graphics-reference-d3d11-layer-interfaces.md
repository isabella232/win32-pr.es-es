---
title: Interfaces de capas
description: Esta sección contiene información sobre las interfaces de capas.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- interfaces, capa de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997185"
---
# <a name="layer-interfaces"></a><span data-ttu-id="f0302-104">Interfaces de capas</span><span class="sxs-lookup"><span data-stu-id="f0302-104">Layer Interfaces</span></span>

<span data-ttu-id="f0302-105">Esta sección contiene información sobre las interfaces de capas.</span><span class="sxs-lookup"><span data-stu-id="f0302-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="f0302-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f0302-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0302-107">Tema</span><span class="sxs-lookup"><span data-stu-id="f0302-107">Topic</span></span></th>
<th><span data-ttu-id="f0302-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0302-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0302-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="f0302-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="f0302-110">Una interfaz de depuración controla la configuración de depuración, valida el estado de la canalización y solo se puede usar si la capa de depuración está activada.</span><span class="sxs-lookup"><span data-stu-id="f0302-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0302-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="f0302-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="f0302-112">Una interfaz de cola de información almacena, recupera y filtra los mensajes de depuración.</span><span class="sxs-lookup"><span data-stu-id="f0302-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="f0302-113">La cola está formada por una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional.</span><span class="sxs-lookup"><span data-stu-id="f0302-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0302-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="f0302-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="f0302-115">La interfaz de seguimiento predeterminada establece las opciones de seguimiento predeterminadas de referencia.</span><span class="sxs-lookup"><span data-stu-id="f0302-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0302-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="f0302-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="f0302-117">La interfaz de seguimiento establece las opciones de seguimiento de referencia.</span><span class="sxs-lookup"><span data-stu-id="f0302-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0302-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="f0302-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="f0302-119">La interfaz <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> y sus métodos no se admiten en Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f0302-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0302-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="f0302-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="f0302-121">La interfaz de dispositivo de seguimiento establece la información de seguimiento del sombreador, que permite el registro y la reproducción precisos de la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="f0302-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f0302-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0302-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0302-123">Referencia de capas</span><span class="sxs-lookup"><span data-stu-id="f0302-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





