---
title: Mensaje WM_POINTERACTIVATE
description: Se envía a una ventana inactiva cuando un puntero primario genera un WM_POINTERDOWN sobre la ventana.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERACTIVATE
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720220"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="50efe-104">Mensaje WM_POINTERACTIVATE</span><span class="sxs-lookup"><span data-stu-id="50efe-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="50efe-105">Se envía a una ventana inactiva cuando un puntero primario genera un [**WM_POINTERDOWN**](wm-pointerdown.md) sobre la ventana.</span><span class="sxs-lookup"><span data-stu-id="50efe-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="50efe-106">Siempre que el mensaje permanezca no controlado, recorre la cadena de la ventana primaria hasta que llega a la ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="50efe-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="50efe-107">Las aplicaciones pueden responder a este mensaje para especificar si desean que se activen.</span><span class="sxs-lookup"><span data-stu-id="50efe-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="50efe-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="50efe-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="50efe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50efe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50efe-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50efe-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50efe-111">Contiene el identificador de puntero e información adicional.</span><span class="sxs-lookup"><span data-stu-id="50efe-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="50efe-112">Use las siguientes macros para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="50efe-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="50efe-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero</span><span class="sxs-lookup"><span data-stu-id="50efe-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="50efe-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): el valor de la prueba de posicionamiento devolvió el procesamiento del mensaje de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="50efe-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="50efe-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50efe-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50efe-116">Contiene el identificador de la ventana de nivel superior de la ventana que se está activando.</span><span class="sxs-lookup"><span data-stu-id="50efe-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50efe-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50efe-117">Return value</span></span>

<span data-ttu-id="50efe-118">Si una aplicación procesa este mensaje, debe devolver uno de los valores descritos en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="50efe-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="50efe-119">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="50efe-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="50efe-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50efe-120">Remarks</span></span>

<span data-ttu-id="50efe-121">Una aplicación puede controlar este mensaje y devolver uno de los valores siguientes para determinar la forma en que el sistema procesa la activación y la entrada de activación:</span><span class="sxs-lookup"><span data-stu-id="50efe-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="50efe-122">PA_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="50efe-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="50efe-123">PA_NOACTIVATE</span><span class="sxs-lookup"><span data-stu-id="50efe-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="50efe-124">Es importante tener en cuenta que, cuando el usuario interactúa con el sistema con varios punteros simultáneos, la oportunidad de activación que el mensaje de **WM_POINTERACTIVATE** representa está disponible para las aplicaciones solo para el primero de esos punteros.</span><span class="sxs-lookup"><span data-stu-id="50efe-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="50efe-125">Por lo tanto, las aplicaciones deben tener en cuenta que pueden seguir recibiendo entradas de punteros mientras están inactivas.</span><span class="sxs-lookup"><span data-stu-id="50efe-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="50efe-126">Si la aplicación no controla este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="50efe-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="50efe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50efe-127">Requirements</span></span>



| <span data-ttu-id="50efe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="50efe-128">Requirement</span></span> | <span data-ttu-id="50efe-129">Value</span><span class="sxs-lookup"><span data-stu-id="50efe-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50efe-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50efe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="50efe-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="50efe-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="50efe-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50efe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="50efe-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="50efe-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50efe-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50efe-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="50efe-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50efe-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50efe-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="50efe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50efe-137">Mensajes</span><span class="sxs-lookup"><span data-stu-id="50efe-137">Messages</span></span>](messages.md)
</dt> </dl>

 

