---
description: El mensaje de PALETTECHANGED de WM \_ se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco de teclado haya realizado su paleta lógica, lo que cambia la paleta del sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Mensaje de WM_PALETTECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813016"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="5a3f4-103">Mensaje de PALETTECHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="5a3f4-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="5a3f4-104">El mensaje de **\_ PALETTECHANGED de WM** se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco de teclado haya realizado su paleta lógica, lo que cambia la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="5a3f4-105">Este mensaje habilita una ventana que usa una paleta de colores, pero no tiene el foco de teclado para obtener su paleta lógica y actualizar su área cliente.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="5a3f4-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5a3f4-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="5a3f4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a3f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3f4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a3f4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3f4-109">Identificador de la ventana que provocó el cambio de la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="5a3f4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a3f4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3f4-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a3f4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a3f4-112">Remarks</span></span>

<span data-ttu-id="5a3f4-113">Este mensaje debe enviarse a todas las ventanas superpuestas y de nivel superior, incluida la que cambió la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="5a3f4-114">Si alguna de las ventanas secundarias usa una paleta de colores, este mensaje también se debe pasar a ellos.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="5a3f4-115">Para evitar la creación de un bucle infinito, una ventana que reciba este mensaje no debe obtener su paleta, a menos que determine que *wParam* no contiene su propio identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="5a3f4-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3f4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a3f4-116">Requirements</span></span>



| <span data-ttu-id="5a3f4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3f4-117">Requirement</span></span> | <span data-ttu-id="5a3f4-118">Value</span><span class="sxs-lookup"><span data-stu-id="5a3f4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3f4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a3f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3f4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a3f4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5a3f4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a3f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3f4-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a3f4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a3f4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a3f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3f4-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3f4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a3f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3f4-126">Información general sobre colores</span><span class="sxs-lookup"><span data-stu-id="5a3f4-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-127">Mensajes de color</span><span class="sxs-lookup"><span data-stu-id="5a3f4-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-128">**PALETTEISCHANGING de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="5a3f4-129">**QUERYNEWPALETTE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5a3f4-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
