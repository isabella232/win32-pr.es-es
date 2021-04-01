---
description: Se envía a una ventana cuando la función SetWindowLong está a punto de cambiar uno o varios estilos de la ventana.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Mensaje de WM_STYLECHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909853"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="09b8a-103">Mensaje de STYLECHANGING de WM \_</span><span class="sxs-lookup"><span data-stu-id="09b8a-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="09b8a-104">Se envía a una ventana cuando la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) está a punto de cambiar uno o varios estilos de la ventana.</span><span class="sxs-lookup"><span data-stu-id="09b8a-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="09b8a-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="09b8a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="09b8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09b8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09b8a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09b8a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09b8a-108">Indica si los estilos de la ventana o de ventana extendida están cambiando.</span><span class="sxs-lookup"><span data-stu-id="09b8a-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="09b8a-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="09b8a-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="09b8a-110">Value</span><span class="sxs-lookup"><span data-stu-id="09b8a-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="09b8a-111">Significado</span><span class="sxs-lookup"><span data-stu-id="09b8a-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="09b8a-112"><dt>**GWL \_ ExStyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="09b8a-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="09b8a-113">Los estilos extendidos de ventana están cambiando.</span><span class="sxs-lookup"><span data-stu-id="09b8a-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="09b8a-114"><dt>**GWL \_ ESTILO**</dt> <dt>: 16</dt></span><span class="sxs-lookup"><span data-stu-id="09b8a-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="09b8a-115">Los estilos de ventana están cambiando.</span><span class="sxs-lookup"><span data-stu-id="09b8a-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="09b8a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09b8a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09b8a-117">Puntero a una estructura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contiene los nuevos estilos propuestos para la ventana.</span><span class="sxs-lookup"><span data-stu-id="09b8a-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="09b8a-118">Una aplicación puede examinar los estilos y, si es necesario, cambiarlos.</span><span class="sxs-lookup"><span data-stu-id="09b8a-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09b8a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09b8a-119">Return value</span></span>

<span data-ttu-id="09b8a-120">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="09b8a-120">Type: **LRESULT**</span></span>

<span data-ttu-id="09b8a-121">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="09b8a-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b8a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09b8a-122">Requirements</span></span>



| <span data-ttu-id="09b8a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="09b8a-123">Requirement</span></span> | <span data-ttu-id="09b8a-124">Value</span><span class="sxs-lookup"><span data-stu-id="09b8a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b8a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09b8a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09b8a-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09b8a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="09b8a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09b8a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09b8a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09b8a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="09b8a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09b8a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="09b8a-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09b8a-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b8a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="09b8a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="09b8a-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="09b8a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="09b8a-133">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="09b8a-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="09b8a-134">**STYLECHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="09b8a-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="09b8a-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="09b8a-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="09b8a-136">Windows</span><span class="sxs-lookup"><span data-stu-id="09b8a-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 
