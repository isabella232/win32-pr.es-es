---
title: Controladores personalizados de archivos y secuencias
description: Controladores personalizados de archivos y secuencias
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Vídeo para Windows (VFW), controladores de archivos personalizados
- Vídeo para Windows (VFW), controladores de secuencias personalizados
- Vídeo para Windows (VFW), controladores de archivos
- Vídeo para Windows (VFW), controladores de secuencias
- VFW (vídeo para Windows), controladores de archivos personalizados
- VFW (vídeo para Windows), controladores de secuencias personalizados
- VFW (vídeo para Windows), controladores de archivo
- VFW (vídeo para Windows), controladores de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486870"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="d4ff7-111">Controladores personalizados de archivos y secuencias</span><span class="sxs-lookup"><span data-stu-id="d4ff7-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="d4ff7-112">Los controladores de archivos y secuencias son controladores que proporcionan interfaces coherentes para una aplicación que controla los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d4ff7-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="d4ff7-113">Los controladores de archivos y secuencias incluidos en el sistema operativo usan datos de vídeo y de onda de audio almacenados en archivos de audio-vídeo intercalado (AVI) y de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="d4ff7-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="d4ff7-114">Puede escribir Controladores para permitir que la aplicación escriba u obtenga acceso a los datos multimedia desde otro origen, como un archivo con un formato de propietario, un archivo AVI que se ha expandido para contener flujos de datos adicionales o un controlador que genera sus propios datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d4ff7-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="d4ff7-115">Si tiene un formato de archivo personalizado para los datos AVI que quiere usar con las [funciones y macros de AVIFile](avifile-functions-and-macros.md), debe escribir un controlador personalizado.</span><span class="sxs-lookup"><span data-stu-id="d4ff7-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="d4ff7-116">Acerca de los controladores de archivos y secuencias personalizados</span><span class="sxs-lookup"><span data-stu-id="d4ff7-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="d4ff7-117">Usar controladores de archivos y de secuencias personalizados</span><span class="sxs-lookup"><span data-stu-id="d4ff7-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="d4ff7-118">Referencia del controlador de archivos y secuencias personalizados</span><span class="sxs-lookup"><span data-stu-id="d4ff7-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 




