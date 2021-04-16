---
title: Controls. getAudioLanguageID (método)
description: El método getAudioLanguageID recupera el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- método getAudioLanguageID de Windows Media Player
- método getAudioLanguageID Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699512"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="f8144-106">Controls. getAudioLanguageID (método)</span><span class="sxs-lookup"><span data-stu-id="f8144-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="f8144-107">El método **getAudioLanguageID** recupera el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.</span><span class="sxs-lookup"><span data-stu-id="f8144-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8144-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8144-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="f8144-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8144-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8144-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f8144-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8144-111">**Número** (**largo**) que especifica el índice del idioma de audio.</span><span class="sxs-lookup"><span data-stu-id="f8144-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8144-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8144-112">Return value</span></span>

<span data-ttu-id="f8144-113">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="f8144-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8144-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8144-114">Remarks</span></span>

<span data-ttu-id="f8144-115">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="f8144-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="f8144-116">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="f8144-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="f8144-117">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve el LCID independiente del idioma (0).</span><span class="sxs-lookup"><span data-stu-id="f8144-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8144-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8144-118">Requirements</span></span>



| <span data-ttu-id="f8144-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8144-119">Requirement</span></span> | <span data-ttu-id="f8144-120">Value</span><span class="sxs-lookup"><span data-stu-id="f8144-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8144-121">Versión</span><span class="sxs-lookup"><span data-stu-id="f8144-121">Version</span></span><br/> | <span data-ttu-id="f8144-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="f8144-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f8144-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8144-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8144-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8144-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8144-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8144-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8144-126">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="f8144-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f8144-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="f8144-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="f8144-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="f8144-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="f8144-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="f8144-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="f8144-130">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="f8144-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="f8144-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="f8144-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





