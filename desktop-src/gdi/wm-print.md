---
description: El mensaje de impresión de WM \_ se envía a una ventana para solicitar que se dibuje en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Mensaje de WM_PRINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082507"
---
# <a name="wm_print-message"></a><span data-ttu-id="bfc34-103">Mensaje de impresión de WM \_</span><span class="sxs-lookup"><span data-stu-id="bfc34-103">WM\_PRINT message</span></span>

<span data-ttu-id="bfc34-104">El mensaje de **\_ impresión de WM** se envía a una ventana para solicitar que se dibuje en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="bfc34-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="bfc34-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bfc34-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="bfc34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfc34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfc34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfc34-108">Identificador del contexto de dispositivo en el que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="bfc34-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="bfc34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfc34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfc34-110">Opciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="bfc34-110">The drawing options.</span></span> <span data-ttu-id="bfc34-111">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfc34-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="bfc34-112">Value</span><span class="sxs-lookup"><span data-stu-id="bfc34-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="bfc34-113">Significado</span><span class="sxs-lookup"><span data-stu-id="bfc34-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="bfc34-114"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="bfc34-115">Dibuja la ventana solo si está visible.</span><span class="sxs-lookup"><span data-stu-id="bfc34-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="bfc34-116"><dt>**\_elementos secundarios PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="bfc34-117">Dibuja todas las ventanas secundarias visibles.</span><span class="sxs-lookup"><span data-stu-id="bfc34-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="bfc34-118"><dt>**\_cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="bfc34-119">Dibuja el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bfc34-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="bfc34-120"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="bfc34-121">Borra el fondo antes de dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="bfc34-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="bfc34-122"><dt>**no \_ cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="bfc34-123">Dibuja el área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bfc34-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="bfc34-124"><dt>**propiedad de PRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="bfc34-125">Dibuja todas las ventanas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bfc34-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfc34-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfc34-126">Remarks</span></span>

<span data-ttu-id="bfc34-127">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa este mensaje en función de la opción de dibujo especificada: si se \_ especifica PRF CHECKVISIBLE y la ventana no está visible, no hace nada, si \_ se especifica PRF nonclient, dibuje el área no cliente en el contexto de dispositivo especificado, si \_ se especifica PRF ERASEBKGND, envíe la ventana a un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , si \_ se especifica el cliente PRF, envíe la ventana a un mensaje de [**WM \_ PRINTCLIENT**](wm-printclient.md) , si se establece un elemento secundario PRF, \_ envíe a cada ventana secundaria visible un **\_** \_ **\_** mensaje de impresión de WM.</span><span class="sxs-lookup"><span data-stu-id="bfc34-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc34-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc34-128">Requirements</span></span>



| <span data-ttu-id="bfc34-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc34-129">Requirement</span></span> | <span data-ttu-id="bfc34-130">Value</span><span class="sxs-lookup"><span data-stu-id="bfc34-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc34-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfc34-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc34-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bfc34-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bfc34-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfc34-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc34-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfc34-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bfc34-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfc34-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc34-136"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfc34-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfc34-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfc34-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc34-138">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="bfc34-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="bfc34-139">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="bfc34-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="bfc34-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bfc34-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bfc34-141">**ERASEBKGND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bfc34-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="bfc34-142">**PRINTCLIENT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bfc34-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
