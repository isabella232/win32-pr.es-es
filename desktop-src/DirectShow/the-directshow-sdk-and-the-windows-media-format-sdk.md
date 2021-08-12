---
description: El SDK DirectShow y el SDK de Windows Media Format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: El SDK DirectShow y el SDK de Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651763"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>El SDK DirectShow y el SDK de Windows Media Format

DirectShow y el SDK Windows Media Format ofrecen soluciones complementarias para escribir aplicaciones que crean y reproducen Windows de formato multimedia. Para obtener más información, vea la sección["Audio y vídeo"](../audio-and-video.md)de MSDN Library.

El filtro ASF Writer acepta cualquier número de flujos de entrada y crea un archivo ASF. El filtro usa el SDK Windows Media Format para convertir archivos de audio o vídeo sin comprimir en Windows contenido basado en multimedia. A continuación, el contenido comprimido se almacena en el formato de contenedor de ASF. Si el contenido es solo audio, se le da una extensión .wma al archivo y se le conoce como un archivo Windows Media Audio. Si el contenido es solo vídeo o vídeo y audio, se le da una extensión .wmv y se conoce como un archivo Windows Media Video. Cualquier tipo de archivo también puede incluir metadatos.

Puede usar WM ASF Writer en varios escenarios, como la captura de vídeo digital (DV), la recom Audio-Video presión de audio y la conversión de archivos multimedia intercalados (AVI) o MPEG para el streaming de red. Este filtro proporciona la única manera de crear archivos de Microsoft® Windows Media™ Audio (WMA) y Windows Media Video (WMV) en DirectShow®. El filtro también puede crear archivos protegidos por Digital Rights Management (DRM) y también puede crear contenido MPEG-4 mediante el codificador Microsoft MPEG-4. Este contenido se almacena en el formato de contenedor de ASF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
