---
title: TEXT. scrollingAmount
description: El atributo scrollingAmount especifica o recupera el número de píxeles que el texto se mueve durante cada movimiento de desplazamiento.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Media Player de Windows TEXT. scrollingAmount
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680295"
---
# <a name="textscrollingamount"></a><span data-ttu-id="62efc-104">TEXT. scrollingAmount</span><span class="sxs-lookup"><span data-stu-id="62efc-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="62efc-105">El atributo **scrollingAmount** especifica o recupera el número de píxeles que el texto se mueve durante cada movimiento de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="62efc-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="62efc-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="62efc-106">Possible Values</span></span>

<span data-ttu-id="62efc-107">Este atributo es un **número** de lectura/escritura positivo (**int**) con un valor predeterminado de 6.</span><span class="sxs-lookup"><span data-stu-id="62efc-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="62efc-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62efc-108">Remarks</span></span>

<span data-ttu-id="62efc-109">Para el desplazamiento suave, **scrollingAmount** debe ser pequeño.</span><span class="sxs-lookup"><span data-stu-id="62efc-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="62efc-110">Para un dibujo rápido con grandes huecos, el **scrollingAmount** debe ser mayor.</span><span class="sxs-lookup"><span data-stu-id="62efc-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="62efc-111">Si **scrolling** = "false", **scrollingAmount** se omite.</span><span class="sxs-lookup"><span data-stu-id="62efc-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="62efc-112">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="62efc-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="62efc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62efc-113">Requirements</span></span>



| <span data-ttu-id="62efc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62efc-114">Requirement</span></span> | <span data-ttu-id="62efc-115">Value</span><span class="sxs-lookup"><span data-stu-id="62efc-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="62efc-116">Versión</span><span class="sxs-lookup"><span data-stu-id="62efc-116">Version</span></span><br/> | <span data-ttu-id="62efc-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="62efc-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62efc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="62efc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62efc-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="62efc-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="62efc-120">**TEXTO. desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="62efc-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





