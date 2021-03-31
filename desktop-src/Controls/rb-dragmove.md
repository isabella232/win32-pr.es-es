---
title: Mensaje de RB_DRAGMOVE (commctrl. h)
description: Actualiza la posición de arrastre en el control rebar después de un \_ mensaje RB BEGINDRAG anterior.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996727"
---
# <a name="rb_dragmove-message"></a><span data-ttu-id="14d35-104">Mensaje de DRAGMOVE de RB \_</span><span class="sxs-lookup"><span data-stu-id="14d35-104">RB\_DRAGMOVE message</span></span>

<span data-ttu-id="14d35-105">Actualiza la posición de arrastre en el control rebar después de un mensaje [**RB \_ BEGINDRAG**](rb-begindrag.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="14d35-105">Updates the drag position in the rebar control after a previous [**RB\_BEGINDRAG**](rb-begindrag.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="14d35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14d35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14d35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14d35-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="14d35-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="14d35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14d35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14d35-110">Valor **DWORD** que contiene las nuevas coordenadas del mouse.</span><span class="sxs-lookup"><span data-stu-id="14d35-110">**DWORD** value that contains the new mouse coordinates.</span></span> <span data-ttu-id="14d35-111">La coordenada horizontal está contenida en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y la coordenada vertical está contenida en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="14d35-111">The horizontal coordinate is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical coordinate is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="14d35-112">Si pasa (DWORD)-1, el control rebar usará la posición del mouse la última vez que el subproceso del control llamó a [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span><span class="sxs-lookup"><span data-stu-id="14d35-112">If you pass (DWORD)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d35-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14d35-113">Return value</span></span>

<span data-ttu-id="14d35-114">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="14d35-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d35-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d35-115">Requirements</span></span>



| <span data-ttu-id="14d35-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d35-116">Requirement</span></span> | <span data-ttu-id="14d35-117">Value</span><span class="sxs-lookup"><span data-stu-id="14d35-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14d35-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d35-118">Minimum supported client</span></span><br/> | <span data-ttu-id="14d35-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="14d35-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14d35-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d35-120">Minimum supported server</span></span><br/> | <span data-ttu-id="14d35-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="14d35-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14d35-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14d35-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d35-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14d35-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d35-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="14d35-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="14d35-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="14d35-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14d35-126">**\_ENDDRAG RB**</span><span class="sxs-lookup"><span data-stu-id="14d35-126">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
</dt> </dl>

 

