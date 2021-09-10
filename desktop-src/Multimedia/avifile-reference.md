---
title: Referencia de AVIFile
description: Referencia de AVIFile
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369847"
---
# <a name="avifile-reference"></a>Referencia de AVIFile

En esta sección se describen las funciones, estructuras y macros de las aplicaciones que usan los servicios AVIFile. Estos elementos se agrupan de la siguiente manera:

## <a name="avifile-library-operations"></a>Operaciones de la biblioteca AVIFile

-   [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a>Abrir y cerrar archivos AVI

-   [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a>Lectura desde un archivo

-   [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a>Escribir en un archivo

-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a>Uso del Portapapeles

-   [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a>Apertura y cierre Secuencias

-   [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a>Lectura de la información de stream

-   [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a>Descompresión de datos de vídeo en una secuencia

-   [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a>Crear un archivo a partir de una Secuencias

-   [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a>Escribir datos individuales Secuencias

-   [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a>Buscar la posición inicial en un flujo

-   [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a>Buscar fotogramas clave y ejemplo

-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a>Cambiar entre muestras y tiempo

-   [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a>Creación de una Secuencias

-   [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a>Edición de Secuencias AVI

-   [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones y macros AVIFile](avifile-functions-and-macros.md)
</dt> </dl>

 

 




