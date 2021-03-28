---
description: El mensaje de DISPLAYCHANGE de WM \_ se envía a todas las ventanas cuando cambia la resolución de pantalla.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Mensaje de WM_DISPLAYCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276448"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="e9f9c-103">Mensaje de DISPLAYCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="e9f9c-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="e9f9c-104">El mensaje de **\_ DISPLAYCHANGE de WM** se envía a todas las ventanas cuando cambia la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9f9c-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="e9f9c-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e9f9c-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="e9f9c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9f9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f9c-108">Nueva profundidad de imagen de la pantalla, en bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="e9f9c-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9f9c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f9c-110">La palabra de orden inferior especifica la resolución horizontal de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9f9c-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="e9f9c-111">La palabra de orden superior especifica la resolución vertical de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9f9c-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f9c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9f9c-112">Remarks</span></span>

<span data-ttu-id="e9f9c-113">Este mensaje solo se envía a las ventanas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e9f9c-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="e9f9c-114">Para todas las demás ventanas que se publican.</span><span class="sxs-lookup"><span data-stu-id="e9f9c-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f9c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9f9c-115">Requirements</span></span>



| <span data-ttu-id="e9f9c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f9c-116">Requirement</span></span> | <span data-ttu-id="e9f9c-117">Value</span><span class="sxs-lookup"><span data-stu-id="e9f9c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f9c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9f9c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f9c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e9f9c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9f9c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9f9c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f9c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9f9c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9f9c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9f9c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f9c-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f9c-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f9c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9f9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f9c-125">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="e9f9c-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="e9f9c-126">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="e9f9c-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="e9f9c-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9f9c-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e9f9c-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9f9c-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 
