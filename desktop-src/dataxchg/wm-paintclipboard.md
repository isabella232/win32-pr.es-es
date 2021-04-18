---
title: Mensaje de WM_PAINTCLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el \_ formato CF OWNERDISPLAY y el área cliente del visor del portapapeles debe volver a dibujarse.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Intercambio de datos de mensajes de WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665967"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="bad28-104">Mensaje de PAINTCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="bad28-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="bad28-105">Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y el área cliente del visor del portapapeles debe volver a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="bad28-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="bad28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bad28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bad28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bad28-108">Identificador de la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="bad28-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="bad28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bad28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bad28-110">Identificador de un objeto de memoria global que contiene una estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="bad28-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="bad28-111">La estructura define la parte del área de cliente que se va a pintar.</span><span class="sxs-lookup"><span data-stu-id="bad28-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad28-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bad28-112">Return value</span></span>

<span data-ttu-id="bad28-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="bad28-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bad28-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bad28-114">Remarks</span></span>

<span data-ttu-id="bad28-115">Para determinar si es necesario volver a dibujar todo el área cliente o solo una parte de ella, el propietario del portapapeles debe comparar las dimensiones del área de dibujo dada en el miembro **rcPaint** de [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) con las dimensiones proporcionadas en el mensaje de [**\_ SIZECLIPBOARD de WM**](wm-sizeclipboard.md) más reciente.</span><span class="sxs-lookup"><span data-stu-id="bad28-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="bad28-116">El propietario del portapapeles debe utilizar la función [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear la memoria que contiene la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="bad28-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="bad28-117">Antes de devolver, el propietario del portapapeles debe desbloquear esa memoria mediante la función [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="bad28-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad28-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad28-118">Requirements</span></span>



| <span data-ttu-id="bad28-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad28-119">Requirement</span></span> | <span data-ttu-id="bad28-120">Value</span><span class="sxs-lookup"><span data-stu-id="bad28-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad28-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bad28-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bad28-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bad28-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bad28-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bad28-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bad28-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bad28-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bad28-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bad28-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad28-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bad28-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad28-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bad28-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bad28-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bad28-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bad28-129">**SIZECLIPBOARD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bad28-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="bad28-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="bad28-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bad28-131">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="bad28-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

