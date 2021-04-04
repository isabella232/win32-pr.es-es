---
title: Compatibilidad con varios idiomas
description: Compatibilidad con varios idiomas
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Listas de reproducción de metarchivos de Windows Media, compatibilidad con varios idiomas
- listas de reproducción de metarchivos, compatibilidad con varios idiomas
- listas de reproducción, compatibilidad con varios idiomas
- Listas de reproducción de metarchivos de Windows Media, compatibilidad con varios idiomas
- listas de reproducción de metarchivos, compatibilidad con varios idiomas
- listas de reproducción, compatibilidad con varios idiomas
- Listas de reproducción de metarchivos de Windows Media, compatibilidad con idiomas
- listas de reproducción de metarchivos, compatibilidad con idiomas
- listas de reproducción, compatibilidad con idiomas
- compatibilidad con varios idiomas
- compatibilidad con varios lenguajes
- compatibilidad con el idioma
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076203"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="1dc0b-115">Compatibilidad con varios idiomas</span><span class="sxs-lookup"><span data-stu-id="1dc0b-115">Support for Multiple Languages</span></span>

<span data-ttu-id="1dc0b-116">Windows Media Player 9 series o posterior admiten los metaarchivos de Windows Media creados con el juego de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1dc0b-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="1dc0b-117">Esto le permite incluir metadatos multilingües en la lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="1dc0b-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="1dc0b-118">Las siguientes reglas rigen el uso de metadatos multilingües en los metaarchivos de Windows Media:</span><span class="sxs-lookup"><span data-stu-id="1dc0b-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="1dc0b-119">Los caracteres se deben codificar mediante el esquema de codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="1dc0b-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="1dc0b-120">La lista de reproducción del metarchivo debe incluir el **parámetro** siguiente en el nivel de lista de reproducción:</span><span class="sxs-lookup"><span data-stu-id="1dc0b-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="1dc0b-121">Solo Windows Media Player 9 series o versiones posteriores admiten esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="1dc0b-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="1dc0b-122">Si la lista de reproducción del metarchivo no se guarda con la codificación UTF-8 y el elemento **param** correcto, se analizará con la página de códigos configuración regional predeterminada del sistema del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="1dc0b-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dc0b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1dc0b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc0b-124">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="1dc0b-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="1dc0b-125">**Información general de los metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1dc0b-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




