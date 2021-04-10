---
title: Mensaje DM_POINTERHITTEST
description: Se envía a una ventana, cuando la entrada de puntero se detecta por primera vez, con el fin de determinar el destino de entrada más probable para la manipulación directa.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- Mensajes y notificaciones de entrada de mensajes de DM_POINTERHITTEST
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150680"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="e61bb-104">Mensaje DM_POINTERHITTEST</span><span class="sxs-lookup"><span data-stu-id="e61bb-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="e61bb-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e61bb-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e61bb-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e61bb-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e61bb-107">Se envía a una ventana, cuando la entrada de puntero se detecta por primera vez, con el fin de determinar el destino de entrada más probable para la [manipulación directa](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span><span class="sxs-lookup"><span data-stu-id="e61bb-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="e61bb-108">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="e61bb-108">\[!Important\]</span></span>  
> <span data-ttu-id="e61bb-109">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="e61bb-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="e61bb-110">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="e61bb-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="e61bb-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="e61bb-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="e61bb-112">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e61bb-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="e61bb-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e61bb-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61bb-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e61bb-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e61bb-115">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e61bb-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e61bb-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e61bb-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e61bb-117">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e61bb-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e61bb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e61bb-118">Return value</span></span>

<span data-ttu-id="e61bb-119">NULL</span><span class="sxs-lookup"><span data-stu-id="e61bb-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="e61bb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61bb-120">Requirements</span></span>



| <span data-ttu-id="e61bb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61bb-121">Requirement</span></span> | <span data-ttu-id="e61bb-122">Value</span><span class="sxs-lookup"><span data-stu-id="e61bb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61bb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e61bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e61bb-124">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e61bb-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e61bb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e61bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e61bb-126">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="e61bb-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e61bb-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e61bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61bb-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e61bb-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61bb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e61bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61bb-130">Mensajes</span><span class="sxs-lookup"><span data-stu-id="e61bb-130">Messages</span></span>](messages.md)
</dt> </dl>

 

