---
description: Una aplicación envía el \_ mensaje de MDIREFRESHMENU de WM a una ventana de cliente de la interfaz de múltiples documentos (MDI) para actualizar el menú ventana de la ventana de marco MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Mensaje de WM_MDIREFRESHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677919"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="8e278-103">Mensaje de MDIREFRESHMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="8e278-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="8e278-104">Una aplicación envía el mensaje de **\_ MDIREFRESHMENU de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para actualizar el menú ventana de la ventana de marco MDI.</span><span class="sxs-lookup"><span data-stu-id="8e278-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="8e278-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e278-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e278-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e278-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e278-107">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8e278-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e278-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e278-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e278-109">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8e278-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e278-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e278-110">Return value</span></span>

<span data-ttu-id="8e278-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="8e278-111">Type: **HMENU**</span></span>

<span data-ttu-id="8e278-112">Si el mensaje se realiza correctamente, el valor devuelto es el identificador del menú de la ventana de marco.</span><span class="sxs-lookup"><span data-stu-id="8e278-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="8e278-113">Si se produce un error en el mensaje, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="8e278-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e278-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e278-114">Remarks</span></span>

<span data-ttu-id="8e278-115">Después de enviar este mensaje, una aplicación debe llamar a la función [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para actualizar la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="8e278-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e278-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e278-116">Requirements</span></span>



| <span data-ttu-id="8e278-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e278-117">Requirement</span></span> | <span data-ttu-id="8e278-118">Value</span><span class="sxs-lookup"><span data-stu-id="8e278-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e278-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e278-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e278-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8e278-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8e278-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e278-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e278-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e278-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e278-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e278-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e278-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e278-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e278-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e278-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e278-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8e278-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e278-127">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="8e278-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="8e278-128">**MDISETMENU de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8e278-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="8e278-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8e278-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8e278-130">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="8e278-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
