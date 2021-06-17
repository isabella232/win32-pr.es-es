---
title: Atributos con varios valores (Windows Media Format SDK 11)
description: Obtenga información sobre los atributos con varios valores en el SDK Windows Media Format 11. Algunos atributos de elementos multimedia pueden tener varios valores.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK,attributes
- Formato de sistemas avanzados (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- attributes,multiple values
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262697"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="6f6c0-108">Atributos con varios valores (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="6f6c0-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="6f6c0-109">Algunos de los atributos predefinidos pueden tener varios valores asignados.</span><span class="sxs-lookup"><span data-stu-id="6f6c0-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="6f6c0-110">Por ejemplo, **Artist** es un atributo que puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="6f6c0-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="6f6c0-111">Puede llamar a [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) varias veces para agregar tantos valores **de Artist** como necesite.</span><span class="sxs-lookup"><span data-stu-id="6f6c0-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="6f6c0-112">Si realiza varias llamadas a **AddAttribute** para atributos que no admiten varios valores, el método puede devolver un código de error o simplemente omitir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f6c0-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="6f6c0-113">En la tabla siguiente se enumeran los atributos que admiten varios valores.</span><span class="sxs-lookup"><span data-stu-id="6f6c0-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="6f6c0-114">Algunos atributos solo pueden tener varios valores en archivos ASF, mientras que otros pueden tener varios valores en archivos ASF y MP3.</span><span class="sxs-lookup"><span data-stu-id="6f6c0-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="6f6c0-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="6f6c0-115">Attribute</span></span>                                                 | <span data-ttu-id="6f6c0-116">Compatibilidad con varios valores</span><span class="sxs-lookup"><span data-stu-id="6f6c0-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="6f6c0-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="6f6c0-118">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="6f6c0-120">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-120">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-121">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="6f6c0-122">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-122">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-123">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="6f6c0-124">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-124">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-125">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="6f6c0-126">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-127">**WM/Conductor**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="6f6c0-128">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-128">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="6f6c0-130">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-130">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-131">**WM/Genre**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="6f6c0-132">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-132">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="6f6c0-134">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-134">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-135">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="6f6c0-136">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-137">**\_WM/Synchronised**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="6f6c0-138">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-139">**WM/Estados de ánimo**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="6f6c0-140">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-141">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="6f6c0-142">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-143">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="6f6c0-144">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-144">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-145">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="6f6c0-146">asf</span><span class="sxs-lookup"><span data-stu-id="6f6c0-146">ASF</span></span>                         |
| [<span data-ttu-id="6f6c0-147">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="6f6c0-148">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="6f6c0-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="6f6c0-150">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="6f6c0-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="6f6c0-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f6c0-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f6c0-152">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="6f6c0-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




