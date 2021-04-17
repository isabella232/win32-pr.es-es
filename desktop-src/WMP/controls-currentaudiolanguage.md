---
title: Controls. currentAudioLanguage
description: La propiedad currentAudioLanguage especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Media Player de Windows Controls. currentAudioLanguage
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699934"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="2803d-104">Controls. currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="2803d-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="2803d-105">La propiedad **currentAudioLanguage** especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="2803d-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="2803d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="2803d-106">Possible Values</span></span>

<span data-ttu-id="2803d-107">Esta propiedad es un **número** de lectura y escritura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2803d-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2803d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2803d-108">Remarks</span></span>

<span data-ttu-id="2803d-109">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2803d-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="2803d-110">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="2803d-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="2803d-111">Al trabajar con contenido de DVD, si se especifica un LCID, se seleccionará la primera pista de audio disponible que tenga el identificador de idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="2803d-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="2803d-112">**Windows Media Player 10 Mobile:** Esta propiedad solo acepta o devuelve el LCID independiente del idioma (0).</span><span class="sxs-lookup"><span data-stu-id="2803d-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="2803d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2803d-113">Requirements</span></span>



| <span data-ttu-id="2803d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2803d-114">Requirement</span></span> | <span data-ttu-id="2803d-115">Value</span><span class="sxs-lookup"><span data-stu-id="2803d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2803d-116">Versión</span><span class="sxs-lookup"><span data-stu-id="2803d-116">Version</span></span><br/> | <span data-ttu-id="2803d-117">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="2803d-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2803d-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2803d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="2803d-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2803d-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2803d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2803d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2803d-121">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="2803d-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="2803d-122">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="2803d-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="2803d-123">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="2803d-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="2803d-124">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="2803d-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="2803d-125">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="2803d-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="2803d-126">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="2803d-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





