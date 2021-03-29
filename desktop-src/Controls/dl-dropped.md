---
title: Código de notificación de DL_DROPPED (commctrl. h)
description: Indica que el usuario ha completado una operación de arrastre soltando el botón primario del mouse. Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre. Para obtener más información, vea arrastrar mensajes de cuadro de lista.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905706"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="54573-106">\_Código de notificación DL quitado</span><span class="sxs-lookup"><span data-stu-id="54573-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="54573-107">Indica que el usuario ha completado una operación de arrastre soltando el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="54573-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="54573-108">Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre.</span><span class="sxs-lookup"><span data-stu-id="54573-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="54573-109">Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="54573-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="54573-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54573-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54573-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54573-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54573-112">Puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de \_ notificación DL quitado, el identificador del cuadro de lista de arrastre y la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="54573-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54573-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54573-113">Return value</span></span>

<span data-ttu-id="54573-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="54573-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54573-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54573-115">Remarks</span></span>

<span data-ttu-id="54573-116">Normalmente, este código de notificación se procesa insertando el elemento que se está arrastrando a la lista delante del elemento bajo el cursor.</span><span class="sxs-lookup"><span data-stu-id="54573-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="54573-117">Para recuperar el índice del elemento en la posición del cursor, utilice la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="54573-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="54573-118">Tenga en cuenta que el \_ código de notificación DL quitado se envía incluso si el cursor no está en un elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="54573-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="54573-119">En ese caso, **LBItemFromPt** devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="54573-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="54573-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54573-120">Requirements</span></span>



| <span data-ttu-id="54573-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="54573-121">Requirement</span></span> | <span data-ttu-id="54573-122">Value</span><span class="sxs-lookup"><span data-stu-id="54573-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54573-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54573-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54573-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="54573-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54573-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54573-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54573-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="54573-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54573-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54573-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="54573-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54573-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





