---
title: LISTBOX. popUp
description: El atributo popUp especifica un valor que indica si el elemento representa un control popUp o de cuadro de lista.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708843"
---
# <a name="listboxpopup"></a><span data-ttu-id="953ad-104">LISTBOX. popUp</span><span class="sxs-lookup"><span data-stu-id="953ad-104">LISTBOX.popUp</span></span>

<span data-ttu-id="953ad-105">El atributo **popUp** especifica un valor que indica si el elemento representa un control popUp o de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="953ad-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="953ad-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="953ad-106">Possible Values</span></span>

<span data-ttu-id="953ad-107">Este atributo es un **valor booleano** especificado solo en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="953ad-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="953ad-108">Value</span><span class="sxs-lookup"><span data-stu-id="953ad-108">Value</span></span> | <span data-ttu-id="953ad-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="953ad-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="953ad-110">true</span><span class="sxs-lookup"><span data-stu-id="953ad-110">true</span></span>  | <span data-ttu-id="953ad-111">El elemento representa un control Popup.</span><span class="sxs-lookup"><span data-stu-id="953ad-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="953ad-112">false</span><span class="sxs-lookup"><span data-stu-id="953ad-112">false</span></span> | <span data-ttu-id="953ad-113">El elemento representa un control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="953ad-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="953ad-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="953ad-114">Remarks</span></span>

<span data-ttu-id="953ad-115">El elemento **popup** representa un control de cuadro de lista que se muestra solo cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="953ad-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="953ad-116">Es idéntico al elemento **ListBox** excepto el valor predeterminado de este atributo, que cambia el comportamiento de presentación.</span><span class="sxs-lookup"><span data-stu-id="953ad-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="953ad-117">En el caso de los elementos **ListBox** , el valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="953ad-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="953ad-118">En el caso de los elementos **emergentes** , el valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="953ad-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="953ad-119">En lugar de especificar este atributo, el **cuadro de lista** o elemento **emergente** debe usarse en función del comportamiento deseado.</span><span class="sxs-lookup"><span data-stu-id="953ad-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="953ad-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="953ad-120">Requirements</span></span>



| <span data-ttu-id="953ad-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="953ad-121">Requirement</span></span> | <span data-ttu-id="953ad-122">Value</span><span class="sxs-lookup"><span data-stu-id="953ad-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="953ad-123">Versión</span><span class="sxs-lookup"><span data-stu-id="953ad-123">Version</span></span><br/> | <span data-ttu-id="953ad-124">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="953ad-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="953ad-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="953ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953ad-126">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="953ad-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="953ad-127">**Elemento POPUP**</span><span class="sxs-lookup"><span data-stu-id="953ad-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





