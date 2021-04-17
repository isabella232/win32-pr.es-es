---
description: Una aplicación envía el mensaje de MDICREATE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para crear una ventana secundaria MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Mensaje de WM_MDICREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716443"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="c03f4-103">Mensaje de MDICREATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="c03f4-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="c03f4-104">Una aplicación envía el mensaje de **\_ MDICREATE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para crear una ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="c03f4-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="c03f4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c03f4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03f4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c03f4-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c03f4-107">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c03f4-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c03f4-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c03f4-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c03f4-109">Puntero a una estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) que contiene información que el sistema usa para crear la ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="c03f4-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03f4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c03f4-110">Return value</span></span>

<span data-ttu-id="c03f4-111">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="c03f4-111">Type: **HWND**</span></span>

<span data-ttu-id="c03f4-112">Si el mensaje se realiza correctamente, el valor devuelto es el identificador de la nueva ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="c03f4-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="c03f4-113">Si se produce un error en el mensaje, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="c03f4-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c03f4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c03f4-114">Remarks</span></span>

<span data-ttu-id="c03f4-115">La ventana secundaria MDI se crea con el [**estilo de ventana**](window-styles.md) bits **WS \_ secundario**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** y **WS \_ MAXIMIZEBOX**, además de los bits de estilo adicionales especificados en la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="c03f4-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="c03f4-116">El sistema agrega el título de la nueva ventana secundaria al menú ventana de la ventana marco.</span><span class="sxs-lookup"><span data-stu-id="c03f4-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="c03f4-117">Una aplicación debe usar este mensaje para crear todas las ventanas secundarias de la ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="c03f4-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="c03f4-118">Si una ventana de cliente MDI recibe cualquier mensaje que cambie la activación de sus ventanas secundarias mientras la ventana secundaria activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria que se acaba de activar.</span><span class="sxs-lookup"><span data-stu-id="c03f4-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="c03f4-119">Cuando se crea una ventana secundaria MDI, el sistema envía el mensaje de [**\_ creación de WM**](wm-create.md) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="c03f4-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="c03f4-120">El parámetro *lParam* del mensaje **de \_ creación de WM** contiene un puntero a una estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="c03f4-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="c03f4-121">El miembro *lpCreateParams* de esta estructura contiene un puntero a la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) pasada con el mensaje de **\_ MDICREATE de WM** que creó la ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="c03f4-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="c03f4-122">Una aplicación no debe enviar un segundo mensaje de **\_ MDICREATE de WM** mientras se sigue procesando un mensaje de **\_ MDICREATE de WM** .</span><span class="sxs-lookup"><span data-stu-id="c03f4-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="c03f4-123">Por ejemplo, no debería enviar un mensaje de **WM \_ MDICREATE** mientras una ventana secundaria MDI esté procesando su mensaje de **WM \_ MDICREATE** .</span><span class="sxs-lookup"><span data-stu-id="c03f4-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c03f4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c03f4-124">Requirements</span></span>



| <span data-ttu-id="c03f4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c03f4-125">Requirement</span></span> | <span data-ttu-id="c03f4-126">Value</span><span class="sxs-lookup"><span data-stu-id="c03f4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c03f4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c03f4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c03f4-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c03f4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c03f4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c03f4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c03f4-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c03f4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c03f4-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c03f4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c03f4-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c03f4-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03f4-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c03f4-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="c03f4-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c03f4-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c03f4-135">**CreateMDIWindow**</span><span class="sxs-lookup"><span data-stu-id="c03f4-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="c03f4-136">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c03f4-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="c03f4-137">**MDICREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c03f4-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="c03f4-138">**creación de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c03f4-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="c03f4-139">**MDIDESTROY de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c03f4-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="c03f4-140">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c03f4-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c03f4-141">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="c03f4-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
