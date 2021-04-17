---
description: Se envía a una ventana después de que la función SetWindowLong haya cambiado uno o varios de los estilos de la ventana.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Mensaje de WM_STYLECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546470"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="2abce-103">Mensaje de STYLECHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="2abce-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="2abce-104">Se envía a una ventana después de que la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) haya cambiado uno o varios de los estilos de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2abce-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="2abce-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2abce-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="2abce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2abce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2abce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2abce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2abce-108">Indica si los estilos de la ventana o de la ventana extendida han cambiado.</span><span class="sxs-lookup"><span data-stu-id="2abce-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="2abce-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2abce-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="2abce-110">Value</span><span class="sxs-lookup"><span data-stu-id="2abce-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="2abce-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2abce-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="2abce-112"><dt>**GWL \_ ExStyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="2abce-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="2abce-113">Los estilos extendidos de ventana han cambiado.</span><span class="sxs-lookup"><span data-stu-id="2abce-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="2abce-114"><dt>**GWL \_ ESTILO**</dt> <dt>: 16</dt></span><span class="sxs-lookup"><span data-stu-id="2abce-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="2abce-115">Los estilos de ventana han cambiado.</span><span class="sxs-lookup"><span data-stu-id="2abce-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="2abce-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2abce-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2abce-117">Puntero a una estructura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contiene los nuevos estilos de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2abce-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="2abce-118">Una aplicación puede examinar los estilos, pero no puede cambiarlos.</span><span class="sxs-lookup"><span data-stu-id="2abce-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2abce-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2abce-119">Return value</span></span>

<span data-ttu-id="2abce-120">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2abce-120">Type: **LRESULT**</span></span>

<span data-ttu-id="2abce-121">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2abce-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abce-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2abce-122">Requirements</span></span>



| <span data-ttu-id="2abce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abce-123">Requirement</span></span> | <span data-ttu-id="2abce-124">Value</span><span class="sxs-lookup"><span data-stu-id="2abce-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abce-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2abce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2abce-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2abce-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2abce-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2abce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2abce-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2abce-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2abce-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2abce-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2abce-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2abce-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abce-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2abce-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2abce-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2abce-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2abce-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="2abce-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="2abce-134">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="2abce-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="2abce-135">**STYLECHANGING de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2abce-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="2abce-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2abce-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2abce-137">Windows</span><span class="sxs-lookup"><span data-stu-id="2abce-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
