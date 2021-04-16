---
title: Controls. currentAudioLanguageIndex
description: La propiedad currentAudioLanguageIndex especifica o recupera el índice basado en uno que corresponde al lenguaje de audio para la reproducción.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Media Player de Windows Controls. currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699933"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="0b6c5-104">Controls. currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="0b6c5-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="0b6c5-105">La propiedad **currentAudioLanguageIndex** especifica o recupera el índice basado en uno que corresponde al lenguaje de audio para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="0b6c5-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0b6c5-106">Possible Values</span></span>

<span data-ttu-id="0b6c5-107">Esta propiedad es un **número** de lectura y escritura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b6c5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b6c5-108">Remarks</span></span>

<span data-ttu-id="0b6c5-109">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="0b6c5-110">Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="0b6c5-111">**Windows Media Player 10 Mobile:** Esta propiedad solo acepta o devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6c5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6c5-112">Requirements</span></span>



| <span data-ttu-id="0b6c5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6c5-113">Requirement</span></span> | <span data-ttu-id="0b6c5-114">Value</span><span class="sxs-lookup"><span data-stu-id="0b6c5-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6c5-115">Versión</span><span class="sxs-lookup"><span data-stu-id="0b6c5-115">Version</span></span><br/> | <span data-ttu-id="0b6c5-116">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0b6c5-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b6c5-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b6c5-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c5-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b6c5-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b6c5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6c5-120">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="0b6c5-121">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="0b6c5-122">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="0b6c5-123">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="0b6c5-124">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="0b6c5-125">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





