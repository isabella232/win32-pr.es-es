---
description: Principales tipos de medios
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Principales tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003404"
---
# <a name="major-media-types"></a><span data-ttu-id="3b81a-103">Principales tipos de medios</span><span class="sxs-lookup"><span data-stu-id="3b81a-103">Major Media Types</span></span>

<span data-ttu-id="3b81a-104">En un tipo de medio, el *tipo principal* describe la categoría general de los datos, como audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b81a-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="3b81a-105">El *subtipo*, si está presente, refina aún más el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="3b81a-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="3b81a-106">Por ejemplo, si el tipo principal es vídeo, el subtipo podría ser un vídeo RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3b81a-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="3b81a-107">Los subtipos también distinguen los formatos codificados, como el vídeo H. 264, de los formatos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="3b81a-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="3b81a-108">El tipo principal y el subtipo se identifican mediante GUID y se almacenan en los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="3b81a-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="3b81a-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="3b81a-109">Attribute</span></span>                                             | <span data-ttu-id="3b81a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b81a-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="3b81a-111">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="3b81a-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="3b81a-112">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="3b81a-112">Major type.</span></span> |
| [<span data-ttu-id="3b81a-113">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="3b81a-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="3b81a-114">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="3b81a-114">Subtype.</span></span>    |



 

<span data-ttu-id="3b81a-115">Se definen los siguientes tipos principales.</span><span class="sxs-lookup"><span data-stu-id="3b81a-115">The following major types are defined.</span></span>



| <span data-ttu-id="3b81a-116">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="3b81a-116">Major Type</span></span>                    | <span data-ttu-id="3b81a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b81a-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="3b81a-118">Subtipos</span><span class="sxs-lookup"><span data-stu-id="3b81a-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b81a-119">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3b81a-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="3b81a-120">Audio.</span><span class="sxs-lookup"><span data-stu-id="3b81a-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="3b81a-121">[GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3b81a-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="3b81a-122">**\_Binario MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3b81a-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="3b81a-123">Secuencia binaria.</span><span class="sxs-lookup"><span data-stu-id="3b81a-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="3b81a-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b81a-124">None.</span></span>                                                |
| <span data-ttu-id="3b81a-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="3b81a-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="3b81a-126">Flujo que contiene archivos de datos.</span><span class="sxs-lookup"><span data-stu-id="3b81a-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="3b81a-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b81a-127">None.</span></span>                                                |
| <span data-ttu-id="3b81a-128">**MFMediaType \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="3b81a-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="3b81a-129">Secuencia HTML.</span><span class="sxs-lookup"><span data-stu-id="3b81a-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="3b81a-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b81a-130">None.</span></span>                                                |
| <span data-ttu-id="3b81a-131">**Imagen de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="3b81a-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="3b81a-132">Secuencia de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="3b81a-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="3b81a-133">[GUID y CLSID de WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="3b81a-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="3b81a-134">**MFMediaType \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="3b81a-134">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="3b81a-135">Medios protegidos.</span><span class="sxs-lookup"><span data-stu-id="3b81a-135">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="3b81a-136">El subtipo especifica el esquema de protección de contenido.</span><span class="sxs-lookup"><span data-stu-id="3b81a-136">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="3b81a-137">**Percepción de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="3b81a-137">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="3b81a-138">Secuencias de un sensor de cámara o una unidad de procesamiento que motiva y comprende datos de vídeo sin procesar y que proporciona información sobre el entorno o los seres humanos que contiene.</span><span class="sxs-lookup"><span data-stu-id="3b81a-138">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="3b81a-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b81a-139">None.</span></span>                                                |
| <span data-ttu-id="3b81a-140">**MFMediaType \_ Sami**</span><span class="sxs-lookup"><span data-stu-id="3b81a-140">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="3b81a-141">Subtítulos de intercambio de medios accesibles (SAMI) sincronizados.</span><span class="sxs-lookup"><span data-stu-id="3b81a-141">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="3b81a-142">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b81a-142">None.</span></span>                                                |
| <span data-ttu-id="3b81a-143">**\_Script MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3b81a-143">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="3b81a-144">Secuencia de script.</span><span class="sxs-lookup"><span data-stu-id="3b81a-144">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="3b81a-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b81a-145">None.</span></span>                                                |
| <span data-ttu-id="3b81a-146">**\_Flujo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3b81a-146">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="3b81a-147">Secuencia multiplexada o secuencia elemental.</span><span class="sxs-lookup"><span data-stu-id="3b81a-147">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="3b81a-148">GUID de subtipos de secuencia</span><span class="sxs-lookup"><span data-stu-id="3b81a-148">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="3b81a-149">**Vídeo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="3b81a-149">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="3b81a-150">Video.</span><span class="sxs-lookup"><span data-stu-id="3b81a-150">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="3b81a-151">[GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3b81a-151">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="3b81a-152">Los componentes de terceros pueden definir nuevos tipos principales y subtipos nuevos.</span><span class="sxs-lookup"><span data-stu-id="3b81a-152">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b81a-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b81a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b81a-154">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3b81a-154">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="3b81a-155">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="3b81a-155">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
