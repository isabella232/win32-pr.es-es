---
title: EQUALIZERSETTINGS. Normalization
description: El atributo Normalization especifica o recupera un valor que indica si está habilitada la normalización.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normal Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699445"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="c86e9-104">EQUALIZERSETTINGS. Normalization</span><span class="sxs-lookup"><span data-stu-id="c86e9-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="c86e9-105">El atributo **Normalization** especifica o recupera un valor que indica si está habilitada la normalización.</span><span class="sxs-lookup"><span data-stu-id="c86e9-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="c86e9-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c86e9-106">Possible Values</span></span>

<span data-ttu-id="c86e9-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="c86e9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c86e9-108">Value</span><span class="sxs-lookup"><span data-stu-id="c86e9-108">Value</span></span> | <span data-ttu-id="c86e9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c86e9-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="c86e9-110">true</span><span class="sxs-lookup"><span data-stu-id="c86e9-110">true</span></span>  | <span data-ttu-id="c86e9-111">La normalización está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c86e9-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="c86e9-112">false</span><span class="sxs-lookup"><span data-stu-id="c86e9-112">false</span></span> | <span data-ttu-id="c86e9-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c86e9-113">Default.</span></span> <span data-ttu-id="c86e9-114">La normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="c86e9-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c86e9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c86e9-115">Remarks</span></span>

<span data-ttu-id="c86e9-116">Cuando se habilita la normalización, la señal de audio de un archivo multimedia digital completo se escala hasta el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="c86e9-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="c86e9-117">Esto permite reproducir varios archivos aproximadamente en el mismo volumen sin necesidad de ajustes de volumen.</span><span class="sxs-lookup"><span data-stu-id="c86e9-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86e9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c86e9-118">Requirements</span></span>



| <span data-ttu-id="c86e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c86e9-119">Requirement</span></span> | <span data-ttu-id="c86e9-120">Value</span><span class="sxs-lookup"><span data-stu-id="c86e9-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="c86e9-121">Versión</span><span class="sxs-lookup"><span data-stu-id="c86e9-121">Version</span></span><br/> | <span data-ttu-id="c86e9-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c86e9-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c86e9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c86e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86e9-124">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="c86e9-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="c86e9-125">**EQUALIZERSETTINGS.normalizationAverage**</span><span class="sxs-lookup"><span data-stu-id="c86e9-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="c86e9-126">**EQUALIZERSETTINGS.normalizationPeak**</span><span class="sxs-lookup"><span data-stu-id="c86e9-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





