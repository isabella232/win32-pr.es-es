---
title: AmbientAttributes. horizontalAlignment
description: El atributo horizontalAlignment especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el tamaño de la vista o la subvista primaria.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes. horizontalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698635"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="a1099-104">AmbientAttributes. horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="a1099-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="a1099-105">El atributo **horizontalAlignment** especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el **tamaño de la vista o la** **subvista** primaria.</span><span class="sxs-lookup"><span data-stu-id="a1099-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="a1099-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a1099-106">Possible Values</span></span>

<span data-ttu-id="a1099-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="a1099-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="a1099-108">Value</span><span class="sxs-lookup"><span data-stu-id="a1099-108">Value</span></span>   | <span data-ttu-id="a1099-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1099-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1099-110">izquierda</span><span class="sxs-lookup"><span data-stu-id="a1099-110">left</span></span>    | <span data-ttu-id="a1099-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a1099-111">Default.</span></span> <span data-ttu-id="a1099-112">Mantiene la posición del control en relación con la parte izquierda de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="a1099-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a1099-113">right</span><span class="sxs-lookup"><span data-stu-id="a1099-113">right</span></span>   | <span data-ttu-id="a1099-114">Mantiene la posición del control en relación con la derecha de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="a1099-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="a1099-115">centro</span><span class="sxs-lookup"><span data-stu-id="a1099-115">center</span></span>  | <span data-ttu-id="a1099-116">Mantiene la posición del control en relación con el centro horizontal de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="a1099-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="a1099-117">ajustar</span><span class="sxs-lookup"><span data-stu-id="a1099-117">stretch</span></span> | <span data-ttu-id="a1099-118">Mantiene la posición del control en relación con los márgenes izquierdo y derecho de la **vista** o la **subvista** primaria cuando se cambia el tamaño.</span><span class="sxs-lookup"><span data-stu-id="a1099-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="a1099-119">El control se ajusta para ajustarse cuando se ajusta la **vista** o la **subvista** .</span><span class="sxs-lookup"><span data-stu-id="a1099-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="a1099-120">La imagen real no aumenta ni se reduce a menos que se puedan cambiar de tamaño, pero el área en la que se hace clic aumenta o disminuye si no está limitada por un **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="a1099-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a1099-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1099-121">Remarks</span></span>

<span data-ttu-id="a1099-122">A menos que **horizontalAlignment** se establezca en "Center", el control conserva su distancia original desde el borde especificado o desde ambos bordes si se especifica "stretch" y se ajusta el tamaño del control.</span><span class="sxs-lookup"><span data-stu-id="a1099-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="a1099-123">Si el control no es de tamaño variable y se especifica "stretch", en su lugar se expande la región en la que se hace clic.</span><span class="sxs-lookup"><span data-stu-id="a1099-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="a1099-124">Puede establecer cualquier combinación de **horizontalAlignment** y **verticalAlignment**.</span><span class="sxs-lookup"><span data-stu-id="a1099-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="a1099-125">Por ejemplo, si desea centrar un control tanto horizontal como verticalmente, establezca horizontalAlignment = "Center" verticalAlignment = "Center".</span><span class="sxs-lookup"><span data-stu-id="a1099-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="a1099-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1099-126">Requirements</span></span>



| <span data-ttu-id="a1099-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1099-127">Requirement</span></span> | <span data-ttu-id="a1099-128">Value</span><span class="sxs-lookup"><span data-stu-id="a1099-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a1099-129">Versión</span><span class="sxs-lookup"><span data-stu-id="a1099-129">Version</span></span><br/> | <span data-ttu-id="a1099-130">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a1099-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1099-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1099-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1099-132">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="a1099-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1099-133">**AmbientAttributes. verticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="a1099-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="a1099-134">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="a1099-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





