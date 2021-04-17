---
title: AmbientAttributes. verticalAlignment
description: El atributo verticalAlignment especifica o recupera un valor que indica la posición vertical del control cuando se ajusta la vista o la subvista primaria.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes. verticalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700193"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="cca2c-104">AmbientAttributes. verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="cca2c-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="cca2c-105">El atributo **verticalAlignment** especifica o recupera un valor que indica la posición vertical del control cuando se ajusta la **vista** o la **subvista** primaria.</span><span class="sxs-lookup"><span data-stu-id="cca2c-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="cca2c-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="cca2c-106">Possible Values</span></span>

<span data-ttu-id="cca2c-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="cca2c-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="cca2c-108">Value</span><span class="sxs-lookup"><span data-stu-id="cca2c-108">Value</span></span>   | <span data-ttu-id="cca2c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cca2c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca2c-110">top</span><span class="sxs-lookup"><span data-stu-id="cca2c-110">top</span></span>     | <span data-ttu-id="cca2c-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cca2c-111">Default.</span></span> <span data-ttu-id="cca2c-112">Mantiene la posición del control en relación con la parte superior de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="cca2c-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="cca2c-113">abajo</span><span class="sxs-lookup"><span data-stu-id="cca2c-113">bottom</span></span>  | <span data-ttu-id="cca2c-114">Mantiene la posición del control en relación con la parte inferior de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="cca2c-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="cca2c-115">centro</span><span class="sxs-lookup"><span data-stu-id="cca2c-115">center</span></span>  | <span data-ttu-id="cca2c-116">Mantiene la posición del control en relación con el centro vertical de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.</span><span class="sxs-lookup"><span data-stu-id="cca2c-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="cca2c-117">ajustar</span><span class="sxs-lookup"><span data-stu-id="cca2c-117">stretch</span></span> | <span data-ttu-id="cca2c-118">Mantiene la posición del control en relación con los márgenes superior e inferior de la vista cuando se cambia el tamaño.</span><span class="sxs-lookup"><span data-stu-id="cca2c-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="cca2c-119">El control se ajusta para ajustarse cuando se ajusta la **vista** o la **subvista** primaria.</span><span class="sxs-lookup"><span data-stu-id="cca2c-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="cca2c-120">La imagen real no aumenta ni se reduce a menos que se puedan cambiar de tamaño, pero el área en la que se hace clic aumenta o disminuye si no está limitada por un **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="cca2c-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cca2c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cca2c-121">Remarks</span></span>

<span data-ttu-id="cca2c-122">A menos que **verticalAlignment** se establezca en "Center", el control conserva su distancia original desde el borde especificado o desde ambos bordes si se especifica "stretch" y se ajusta el tamaño del control.</span><span class="sxs-lookup"><span data-stu-id="cca2c-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="cca2c-123">Si el control no es de tamaño variable y se especifica "stretch", en su lugar se expande la región en la que se hace clic.</span><span class="sxs-lookup"><span data-stu-id="cca2c-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="cca2c-124">Puede establecer cualquier combinación de los atributos **horizontalAlignment** y **verticalAlignment** .</span><span class="sxs-lookup"><span data-stu-id="cca2c-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="cca2c-125">Por ejemplo, si desea que un control se Centre tanto horizontal como verticalmente, establezca **horizontalAlignment** en "Center" y **verticalAlignment** en "Center".</span><span class="sxs-lookup"><span data-stu-id="cca2c-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="cca2c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cca2c-126">Requirements</span></span>



| <span data-ttu-id="cca2c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca2c-127">Requirement</span></span> | <span data-ttu-id="cca2c-128">Value</span><span class="sxs-lookup"><span data-stu-id="cca2c-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cca2c-129">Versión</span><span class="sxs-lookup"><span data-stu-id="cca2c-129">Version</span></span><br/> | <span data-ttu-id="cca2c-130">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cca2c-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cca2c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cca2c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca2c-132">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="cca2c-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="cca2c-133">**AmbientAttributes. horizontalAlignment**</span><span class="sxs-lookup"><span data-stu-id="cca2c-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





