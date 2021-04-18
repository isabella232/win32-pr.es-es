---
title: THEME. openViewRelative
description: El método openViewRelative abre una vista en una nueva ventana en la posición inicial especificada relativa a la esquina superior izquierda de la máscara.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- Media Player de Windows de THEME. openViewRelative
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680246"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="6233b-104">THEME. openViewRelative</span><span class="sxs-lookup"><span data-stu-id="6233b-104">THEME.openViewRelative</span></span>

<span data-ttu-id="6233b-105">El método **openViewRelative** abre una **vista** en una nueva ventana en la posición inicial especificada relativa a la esquina superior izquierda de la máscara.</span><span class="sxs-lookup"><span data-stu-id="6233b-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="6233b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6233b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6233b-107"><span id="view"></span><span id="VIEW"></span>*Visores*</span><span class="sxs-lookup"><span data-stu-id="6233b-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="6233b-108">**Cadena** que especifica el **identificador** de la **vista** que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="6233b-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="6233b-109"><span id="left"></span><span id="LEFT"></span>*salido*</span><span class="sxs-lookup"><span data-stu-id="6233b-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="6233b-110">**Número** (**Long**) que especifica la distancia inicial en píxeles del borde izquierdo de la **vista** desde el borde izquierdo de la máscara.</span><span class="sxs-lookup"><span data-stu-id="6233b-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="6233b-111">Un valor negativo indica una posición inicial a la izquierda del borde de la máscara.</span><span class="sxs-lookup"><span data-stu-id="6233b-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="6233b-112"><span id="top"></span><span id="TOP"></span>*Arriba*</span><span class="sxs-lookup"><span data-stu-id="6233b-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="6233b-113">**Número** (**Long**) que especifica la posición inicial del borde superior de la **vista** con respecto al borde superior de la máscara.</span><span class="sxs-lookup"><span data-stu-id="6233b-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="6233b-114">Un valor negativo indica una posición inicial sobre el borde de la máscara.</span><span class="sxs-lookup"><span data-stu-id="6233b-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6233b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6233b-115">Return Value</span></span>

<span data-ttu-id="6233b-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6233b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6233b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6233b-117">Remarks</span></span>

<span data-ttu-id="6233b-118">La posición especificada para la **vista** se usa la primera vez que se llama a este método, después de lo cual el usuario puede arrastrar la **vista** a otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="6233b-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="6233b-119">La nueva posición se guarda y, en las llamadas posteriores, se usa la posición más reciente.</span><span class="sxs-lookup"><span data-stu-id="6233b-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="6233b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6233b-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="6233b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6233b-121">Requirements</span></span>



| <span data-ttu-id="6233b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6233b-122">Requirement</span></span> | <span data-ttu-id="6233b-123">Value</span><span class="sxs-lookup"><span data-stu-id="6233b-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6233b-124">Versión</span><span class="sxs-lookup"><span data-stu-id="6233b-124">Version</span></span><br/> | <span data-ttu-id="6233b-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="6233b-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6233b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6233b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6233b-127">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="6233b-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="6233b-128">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="6233b-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="6233b-129">**THEME. openView**</span><span class="sxs-lookup"><span data-stu-id="6233b-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





