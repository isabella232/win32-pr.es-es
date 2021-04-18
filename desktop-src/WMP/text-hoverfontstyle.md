---
title: TEXT. hoverFontStyle
description: El atributo hoverFontStyle especifica o recupera el estilo de fuente utilizado para el control de texto cuando el cursor del mouse se desplaza sobre él.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- Media Player de Windows TEXT. hoverFontStyle
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649642"
---
# <a name="texthoverfontstyle"></a><span data-ttu-id="efe7e-104">TEXT. hoverFontStyle</span><span class="sxs-lookup"><span data-stu-id="efe7e-104">TEXT.hoverFontStyle</span></span>

<span data-ttu-id="efe7e-105">El atributo **hoverFontStyle** especifica o recupera el estilo de fuente utilizado para el control de texto cuando el cursor del mouse se desplaza sobre él.</span><span class="sxs-lookup"><span data-stu-id="efe7e-105">The **hoverFontStyle** attribute specifies or retrieves the font style used for the Text control when the mouse cursor hovers over it.</span></span>

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="efe7e-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="efe7e-106">Possible Values</span></span>

<span data-ttu-id="efe7e-107">Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="efe7e-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="efe7e-108">Value</span><span class="sxs-lookup"><span data-stu-id="efe7e-108">Value</span></span>     | <span data-ttu-id="efe7e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="efe7e-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="efe7e-110">Bold</span><span class="sxs-lookup"><span data-stu-id="efe7e-110">Bold</span></span>      | <span data-ttu-id="efe7e-111">Estilo de fuente en negrita.</span><span class="sxs-lookup"><span data-stu-id="efe7e-111">Bold font style.</span></span>      |
| <span data-ttu-id="efe7e-112">Cursiva</span><span class="sxs-lookup"><span data-stu-id="efe7e-112">Italic</span></span>    | <span data-ttu-id="efe7e-113">Estilo de fuente cursiva.</span><span class="sxs-lookup"><span data-stu-id="efe7e-113">Italic font style.</span></span>    |
| <span data-ttu-id="efe7e-114">Subrayado</span><span class="sxs-lookup"><span data-stu-id="efe7e-114">Underline</span></span> | <span data-ttu-id="efe7e-115">Estilo de fuente de subrayado.</span><span class="sxs-lookup"><span data-stu-id="efe7e-115">Underline font style.</span></span> |
| <span data-ttu-id="efe7e-116">Tacha</span><span class="sxs-lookup"><span data-stu-id="efe7e-116">Strikeout</span></span> | <span data-ttu-id="efe7e-117">Estilo de fuente de tachado.</span><span class="sxs-lookup"><span data-stu-id="efe7e-117">Strikeout font style.</span></span> |
| <span data-ttu-id="efe7e-118">Normal</span><span class="sxs-lookup"><span data-stu-id="efe7e-118">Normal</span></span>    | <span data-ttu-id="efe7e-119">Estilo de fuente normal.</span><span class="sxs-lookup"><span data-stu-id="efe7e-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="efe7e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efe7e-120">Remarks</span></span>

<span data-ttu-id="efe7e-121">Se puede usar cualquier combinación de valores, separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="efe7e-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="efe7e-122">El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.</span><span class="sxs-lookup"><span data-stu-id="efe7e-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="efe7e-123">Si no se especifica **hoverFontStyle** , se usa **fontStyle** .</span><span class="sxs-lookup"><span data-stu-id="efe7e-123">If **hoverFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="efe7e-124">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="efe7e-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe7e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe7e-125">Requirements</span></span>



| <span data-ttu-id="efe7e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe7e-126">Requirement</span></span> | <span data-ttu-id="efe7e-127">Value</span><span class="sxs-lookup"><span data-stu-id="efe7e-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="efe7e-128">Versión</span><span class="sxs-lookup"><span data-stu-id="efe7e-128">Version</span></span><br/> | <span data-ttu-id="efe7e-129">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="efe7e-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efe7e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="efe7e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe7e-131">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="efe7e-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="efe7e-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="efe7e-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





