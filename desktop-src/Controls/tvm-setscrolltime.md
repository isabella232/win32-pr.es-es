---
title: Mensaje de TVM_SETSCROLLTIME (commctrl. h)
description: Establece el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetScrollTime de TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658225"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="74fc3-105">\_Mensaje de SETSCROLLTIME TVM</span><span class="sxs-lookup"><span data-stu-id="74fc3-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="74fc3-106">Establece el tiempo de desplazamiento máximo para el control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="74fc3-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="74fc3-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetScrollTime de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="74fc3-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="74fc3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74fc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74fc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74fc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74fc3-110">Nuevo tiempo de desplazamiento máximo, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="74fc3-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="74fc3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74fc3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74fc3-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="74fc3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74fc3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74fc3-113">Return value</span></span>

<span data-ttu-id="74fc3-114">Devuelve el tiempo de desplazamiento máximo anterior, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="74fc3-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="74fc3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74fc3-115">Remarks</span></span>

<span data-ttu-id="74fc3-116">El tiempo de desplazamiento máximo es la cantidad más larga de tiempo que puede tardar una operación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="74fc3-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="74fc3-117">El desplazamiento se ajustará para que el desplazamiento tenga lugar dentro del tiempo de desplazamiento máximo.</span><span class="sxs-lookup"><span data-stu-id="74fc3-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="74fc3-118">Una operación de desplazamiento puede tardar menos tiempo que el máximo.</span><span class="sxs-lookup"><span data-stu-id="74fc3-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="74fc3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74fc3-119">Requirements</span></span>



| <span data-ttu-id="74fc3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="74fc3-120">Requirement</span></span> | <span data-ttu-id="74fc3-121">Value</span><span class="sxs-lookup"><span data-stu-id="74fc3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74fc3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74fc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74fc3-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74fc3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74fc3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74fc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74fc3-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74fc3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74fc3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74fc3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="74fc3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74fc3-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74fc3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="74fc3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74fc3-129">**TVM \_ GETSCROLLTIME**</span><span class="sxs-lookup"><span data-stu-id="74fc3-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





