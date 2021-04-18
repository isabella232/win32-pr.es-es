---
description: Una aplicación envía el \_ mensaje de MDISETMENU de WM a una ventana de cliente de la interfaz de múltiples documentos (MDI) para reemplazar el menú completo de una ventana de marco MDI, para reemplazar el menú ventana de la ventana marco o ambos.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Mensaje de WM_MDISETMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720530"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="c8742-103">Mensaje de MDISETMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="c8742-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="c8742-104">Una aplicación envía el mensaje de **\_ MDISETMENU de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para reemplazar el menú completo de una ventana de marco MDI, para reemplazar el menú ventana de la ventana marco o ambos.</span><span class="sxs-lookup"><span data-stu-id="c8742-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="c8742-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8742-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8742-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8742-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8742-107">Identificador del nuevo menú de la ventana de marco.</span><span class="sxs-lookup"><span data-stu-id="c8742-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="c8742-108">Si este parámetro es **null**, el menú de la ventana de marco no cambia.</span><span class="sxs-lookup"><span data-stu-id="c8742-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="c8742-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8742-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8742-110">Identificador del menú de nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c8742-110">A handle to the new window menu.</span></span> <span data-ttu-id="c8742-111">Si este parámetro es **null**, el menú ventana no cambia.</span><span class="sxs-lookup"><span data-stu-id="c8742-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8742-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8742-112">Return value</span></span>

<span data-ttu-id="c8742-113">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="c8742-113">Type: **HMENU**</span></span>

<span data-ttu-id="c8742-114">Si el mensaje se realiza correctamente, el valor devuelto es el identificador del menú de la ventana de marco anterior.</span><span class="sxs-lookup"><span data-stu-id="c8742-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="c8742-115">Si se produce un error en el mensaje, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="c8742-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8742-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8742-116">Remarks</span></span>

<span data-ttu-id="c8742-117">Después de enviar este mensaje, una aplicación debe llamar a la función [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para actualizar la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="c8742-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="c8742-118">Si este mensaje reemplaza el menú ventana, los elementos de menú de la ventana secundaria MDI se quitan del menú ventana anterior y se agregan al menú nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c8742-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="c8742-119">Si una ventana secundaria MDI está maximizada y este mensaje reemplaza el menú ventana marco MDI, el icono de menú ventana y el icono restaurar se quitan del menú ventana de marco anterior y se agregan al menú nueva ventana marco.</span><span class="sxs-lookup"><span data-stu-id="c8742-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8742-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8742-120">Requirements</span></span>



| <span data-ttu-id="c8742-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8742-121">Requirement</span></span> | <span data-ttu-id="c8742-122">Value</span><span class="sxs-lookup"><span data-stu-id="c8742-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8742-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8742-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8742-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8742-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8742-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8742-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8742-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8742-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8742-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8742-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8742-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8742-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8742-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8742-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8742-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c8742-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8742-131">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="c8742-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="c8742-132">**MDIREFRESHMENU de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c8742-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="c8742-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c8742-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8742-134">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="c8742-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
