---
title: EFFECTs. currentEffectType
description: El atributo currentEffectType especifica o recupera el nombre del registro de la visualización actual. Este nombre es un identificador único definido por el autor de la visualización.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699372"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="88ae8-105">EFFECTs. currentEffectType</span><span class="sxs-lookup"><span data-stu-id="88ae8-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="88ae8-106">El atributo **currentEffectType** especifica o recupera el nombre del registro de la visualización actual.</span><span class="sxs-lookup"><span data-stu-id="88ae8-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="88ae8-107">Este nombre es un identificador único definido por el autor de la visualización.</span><span class="sxs-lookup"><span data-stu-id="88ae8-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="88ae8-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="88ae8-108">Possible Values</span></span>

<span data-ttu-id="88ae8-109">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="88ae8-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ae8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88ae8-110">Remarks</span></span>

<span data-ttu-id="88ae8-111">Puede utilizar este atributo en tiempo de ejecución para cambiar el efecto que se muestra actualmente.</span><span class="sxs-lookup"><span data-stu-id="88ae8-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="88ae8-112">Para ello, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="88ae8-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="88ae8-113">Use **effectCount** para recuperar el recuento de efectos registrados.</span><span class="sxs-lookup"><span data-stu-id="88ae8-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="88ae8-114">En un bucle, recupere el nombre de cada efecto registrado mediante **effectType**.</span><span class="sxs-lookup"><span data-stu-id="88ae8-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="88ae8-115">Especifique uno de los nombres que recuperó para **currentEffectType** para establecer el efecto actual.</span><span class="sxs-lookup"><span data-stu-id="88ae8-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ae8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88ae8-116">Requirements</span></span>



| <span data-ttu-id="88ae8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ae8-117">Requirement</span></span> | <span data-ttu-id="88ae8-118">Value</span><span class="sxs-lookup"><span data-stu-id="88ae8-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="88ae8-119">Versión</span><span class="sxs-lookup"><span data-stu-id="88ae8-119">Version</span></span><br/> | <span data-ttu-id="88ae8-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="88ae8-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88ae8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="88ae8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ae8-122">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="88ae8-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="88ae8-123">**EFFECTs. currentEffect**</span><span class="sxs-lookup"><span data-stu-id="88ae8-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="88ae8-124">**EFFECTs. effectCount**</span><span class="sxs-lookup"><span data-stu-id="88ae8-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="88ae8-125">**EFFECTs. effectType**</span><span class="sxs-lookup"><span data-stu-id="88ae8-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 





