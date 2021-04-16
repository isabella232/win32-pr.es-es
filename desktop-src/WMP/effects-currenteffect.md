---
title: EFFECTs. currentEffect
description: El atributo currentEffect especifica o recupera la visualización actual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699379"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="80e21-104">EFFECTs. currentEffect</span><span class="sxs-lookup"><span data-stu-id="80e21-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="80e21-105">El atributo **currentEffect** especifica o recupera la visualización actual.</span><span class="sxs-lookup"><span data-stu-id="80e21-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="80e21-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="80e21-106">Possible Values</span></span>

<span data-ttu-id="80e21-107">Este atributo es un **objeto** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="80e21-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="80e21-108">El valor predeterminado es la primera visualización del orden de creación.</span><span class="sxs-lookup"><span data-stu-id="80e21-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="80e21-109">Si no se crean visualizaciones en la máscara, el valor predeterminado es la primera visualización del registro.</span><span class="sxs-lookup"><span data-stu-id="80e21-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e21-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80e21-110">Remarks</span></span>

<span data-ttu-id="80e21-111">Puede usar este objeto para tener acceso a las visualizaciones personalizadas que ha creado.</span><span class="sxs-lookup"><span data-stu-id="80e21-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="80e21-112">Por ejemplo, puede exponer una propiedad a través de la interfaz **IDispatch** en la visualización.</span><span class="sxs-lookup"><span data-stu-id="80e21-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="80e21-113">Después, puede cambiar el valor de la propiedad de la máscara haciendo que la visualización sea el efecto actual y usando el objeto **currentEffect** para establecer un nuevo valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="80e21-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="80e21-114">Por ejemplo, si la visualización expone una propiedad denominada backgroundColor, el código JScript siguiente especifica un nuevo valor:</span><span class="sxs-lookup"><span data-stu-id="80e21-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="80e21-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80e21-115">Requirements</span></span>



| <span data-ttu-id="80e21-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e21-116">Requirement</span></span> | <span data-ttu-id="80e21-117">Value</span><span class="sxs-lookup"><span data-stu-id="80e21-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="80e21-118">Versión</span><span class="sxs-lookup"><span data-stu-id="80e21-118">Version</span></span><br/> | <span data-ttu-id="80e21-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="80e21-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80e21-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="80e21-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e21-121">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="80e21-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="80e21-122">**EFFECTs. currentEffectTitle**</span><span class="sxs-lookup"><span data-stu-id="80e21-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="80e21-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="80e21-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





