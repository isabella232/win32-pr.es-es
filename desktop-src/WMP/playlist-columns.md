---
title: Lista de reproducción. columnas
description: El atributo Columns define las columnas que aparecen en el elemento de lista de reproducción.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- Lista de reproducción. columnas Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708290"
---
# <a name="playlistcolumns"></a><span data-ttu-id="2e657-104">Lista de reproducción. columnas</span><span class="sxs-lookup"><span data-stu-id="2e657-104">PLAYLIST.columns</span></span>

<span data-ttu-id="2e657-105">El atributo **Columns** define las columnas que aparecen en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="2e657-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="2e657-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="2e657-106">Possible Values</span></span>

<span data-ttu-id="2e657-107">Este atributo es una **cadena** de lectura/escritura con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="2e657-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="2e657-108">nombre de la base de BD \_ = \_ nombre descriptivo; nombre de la base de BD \_ = \_ nombre descriptivo;</span><span class="sxs-lookup"><span data-stu-id="2e657-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="2e657-109">\_Nombre descriptivo es el valor que se muestra en el encabezado de columna del elemento playlist y DB \_ Name es un valor de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2e657-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="2e657-110">Tenga en cuenta que un elemento de lista de reproducción puede ser un elemento multimedia de la biblioteca o de un CD, o puede ser otra **lista de reproducción** que sea creada por el usuario o tomada de un CD.</span><span class="sxs-lookup"><span data-stu-id="2e657-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="2e657-111">Algunas columnas solo son válidas con determinados elementos de lista de reproducción, como se indica en la columna Descripción.</span><span class="sxs-lookup"><span data-stu-id="2e657-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="2e657-112">Value</span><span class="sxs-lookup"><span data-stu-id="2e657-112">Value</span></span>             | <span data-ttu-id="2e657-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e657-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e657-114">Álbum</span><span class="sxs-lookup"><span data-stu-id="2e657-114">Album</span></span>             | <span data-ttu-id="2e657-115">Nombre del álbum.</span><span class="sxs-lookup"><span data-stu-id="2e657-115">The name of the album.</span></span> <span data-ttu-id="2e657-116">Se usa solo con elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e657-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="2e657-117">Artistas</span><span class="sxs-lookup"><span data-stu-id="2e657-117">Artist</span></span>            | <span data-ttu-id="2e657-118">Nombre del intérprete.</span><span class="sxs-lookup"><span data-stu-id="2e657-118">The name of the artist.</span></span> <span data-ttu-id="2e657-119">No se utiliza con listas de reproducción creadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2e657-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="2e657-120">Autor</span><span class="sxs-lookup"><span data-stu-id="2e657-120">Author</span></span>            | <span data-ttu-id="2e657-121">Nombre del intérprete.</span><span class="sxs-lookup"><span data-stu-id="2e657-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="2e657-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="2e657-122">Bitrate</span></span>           | <span data-ttu-id="2e657-123">La velocidad de bits del contenido.</span><span class="sxs-lookup"><span data-stu-id="2e657-123">The bit rate of the content.</span></span> <span data-ttu-id="2e657-124">Solo se usa con elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e657-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="2e657-125">CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="2e657-125">CDTrackEnabled</span></span>    | <span data-ttu-id="2e657-126">Indica si la pista del CD está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2e657-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="2e657-127">Solo se utiliza con elementos multimedia de CD.</span><span class="sxs-lookup"><span data-stu-id="2e657-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="2e657-128">Activada</span><span class="sxs-lookup"><span data-stu-id="2e657-128">Checked</span></span>           | <span data-ttu-id="2e657-129">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-130">Copyright</span><span class="sxs-lookup"><span data-stu-id="2e657-130">Copyright</span></span>         | <span data-ttu-id="2e657-131">Copyright de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2e657-131">The copyright of the playlist.</span></span> <span data-ttu-id="2e657-132">No se utiliza con listas de reproducción de CD o elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e657-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="2e657-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="2e657-133">CreationDate</span></span>      | <span data-ttu-id="2e657-134">Fecha y hora en que se creó la entrada en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e657-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="2e657-135">Solo se usa con elementos de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e657-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="2e657-136">DigitallySecure</span><span class="sxs-lookup"><span data-stu-id="2e657-136">DigitallySecure</span></span>   | <span data-ttu-id="2e657-137">Indica si el elemento está protegido con el administrador de derechos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2e657-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="2e657-138">Solo se usa con elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e657-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="2e657-139">Duration</span><span class="sxs-lookup"><span data-stu-id="2e657-139">Duration</span></span>          | <span data-ttu-id="2e657-140">La duración del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e657-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="2e657-141">FileType</span><span class="sxs-lookup"><span data-stu-id="2e657-141">FileType</span></span>          | <span data-ttu-id="2e657-142">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-143">Género</span><span class="sxs-lookup"><span data-stu-id="2e657-143">Genre</span></span>             | <span data-ttu-id="2e657-144">El género de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2e657-144">The genre of the playlist.</span></span> <span data-ttu-id="2e657-145">No se utiliza con listas de reproducción de CDs.</span><span class="sxs-lookup"><span data-stu-id="2e657-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="2e657-146">MediaAttribute</span><span class="sxs-lookup"><span data-stu-id="2e657-146">MediaAttribute</span></span>    | <span data-ttu-id="2e657-147">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="2e657-148">MediaType</span></span>         | <span data-ttu-id="2e657-149">Tipo del elemento multimedia (audio o vídeo).</span><span class="sxs-lookup"><span data-stu-id="2e657-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="2e657-150">Metadatasource</span><span class="sxs-lookup"><span data-stu-id="2e657-150">MetadataSource</span></span>    | <span data-ttu-id="2e657-151">El origen de los metadatos de esta pista de CD (AMG, WindowsMedia.com, etc.).</span><span class="sxs-lookup"><span data-stu-id="2e657-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="2e657-152">Solo se utiliza con elementos multimedia de CD.</span><span class="sxs-lookup"><span data-stu-id="2e657-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="2e657-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="2e657-153">ModifiedBy</span></span>        | <span data-ttu-id="2e657-154">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-155">Nombre</span><span class="sxs-lookup"><span data-stu-id="2e657-155">Name</span></span>              | <span data-ttu-id="2e657-156">Nombre de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2e657-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="2e657-157">OriginalIndex</span><span class="sxs-lookup"><span data-stu-id="2e657-157">OriginalIndex</span></span>     | <span data-ttu-id="2e657-158">Si es aplicable, el identificador de pista de CD correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2e657-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="2e657-159">Solo se utiliza con elementos multimedia de CD.</span><span class="sxs-lookup"><span data-stu-id="2e657-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="2e657-160">PlayCount</span><span class="sxs-lookup"><span data-stu-id="2e657-160">PlayCount</span></span>         | <span data-ttu-id="2e657-161">Número de veces que el contenido se ha reproducido hasta el final.</span><span class="sxs-lookup"><span data-stu-id="2e657-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="2e657-162">Solo se usa con elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e657-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="2e657-163">PlaylistAttribute</span><span class="sxs-lookup"><span data-stu-id="2e657-163">PlaylistAttribute</span></span> | <span data-ttu-id="2e657-164">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-165">Rating</span><span class="sxs-lookup"><span data-stu-id="2e657-165">Rating</span></span>            | <span data-ttu-id="2e657-166">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-167">SourceURL</span><span class="sxs-lookup"><span data-stu-id="2e657-167">SourceURL</span></span>         | <span data-ttu-id="2e657-168">La ruta de acceso o dirección URL del contenido.</span><span class="sxs-lookup"><span data-stu-id="2e657-168">The path or URL to the content.</span></span> <span data-ttu-id="2e657-169">Solo se usa con elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e657-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="2e657-170">Status</span><span class="sxs-lookup"><span data-stu-id="2e657-170">Status</span></span>            | <span data-ttu-id="2e657-171">Estado de copia de una pista de CD que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="2e657-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="2e657-172">Solo se utiliza con elementos multimedia de CD.</span><span class="sxs-lookup"><span data-stu-id="2e657-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="2e657-173">Estilo</span><span class="sxs-lookup"><span data-stu-id="2e657-173">Style</span></span>             | <span data-ttu-id="2e657-174">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2e657-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="2e657-175">TABLA DE CONTENIDO</span><span class="sxs-lookup"><span data-stu-id="2e657-175">TOC</span></span>               | <span data-ttu-id="2e657-176">Si es aplicable, el identificador de la tabla de contenido del CD correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2e657-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="2e657-177">No se utiliza con listas de reproducción creadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2e657-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="2e657-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e657-178">Remarks</span></span>

<span data-ttu-id="2e657-179">Si una de las columnas no existe en la biblioteca, se deja en blanco.</span><span class="sxs-lookup"><span data-stu-id="2e657-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="2e657-180">Se puede especificar un máximo de 31 columnas.</span><span class="sxs-lookup"><span data-stu-id="2e657-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="2e657-181">Si especifica una columna duplicada, los datos de la primera columna estarán alineados a la izquierda, pero todas las demás columnas duplicadas estarán alineadas a la derecha.</span><span class="sxs-lookup"><span data-stu-id="2e657-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="2e657-182">Por ejemplo, si tiene dos columnas de duración, los datos se alinean a la izquierda en la primera y la alineación a la derecha en el segundo.</span><span class="sxs-lookup"><span data-stu-id="2e657-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e657-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e657-183">Requirements</span></span>



| <span data-ttu-id="2e657-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e657-184">Requirement</span></span> | <span data-ttu-id="2e657-185">Value</span><span class="sxs-lookup"><span data-stu-id="2e657-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2e657-186">Versión</span><span class="sxs-lookup"><span data-stu-id="2e657-186">Version</span></span><br/> | <span data-ttu-id="2e657-187">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2e657-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e657-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e657-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e657-189">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2e657-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="2e657-190">**Lista de reproducción. columnsVisible**</span><span class="sxs-lookup"><span data-stu-id="2e657-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





