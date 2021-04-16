---
title: EQUALIZERSETTINGS.gainLevels
description: El atributo gainLevels especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS. gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699446"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="72e86-104">EQUALIZERSETTINGS.gainLevels</span><span class="sxs-lookup"><span data-stu-id="72e86-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="72e86-105">El atributo **gainLevels** especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.</span><span class="sxs-lookup"><span data-stu-id="72e86-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="72e86-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="72e86-106">Possible Values</span></span>

<span data-ttu-id="72e86-107">Este atributo es un **número** de lectura/escritura (**float**) con un valor que normalmente oscila entre 20 y + 20.</span><span class="sxs-lookup"><span data-stu-id="72e86-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="72e86-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72e86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e86-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*la banda*</span><span class="sxs-lookup"><span data-stu-id="72e86-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="72e86-110">**Número**(**largo**) entre 1 y 10 que indica el índice de la banda.</span><span class="sxs-lookup"><span data-stu-id="72e86-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72e86-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72e86-111">Remarks</span></span>

<span data-ttu-id="72e86-112">Este atributo toma un parámetro, pero su valor se especifica en el código de script de la misma manera que otros valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="72e86-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="72e86-113">No se puede especificar en el elemento EQUALIZERSETTINGS, ni puede usarse con el atributo de escucha **wmpprop** .</span><span class="sxs-lookup"><span data-stu-id="72e86-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="72e86-114">En su lugar, se proporcionan los atributos de nivel de ganancia numerado para estas situaciones.</span><span class="sxs-lookup"><span data-stu-id="72e86-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e86-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72e86-115">Requirements</span></span>



| <span data-ttu-id="72e86-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e86-116">Requirement</span></span> | <span data-ttu-id="72e86-117">Value</span><span class="sxs-lookup"><span data-stu-id="72e86-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="72e86-118">Versión</span><span class="sxs-lookup"><span data-stu-id="72e86-118">Version</span></span><br/> | <span data-ttu-id="72e86-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="72e86-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72e86-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="72e86-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e86-121">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="72e86-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="72e86-122">**Atributos de escucha**</span><span class="sxs-lookup"><span data-stu-id="72e86-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 





