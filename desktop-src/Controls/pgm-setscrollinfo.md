---
title: Mensaje de PGM_SETSCROLLINFO (commctrl. h)
description: Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro SetScrollInfo de buscapersonas \_ .
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905171"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="920a7-105">\_Mensaje SETSCROLLINFO PGM</span><span class="sxs-lookup"><span data-stu-id="920a7-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="920a7-106">\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="920a7-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="920a7-107">Es posible que este mensaje no se admita en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="920a7-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="920a7-108">Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea.</span><span class="sxs-lookup"><span data-stu-id="920a7-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="920a7-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetScrollInfo de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="920a7-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="920a7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="920a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="920a7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="920a7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="920a7-112">**Uint** que especifica el valor de tiempo de espera para el desplazamiento, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="920a7-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="920a7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="920a7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="920a7-114">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **uint** que especifica el número de líneas que se va a desplazar por tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="920a7-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="920a7-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **uint** que especifica el número de píxeles por línea.</span><span class="sxs-lookup"><span data-stu-id="920a7-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="920a7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="920a7-116">Return value</span></span>

<span data-ttu-id="920a7-117">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="920a7-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="920a7-118">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="920a7-118">Security Considerations</span></span>

<span data-ttu-id="920a7-119">El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="920a7-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="920a7-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="920a7-120">Remarks</span></span>

<span data-ttu-id="920a7-121">El valor de tiempo de espera de *wParam* controla la velocidad a la que el control de paginación genera eventos de desplazamiento cuando el control ha capturado la entrada del mouse y se presiona el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="920a7-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="920a7-122">Los valores más pequeños dan como resultado un desplazamiento más rápido; los valores más grandes producen un desplazamiento más lento.</span><span class="sxs-lookup"><span data-stu-id="920a7-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="920a7-123">El valor predeterminado es un octavo de la hora de doble clic.</span><span class="sxs-lookup"><span data-stu-id="920a7-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="920a7-124">Para obtener más información, vea [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span><span class="sxs-lookup"><span data-stu-id="920a7-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="920a7-125">De forma predeterminada, con cada evento de desplazamiento, el control de paginación desplaza una cantidad igual a todo el ancho o alto del control, en función de si el control de paginación tiene una orientación horizontal o vertical.</span><span class="sxs-lookup"><span data-stu-id="920a7-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="920a7-126">Los valores de *lParam* se utilizan para invalidar la cantidad de desplazamiento predeterminada.</span><span class="sxs-lookup"><span data-stu-id="920a7-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="920a7-127">Si se proporcionan valores distintos de cero, la cantidad de desplazamiento es el producto de los dos valores (LOWORD (*lParam*) \* HIWORD (*lParam*)).</span><span class="sxs-lookup"><span data-stu-id="920a7-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="920a7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="920a7-128">Requirements</span></span>



| <span data-ttu-id="920a7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="920a7-129">Requirement</span></span> | <span data-ttu-id="920a7-130">Value</span><span class="sxs-lookup"><span data-stu-id="920a7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="920a7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="920a7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="920a7-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="920a7-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="920a7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="920a7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="920a7-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="920a7-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="920a7-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="920a7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="920a7-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="920a7-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="920a7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="920a7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="920a7-138">**Buscapersonas \_ SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="920a7-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

