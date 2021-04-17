---
title: VISTA. tamaño
description: El método size cambia el tamaño de la vista en un borde especificado.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VISTA. tamaño de Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708274"
---
# <a name="viewsize"></a><span data-ttu-id="8d1f6-104">VISTA. tamaño</span><span class="sxs-lookup"><span data-stu-id="8d1f6-104">VIEW.size</span></span>

<span data-ttu-id="8d1f6-105">El método **size cambia** el tamaño de la **vista** en un borde especificado.</span><span class="sxs-lookup"><span data-stu-id="8d1f6-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="8d1f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d1f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d1f6-107"><span id="handle"></span><span id="HANDLE"></span>*asa*</span><span class="sxs-lookup"><span data-stu-id="8d1f6-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="8d1f6-108">Cadena que especifica el borde o la esquina que se va a desplace al ajustar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="8d1f6-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="8d1f6-109">Esta cadena debe tener uno de los ocho valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8d1f6-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="8d1f6-110">Edge</span><span class="sxs-lookup"><span data-stu-id="8d1f6-110">Edge</span></span>   | <span data-ttu-id="8d1f6-111">Esquina</span><span class="sxs-lookup"><span data-stu-id="8d1f6-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="8d1f6-112">top</span><span class="sxs-lookup"><span data-stu-id="8d1f6-112">top</span></span>    | <span data-ttu-id="8d1f6-113">esquina superior</span><span class="sxs-lookup"><span data-stu-id="8d1f6-113">topright</span></span>    |
| <span data-ttu-id="8d1f6-114">right</span><span class="sxs-lookup"><span data-stu-id="8d1f6-114">right</span></span>  | <span data-ttu-id="8d1f6-115">PivotDetailRange</span><span class="sxs-lookup"><span data-stu-id="8d1f6-115">bottomright</span></span> |
| <span data-ttu-id="8d1f6-116">abajo</span><span class="sxs-lookup"><span data-stu-id="8d1f6-116">bottom</span></span> | <span data-ttu-id="8d1f6-117">bottomleft</span><span class="sxs-lookup"><span data-stu-id="8d1f6-117">bottomleft</span></span>  |
| <span data-ttu-id="8d1f6-118">izquierda</span><span class="sxs-lookup"><span data-stu-id="8d1f6-118">left</span></span>   | <span data-ttu-id="8d1f6-119">a la izquierda</span><span class="sxs-lookup"><span data-stu-id="8d1f6-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d1f6-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d1f6-120">Return Value</span></span>

<span data-ttu-id="8d1f6-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8d1f6-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1f6-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d1f6-122">Remarks</span></span>

<span data-ttu-id="8d1f6-123">Normalmente, este método se llama desde dentro de un controlador **OnMouseDown** .</span><span class="sxs-lookup"><span data-stu-id="8d1f6-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="8d1f6-124">Se encarga del cambio de tamaño mientras se arrastra el mouse y se detiene el cambio de tamaño cuando se suelta el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="8d1f6-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="8d1f6-125">Si el tamaño de la **vista** está restringido, no puede arrastrar el mouse para cambiar el tamaño de la **vista** más allá de los límites restringidos.</span><span class="sxs-lookup"><span data-stu-id="8d1f6-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="8d1f6-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d1f6-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="8d1f6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d1f6-127">Requirements</span></span>



| <span data-ttu-id="8d1f6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d1f6-128">Requirement</span></span> | <span data-ttu-id="8d1f6-129">Value</span><span class="sxs-lookup"><span data-stu-id="8d1f6-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8d1f6-130">Versión</span><span class="sxs-lookup"><span data-stu-id="8d1f6-130">Version</span></span><br/> | <span data-ttu-id="8d1f6-131">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8d1f6-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d1f6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d1f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1f6-133">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="8d1f6-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





