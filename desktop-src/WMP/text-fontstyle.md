---
title: TEXT. fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control de texto.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649551"
---
# <a name="textfontstyle"></a><span data-ttu-id="8caab-104">TEXT. fontStyle</span><span class="sxs-lookup"><span data-stu-id="8caab-104">TEXT.fontStyle</span></span>

<span data-ttu-id="8caab-105">El atributo **fontStyle** especifica o recupera el estilo de fuente para el control de texto.</span><span class="sxs-lookup"><span data-stu-id="8caab-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="8caab-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="8caab-106">Possible Values</span></span>

<span data-ttu-id="8caab-107">Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8caab-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="8caab-108">Value</span><span class="sxs-lookup"><span data-stu-id="8caab-108">Value</span></span>     | <span data-ttu-id="8caab-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8caab-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="8caab-110">Bold</span><span class="sxs-lookup"><span data-stu-id="8caab-110">Bold</span></span>      | <span data-ttu-id="8caab-111">Estilo de fuente en negrita.</span><span class="sxs-lookup"><span data-stu-id="8caab-111">Bold font style.</span></span>            |
| <span data-ttu-id="8caab-112">Cursiva</span><span class="sxs-lookup"><span data-stu-id="8caab-112">Italic</span></span>    | <span data-ttu-id="8caab-113">Estilo de fuente cursiva.</span><span class="sxs-lookup"><span data-stu-id="8caab-113">Italic font style.</span></span>          |
| <span data-ttu-id="8caab-114">Subrayado</span><span class="sxs-lookup"><span data-stu-id="8caab-114">Underline</span></span> | <span data-ttu-id="8caab-115">Estilo de fuente de subrayado.</span><span class="sxs-lookup"><span data-stu-id="8caab-115">Underline font style.</span></span>       |
| <span data-ttu-id="8caab-116">Tacha</span><span class="sxs-lookup"><span data-stu-id="8caab-116">Strikeout</span></span> | <span data-ttu-id="8caab-117">Estilo de fuente de tachado.</span><span class="sxs-lookup"><span data-stu-id="8caab-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="8caab-118">Normal</span><span class="sxs-lookup"><span data-stu-id="8caab-118">Normal</span></span>    | <span data-ttu-id="8caab-119">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8caab-119">Default.</span></span> <span data-ttu-id="8caab-120">Estilo de fuente normal.</span><span class="sxs-lookup"><span data-stu-id="8caab-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8caab-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8caab-121">Remarks</span></span>

<span data-ttu-id="8caab-122">Se puede usar cualquier combinación de valores, separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="8caab-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="8caab-123">El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.</span><span class="sxs-lookup"><span data-stu-id="8caab-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="8caab-124">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="8caab-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8caab-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8caab-125">Requirements</span></span>



| <span data-ttu-id="8caab-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8caab-126">Requirement</span></span> | <span data-ttu-id="8caab-127">Value</span><span class="sxs-lookup"><span data-stu-id="8caab-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8caab-128">Versión</span><span class="sxs-lookup"><span data-stu-id="8caab-128">Version</span></span><br/> | <span data-ttu-id="8caab-129">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8caab-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8caab-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8caab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8caab-131">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="8caab-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





