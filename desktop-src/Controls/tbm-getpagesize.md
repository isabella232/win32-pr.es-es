---
title: Mensaje de TBM_GETPAGESIZE (commctrl. h)
description: Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150311"
---
# <a name="tbm_getpagesize-message"></a><span data-ttu-id="69420-104">TBM \_ GETPAGESIZE</span><span class="sxs-lookup"><span data-stu-id="69420-104">TBM\_GETPAGESIZE message</span></span>

<span data-ttu-id="69420-105">Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="69420-105">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="69420-106">Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.</span><span class="sxs-lookup"><span data-stu-id="69420-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="69420-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69420-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69420-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69420-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="69420-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="69420-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="69420-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69420-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="69420-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="69420-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69420-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69420-112">Return value</span></span>

<span data-ttu-id="69420-113">Devuelve un valor de 32 bits que especifica el tamaño de página para el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="69420-113">Returns a 32-bit value that specifies the page size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="69420-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69420-114">Remarks</span></span>

<span data-ttu-id="69420-115">La barra de desplazamiento también envía un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los \_ códigos de notificación TB RePág y TB \_ Av Pág a su ventana primaria cuando recibe la entrada del teclado o del mouse que se desplaza por la página.</span><span class="sxs-lookup"><span data-stu-id="69420-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="69420-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69420-116">Requirements</span></span>



| <span data-ttu-id="69420-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69420-117">Requirement</span></span> | <span data-ttu-id="69420-118">Value</span><span class="sxs-lookup"><span data-stu-id="69420-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69420-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69420-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69420-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="69420-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69420-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69420-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69420-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="69420-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69420-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69420-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69420-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69420-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69420-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="69420-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69420-126">**TBM \_ SETPAGESIZE**</span><span class="sxs-lookup"><span data-stu-id="69420-126">**TBM\_SETPAGESIZE**</span></span>](tbm-setpagesize.md)
</dt> </dl>

 

 





