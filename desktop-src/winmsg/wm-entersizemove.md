---
description: Se envía una vez a una ventana una vez que entra en el bucle modal de movimiento o de ajuste de tamaño.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Mensaje de WM_ENTERSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706671"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="d1828-103">Mensaje de ENTERSIZEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="d1828-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="d1828-104">Se envía una vez a una ventana una vez que entra en el bucle modal de movimiento o de ajuste de tamaño.</span><span class="sxs-lookup"><span data-stu-id="d1828-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="d1828-105">La ventana entra en el bucle modal de movimiento o cambio de tamaño cuando el usuario hace clic en la barra de título o en el borde de tamaño de la ventana, o cuando la ventana pasa el mensaje de [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y el parámetro *wParam* del mensaje especifica el valor **SC \_ Move** o **SC \_ size** .</span><span class="sxs-lookup"><span data-stu-id="d1828-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="d1828-106">La operación se completa cuando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve.</span><span class="sxs-lookup"><span data-stu-id="d1828-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="d1828-107">El sistema envía el mensaje de **WM \_ ENTERSIZEMOVE** independientemente de si está habilitada la opción de arrastrar ventanas completas.</span><span class="sxs-lookup"><span data-stu-id="d1828-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="d1828-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1828-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="d1828-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1828-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1828-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1828-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1828-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d1828-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d1828-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1828-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1828-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d1828-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1828-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1828-114">Return value</span></span>

<span data-ttu-id="d1828-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d1828-115">Type: **LRESULT**</span></span>

<span data-ttu-id="d1828-116">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1828-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1828-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1828-117">Requirements</span></span>



| <span data-ttu-id="d1828-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1828-118">Requirement</span></span> | <span data-ttu-id="d1828-119">Value</span><span class="sxs-lookup"><span data-stu-id="d1828-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1828-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1828-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1828-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d1828-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d1828-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1828-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1828-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1828-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1828-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1828-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1828-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1828-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1828-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1828-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1828-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d1828-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1828-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d1828-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d1828-129">**EXITSIZEMOVE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d1828-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="d1828-130">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d1828-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="d1828-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d1828-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1828-132">Windows</span><span class="sxs-lookup"><span data-stu-id="d1828-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
