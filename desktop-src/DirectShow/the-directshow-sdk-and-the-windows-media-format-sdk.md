---
description: El SDK de DirectShow y el SDK de Windows Media Format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: El SDK de DirectShow y el SDK de Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361931"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>El SDK de DirectShow y el SDK de Windows Media Format

DirectShow y el SDK de Windows Media Format ofrecen soluciones complementarias para escribir aplicaciones que crean y reproducen secuencias de formato de Windows Media. Para obtener más información, vea la sección "[audio y vídeo](../audio-and-video.md)" de MSDN Library.

El filtro del escritor ASF acepta cualquier número de flujos de entrada y crea un archivo ASF. El filtro usa el SDK de Windows Media Format para convertir archivos de audio o vídeo sin comprimir en contenido basado en Windows Media. El contenido comprimido se almacena en el formato de contenedor ASF. Si el contenido es solo de audio, el archivo recibe una extensión. WMA y se conoce como archivo de Windows Media Audio. Si el contenido es solo de vídeo o de vídeo y audio, el archivo recibe una extensión. WMV y se conoce como archivo de Windows Media Video. Cualquier tipo de archivo también puede incluir metadatos.

Puede usar el escritor ASF de WM en varios escenarios, como la captura Audio-Video de vídeo digital (DV), la recompresión de audio y la conversión de archivos multimedia intercalados (AVI) o MPEG para la transmisión por secuencias de la red. Este filtro proporciona la única manera de crear archivos de Microsoft® Windows Media™ Audio (WMA) y Windows Media Video (WMV) en DirectShow®. El filtro también puede crear archivos protegidos por Rights Management digitales (DRM), y también puede crear contenido MPEG-4 mediante el codificador MPEG-4 de Microsoft. Este contenido se almacena en formato de contenedor ASF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
