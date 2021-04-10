---
title: Referencia del administrador de compresión de vídeo
description: Referencia del administrador de compresión de vídeo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Vídeo para Windows (VFW), administrador de compresión de vídeo (VCM)
- VFW (vídeo para Windows), administrador de compresión de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268467"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="e7888-105">Referencia del administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e7888-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="e7888-106">En esta sección se describen las funciones, las estructuras, los mensajes y las macros, asociados a VCM.</span><span class="sxs-lookup"><span data-stu-id="e7888-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="e7888-107">Estos elementos se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="e7888-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="e7888-108">Instalación y eliminación del compresor</span><span class="sxs-lookup"><span data-stu-id="e7888-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="e7888-109">**ICInstall**</span><span class="sxs-lookup"><span data-stu-id="e7888-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="e7888-110">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="e7888-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="e7888-111">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="e7888-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="e7888-112">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="e7888-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="e7888-113">**ICRemove**</span><span class="sxs-lookup"><span data-stu-id="e7888-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="e7888-114">**ICOpenFunction**</span><span class="sxs-lookup"><span data-stu-id="e7888-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="e7888-115">Buscar y abrir un compresor</span><span class="sxs-lookup"><span data-stu-id="e7888-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="e7888-116">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="e7888-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="e7888-117">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="e7888-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="e7888-118">**ICDecompressOpen**</span><span class="sxs-lookup"><span data-stu-id="e7888-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="e7888-119">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="e7888-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="e7888-120">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="e7888-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="e7888-121">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="e7888-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="e7888-122">Seleccionar compresores</span><span class="sxs-lookup"><span data-stu-id="e7888-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="e7888-123">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="e7888-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="e7888-124">**ICCompressorFree**</span><span class="sxs-lookup"><span data-stu-id="e7888-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="e7888-125">**COMPVARS**</span><span class="sxs-lookup"><span data-stu-id="e7888-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="e7888-126">Configurar compresores</span><span class="sxs-lookup"><span data-stu-id="e7888-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="e7888-127">**configuración de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="e7888-128">**\_GETSTATE ICM**</span><span class="sxs-lookup"><span data-stu-id="e7888-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="e7888-129">**ICM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="e7888-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="e7888-130">**ICSendMessage**</span><span class="sxs-lookup"><span data-stu-id="e7888-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="e7888-131">Información del compresor</span><span class="sxs-lookup"><span data-stu-id="e7888-131">Compressor Information</span></span>

-   [<span data-ttu-id="e7888-132">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7888-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="e7888-133">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="e7888-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="e7888-134">**\_GETDEFAULTKEYFRAMERATE ICM**</span><span class="sxs-lookup"><span data-stu-id="e7888-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="e7888-135">**ICGetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="e7888-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="e7888-136">**\_GETDEFAULTQUALITY ICM**</span><span class="sxs-lookup"><span data-stu-id="e7888-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="e7888-137">**\_acerca de**</span><span class="sxs-lookup"><span data-stu-id="e7888-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="e7888-138">Compresión de una sola imagen</span><span class="sxs-lookup"><span data-stu-id="e7888-138">Single Image Compression</span></span>

-   [<span data-ttu-id="e7888-139">**ICImageCompress**</span><span class="sxs-lookup"><span data-stu-id="e7888-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="e7888-140">Compresión de secuencia</span><span class="sxs-lookup"><span data-stu-id="e7888-140">Sequence Compression</span></span>

-   [<span data-ttu-id="e7888-141">**ICSeqCompressFrame**</span><span class="sxs-lookup"><span data-stu-id="e7888-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="e7888-142">**ICSeqCompressFrameStart**</span><span class="sxs-lookup"><span data-stu-id="e7888-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="e7888-143">**ICSeqCompressFrameEnd**</span><span class="sxs-lookup"><span data-stu-id="e7888-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="e7888-144">COMPVARS</span><span class="sxs-lookup"><span data-stu-id="e7888-144">COMPVARS</span></span>

-   [<span data-ttu-id="e7888-145">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="e7888-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="e7888-146">Compresión de datos de imagen</span><span class="sxs-lookup"><span data-stu-id="e7888-146">Image Data Compression</span></span>

-   [<span data-ttu-id="e7888-147">**ICCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="e7888-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="e7888-148">**\_formato de compresión ICM \_ Get \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="e7888-149">**\_consulta de compresión ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="e7888-150">**\_ \_ obtener tamaño de compresión ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="e7888-151">**\_Inicio de compress de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="e7888-152">**\_fin de comprimir ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="e7888-153">Supervisión del compresor</span><span class="sxs-lookup"><span data-stu-id="e7888-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="e7888-154">**ICSETSTATUSPROC**</span><span class="sxs-lookup"><span data-stu-id="e7888-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="e7888-155">Descomprimir imágenes únicas</span><span class="sxs-lookup"><span data-stu-id="e7888-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="e7888-156">**ICImageDecompress**</span><span class="sxs-lookup"><span data-stu-id="e7888-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="e7888-157">Descomprimir datos de imagen</span><span class="sxs-lookup"><span data-stu-id="e7888-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="e7888-158">**ICDECOMPRESSEX**</span><span class="sxs-lookup"><span data-stu-id="e7888-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="e7888-159">**ICDecompressExBegin**</span><span class="sxs-lookup"><span data-stu-id="e7888-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="e7888-160">**\_fin de DECOMPRESSEX ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="e7888-161">**\_ \_ obtener formato de DEScompresión ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="e7888-162">**\_paleta de \_ obtención de compresión ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="e7888-163">**ICDecompressExQuery**</span><span class="sxs-lookup"><span data-stu-id="e7888-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="e7888-164">**ICDECOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="e7888-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="e7888-165">**Inicio de la \_ descompresión de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="e7888-166">**\_fin de descomprimir ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="e7888-167">**\_consulta de descompresión ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="e7888-168">Uso de funciones de Hardware-Drawing</span><span class="sxs-lookup"><span data-stu-id="e7888-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="e7888-169">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7888-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="e7888-170">**ICDRAWBEGIN**</span><span class="sxs-lookup"><span data-stu-id="e7888-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="e7888-171">**\_final del dibujo ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="e7888-172">**\_vaciado de dibujo de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="e7888-173">**\_consulta de Draw ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="e7888-174">**ICDrawSuggestFormat**</span><span class="sxs-lookup"><span data-stu-id="e7888-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="e7888-175">**\_Inicio de dibujo de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="e7888-176">**\_detención de Draw ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="e7888-177">**\_GETBUFFERSWANTED ICM**</span><span class="sxs-lookup"><span data-stu-id="e7888-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="e7888-178">**\_realización del dibujo ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="e7888-179">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="e7888-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="e7888-180">**ICDRAW**</span><span class="sxs-lookup"><span data-stu-id="e7888-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="e7888-181">**\_GETTIME de dibujo ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="e7888-182">**dibujar seicm \_ \_ SETTIME**</span><span class="sxs-lookup"><span data-stu-id="e7888-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="e7888-183">**\_ventana dibujo \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="e7888-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="e7888-184">**\_realización del dibujo ICM \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="e7888-185">**\_CHANGEPALETTE ICM Draw \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="e7888-186">**\_RENDERBUFFER ICM Draw \_**</span><span class="sxs-lookup"><span data-stu-id="e7888-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="e7888-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7888-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7888-188">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e7888-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




