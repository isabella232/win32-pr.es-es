---
title: Acerca de los controladores de archivos y secuencias personalizados
description: Acerca de los controladores de archivos y secuencias personalizados
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
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
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903860"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="31ea1-111">Acerca de los controladores de archivos y secuencias personalizados</span><span class="sxs-lookup"><span data-stu-id="31ea1-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="31ea1-112">La aplicación puede usar un controlador de archivos personalizado para leer de un archivo o escribir en un archivo que se encuentra en un formato no estándar.</span><span class="sxs-lookup"><span data-stu-id="31ea1-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="31ea1-113">Para ello, la aplicación simplemente usa el nombre del controlador de archivos al abrir el archivo o asignar la interfaz de archivo.</span><span class="sxs-lookup"><span data-stu-id="31ea1-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="31ea1-114">A continuación, la biblioteca AVIFile usa las funciones del controlador de archivos en lugar de las de otro controlador de archivos.</span><span class="sxs-lookup"><span data-stu-id="31ea1-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="31ea1-115">El formato no estándar aparece como datos AVI estándar en la aplicación o en cualquier otra aplicación mediante el controlador de archivos personalizado.</span><span class="sxs-lookup"><span data-stu-id="31ea1-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="31ea1-116">Del mismo modo, la aplicación puede usar un controlador de flujo personalizado para leer una secuencia que se encuentra en un formato no estándar.</span><span class="sxs-lookup"><span data-stu-id="31ea1-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="31ea1-117">Un flujo, ya sea que constituye audio, vídeo, MIDI, texto o datos personalizados, es un componente de un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="31ea1-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="31ea1-118">Por ejemplo, un archivo AVI que contiene una secuencia de vídeo, una banda sonora en inglés y una banda sonora en francés consta de tres flujos.</span><span class="sxs-lookup"><span data-stu-id="31ea1-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="31ea1-119">La aplicación puede especificar las secuencias en un archivo AVI para procesar y dirigir cada una de ellas a un controlador que puede procesar de forma óptima el tipo adecuado de datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="31ea1-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="31ea1-120">Debe colocar los controladores de archivos y secuencias personalizados en uno o varios archivos dll, separados de los archivos de aplicación principales.</span><span class="sxs-lookup"><span data-stu-id="31ea1-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




