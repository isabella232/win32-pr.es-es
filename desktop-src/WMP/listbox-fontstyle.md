---
title: LISTBOX. fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control de cuadro de lista.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699635"
---
# <a name="listboxfontstyle"></a><span data-ttu-id="f6b32-104">LISTBOX. fontStyle</span><span class="sxs-lookup"><span data-stu-id="f6b32-104">LISTBOX.fontStyle</span></span>

<span data-ttu-id="f6b32-105">El atributo **fontStyle** especifica o recupera el estilo de fuente para el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="f6b32-105">The **fontStyle** attribute specifies or retrieves the font style for the list box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="f6b32-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f6b32-106">Possible Values</span></span>

<span data-ttu-id="f6b32-107">Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f6b32-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="f6b32-108">Value</span><span class="sxs-lookup"><span data-stu-id="f6b32-108">Value</span></span>     | <span data-ttu-id="f6b32-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6b32-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="f6b32-110">Bold</span><span class="sxs-lookup"><span data-stu-id="f6b32-110">Bold</span></span>      | <span data-ttu-id="f6b32-111">Estilo de fuente en negrita.</span><span class="sxs-lookup"><span data-stu-id="f6b32-111">Bold font style.</span></span>      |
| <span data-ttu-id="f6b32-112">Cursiva</span><span class="sxs-lookup"><span data-stu-id="f6b32-112">Italic</span></span>    | <span data-ttu-id="f6b32-113">Estilo de fuente cursiva.</span><span class="sxs-lookup"><span data-stu-id="f6b32-113">Italic font style.</span></span>    |
| <span data-ttu-id="f6b32-114">Subrayado</span><span class="sxs-lookup"><span data-stu-id="f6b32-114">Underline</span></span> | <span data-ttu-id="f6b32-115">Estilo de fuente de subrayado.</span><span class="sxs-lookup"><span data-stu-id="f6b32-115">Underline font style.</span></span> |
| <span data-ttu-id="f6b32-116">Tacha</span><span class="sxs-lookup"><span data-stu-id="f6b32-116">Strikeout</span></span> | <span data-ttu-id="f6b32-117">Estilo de fuente de tachado.</span><span class="sxs-lookup"><span data-stu-id="f6b32-117">Strikeout font style.</span></span> |
| <span data-ttu-id="f6b32-118">Normal</span><span class="sxs-lookup"><span data-stu-id="f6b32-118">Normal</span></span>    | <span data-ttu-id="f6b32-119">Estilo de fuente normal.</span><span class="sxs-lookup"><span data-stu-id="f6b32-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="f6b32-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6b32-120">Remarks</span></span>

<span data-ttu-id="f6b32-121">Se puede usar cualquier combinación de valores, separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="f6b32-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="f6b32-122">El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.</span><span class="sxs-lookup"><span data-stu-id="f6b32-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="f6b32-123">Para fines de representación, el estilo de fuente predeterminado es normal.</span><span class="sxs-lookup"><span data-stu-id="f6b32-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="f6b32-124">El valor predeterminado recuperado de este atributo es "" (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="f6b32-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b32-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b32-125">Requirements</span></span>



| <span data-ttu-id="f6b32-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b32-126">Requirement</span></span> | <span data-ttu-id="f6b32-127">Value</span><span class="sxs-lookup"><span data-stu-id="f6b32-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="f6b32-128">Versión</span><span class="sxs-lookup"><span data-stu-id="f6b32-128">Version</span></span><br/> | <span data-ttu-id="f6b32-129">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="f6b32-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6b32-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6b32-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b32-131">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="f6b32-131">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="f6b32-132">**LISTBOX. FontSize**</span><span class="sxs-lookup"><span data-stu-id="f6b32-132">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> </dl>

 

 





