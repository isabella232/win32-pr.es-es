---
title: Atributos con varios valores (Windows Media Format 11 SDK)
description: Atributos con varios valores
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, varios valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078716"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="a131a-107">Atributos con varios valores (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a131a-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a131a-108">Algunos de los atributos predefinidos pueden tener varios valores asignados.</span><span class="sxs-lookup"><span data-stu-id="a131a-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="a131a-109">Por ejemplo, **artista** es un atributo que puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="a131a-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="a131a-110">Puede llamar a [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) varias veces para agregar tantos valores de **intérprete** como necesite.</span><span class="sxs-lookup"><span data-stu-id="a131a-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="a131a-111">Si realiza varias llamadas a **AddAttribute** para los atributos que no admiten varios valores, el método puede devolver un código de error o simplemente omitir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a131a-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="a131a-112">En la tabla siguiente se enumeran los atributos que admiten varios valores.</span><span class="sxs-lookup"><span data-stu-id="a131a-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="a131a-113">Algunos atributos solo pueden tener varios valores en archivos ASF, mientras que otros pueden tener varios valores en archivos ASF y MP3.</span><span class="sxs-lookup"><span data-stu-id="a131a-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="a131a-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="a131a-114">Attribute</span></span>                                                 | <span data-ttu-id="a131a-115">Compatibilidad con varios valores</span><span class="sxs-lookup"><span data-stu-id="a131a-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="a131a-116">**Autor**</span><span class="sxs-lookup"><span data-stu-id="a131a-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="a131a-117">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-118">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="a131a-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="a131a-119">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-119">ASF</span></span>                         |
| [<span data-ttu-id="a131a-120">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="a131a-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="a131a-121">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-121">ASF</span></span>                         |
| [<span data-ttu-id="a131a-122">**WM/categoría**</span><span class="sxs-lookup"><span data-stu-id="a131a-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="a131a-123">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-123">ASF</span></span>                         |
| [<span data-ttu-id="a131a-124">**WM/compositor**</span><span class="sxs-lookup"><span data-stu-id="a131a-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="a131a-125">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-126">**WM/conductor**</span><span class="sxs-lookup"><span data-stu-id="a131a-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="a131a-127">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-127">ASF</span></span>                         |
| [<span data-ttu-id="a131a-128">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="a131a-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="a131a-129">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-129">ASF</span></span>                         |
| [<span data-ttu-id="a131a-130">**WM/género**</span><span class="sxs-lookup"><span data-stu-id="a131a-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="a131a-131">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-131">ASF</span></span>                         |
| [<span data-ttu-id="a131a-132">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="a131a-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="a131a-133">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-133">ASF</span></span>                         |
| [<span data-ttu-id="a131a-134">**WM/lenguaje**</span><span class="sxs-lookup"><span data-stu-id="a131a-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="a131a-135">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-136">**WM/Letras \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="a131a-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="a131a-137">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-138">**WM/humor**</span><span class="sxs-lookup"><span data-stu-id="a131a-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="a131a-139">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-140">**WM/imagen**</span><span class="sxs-lookup"><span data-stu-id="a131a-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="a131a-141">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-142">**WM/productor**</span><span class="sxs-lookup"><span data-stu-id="a131a-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="a131a-143">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-143">ASF</span></span>                         |
| [<span data-ttu-id="a131a-144">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="a131a-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="a131a-145">asf</span><span class="sxs-lookup"><span data-stu-id="a131a-145">ASF</span></span>                         |
| [<span data-ttu-id="a131a-146">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="a131a-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="a131a-147">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="a131a-148">**WM/escritor**</span><span class="sxs-lookup"><span data-stu-id="a131a-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="a131a-149">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="a131a-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a131a-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a131a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a131a-151">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="a131a-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




