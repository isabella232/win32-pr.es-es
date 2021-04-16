---
title: TEXT. scrollingDelay
description: El atributo scrollingDelay especifica o recupera el tiempo de retardo entre los movimientos de desplazamiento.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Media Player de Windows TEXT. scrollingDelay
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680294"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="50908-104">TEXT. scrollingDelay</span><span class="sxs-lookup"><span data-stu-id="50908-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="50908-105">El atributo **scrollingDelay** especifica o recupera el tiempo de retardo entre los movimientos de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="50908-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="50908-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="50908-106">Possible Values</span></span>

<span data-ttu-id="50908-107">Este atributo es un **número** de lectura/escritura (**int**) que especifica el retraso en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="50908-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="50908-108">Tiene un valor mínimo de 30 y un valor predeterminado de 85.</span><span class="sxs-lookup"><span data-stu-id="50908-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="50908-109">Si se especifica un valor menor que el mínimo, se utiliza el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="50908-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="50908-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50908-110">Remarks</span></span>

<span data-ttu-id="50908-111">Si el **desplazamiento** se establece en false, se omite **scrollingDelay** .</span><span class="sxs-lookup"><span data-stu-id="50908-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="50908-112">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="50908-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="50908-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50908-113">Requirements</span></span>



| <span data-ttu-id="50908-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50908-114">Requirement</span></span> | <span data-ttu-id="50908-115">Value</span><span class="sxs-lookup"><span data-stu-id="50908-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="50908-116">Versión</span><span class="sxs-lookup"><span data-stu-id="50908-116">Version</span></span><br/> | <span data-ttu-id="50908-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="50908-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50908-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="50908-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50908-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="50908-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="50908-120">**TEXTO. desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="50908-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





