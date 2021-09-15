---
title: Referencia del Administrador de compresión de vídeo
description: Referencia del Administrador de compresión de vídeo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Vídeo para Windows (VFW), administrador de compresión de vídeo (VCM)
- VFW (vídeo para Windows),administrador de compresión de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476774"
---
# <a name="video-compression-manager-reference"></a>Referencia del Administrador de compresión de vídeo

En esta sección se describen las funciones, estructuras, mensajes y macros asociados a VCM. Estos elementos se agrupan como se muestra a continuación.

## <a name="compressor-installation-and-removal"></a>Instalación y eliminación de la instalación y eliminación de instalaciones

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Buscar y abrir un archivo Desenlazador

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressAbrir**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Selección de la opción Desafuerciones

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Configuración de los trastes

-   [**\_ICM CONFIGURAR**](icm-configure.md)
-   [**\_ICM GETSTATE**](icm-getstate.md)
-   [**\_ICM SETSTATE**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Información sobre el resalte

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**\_ICM GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**\_ICM GETDEFAULTQUALITY**](icm-getdefaultquality.md)
-   [**\_ICM ACERCA DE**](icm-about.md)

## <a name="single-image-compression"></a>Compresión de imagen única

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Compresión de secuencia

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Compresión de datos de imagen

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**\_ICM COMPRIMIR \_ GET \_ FORMAT**](icm-compress-get-format.md)
-   [**\_ICM COMPRESS \_ QUERY**](icm-compress-query.md)
-   [**\_ICM COMPRIMIR \_ GET \_ SIZE**](icm-compress-get-size.md)
-   [**\_ICM COMPRESS \_ BEGIN**](icm-compress-begin.md)
-   [**\_ICM COMPRESS \_ END**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Supervisión de supervisión de supervisión

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Descompresión de imágenes únicas

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Descompresión de datos de imagen

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_ICM DECOMPRESSEX \_ END**](icm-decompressex-end.md)
-   [**\_ICM OBTENER FORMATO DE DESCOMPRESIÓN \_ \_**](icm-decompress-get-format.md)
-   [**\_ICM DESCOMPRESIÓN \_ DE LA PALETA GET \_**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**\_ICM DECOMPRESS \_ BEGIN**](icm-decompress-begin.md)
-   [**\_ICM DESCOMPRESIÓN \_ FINAL**](icm-decompress-end.md)
-   [**\_ICM CONSULTA DE DESCOMPRESIÓN \_**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Uso de Hardware-Drawing funcionalidades

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_ICM DRAW \_ END**](icm-draw-end.md)
-   [**\_ICM DRAW \_ FLUSH**](icm-draw-flush.md)
-   [**\_ICM DRAW \_ QUERY**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_ICM DRAW \_ START**](icm-draw-start.md)
-   [**\_ICM DRAW \_ STOP**](icm-draw-stop.md)
-   [**\_ICM GETBUFFERSWANTED**](icm-getbufferswanted.md)
-   [**\_ICM DRAW \_ REALIZE**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**\_ICM DRAW \_ GETTIME**](icm-draw-gettime.md)
-   [**\_ICM DRAW \_ SETTIME**](icm-draw-settime.md)
-   [**\_ICM VENTANA \_ DIBUJAR**](icm-draw-window.md)
-   [**\_ICM DRAW \_ REALIZE**](icm-draw-realize.md)
-   [**\_ICM DRAW \_ CHANGEPALETTE**](icm-draw-changepalette.md)
-   [**\_ICM DRAW \_ RENDERBUFFER**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> </dl>

 

 




