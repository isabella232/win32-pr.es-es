---
title: Acerca de los metadatos
description: Acerca de los metadatos
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Media Player de Windows, metadatos
- metadatos, acerca de
- metadatos, atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356733"
---
# <a name="about-the-metadata"></a><span data-ttu-id="b427c-106">Acerca de los metadatos</span><span class="sxs-lookup"><span data-stu-id="b427c-106">About the Metadata</span></span>

<span data-ttu-id="b427c-107">Windows Media Player 10 o posterior intenta sincronizar los siguientes atributos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="b427c-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="b427c-108">Atributo Player</span><span class="sxs-lookup"><span data-stu-id="b427c-108">Player attribute</span></span> | <span data-ttu-id="b427c-109">Constante global de WMDM</span><span class="sxs-lookup"><span data-stu-id="b427c-109">WMDM global constant</span></span>  | <span data-ttu-id="b427c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b427c-110">Description</span></span>                                                                                                 | <span data-ttu-id="b427c-111">Versión requerida</span><span class="sxs-lookup"><span data-stu-id="b427c-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="b427c-112">AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="b427c-112">AlbumArtist</span></span>      | <span data-ttu-id="b427c-113">g \_ wszWMDMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="b427c-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="b427c-114">**Cadena** terminada en null que contiene el nombre del intérprete principal del álbum.</span><span class="sxs-lookup"><span data-stu-id="b427c-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="b427c-115">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-116">Álbum</span><span class="sxs-lookup"><span data-stu-id="b427c-116">Album</span></span>            | <span data-ttu-id="b427c-117">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="b427c-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="b427c-118">**Cadena** terminada en null que contiene el título del álbum en el que se liberó originalmente el contenido.</span><span class="sxs-lookup"><span data-stu-id="b427c-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="b427c-119">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-120">Autor</span><span class="sxs-lookup"><span data-stu-id="b427c-120">Author</span></span>           | <span data-ttu-id="b427c-121">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="b427c-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="b427c-122">**Cadena** terminada en null que contiene el nombre del intérprete multimedia o actor asociado con el contenido.</span><span class="sxs-lookup"><span data-stu-id="b427c-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="b427c-123">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-124">BuyNow</span><span class="sxs-lookup"><span data-stu-id="b427c-124">BuyNow</span></span>           | <span data-ttu-id="b427c-125">g \_ wszWMDMBuyNow</span><span class="sxs-lookup"><span data-stu-id="b427c-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="b427c-126">**Valor booleano** que indica si el usuario ha elegido comprar el contenido.</span><span class="sxs-lookup"><span data-stu-id="b427c-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="b427c-127">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="b427c-128">WM/género</span><span class="sxs-lookup"><span data-stu-id="b427c-128">WM/Genre</span></span>         | <span data-ttu-id="b427c-129">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="b427c-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="b427c-130">**Cadena** terminada en null que contiene el género del contenido.</span><span class="sxs-lookup"><span data-stu-id="b427c-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="b427c-131">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-132">UserPlayCount</span><span class="sxs-lookup"><span data-stu-id="b427c-132">UserPlayCount</span></span>    | <span data-ttu-id="b427c-133">g \_ wszWMDMPlayCount</span><span class="sxs-lookup"><span data-stu-id="b427c-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="b427c-134">**DWORD** que contiene el número de veces que el usuario ha reproducido el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="b427c-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="b427c-135">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="b427c-136">ReleaseDate</span><span class="sxs-lookup"><span data-stu-id="b427c-136">ReleaseDate</span></span>      | <span data-ttu-id="b427c-137">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="b427c-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="b427c-138">Fecha de la versión original del elemento.</span><span class="sxs-lookup"><span data-stu-id="b427c-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="b427c-139">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-140">Title</span><span class="sxs-lookup"><span data-stu-id="b427c-140">Title</span></span>            | <span data-ttu-id="b427c-141">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="b427c-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="b427c-142">**Cadena** terminada en null que contiene el título.</span><span class="sxs-lookup"><span data-stu-id="b427c-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="b427c-143">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-144">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="b427c-144">WM/TrackNumber</span></span>   | <span data-ttu-id="b427c-145">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="b427c-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="b427c-146">**DWORD** que contiene el número de pista del elemento en el álbum en el que se liberó originalmente.</span><span class="sxs-lookup"><span data-stu-id="b427c-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="b427c-147">Windows Media Player 11 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="b427c-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="b427c-148">UserRating</span></span>       | <span data-ttu-id="b427c-149">g \_ wszWMDMUserRating</span><span class="sxs-lookup"><span data-stu-id="b427c-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="b427c-150">**DWORD** que contiene un valor que representa la clasificación por estrellas del usuario especificado para el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="b427c-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="b427c-151">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b427c-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b427c-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b427c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b427c-153">**Extensiones de dispositivo para la transferencia de metadatos acelerada**</span><span class="sxs-lookup"><span data-stu-id="b427c-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




