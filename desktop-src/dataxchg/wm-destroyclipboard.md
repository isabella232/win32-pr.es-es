---
title: Mensaje de WM_DESTROYCLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles cuando una llamada a la función EmptyClipboard vacía el portapapeles. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- Intercambio de datos de mensajes de WM_DESTROYCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997121"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="b251b-105">Mensaje de DESTROYCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="b251b-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="b251b-106">Se envía al propietario del portapapeles cuando una llamada a la función [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) vacía el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="b251b-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="b251b-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b251b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="b251b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b251b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b251b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b251b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b251b-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b251b-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b251b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b251b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b251b-112">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b251b-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b251b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b251b-113">Return value</span></span>

<span data-ttu-id="b251b-114">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="b251b-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b251b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b251b-115">Requirements</span></span>



| <span data-ttu-id="b251b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b251b-116">Requirement</span></span> | <span data-ttu-id="b251b-117">Value</span><span class="sxs-lookup"><span data-stu-id="b251b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b251b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b251b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b251b-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b251b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b251b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b251b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b251b-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b251b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b251b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b251b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b251b-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b251b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b251b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b251b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="b251b-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b251b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b251b-126">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="b251b-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="b251b-127">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b251b-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b251b-128">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="b251b-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

