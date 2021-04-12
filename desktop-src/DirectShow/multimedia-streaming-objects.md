---
description: Objetos de streaming multimedia
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Objetos de streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361936"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="b80a9-103">Objetos de streaming multimedia</span><span class="sxs-lookup"><span data-stu-id="b80a9-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="b80a9-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="b80a9-104">This API is deprecated.</span></span> <span data-ttu-id="b80a9-105">Las nuevas aplicaciones no deben utilizarla.</span><span class="sxs-lookup"><span data-stu-id="b80a9-105">New applications should not use it.</span></span>

 

<span data-ttu-id="b80a9-106">En la tabla siguiente se describen los objetos de streaming multimedia.</span><span class="sxs-lookup"><span data-stu-id="b80a9-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b80a9-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="b80a9-107">CLSID</span></span></th>
<th><span data-ttu-id="b80a9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b80a9-108">Description</span></span></th>
<th><span data-ttu-id="b80a9-109">Interfaces admitidas</span><span class="sxs-lookup"><span data-stu-id="b80a9-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b80a9-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="b80a9-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="b80a9-111">Puede crear ejemplos de medios para cualquier tipo de datos compatible con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b80a9-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b80a9-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="b80a9-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="b80a9-117">Implementación del objeto contenedor de audio <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b80a9-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b80a9-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="b80a9-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="b80a9-120">Secuencia multimedia de DirectDraw que se puede Agregar a una secuencia de multimedia de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b80a9-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b80a9-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="b80a9-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="b80a9-127">Implementación de DirectShow de la secuencia de multimedia.</span><span class="sxs-lookup"><span data-stu-id="b80a9-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b80a9-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="b80a9-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="b80a9-131">Proporciona la funcionalidad de streaming multimedia para el objeto CLSID_AMMultiMediaStream a través de la interfaz <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b80a9-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b80a9-133">N/D</span><span class="sxs-lookup"><span data-stu-id="b80a9-133">N/A</span></span></td>
<td><span data-ttu-id="b80a9-134">Ejemplos creados por el objeto CLSID_AMMediaTypeStream.</span><span class="sxs-lookup"><span data-stu-id="b80a9-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b80a9-138">N/D</span><span class="sxs-lookup"><span data-stu-id="b80a9-138">N/A</span></span></td>
<td><span data-ttu-id="b80a9-139">Ejemplos creados por el flujo de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="b80a9-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="b80a9-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="b80a9-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="b80a9-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



