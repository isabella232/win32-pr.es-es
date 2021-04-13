---
title: Mensaje de WM_GETHOTKEY (Winuser. h)
description: Se envía para determinar la tecla de acceso rápido asociada a una ventana.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Entrada de mouse y teclado de mensaje de WM_GETHOTKEY
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490049"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="67b07-104">Mensaje de GETHOTKEY de WM \_</span><span class="sxs-lookup"><span data-stu-id="67b07-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="67b07-105">Se envía para determinar la tecla de acceso rápido asociada a una ventana.</span><span class="sxs-lookup"><span data-stu-id="67b07-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="67b07-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67b07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67b07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67b07-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="67b07-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67b07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67b07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67b07-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="67b07-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b07-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67b07-111">Return value</span></span>

<span data-ttu-id="67b07-112">El valor devuelto es el código de tecla virtual y los modificadores de la tecla de acceso rápido, o **null** si no hay ninguna tecla de acceso rápido asociada a la ventana.</span><span class="sxs-lookup"><span data-stu-id="67b07-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="67b07-113">El código de tecla virtual está en el byte bajo del valor devuelto y los modificadores se encuentran en el byte superior.</span><span class="sxs-lookup"><span data-stu-id="67b07-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="67b07-114">Los modificadores pueden ser una combinación de las siguientes marcas de CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="67b07-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="67b07-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67b07-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="67b07-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="67b07-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="67b07-117"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="67b07-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="67b07-118">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="67b07-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="67b07-119"><dt>**HOTKEYF \_ CONTROL**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="67b07-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="67b07-120">Tecla CTRL</span><span class="sxs-lookup"><span data-stu-id="67b07-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="67b07-121"><dt>**HOTKEYF \_ EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="67b07-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="67b07-122">Clave extendida</span><span class="sxs-lookup"><span data-stu-id="67b07-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="67b07-123"><dt>**HOTKEYF \_ Mayús**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="67b07-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="67b07-124">Tecla Mayús</span><span class="sxs-lookup"><span data-stu-id="67b07-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="67b07-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67b07-125">Remarks</span></span>

<span data-ttu-id="67b07-126">Estas teclas de acceso directo no están relacionadas con las teclas de acceso rápido establecidas por la función [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .</span><span class="sxs-lookup"><span data-stu-id="67b07-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b07-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67b07-127">Requirements</span></span>



| <span data-ttu-id="67b07-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="67b07-128">Requirement</span></span> | <span data-ttu-id="67b07-129">Value</span><span class="sxs-lookup"><span data-stu-id="67b07-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b07-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67b07-130">Minimum supported client</span></span><br/> | <span data-ttu-id="67b07-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="67b07-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="67b07-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67b07-132">Minimum supported server</span></span><br/> | <span data-ttu-id="67b07-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67b07-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67b07-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67b07-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="67b07-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67b07-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b07-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="67b07-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="67b07-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="67b07-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67b07-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="67b07-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="67b07-139">**SETHOTKEY de WM \_**</span><span class="sxs-lookup"><span data-stu-id="67b07-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="67b07-140">**Vista**</span><span class="sxs-lookup"><span data-stu-id="67b07-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67b07-141">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="67b07-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

