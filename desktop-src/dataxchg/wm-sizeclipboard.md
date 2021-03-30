---
title: Mensaje de WM_SIZECLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el \_ formato CF OWNERDISPLAY y el área cliente del visor del portapapeles ha cambiado de tamaño.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Intercambio de datos de mensajes de WM_SIZECLIPBOARD
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802546"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="72715-104">Mensaje de SIZECLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="72715-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="72715-105">Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y el área cliente del visor del portapapeles ha cambiado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="72715-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="72715-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72715-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72715-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72715-108">Identificador de la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="72715-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="72715-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72715-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72715-110">Identificador de un objeto de memoria global que contiene una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="72715-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="72715-111">La estructura especifica las nuevas dimensiones del área cliente del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="72715-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72715-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72715-112">Return value</span></span>

<span data-ttu-id="72715-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="72715-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="72715-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72715-114">Remarks</span></span>

<span data-ttu-id="72715-115">Cuando se va a destruir o cambiar el tamaño de la ventana del visor del portapapeles, se envía un mensaje de **WM \_ SIZECLIPBOARD** con un rectángulo nulo (0, 0, 0,0) como el nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="72715-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="72715-116">Esto permite que el propietario del portapapeles libere sus recursos para mostrar.</span><span class="sxs-lookup"><span data-stu-id="72715-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="72715-117">El propietario del portapapeles debe utilizar la función [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear el objeto de memoria que contiene [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72715-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="72715-118">Antes de devolver, el propietario del portapapeles debe desbloquear el objeto mediante la función [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="72715-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="72715-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72715-119">Requirements</span></span>



| <span data-ttu-id="72715-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="72715-120">Requirement</span></span> | <span data-ttu-id="72715-121">Value</span><span class="sxs-lookup"><span data-stu-id="72715-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72715-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72715-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72715-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="72715-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="72715-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72715-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72715-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72715-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72715-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72715-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="72715-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72715-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72715-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="72715-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="72715-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="72715-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="72715-130">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="72715-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

