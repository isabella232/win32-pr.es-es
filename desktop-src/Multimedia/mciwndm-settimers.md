---
title: Mensaje de MCIWNDM_SETTIMERS (VFW. h)
description: El \_ mensaje MCIWNDM SETTIMERS establece los períodos de actualización usados por MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- Mensaje de MCIWNDM_SETTIMERS de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801327"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="6e1e5-104">MCIWNDM \_ SETTIMERS</span><span class="sxs-lookup"><span data-stu-id="6e1e5-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="6e1e5-105">El mensaje **MCIWNDM \_ SETTIMERS** establece los períodos de actualización usados por MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="6e1e5-106">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="6e1e5-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="6e1e5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e1e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e1e5-108"><span id="active"></span><span id="ACTIVE"></span>*Active*</span><span class="sxs-lookup"><span data-stu-id="6e1e5-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="6e1e5-109">Período de actualización usado por MCIWnd cuando se trata de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="6e1e5-110">El valor predeterminado es 500 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="6e1e5-111">El almacenamiento de este valor está limitado a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="6e1e5-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactiva*</span><span class="sxs-lookup"><span data-stu-id="6e1e5-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="6e1e5-113">Período de actualización usado por MCIWnd cuando se trata de la ventana inactiva.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="6e1e5-114">El valor predeterminado es 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="6e1e5-115">El almacenamiento de este valor está limitado a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e1e5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e1e5-116">Return Value</span></span>

<span data-ttu-id="6e1e5-117">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6e1e5-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1e5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e1e5-118">Requirements</span></span>



| <span data-ttu-id="6e1e5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e1e5-119">Requirement</span></span> | <span data-ttu-id="6e1e5-120">Value</span><span class="sxs-lookup"><span data-stu-id="6e1e5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6e1e5-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e1e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1e5-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6e1e5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6e1e5-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e1e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1e5-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e1e5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e1e5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e1e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e1e5-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e1e5-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1e5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e1e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1e5-128">**MCIWndSetTimers**</span><span class="sxs-lookup"><span data-stu-id="6e1e5-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





