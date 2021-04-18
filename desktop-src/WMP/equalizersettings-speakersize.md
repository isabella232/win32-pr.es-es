---
title: EQUALIZERSETTINGS. Speaker
description: El atributo Speakers especifica o recupera el número de índice del tamaño actual del altavoz.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. pone en altavoz Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699594"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="8302a-104">EQUALIZERSETTINGS. Speaker</span><span class="sxs-lookup"><span data-stu-id="8302a-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="8302a-105">El atributo **Speakers** especifica o recupera el número de índice del tamaño actual del altavoz.</span><span class="sxs-lookup"><span data-stu-id="8302a-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="8302a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="8302a-106">Possible Values</span></span>

<span data-ttu-id="8302a-107">Este atributo es un **número** de lectura y escritura (Long) que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8302a-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="8302a-108">Value</span><span class="sxs-lookup"><span data-stu-id="8302a-108">Value</span></span> | <span data-ttu-id="8302a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8302a-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="8302a-110">0</span><span class="sxs-lookup"><span data-stu-id="8302a-110">0</span></span>     | <span data-ttu-id="8302a-111">Los altavoces actuales son auriculares.</span><span class="sxs-lookup"><span data-stu-id="8302a-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="8302a-112">1</span><span class="sxs-lookup"><span data-stu-id="8302a-112">1</span></span>     | <span data-ttu-id="8302a-113">Los altavoces actuales tienen un tamaño normal.</span><span class="sxs-lookup"><span data-stu-id="8302a-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="8302a-114">2</span><span class="sxs-lookup"><span data-stu-id="8302a-114">2</span></span>     | <span data-ttu-id="8302a-115">Los altavoces actuales son grandes.</span><span class="sxs-lookup"><span data-stu-id="8302a-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="8302a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8302a-116">Remarks</span></span>

<span data-ttu-id="8302a-117">El nombre descriptivo del tamaño del altavoz se puede recuperar mediante el atributo **currentSpeakerName** .</span><span class="sxs-lookup"><span data-stu-id="8302a-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="8302a-118">Este atributo se omite si **enhancedAudio** está establecido en false.</span><span class="sxs-lookup"><span data-stu-id="8302a-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="8302a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8302a-119">Requirements</span></span>



| <span data-ttu-id="8302a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8302a-120">Requirement</span></span> | <span data-ttu-id="8302a-121">Value</span><span class="sxs-lookup"><span data-stu-id="8302a-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8302a-122">Versión</span><span class="sxs-lookup"><span data-stu-id="8302a-122">Version</span></span><br/> | <span data-ttu-id="8302a-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="8302a-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8302a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8302a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8302a-125">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="8302a-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="8302a-126">**EQUALIZERSETTINGS.currentSpeakerName**</span><span class="sxs-lookup"><span data-stu-id="8302a-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="8302a-127">**EQUALIZERSETTINGS.enhancedAudio**</span><span class="sxs-lookup"><span data-stu-id="8302a-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





