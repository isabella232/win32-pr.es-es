---
description: Tipos de medios principales
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Tipos de medios principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549580"
---
# <a name="major-media-types"></a><span data-ttu-id="d1ca8-103">Tipos de medios principales</span><span class="sxs-lookup"><span data-stu-id="d1ca8-103">Major Media Types</span></span>

<span data-ttu-id="d1ca8-104">En un tipo de medio, el *tipo principal* describe la categoría general de los datos, como audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="d1ca8-105">El *subtipo*, si está presente, refina aún más el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="d1ca8-106">Por ejemplo, si el tipo principal es vídeo, el subtipo podría ser vídeo RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="d1ca8-107">Los subtipos también distinguen los formatos codificados, como el vídeo H.264, de los formatos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="d1ca8-108">El tipo principal y el subtipo se identifican mediante GUID y se almacenan en los atributos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d1ca8-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="d1ca8-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="d1ca8-109">Attribute</span></span>                                             | <span data-ttu-id="d1ca8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1ca8-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="d1ca8-111">TIPO \_ PRINCIPAL DE MT \_ DE \_ MF</span><span class="sxs-lookup"><span data-stu-id="d1ca8-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="d1ca8-112">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-112">Major type.</span></span> |
| [<span data-ttu-id="d1ca8-113">\_SUBTIPO DE MT DE MF \_</span><span class="sxs-lookup"><span data-stu-id="d1ca8-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="d1ca8-114">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-114">Subtype.</span></span>    |



 

<span data-ttu-id="d1ca8-115">Se definen los siguientes tipos principales.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-115">The following major types are defined.</span></span>



| <span data-ttu-id="d1ca8-116">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="d1ca8-116">Major Type</span></span>                    | <span data-ttu-id="d1ca8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1ca8-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="d1ca8-118">Subtipos</span><span class="sxs-lookup"><span data-stu-id="d1ca8-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1ca8-119">**MFMediaType \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="d1ca8-120">Audio.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="d1ca8-121">[GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d1ca8-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="d1ca8-122">**MFMediaType \_ Binary**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="d1ca8-123">Secuencia binaria.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="d1ca8-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-124">None.</span></span>                                                |
| <span data-ttu-id="d1ca8-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="d1ca8-126">Secuencia que contiene archivos de datos.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="d1ca8-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-127">None.</span></span>                                                |
| <span data-ttu-id="d1ca8-128">**MFMediaType \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="d1ca8-129">Secuencia HTML.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="d1ca8-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-130">None.</span></span>                                                |
| <span data-ttu-id="d1ca8-131">**Imagen \_ MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="d1ca8-132">Todavía secuencia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="d1ca8-133">[GUID de WIC y CLID](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="d1ca8-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="d1ca8-134">**Metadatos de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="d1ca8-135">Flujo de metadatos.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="d1ca8-136">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-136">None.</span></span>       |
| <span data-ttu-id="d1ca8-137">**MFMediaType \_ Protected**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="d1ca8-138">Medios protegidos.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="d1ca8-139">El subtipo especifica el esquema de protección de contenido.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="d1ca8-140">**MFMediaType \_ Perception**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="d1ca8-141">Secuencias desde un sensor de cámara o una unidad de procesamiento que explican y entienden los datos de vídeo sin procesar y proporcionan información sobre el entorno o los seres humanos que contiene.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="d1ca8-142">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-142">None.</span></span>                                                |
| <span data-ttu-id="d1ca8-143">**MFMediaType \_ SAMI**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="d1ca8-144">Títulos de intercambio multimedia accesible sincronizado (SAMI).</span><span class="sxs-lookup"><span data-stu-id="d1ca8-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="d1ca8-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-145">None.</span></span>                                                |
| <span data-ttu-id="d1ca8-146">**MFMediaType \_ Script**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="d1ca8-147">Secuencia de scripts.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="d1ca8-148">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-148">None.</span></span>                                                |
| <span data-ttu-id="d1ca8-149">**Flujo \_ MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="d1ca8-150">Secuencia multiplexada o secuencia elemental.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="d1ca8-151">GUID de subtipo de secuencia</span><span class="sxs-lookup"><span data-stu-id="d1ca8-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="d1ca8-152">**VÍDEO \_ MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="d1ca8-153">Video.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="d1ca8-154">[GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d1ca8-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="d1ca8-155">Los componentes de terceros pueden definir nuevos tipos principales y nuevos subtipos.</span><span class="sxs-lookup"><span data-stu-id="d1ca8-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1ca8-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1ca8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1ca8-157">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1ca8-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d1ca8-158">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="d1ca8-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
