---
description: El mensaje de SYNCPAINT de WM \_ se usa para sincronizar el dibujo y evitar la vinculación de subprocesos GUI independientes.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Mensaje de WM_SYNCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997641"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="def99-103">Mensaje de SYNCPAINT de WM \_</span><span class="sxs-lookup"><span data-stu-id="def99-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="def99-104">El mensaje de **\_ SYNCPAINT de WM** se usa para sincronizar el dibujo y evitar la vinculación de subprocesos GUI independientes.</span><span class="sxs-lookup"><span data-stu-id="def99-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="def99-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="def99-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="def99-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="def99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def99-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="def99-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def99-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="def99-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="def99-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="def99-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def99-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="def99-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def99-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="def99-111">Return value</span></span>

<span data-ttu-id="def99-112">Una aplicación devuelve cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="def99-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="def99-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="def99-113">Remarks</span></span>

<span data-ttu-id="def99-114">Cuando se oculta, se muestra, se mueve o se cambia el tamaño de una ventana, el sistema puede determinar que es necesario enviar un mensaje de **WM \_ SYNCPAINT** a las ventanas de nivel superior de otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="def99-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="def99-115">Las aplicaciones deben pasar **WM \_ SYNCPAINT** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="def99-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="def99-116">La función **DefWindowProc** enviará un mensaje de [**WM \_ NCPAINT**](wm-ncpaint.md) al procedimiento de ventana si se debe pintar el marco de ventana y enviar un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si se debe borrar el fondo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="def99-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="def99-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def99-117">Requirements</span></span>



| <span data-ttu-id="def99-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="def99-118">Requirement</span></span> | <span data-ttu-id="def99-119">Value</span><span class="sxs-lookup"><span data-stu-id="def99-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def99-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="def99-120">Minimum supported client</span></span><br/> | <span data-ttu-id="def99-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="def99-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="def99-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="def99-122">Minimum supported server</span></span><br/> | <span data-ttu-id="def99-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="def99-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="def99-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="def99-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="def99-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="def99-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def99-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="def99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def99-127">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="def99-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="def99-128">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="def99-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="def99-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="def99-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="def99-130">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="def99-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="def99-131">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="def99-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="def99-132">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="def99-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
