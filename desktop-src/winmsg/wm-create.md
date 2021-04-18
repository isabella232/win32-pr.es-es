---
description: Se envía cuando una aplicación solicita que se cree una ventana mediante una llamada a la función CreateWindowEx o CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Mensaje de WM_CREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706672"
---
# <a name="wm_create-message"></a><span data-ttu-id="912ca-103">\_Crear mensaje de WM</span><span class="sxs-lookup"><span data-stu-id="912ca-103">WM\_CREATE message</span></span>

<span data-ttu-id="912ca-104">Se envía cuando una aplicación solicita que se cree una ventana mediante una llamada a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="912ca-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="912ca-105">(El mensaje se envía antes de que se devuelva la función). El procedimiento de ventana de la ventana nueva recibe este mensaje después de crear la ventana, pero antes de que la ventana se vuelva visible.</span><span class="sxs-lookup"><span data-stu-id="912ca-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="912ca-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="912ca-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="912ca-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="912ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="912ca-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="912ca-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="912ca-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="912ca-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="912ca-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="912ca-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="912ca-111">Puntero a una estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contiene información sobre la ventana que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="912ca-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="912ca-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="912ca-112">Return value</span></span>

<span data-ttu-id="912ca-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="912ca-113">Type: **LRESULT**</span></span>

<span data-ttu-id="912ca-114">Si una aplicación procesa este mensaje, debe devolver cero para continuar con la creación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="912ca-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="912ca-115">Si la aplicación devuelve – 1, se destruye la ventana y la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) devuelve un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="912ca-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="912ca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="912ca-116">Requirements</span></span>



| <span data-ttu-id="912ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="912ca-117">Requirement</span></span> | <span data-ttu-id="912ca-118">Value</span><span class="sxs-lookup"><span data-stu-id="912ca-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="912ca-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="912ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="912ca-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="912ca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="912ca-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="912ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="912ca-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="912ca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="912ca-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="912ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="912ca-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="912ca-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="912ca-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="912ca-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="912ca-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="912ca-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="912ca-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="912ca-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="912ca-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="912ca-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="912ca-129">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="912ca-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="912ca-130">**NCCREATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="912ca-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="912ca-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="912ca-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="912ca-132">Windows</span><span class="sxs-lookup"><span data-stu-id="912ca-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
