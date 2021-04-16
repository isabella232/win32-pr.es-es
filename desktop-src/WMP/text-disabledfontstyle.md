---
title: TEXT. disabledFontStyle
description: El atributo disabledFontStyle especifica o recupera el estilo de fuente utilizado para el control de texto cuando está deshabilitado.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Media Player de Windows TEXT. disabledFontStyle
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718821"
---
# <a name="textdisabledfontstyle"></a><span data-ttu-id="e283f-104">TEXT. disabledFontStyle</span><span class="sxs-lookup"><span data-stu-id="e283f-104">TEXT.disabledFontStyle</span></span>

<span data-ttu-id="e283f-105">El atributo **disabledFontStyle** especifica o recupera el estilo de fuente utilizado para el control de texto cuando está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e283f-105">The **disabledFontStyle** attribute specifies or retrieves the font style used for the Text control when it is disabled.</span></span>

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="e283f-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e283f-106">Possible Values</span></span>

<span data-ttu-id="e283f-107">Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e283f-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="e283f-108">Value</span><span class="sxs-lookup"><span data-stu-id="e283f-108">Value</span></span>     | <span data-ttu-id="e283f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e283f-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="e283f-110">Bold</span><span class="sxs-lookup"><span data-stu-id="e283f-110">Bold</span></span>      | <span data-ttu-id="e283f-111">Estilo de fuente en negrita.</span><span class="sxs-lookup"><span data-stu-id="e283f-111">Bold font style.</span></span>      |
| <span data-ttu-id="e283f-112">Cursiva</span><span class="sxs-lookup"><span data-stu-id="e283f-112">Italic</span></span>    | <span data-ttu-id="e283f-113">Estilo de fuente cursiva.</span><span class="sxs-lookup"><span data-stu-id="e283f-113">Italic font style.</span></span>    |
| <span data-ttu-id="e283f-114">Subrayado</span><span class="sxs-lookup"><span data-stu-id="e283f-114">Underline</span></span> | <span data-ttu-id="e283f-115">Estilo de fuente de subrayado.</span><span class="sxs-lookup"><span data-stu-id="e283f-115">Underline font style.</span></span> |
| <span data-ttu-id="e283f-116">Tacha</span><span class="sxs-lookup"><span data-stu-id="e283f-116">Strikeout</span></span> | <span data-ttu-id="e283f-117">Estilo de fuente de tachado.</span><span class="sxs-lookup"><span data-stu-id="e283f-117">Strikeout font style.</span></span> |
| <span data-ttu-id="e283f-118">Normal</span><span class="sxs-lookup"><span data-stu-id="e283f-118">Normal</span></span>    | <span data-ttu-id="e283f-119">Estilo de fuente normal.</span><span class="sxs-lookup"><span data-stu-id="e283f-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="e283f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e283f-120">Remarks</span></span>

<span data-ttu-id="e283f-121">Se puede usar cualquier combinación de valores, separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="e283f-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="e283f-122">El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.</span><span class="sxs-lookup"><span data-stu-id="e283f-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="e283f-123">Si no se especifica **disabledFontStyle** , se usa **fontStyle** .</span><span class="sxs-lookup"><span data-stu-id="e283f-123">If **disabledFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="e283f-124">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="e283f-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e283f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e283f-125">Requirements</span></span>



| <span data-ttu-id="e283f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e283f-126">Requirement</span></span> | <span data-ttu-id="e283f-127">Value</span><span class="sxs-lookup"><span data-stu-id="e283f-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e283f-128">Versión</span><span class="sxs-lookup"><span data-stu-id="e283f-128">Version</span></span><br/> | <span data-ttu-id="e283f-129">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e283f-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e283f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e283f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e283f-131">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="e283f-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="e283f-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="e283f-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





