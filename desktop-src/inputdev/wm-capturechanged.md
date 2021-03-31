---
title: Mensaje de WM_CAPTURECHANGED (Winuser. h)
description: Se envía a la ventana que está perdiendo la captura del mouse.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- Entrada de mouse y teclado de mensaje de WM_CAPTURECHANGED
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150156"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="26e9d-104">Mensaje de CAPTURECHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="26e9d-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="26e9d-105">Se envía a la ventana que está perdiendo la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="26e9d-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="26e9d-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="26e9d-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="26e9d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26e9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e9d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26e9d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26e9d-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="26e9d-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="26e9d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26e9d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26e9d-111">Identificador de la ventana que obtiene la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="26e9d-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e9d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26e9d-112">Return value</span></span>

<span data-ttu-id="26e9d-113">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="26e9d-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e9d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26e9d-114">Remarks</span></span>

<span data-ttu-id="26e9d-115">Una ventana recibe este mensaje incluso si llama a [**releaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="26e9d-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="26e9d-116">Una aplicación no debe intentar establecer la captura del mouse en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="26e9d-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="26e9d-117">Cuando recibe este mensaje, una ventana debe volver a dibujarse, si es necesario, para reflejar el nuevo estado de la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="26e9d-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e9d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26e9d-118">Requirements</span></span>



| <span data-ttu-id="26e9d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26e9d-119">Requirement</span></span> | <span data-ttu-id="26e9d-120">Value</span><span class="sxs-lookup"><span data-stu-id="26e9d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e9d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26e9d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26e9d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26e9d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="26e9d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26e9d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26e9d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26e9d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26e9d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26e9d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e9d-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26e9d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e9d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="26e9d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="26e9d-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="26e9d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="26e9d-129">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="26e9d-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="26e9d-130">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="26e9d-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="26e9d-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="26e9d-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="26e9d-132">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="26e9d-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

