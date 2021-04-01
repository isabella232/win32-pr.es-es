---
title: Mensaje de WM_GESTURENOTIFY (Winuser. h)
description: Le ofrece la posibilidad de establecer la configuración de gestos.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- Mensaje de WM_GESTURENOTIFY de Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150569"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="03f2b-104">Mensaje de GESTURENOTIFY de WM \_</span><span class="sxs-lookup"><span data-stu-id="03f2b-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="03f2b-105">Le ofrece la posibilidad de establecer la configuración de gestos.</span><span class="sxs-lookup"><span data-stu-id="03f2b-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="03f2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03f2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f2b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03f2b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03f2b-108">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="03f2b-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="03f2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03f2b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03f2b-110">Un puntero a un [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span><span class="sxs-lookup"><span data-stu-id="03f2b-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f2b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03f2b-111">Return value</span></span>

<span data-ttu-id="03f2b-112">Se debe devolver un valor de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="03f2b-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="03f2b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03f2b-113">Remarks</span></span>

<span data-ttu-id="03f2b-114">Cuando se recibe el mensaje de **\_ GESTURENOTIFY de WM** , la aplicación puede usar [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) para especificar los gestos que se van a recibir.</span><span class="sxs-lookup"><span data-stu-id="03f2b-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="03f2b-115">Este mensaje se debe propagar siempre mediante la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="03f2b-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="03f2b-116">Al controlar el mensaje de **\_ GESTURENOTIFY de WM** , se cambiará la configuración de gestos para la duración de la ventana, no solo para el gesto siguiente.</span><span class="sxs-lookup"><span data-stu-id="03f2b-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="03f2b-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="03f2b-117">Examples</span></span>

<span data-ttu-id="03f2b-118">En el ejemplo siguiente se muestra cómo habilitar todos los gestos.</span><span class="sxs-lookup"><span data-stu-id="03f2b-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="03f2b-119">Para obtener más ejemplos, vea [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="03f2b-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="03f2b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03f2b-120">Requirements</span></span>



| <span data-ttu-id="03f2b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f2b-121">Requirement</span></span> | <span data-ttu-id="03f2b-122">Value</span><span class="sxs-lookup"><span data-stu-id="03f2b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f2b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03f2b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="03f2b-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="03f2b-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="03f2b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03f2b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="03f2b-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="03f2b-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="03f2b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03f2b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f2b-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03f2b-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f2b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="03f2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f2b-130">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="03f2b-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="03f2b-131">Guía de programación de gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="03f2b-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="03f2b-132">**GESTURENOTIFYSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="03f2b-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="03f2b-133">**SetGestureConfig**</span><span class="sxs-lookup"><span data-stu-id="03f2b-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

