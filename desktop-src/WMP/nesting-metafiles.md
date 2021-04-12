---
title: Anidar metaarchivos
description: Anidar metaarchivos
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Metaarchivos de Windows Media, anidamiento
- Metaarchivos de Windows Media, hacer referencia a otros metaarchivos
- anidar metaarchivos
- metaarchivos, anidamiento
- metaarchivos, hacer referencia a otros metaarchivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356747"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="181f2-108">Anidar metaarchivos</span><span class="sxs-lookup"><span data-stu-id="181f2-108">Nesting Metafiles</span></span>

<span data-ttu-id="181f2-109">Un metarchivo puede hacer referencia A otro metarchivo.</span><span class="sxs-lookup"><span data-stu-id="181f2-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="181f2-110">Para hacer referencia a otro metarchivo, use el elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="181f2-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="181f2-111">Un elemento **ENTRYREF** del metarchivo principal apunta a un metarchivo externo.</span><span class="sxs-lookup"><span data-stu-id="181f2-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="181f2-112">El control Media Player de Windows procesa los elementos de **entrada** del metarchivo al que se hace referencia como si estuvieran incluidos en el metarchivo principal situado en la posición del elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="181f2-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="181f2-113">Sin embargo, omite cualquier elemento de **entrada** del metarchivo al que se hace referencia que tenga el atributo **SKIPIFREF** establecido en sí.</span><span class="sxs-lookup"><span data-stu-id="181f2-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="181f2-114">Los controles Windows Media Player 7,0, 7,1 y Windows Media Player para Windows XP omiten los elementos **ENTRYREF** del metarchivo al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="181f2-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="181f2-115">Por lo tanto, los metaarchivos solo se pueden anidar un nivel en profundidad con estas versiones.</span><span class="sxs-lookup"><span data-stu-id="181f2-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="181f2-116">Estas versiones también omiten el elemento **ASX** y sus atributos en el archivo al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="181f2-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="181f2-117">Windows Media Player 9 series o posterior admiten la anidación de metaarchivos hasta 5 de profundidad.</span><span class="sxs-lookup"><span data-stu-id="181f2-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="181f2-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="181f2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="181f2-119">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="181f2-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




