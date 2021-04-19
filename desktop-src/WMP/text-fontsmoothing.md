---
title: TEXT. fontSmoothing
description: El atributo fontSmoothing especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Media Player de Windows TEXT. fontSmoothing
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698704"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="acaf0-104">TEXT. fontSmoothing</span><span class="sxs-lookup"><span data-stu-id="acaf0-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="acaf0-105">El atributo **fontSmoothing** especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.</span><span class="sxs-lookup"><span data-stu-id="acaf0-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="acaf0-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="acaf0-106">Possible Values</span></span>

<span data-ttu-id="acaf0-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="acaf0-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="acaf0-108">Value</span><span class="sxs-lookup"><span data-stu-id="acaf0-108">Value</span></span> | <span data-ttu-id="acaf0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="acaf0-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="acaf0-110">true</span><span class="sxs-lookup"><span data-stu-id="acaf0-110">true</span></span>  | <span data-ttu-id="acaf0-111">El suavizado de fuentes está habilitado.</span><span class="sxs-lookup"><span data-stu-id="acaf0-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="acaf0-112">false</span><span class="sxs-lookup"><span data-stu-id="acaf0-112">false</span></span> | <span data-ttu-id="acaf0-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="acaf0-113">Default.</span></span> <span data-ttu-id="acaf0-114">El suavizado de fuentes está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="acaf0-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="acaf0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acaf0-115">Remarks</span></span>

<span data-ttu-id="acaf0-116">El suavizado de fuentes utiliza la característica de suavizado de contorno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="acaf0-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="acaf0-117">Si el suavizado de fuentes está habilitado y el sistema operativo admite el suavizado de contorno, Windows Media Player intenta suavizar el texto.</span><span class="sxs-lookup"><span data-stu-id="acaf0-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="acaf0-118">No todas las fuentes admiten el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="acaf0-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="acaf0-119">Windows Media Player 10 usa el método de suavizado de contorno ClearType de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="acaf0-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="acaf0-120">**ADVERTENCIA** de El suavizado de fuentes sobre un color transparente puede hacer que el color transparente se mezcle en los caracteres.</span><span class="sxs-lookup"><span data-stu-id="acaf0-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="acaf0-121">No se recomienda usar **fontSmoothing** si el texto se va a mostrar sobre una transparencia.</span><span class="sxs-lookup"><span data-stu-id="acaf0-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="acaf0-122">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="acaf0-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="acaf0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acaf0-123">Requirements</span></span>



| <span data-ttu-id="acaf0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="acaf0-124">Requirement</span></span> | <span data-ttu-id="acaf0-125">Value</span><span class="sxs-lookup"><span data-stu-id="acaf0-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="acaf0-126">Versión</span><span class="sxs-lookup"><span data-stu-id="acaf0-126">Version</span></span><br/> | <span data-ttu-id="acaf0-127">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="acaf0-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="acaf0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="acaf0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acaf0-129">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="acaf0-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





