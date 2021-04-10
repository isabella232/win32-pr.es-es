---
title: Instrucciones de extensión de nombre de archivo
description: Instrucciones de extensión de nombre de archivo
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- SDK de Windows Media Format, extensiones de nombre de archivo
- Advanced Systems Format (ASF), extensiones de nombre de archivo
- ASF (formato de sistemas avanzados), extensiones de nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994182"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="75651-106">Instrucciones de extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="75651-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="75651-107">Una extensión de nombre de archivo proporciona a un fabricante de software independiente información sobre los requisitos de representación de una aplicación que utiliza esa extensión concreta.</span><span class="sxs-lookup"><span data-stu-id="75651-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="75651-108">La extensión de nombre de archivo que se debe usar para un archivo creado por una aplicación basada en el SDK de Windows Media Format viene determinada por el tipo de contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="75651-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="75651-109">Use la siguiente lógica para determinar la extensión de nombre de archivo que debe usar.</span><span class="sxs-lookup"><span data-stu-id="75651-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="75651-110">Si el archivo contiene secuencias codificadas con códecs de terceros o datos sin comprimir no admitidos (incluidos los datos arbitrarios), el archivo debe utilizar la extensión. ASF.</span><span class="sxs-lookup"><span data-stu-id="75651-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="75651-111">Si el archivo no contiene secuencias no compatibles y contiene una o varias secuencias de vídeo descomprimidas o codificadas con un códec de vídeo de Windows Media, el archivo debe usar la extensión. wmv.</span><span class="sxs-lookup"><span data-stu-id="75651-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="75651-112">Estos archivos también pueden incluir secuencias de audio PCM, secuencias de audio codificadas con cualquier códec de audio de Windows Media, secuencias de scripts y secuencias Web.</span><span class="sxs-lookup"><span data-stu-id="75651-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="75651-113">Si el archivo no contiene secuencias no compatibles y no hay secuencias de vídeo compatibles, y contiene una o varias secuencias de audio descomprimidos PCM o codificadas con cualquier códec de audio de Windows Media, el archivo debe usar la extensión. WMA.</span><span class="sxs-lookup"><span data-stu-id="75651-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="75651-114">Estos archivos también pueden contener secuencias de scripts y secuencias Web.</span><span class="sxs-lookup"><span data-stu-id="75651-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="75651-115">Si el archivo solo contiene flujos que no son audio ni vídeo, debe utilizar la extensión. ASF.</span><span class="sxs-lookup"><span data-stu-id="75651-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="75651-116">Los tipos de vídeo sin comprimir admitidos son RGB8, RGB565, RGB555, RGB24, RGB32, i420, IYUV, YV12, YUY2, UYVY, YVYU y YVU9.</span><span class="sxs-lookup"><span data-stu-id="75651-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75651-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75651-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75651-118">**Consideraciones del proyecto**</span><span class="sxs-lookup"><span data-stu-id="75651-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




