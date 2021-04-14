---
description: Una aplicación envía el mensaje de MDIACTIVATE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para indicar a la ventana de cliente que active una ventana secundaria MDI diferente.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Mensaje de WM_MDIACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648389"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="2ac72-103">Mensaje de MDIACTIVATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="2ac72-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="2ac72-104">Una aplicación envía el mensaje de **\_ MDIACTIVATE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para indicar a la ventana de cliente que active una ventana secundaria MDI diferente.</span><span class="sxs-lookup"><span data-stu-id="2ac72-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="2ac72-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ac72-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac72-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ac72-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac72-107">Identificador de la ventana secundaria MDI que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="2ac72-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="2ac72-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ac72-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac72-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2ac72-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac72-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ac72-110">Return value</span></span>

<span data-ttu-id="2ac72-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ac72-111">Type: **LRESULT**</span></span>

<span data-ttu-id="2ac72-112">Si una aplicación envía este mensaje a una ventana de cliente MDI, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="2ac72-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="2ac72-113">Una ventana secundaria MDI debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ac72-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac72-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ac72-114">Remarks</span></span>

<span data-ttu-id="2ac72-115">A medida que la ventana de cliente procesa este mensaje, envía **WM \_ MDIACTIVATE** a la ventana secundaria que se está desactivando y a la ventana secundaria que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="2ac72-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="2ac72-116">Los parámetros de mensaje recibidos por una ventana secundaria MDI son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ac72-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="2ac72-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ac72-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2ac72-118">Identificador de la ventana secundaria MDI que se va a desactivar.</span><span class="sxs-lookup"><span data-stu-id="2ac72-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="2ac72-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ac72-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2ac72-120">Identificador de la ventana secundaria MDI que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="2ac72-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="2ac72-121">Una ventana secundaria MDI se activa independientemente de la ventana de marco MDI.</span><span class="sxs-lookup"><span data-stu-id="2ac72-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="2ac72-122">Cuando la ventana de marco se activa, la ventana secundaria que se activó por última vez con el mensaje de **\_ MDIACTIVATE de WM** recibe el mensaje de [**\_ NCACTIVATE de WM**](wm-ncactivate.md) para dibujar un marco de ventana activo y una barra de título; la ventana secundaria no recibe otro mensaje de **\_ MDIACTIVATE de WM** .</span><span class="sxs-lookup"><span data-stu-id="2ac72-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac72-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ac72-123">Requirements</span></span>



| <span data-ttu-id="2ac72-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac72-124">Requirement</span></span> | <span data-ttu-id="2ac72-125">Value</span><span class="sxs-lookup"><span data-stu-id="2ac72-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac72-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ac72-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac72-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ac72-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2ac72-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ac72-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac72-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ac72-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ac72-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ac72-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac72-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ac72-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac72-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ac72-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ac72-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2ac72-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ac72-134">**MDIGETACTIVE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2ac72-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="2ac72-135">**MDINEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2ac72-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="2ac72-136">**NCACTIVATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2ac72-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="2ac72-137">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2ac72-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2ac72-138">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="2ac72-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




