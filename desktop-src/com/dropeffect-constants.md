---
title: Constantes DROPEFFECT (OleIdl. h)
description: Representa información sobre los efectos de una operación de arrastrar y colocar.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696048"
---
# <a name="dropeffect-constants"></a><span data-ttu-id="0db17-103">Constantes de DROPEFFECT</span><span class="sxs-lookup"><span data-stu-id="0db17-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="0db17-104">Representa información sobre los efectos de una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="0db17-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="0db17-105">La función [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) y muchos de los métodos de [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) y [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) usan los valores de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="0db17-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="0db17-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="0db17-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="0db17-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0db17-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="0db17-108"><dt>**DROPEFFECT \_ NINGUNO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0db17-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="0db17-109">El destino de colocación no puede aceptar los datos.</span><span class="sxs-lookup"><span data-stu-id="0db17-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="0db17-110"><dt>**DROPEFFECT \_ COPIAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0db17-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="0db17-111">Drop da como resultado una copia.</span><span class="sxs-lookup"><span data-stu-id="0db17-111">Drop results in a copy.</span></span> <span data-ttu-id="0db17-112">El origen de arrastre no toca los datos originales.</span><span class="sxs-lookup"><span data-stu-id="0db17-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="0db17-113"><dt>**DROPEFFECT \_ MOVIMIENTO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0db17-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="0db17-114">El origen de arrastre debe quitar los datos.</span><span class="sxs-lookup"><span data-stu-id="0db17-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="0db17-115"><dt>**DROPEFFECT \_ VÍNCULO**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0db17-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="0db17-116">Arrastrar origen debe crear un vínculo a los datos originales.</span><span class="sxs-lookup"><span data-stu-id="0db17-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="0db17-117"><dt>**DROPEFFECT \_ DESPLAZAMIENTO**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="0db17-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="0db17-118">El desplazamiento está a punto de iniciarse o está ocurriendo actualmente en el destino.</span><span class="sxs-lookup"><span data-stu-id="0db17-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="0db17-119">Este valor se usa además de los demás valores.</span><span class="sxs-lookup"><span data-stu-id="0db17-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0db17-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0db17-120">Remarks</span></span>

<span data-ttu-id="0db17-121">La aplicación siempre debe enmascarar los valores de la enumeración **DROPEFFECT** para garantizar la compatibilidad con implementaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="0db17-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="0db17-122">Actualmente, solo algunas de las posiciones de un valor de **DROPEFFECT** tienen significado.</span><span class="sxs-lookup"><span data-stu-id="0db17-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="0db17-123">En el futuro, se agregarán más interpretaciones para los bits.</span><span class="sxs-lookup"><span data-stu-id="0db17-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="0db17-124">Los orígenes de arrastre y los destinos de colocación deben enmascarar cuidadosamente estos valores adecuadamente antes de la comparación.</span><span class="sxs-lookup"><span data-stu-id="0db17-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="0db17-125">Nunca deben comparar un **DROPEFFECT** con, por ejemplo, la copia DROPEFFECT, para lo que debe \_ hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0db17-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="0db17-126">En su lugar, la aplicación siempre debe enmascarar el valor o los valores que se buscan como si utilizara una de las técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0db17-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="0db17-127">Esto permite la definición de nuevos efectos de colocación, a la vez que conserva la compatibilidad con versiones anteriores con el código existente.</span><span class="sxs-lookup"><span data-stu-id="0db17-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db17-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db17-128">Requirements</span></span>



| <span data-ttu-id="0db17-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db17-129">Requirement</span></span> | <span data-ttu-id="0db17-130">Value</span><span class="sxs-lookup"><span data-stu-id="0db17-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0db17-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db17-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0db17-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0db17-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0db17-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db17-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0db17-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0db17-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0db17-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0db17-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db17-136"><dt>OleIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db17-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db17-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0db17-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db17-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="0db17-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="0db17-139">**IDropSource**</span><span class="sxs-lookup"><span data-stu-id="0db17-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="0db17-140">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="0db17-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





