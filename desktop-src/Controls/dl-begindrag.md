---
title: Código de notificación de DL_BEGINDRAG (commctrl. h)
description: Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario hizo clic con el botón primario del mouse en un elemento. Un cuadro de lista de arrastre envía este código de notificación en forma de mensaje de la lista de arrastre. Para obtener más información, vea arrastrar mensajes de cuadro de lista.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905705"
---
# <a name="dl_begindrag-notification-code"></a><span data-ttu-id="76f8b-106">Código de notificación de DL \_ BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="76f8b-106">DL\_BEGINDRAG notification code</span></span>

<span data-ttu-id="76f8b-107">Notifica a la ventana primaria del cuadro de lista de arrastre que el usuario hizo clic con el botón primario del mouse en un elemento.</span><span class="sxs-lookup"><span data-stu-id="76f8b-107">Notifies the drag list box's parent window that the user has clicked the left mouse button on an item.</span></span> <span data-ttu-id="76f8b-108">Un cuadro de lista de arrastre envía este código de notificación en forma de mensaje de la lista de arrastre.</span><span class="sxs-lookup"><span data-stu-id="76f8b-108">A drag list box sends this notification code in the form of a drag list message.</span></span> <span data-ttu-id="76f8b-109">Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="76f8b-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="76f8b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76f8b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f8b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76f8b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76f8b-112">Un puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el \_ código de notificación DL BEGINDRAG, el identificador del cuadro de lista de arrastre y la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="76f8b-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_BEGINDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f8b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76f8b-113">Return value</span></span>

<span data-ttu-id="76f8b-114">Devuelva **true** para comenzar la operación de arrastre o **false** para evitar la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="76f8b-114">Return **TRUE** to begin the drag operation, or **FALSE** to prevent the drag operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f8b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76f8b-115">Remarks</span></span>

<span data-ttu-id="76f8b-116">Al procesar este código de notificación, un procedimiento de ventana normalmente determina el elemento de lista en la posición del cursor especificada mediante la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="76f8b-116">When processing this notification code, a window procedure typically determines the list item at the specified cursor position by using the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="76f8b-117">Después, devuelve **true** o **false**, en función de si se debe arrastrar el elemento.</span><span class="sxs-lookup"><span data-stu-id="76f8b-117">It then returns **TRUE** or **FALSE**, depending on whether the item should be dragged.</span></span> <span data-ttu-id="76f8b-118">Antes de devolver **true**, el procedimiento de ventana debe guardar el índice del elemento de lista para que la aplicación sepa qué elemento se va a deshacer o copiar cuando se complete la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="76f8b-118">Before returning **TRUE**, the window procedure should save the index of the list item so the application knows which item to move or copy when the drag operation is completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f8b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76f8b-119">Requirements</span></span>



| <span data-ttu-id="76f8b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f8b-120">Requirement</span></span> | <span data-ttu-id="76f8b-121">Value</span><span class="sxs-lookup"><span data-stu-id="76f8b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76f8b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76f8b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76f8b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76f8b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76f8b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76f8b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76f8b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="76f8b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76f8b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76f8b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f8b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f8b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





