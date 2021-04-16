---
title: Controls. getAudioLanguageDescription (método)
description: El método getAudioLanguageDescription recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- método getAudioLanguageDescription de Windows Media Player
- método getAudioLanguageDescription Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699513"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="93410-106">Controls. getAudioLanguageDescription (método)</span><span class="sxs-lookup"><span data-stu-id="93410-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="93410-107">El método **getAudioLanguageDescription** recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.</span><span class="sxs-lookup"><span data-stu-id="93410-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="93410-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93410-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="93410-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93410-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93410-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="93410-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93410-111">**Número** (**largo**) que especifica el índice de idioma de audio basado en uno.</span><span class="sxs-lookup"><span data-stu-id="93410-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93410-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93410-112">Return value</span></span>

<span data-ttu-id="93410-113">Este método devuelve un valor de **cadena** .</span><span class="sxs-lookup"><span data-stu-id="93410-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93410-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93410-114">Remarks</span></span>

<span data-ttu-id="93410-115">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="93410-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="93410-116">Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.</span><span class="sxs-lookup"><span data-stu-id="93410-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="93410-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="93410-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="93410-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93410-118">Requirements</span></span>



| <span data-ttu-id="93410-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93410-119">Requirement</span></span> | <span data-ttu-id="93410-120">Value</span><span class="sxs-lookup"><span data-stu-id="93410-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93410-121">Versión</span><span class="sxs-lookup"><span data-stu-id="93410-121">Version</span></span><br/> | <span data-ttu-id="93410-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="93410-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="93410-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93410-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="93410-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93410-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93410-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="93410-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93410-126">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="93410-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="93410-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="93410-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="93410-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="93410-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="93410-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="93410-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="93410-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="93410-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="93410-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="93410-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





