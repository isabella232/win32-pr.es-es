---
description: El mensaje de QUERYNEWPALETTE de WM \_ informa a una ventana de que está a punto de recibir el foco de teclado, lo que permite a la ventana tener la oportunidad de obtener su paleta lógica cuando recibe el foco.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Mensaje de WM_QUERYNEWPALETTE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985338"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="11c84-103">Mensaje de QUERYNEWPALETTE de WM \_</span><span class="sxs-lookup"><span data-stu-id="11c84-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="11c84-104">El mensaje de **\_ QUERYNEWPALETTE de WM** informa a una ventana de que está a punto de recibir el foco de teclado, lo que permite a la ventana tener la oportunidad de obtener su paleta lógica cuando recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="11c84-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="11c84-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="11c84-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="11c84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11c84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11c84-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="11c84-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11c84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11c84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11c84-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="11c84-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c84-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11c84-111">Return value</span></span>

<span data-ttu-id="11c84-112">Si la ventana detecta su paleta lógica, debe devolver **true**; de lo contrario, debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="11c84-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c84-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c84-113">Requirements</span></span>



| <span data-ttu-id="11c84-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c84-114">Requirement</span></span> | <span data-ttu-id="11c84-115">Value</span><span class="sxs-lookup"><span data-stu-id="11c84-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c84-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11c84-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11c84-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="11c84-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="11c84-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11c84-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11c84-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11c84-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="11c84-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11c84-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c84-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11c84-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c84-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="11c84-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c84-123">Información general sobre colores</span><span class="sxs-lookup"><span data-stu-id="11c84-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="11c84-124">Mensajes de color</span><span class="sxs-lookup"><span data-stu-id="11c84-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="11c84-125">**PALETTECHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="11c84-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="11c84-126">**PALETTEISCHANGING de WM \_**</span><span class="sxs-lookup"><span data-stu-id="11c84-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 
