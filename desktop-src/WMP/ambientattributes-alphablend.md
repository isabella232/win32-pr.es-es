---
title: AmbientAttributes.alphaBlend
description: El atributo alphaBlend especifica o recupera un valor para la combinación alfa de cualquier vista, subvista o widget de interfaz de usuario.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AmbientAttributes. alphaBlend Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700070"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="034ce-104">AmbientAttributes.alphaBlend</span><span class="sxs-lookup"><span data-stu-id="034ce-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="034ce-105">El atributo **alphaBlend** especifica o recupera un valor para la combinación alfa de cualquier **vista**, **subvista** o widget de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="034ce-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="034ce-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="034ce-106">Possible Values</span></span>

<span data-ttu-id="034ce-107">Este atributo es un **número** de lectura y escritura (**Long**) con un valor comprendido entre 0 (sin opacidad) y 255 (opacidad completa) y un valor predeterminado de 255.</span><span class="sxs-lookup"><span data-stu-id="034ce-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="034ce-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="034ce-108">Remarks</span></span>

<span data-ttu-id="034ce-109">Este atributo permite que un elemento parezca semitransparente, dependiendo de la cantidad del conjunto de opacidad.</span><span class="sxs-lookup"><span data-stu-id="034ce-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="034ce-110">Cuanto menor sea la opacidad, más transparente aparecerá el elemento.</span><span class="sxs-lookup"><span data-stu-id="034ce-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="034ce-111">Cada elemento de la máscara puede tener un valor de opacidad independiente, excepto para los elementos de botón en un control **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="034ce-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="034ce-112">Cuando **alphaBlend** se establece en la **vista**, se establecerá la opacidad de toda la máscara.</span><span class="sxs-lookup"><span data-stu-id="034ce-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="034ce-113">Alpha Blend no funcionará con los controles con ventanas, como **listas de reproducción**, **efectos**, cuadros de **lista**, **ventanas emergentes, cuadro** de **edición** y **vídeo** (si **Windowless** está establecido en false).</span><span class="sxs-lookup"><span data-stu-id="034ce-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="034ce-114">Cuando **alphaBlend** se establece en la **vista**, toda la máscara se vuelve transparente.</span><span class="sxs-lookup"><span data-stu-id="034ce-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="034ce-115">Los atributos **transparencyColor** utilizados por varios elementos no se admiten con **alphaBlend**.</span><span class="sxs-lookup"><span data-stu-id="034ce-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="034ce-116">Cuando se usa **alphaBlend** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro.</span><span class="sxs-lookup"><span data-stu-id="034ce-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="034ce-117">Si el color de primer plano también es negro (que es el valor predeterminado del *texto*).**foregroundColor**), es posible que el texto sea ilegible.</span><span class="sxs-lookup"><span data-stu-id="034ce-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="034ce-118">Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.</span><span class="sxs-lookup"><span data-stu-id="034ce-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="034ce-119">Este atributo no se admite en Windows 98.</span><span class="sxs-lookup"><span data-stu-id="034ce-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="034ce-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="034ce-120">Requirements</span></span>



| <span data-ttu-id="034ce-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="034ce-121">Requirement</span></span> | <span data-ttu-id="034ce-122">Value</span><span class="sxs-lookup"><span data-stu-id="034ce-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="034ce-123">Versión</span><span class="sxs-lookup"><span data-stu-id="034ce-123">Version</span></span><br/> | <span data-ttu-id="034ce-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="034ce-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="034ce-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="034ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034ce-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="034ce-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="034ce-127">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="034ce-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="034ce-128">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="034ce-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="034ce-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="034ce-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="034ce-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="034ce-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





