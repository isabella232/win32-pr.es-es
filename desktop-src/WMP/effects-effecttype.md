---
title: EFFECTs. effectType
description: El método effectType recupera el nombre del registro de la visualización con el índice del registro especificado. Este nombre es un identificador único definido por el autor de la visualización.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699700"
---
# <a name="effectseffecttype"></a><span data-ttu-id="1f0e2-105">EFFECTs. effectType</span><span class="sxs-lookup"><span data-stu-id="1f0e2-105">EFFECTS.effectType</span></span>

<span data-ttu-id="1f0e2-106">El método **effectType** recupera el nombre del registro de la visualización con el índice del registro especificado.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="1f0e2-107">Este nombre es un identificador único definido por el autor de la visualización.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="1f0e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f0e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f0e2-109"><span id="index"></span><span id="INDEX"></span>*ajustar*</span><span class="sxs-lookup"><span data-stu-id="1f0e2-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="1f0e2-110">**Número** (**largo**) que contiene el índice del registro de una visualización.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f0e2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f0e2-111">Return Value</span></span>

<span data-ttu-id="1f0e2-112">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0e2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f0e2-113">Remarks</span></span>

<span data-ttu-id="1f0e2-114">Este método es útil para cambiar entre visualizaciones en el script.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="1f0e2-115">Una interfaz de usuario podría mostrar el conjunto de títulos, pero cuando el usuario selecciona uno, el script debe usar **currentEffectType** para cambiar las visualizaciones.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0e2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f0e2-116">Requirements</span></span>



| <span data-ttu-id="1f0e2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f0e2-117">Requirement</span></span> | <span data-ttu-id="1f0e2-118">Value</span><span class="sxs-lookup"><span data-stu-id="1f0e2-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1f0e2-119">Versión</span><span class="sxs-lookup"><span data-stu-id="1f0e2-119">Version</span></span><br/> | <span data-ttu-id="1f0e2-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="1f0e2-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f0e2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f0e2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f0e2-122">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="1f0e2-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="1f0e2-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="1f0e2-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





