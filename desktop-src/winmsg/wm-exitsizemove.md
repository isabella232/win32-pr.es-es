---
description: Se envía una vez a una ventana, una vez que ha salido del bucle modal de movimiento o de ajuste de tamaño.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Mensaje de WM_EXITSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720608"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="baed9-103">Mensaje de EXITSIZEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="baed9-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="baed9-104">Se envía una vez a una ventana, una vez que ha salido del bucle modal de movimiento o de ajuste de tamaño.</span><span class="sxs-lookup"><span data-stu-id="baed9-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="baed9-105">La ventana especifica el bucle modal de movimiento o cambio de tamaño cuando el usuario hace clic en la barra de título o en el borde de tamaño de la ventana, o cuando la ventana pasa el mensaje de [**\_ SYSCOMMAND de WM**](../menurc/wm-syscommand.md) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y el parámetro *wParam* del mensaje especifica el valor de **\_ tamaño** **SC \_ MOV** E o SC.</span><span class="sxs-lookup"><span data-stu-id="baed9-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="baed9-106">La operación se completa cuando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve.</span><span class="sxs-lookup"><span data-stu-id="baed9-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="baed9-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="baed9-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="baed9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baed9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baed9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="baed9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baed9-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="baed9-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="baed9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baed9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baed9-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="baed9-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baed9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baed9-113">Return value</span></span>

<span data-ttu-id="baed9-114">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="baed9-114">Type: **LRESULT**</span></span>

<span data-ttu-id="baed9-115">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="baed9-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="baed9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baed9-116">Requirements</span></span>



| <span data-ttu-id="baed9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="baed9-117">Requirement</span></span> | <span data-ttu-id="baed9-118">Value</span><span class="sxs-lookup"><span data-stu-id="baed9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baed9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baed9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="baed9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="baed9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="baed9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baed9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="baed9-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="baed9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="baed9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baed9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="baed9-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baed9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baed9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="baed9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="baed9-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="baed9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="baed9-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="baed9-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="baed9-128">**ENTERSIZEMOVE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="baed9-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="baed9-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="baed9-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="baed9-130">Windows</span><span class="sxs-lookup"><span data-stu-id="baed9-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
