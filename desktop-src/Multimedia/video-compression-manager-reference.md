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
# <a name="video-compression-manager-reference"></a>Referencia del administrador de compresión de vídeo

En esta sección se describen las funciones, las estructuras, los mensajes y las macros, asociados a VCM. Estos elementos se agrupan de la siguiente manera.

## <a name="compressor-installation-and-removal"></a>Instalación y eliminación del compresor

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Buscar y abrir un compresor

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Seleccionar compresores

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Configurar compresores

-   [**configuración de ICM \_**](icm-configure.md)
-   [**\_GETSTATE ICM**](icm-getstate.md)
-   [**ICM \_ SETSTATE**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Información del compresor

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**\_GETDEFAULTKEYFRAMERATE ICM**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**\_GETDEFAULTQUALITY ICM**](icm-getdefaultquality.md)
-   [**\_acerca de**](icm-about.md)

## <a name="single-image-compression"></a>Compresión de una sola imagen

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Compresión de secuencia

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Compresión de datos de imagen

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**\_formato de compresión ICM \_ Get \_**](icm-compress-get-format.md)
-   [**\_consulta de compresión ICM \_**](icm-compress-query.md)
-   [**\_ \_ obtener tamaño de compresión ICM \_**](icm-compress-get-size.md)
-   [**\_Inicio de compress de ICM \_**](icm-compress-begin.md)
-   [**\_fin de comprimir ICM \_**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Supervisión del compresor

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Descomprimir imágenes únicas

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Descomprimir datos de imagen

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_fin de DECOMPRESSEX ICM \_**](icm-decompressex-end.md)
-   [**\_ \_ obtener formato de DEScompresión ICM \_**](icm-decompress-get-format.md)
-   [**\_paleta de \_ obtención de compresión ICM \_**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**Inicio de la \_ descompresión de ICM \_**](icm-decompress-begin.md)
-   [**\_fin de descomprimir ICM \_**](icm-decompress-end.md)
-   [**\_consulta de descompresión ICM \_**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Uso de funciones de Hardware-Drawing

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_final del dibujo ICM \_**](icm-draw-end.md)
-   [**\_vaciado de dibujo de ICM \_**](icm-draw-flush.md)
-   [**\_consulta de Draw ICM \_**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_Inicio de dibujo de ICM \_**](icm-draw-start.md)
-   [**\_detención de Draw ICM \_**](icm-draw-stop.md)
-   [**\_GETBUFFERSWANTED ICM**](icm-getbufferswanted.md)
-   [**\_realización del dibujo ICM \_**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**\_GETTIME de dibujo ICM \_**](icm-draw-gettime.md)
-   [**dibujar seicm \_ \_ SETTIME**](icm-draw-settime.md)
-   [**\_ventana dibujo \_ ICM**](icm-draw-window.md)
-   [**\_realización del dibujo ICM \_**](icm-draw-realize.md)
-   [**\_CHANGEPALETTE ICM Draw \_**](icm-draw-changepalette.md)
-   [**\_RENDERBUFFER ICM Draw \_**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> </dl>

 

 




