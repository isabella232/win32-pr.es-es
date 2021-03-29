---
title: Código de notificación de DL_DRAGGING (commctrl. h)
description: Indica que el usuario ha desplazado el mouse mientras arrastra un elemento.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535650"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="616d5-104">Código de notificación de arrastre de DL \_</span><span class="sxs-lookup"><span data-stu-id="616d5-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="616d5-105">Indica que el usuario ha desplazado el mouse mientras arrastra un elemento.</span><span class="sxs-lookup"><span data-stu-id="616d5-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="616d5-106">\_La acción de arrastrar DL también se envía periódicamente durante el arrastre incluso si el mouse no se mueve.</span><span class="sxs-lookup"><span data-stu-id="616d5-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="616d5-107">Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre.</span><span class="sxs-lookup"><span data-stu-id="616d5-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="616d5-108">Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="616d5-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="616d5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="616d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616d5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="616d5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="616d5-111">Identificador del control del cuadro de lista de arrastre.</span><span class="sxs-lookup"><span data-stu-id="616d5-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="616d5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="616d5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="616d5-113">Puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de \_ notificación de arrastre DL, el identificador del cuadro de lista de arrastre y la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="616d5-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616d5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="616d5-114">Return value</span></span>

<span data-ttu-id="616d5-115">El valor devuelto determina el tipo de cursor del mouse que debe establecer la lista de arrastre; puede ser el valor DL \_ STOPCURSOR, DL \_ COPYCURSOR o DL \_ MOVECURSOR.</span><span class="sxs-lookup"><span data-stu-id="616d5-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="616d5-116">Si se devuelve cualquier otro valor, el cursor no cambia.</span><span class="sxs-lookup"><span data-stu-id="616d5-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="616d5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="616d5-117">Remarks</span></span>

<span data-ttu-id="616d5-118">Un procedimiento de ventana normalmente procesa el código de la notificación de arrastre de la DL \_ determinando el elemento bajo el cursor y dibujando un icono de inserción.</span><span class="sxs-lookup"><span data-stu-id="616d5-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="616d5-119">Para recuperar el elemento bajo el cursor, utilice la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , especificando **true** para el parámetro *bAutoScroll* .</span><span class="sxs-lookup"><span data-stu-id="616d5-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="616d5-120">Esta opción hace que el cuadro de lista de arrastre se desplace periódicamente si el cursor está por encima o por debajo de su área de cliente.</span><span class="sxs-lookup"><span data-stu-id="616d5-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="616d5-121">Para dibujar el icono de inserción, utilice la función [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .</span><span class="sxs-lookup"><span data-stu-id="616d5-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="616d5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="616d5-122">Requirements</span></span>



| <span data-ttu-id="616d5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="616d5-123">Requirement</span></span> | <span data-ttu-id="616d5-124">Value</span><span class="sxs-lookup"><span data-stu-id="616d5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="616d5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="616d5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="616d5-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="616d5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="616d5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="616d5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="616d5-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="616d5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="616d5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="616d5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="616d5-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="616d5-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





