---
title: AmbientAttributes. zIndex
description: El atributo zIndex especifica o recupera el orden en el que se representa el control.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Media Player de Windows AmbientAttributes. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700091"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="b7ae1-104">AmbientAttributes. zIndex</span><span class="sxs-lookup"><span data-stu-id="b7ae1-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="b7ae1-105">El atributo **ZIndex** especifica o recupera el orden en el que se representa el control.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="b7ae1-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="b7ae1-106">Possible Values</span></span>

<span data-ttu-id="b7ae1-107">Este atributo es un **número** de lectura y escritura (**Long**) con un valor predeterminado de cero.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="b7ae1-108">El intervalo es el de un entero largo con signo.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7ae1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7ae1-109">Remarks</span></span>

<span data-ttu-id="b7ae1-110">El mapa de bits de fondo de una **vista** o una **subvista** tiene un índice z fijo de cero.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="b7ae1-111">Si desea que un control esté detrás del fondo, el valor de **ZIndex** debe establecerse en un número negativo.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="b7ae1-112">El índice z de una **vista** o una **subvista** es un índice absoluto, mientras que el índice z de un control es relativo al índice z de la **vista** o la **subvista** que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="b7ae1-113">El atributo **ZIndex** no es compatible con los elementos de la **lista de reproducción** y el **Explorador** .</span><span class="sxs-lookup"><span data-stu-id="b7ae1-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="b7ae1-114">No funcionará con el elemento de **vídeo** si se trata de un *vídeo*. **Windowless** está establecido en false, y en el elemento **Effects** si tiene **efectos**. **windowed** está establecido en true.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="b7ae1-115">Los elementos **BUTTONELEMENT** usan el **ZIndex** de sus **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b7ae1-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ae1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7ae1-116">Requirements</span></span>



| <span data-ttu-id="b7ae1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7ae1-117">Requirement</span></span> | <span data-ttu-id="b7ae1-118">Value</span><span class="sxs-lookup"><span data-stu-id="b7ae1-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b7ae1-119">Versión</span><span class="sxs-lookup"><span data-stu-id="b7ae1-119">Version</span></span><br/> | <span data-ttu-id="b7ae1-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b7ae1-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7ae1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7ae1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ae1-122">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="b7ae1-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





