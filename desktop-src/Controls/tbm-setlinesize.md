---
title: Mensaje de TBM_SETLINESIZE (commctrl. h)
description: Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996059"
---
# <a name="tbm_setlinesize-message"></a><span data-ttu-id="f2f1d-105">TBM \_ SETLINESIZE</span><span class="sxs-lookup"><span data-stu-id="f2f1d-105">TBM\_SETLINESIZE message</span></span>

<span data-ttu-id="f2f1d-106">Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-106">Sets the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="f2f1d-107">Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2f1d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f1d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2f1d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2f1d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2f1d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2f1d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2f1d-112">Nuevo tamaño de línea.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-112">New line size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f1d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f1d-113">Return value</span></span>

<span data-ttu-id="f2f1d-114">Devuelve un valor de 32 bits que especifica el tamaño de línea anterior.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-114">Returns a 32-bit value that specifies the previous line size.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f1d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2f1d-115">Remarks</span></span>

<span data-ttu-id="f2f1d-116">La configuración predeterminada para el tamaño de línea es 1.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="f2f1d-117">La barra de control también envía un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los \_ códigos de notificación de línea TB y TB \_ LINEDOWN a su ventana primaria cuando el usuario presiona las teclas de dirección.</span><span class="sxs-lookup"><span data-stu-id="f2f1d-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f1d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f1d-118">Requirements</span></span>



| <span data-ttu-id="f2f1d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f1d-119">Requirement</span></span> | <span data-ttu-id="f2f1d-120">Value</span><span class="sxs-lookup"><span data-stu-id="f2f1d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f1d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f1d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f1d-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f1d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2f1d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f1d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f1d-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f1d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2f1d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f1d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f1d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f1d-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f1d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f1d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f1d-128">**TBM \_ GETLINESIZE**</span><span class="sxs-lookup"><span data-stu-id="f2f1d-128">**TBM\_GETLINESIZE**</span></span>](tbm-getlinesize.md)
</dt> </dl>

 

 





