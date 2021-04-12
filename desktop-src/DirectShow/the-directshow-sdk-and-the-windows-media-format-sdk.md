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
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="e12ef-103">El SDK de DirectShow y el SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="e12ef-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="e12ef-104">DirectShow y el SDK de Windows Media Format ofrecen soluciones complementarias para escribir aplicaciones que crean y reproducen secuencias de formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e12ef-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="e12ef-105">Para obtener más información, vea la sección "[audio y vídeo](../audio-and-video.md)" de MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="e12ef-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="e12ef-106">El filtro del escritor ASF acepta cualquier número de flujos de entrada y crea un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e12ef-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="e12ef-107">El filtro usa el SDK de Windows Media Format para convertir archivos de audio o vídeo sin comprimir en contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e12ef-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="e12ef-108">El contenido comprimido se almacena en el formato de contenedor ASF.</span><span class="sxs-lookup"><span data-stu-id="e12ef-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="e12ef-109">Si el contenido es solo de audio, el archivo recibe una extensión. WMA y se conoce como archivo de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="e12ef-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="e12ef-110">Si el contenido es solo de vídeo o de vídeo y audio, el archivo recibe una extensión. WMV y se conoce como archivo de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="e12ef-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="e12ef-111">Cualquier tipo de archivo también puede incluir metadatos.</span><span class="sxs-lookup"><span data-stu-id="e12ef-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="e12ef-112">Puede usar el escritor ASF de WM en varios escenarios, como la captura Audio-Video de vídeo digital (DV), la recompresión de audio y la conversión de archivos multimedia intercalados (AVI) o MPEG para la transmisión por secuencias de la red.</span><span class="sxs-lookup"><span data-stu-id="e12ef-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="e12ef-113">Este filtro proporciona la única manera de crear archivos de Microsoft® Windows Media™ Audio (WMA) y Windows Media Video (WMV) en DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="e12ef-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="e12ef-114">El filtro también puede crear archivos protegidos por Rights Management digitales (DRM), y también puede crear contenido MPEG-4 mediante el codificador MPEG-4 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e12ef-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="e12ef-115">Este contenido se almacena en formato de contenedor ASF.</span><span class="sxs-lookup"><span data-stu-id="e12ef-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e12ef-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e12ef-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e12ef-117">Crear archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e12ef-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
