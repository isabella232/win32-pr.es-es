---
title: Protocolo WMPDVD
description: Protocolo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolos
- Modelo de objetos de Windows Media Player, protocolos
- modelo de objetos, protocolos
- Control ActiveX de Windows Media Player, protocolos para el modelo de objetos
- Control ActiveX, protocolos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, protocolos para el modelo de objetos
- Windows Media Player Mobile, protocolos para el modelo de objetos
- protocolos, modelo de objetos de Windows Media Player
- protocolos, WMPDVD
- Protocolo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357019"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="bdc99-113">Protocolo WMPDVD</span><span class="sxs-lookup"><span data-stu-id="bdc99-113">WMPDVD Protocol</span></span>

<span data-ttu-id="bdc99-114">El protocolo WMPDVD le permite especificar medios desde un DVD mediante la sintaxis de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="bdc99-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="bdc99-115">Esta es la forma general del Protocolo:</span><span class="sxs-lookup"><span data-stu-id="bdc99-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="bdc99-116">El segmento de la *unidad* es la letra de la unidad de DVD; no incluye los dos puntos que se suelen usar con especificadores de unidad.</span><span class="sxs-lookup"><span data-stu-id="bdc99-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="bdc99-117">Este segmento siempre es necesario.</span><span class="sxs-lookup"><span data-stu-id="bdc99-117">This segment is always required.</span></span>

<span data-ttu-id="bdc99-118">El segmento de *título* es el número del título que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="bdc99-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="bdc99-119">No es necesario a menos que desee iniciar la reproducción en un título específico o en un capítulo específico de un título específico.</span><span class="sxs-lookup"><span data-stu-id="bdc99-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="bdc99-120">El segmento de *capítulo* es el número del capítulo que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="bdc99-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="bdc99-121">No es necesario a menos que desee iniciar la reproducción en un capítulo específico de un título específico.</span><span class="sxs-lookup"><span data-stu-id="bdc99-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="bdc99-122">El argumento contentdir y es la ruta de acceso a un vídeo \_ TS. Archivo IFO, que puede estar en el almacenamiento local o en un recurso compartido de red.</span><span class="sxs-lookup"><span data-stu-id="bdc99-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="bdc99-123">Si incluye este segmento, el segmento de la *unidad* se omite aunque siga siendo necesario.</span><span class="sxs-lookup"><span data-stu-id="bdc99-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="bdc99-124">Si también incluye el segmento de *título* o los segmentos de *título* y *capítulo* , son relativos al contenido del DVD especificado en el segmento contentdir y, no al segmento de la *unidad* .</span><span class="sxs-lookup"><span data-stu-id="bdc99-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="bdc99-125">En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el DVD desde el principio, como si se iniciara automáticamente.</span><span class="sxs-lookup"><span data-stu-id="bdc99-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="bdc99-126">En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el DVD desde el principio del título especificado.</span><span class="sxs-lookup"><span data-stu-id="bdc99-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="bdc99-127">En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el DVD del capítulo especificado.</span><span class="sxs-lookup"><span data-stu-id="bdc99-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="bdc99-128">En el ejemplo siguiente se usa el protocolo WMPDVD para reproducir el contenido del DVD del almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="bdc99-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="bdc99-129">La cadena de *ruta de acceso* finaliza con la carpeta que contiene el vídeo \_ TS. Archivo IFO; no incluye el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="bdc99-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="bdc99-130">En este ejemplo, el valor del segmento de *unidad* no tiene ningún efecto aunque sea necesario y la reproducción comienza en el capítulo 4 del título 2.</span><span class="sxs-lookup"><span data-stu-id="bdc99-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="bdc99-131">La asignación de una cadena WMPDVD a la propiedad **URL** requiere Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="bdc99-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc99-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdc99-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc99-133">**Tipos de archivos y protocolos admitidos**</span><span class="sxs-lookup"><span data-stu-id="bdc99-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




