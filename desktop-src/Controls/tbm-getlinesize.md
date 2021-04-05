---
title: Mensaje de TBM_GETLINESIZE (commctrl. h)
description: Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997168"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="986c9-105">TBM \_ GETLINESIZE</span><span class="sxs-lookup"><span data-stu-id="986c9-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="986c9-106">Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o.</span><span class="sxs-lookup"><span data-stu-id="986c9-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="986c9-107">Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo.</span><span class="sxs-lookup"><span data-stu-id="986c9-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="986c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="986c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="986c9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="986c9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="986c9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="986c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="986c9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="986c9-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="986c9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986c9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="986c9-113">Return value</span></span>

<span data-ttu-id="986c9-114">Devuelve un valor de 32 bits que especifica el tamaño de línea para el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="986c9-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="986c9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="986c9-115">Remarks</span></span>

<span data-ttu-id="986c9-116">La configuración predeterminada para el tamaño de línea es 1.</span><span class="sxs-lookup"><span data-stu-id="986c9-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="986c9-117">La barra de control también envía un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con los \_ códigos de notificación de línea TB y TB \_ LINEDOWN a su ventana primaria cuando el usuario presiona las teclas de dirección.</span><span class="sxs-lookup"><span data-stu-id="986c9-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="986c9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="986c9-118">Requirements</span></span>



| <span data-ttu-id="986c9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="986c9-119">Requirement</span></span> | <span data-ttu-id="986c9-120">Value</span><span class="sxs-lookup"><span data-stu-id="986c9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="986c9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="986c9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="986c9-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="986c9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="986c9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="986c9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="986c9-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="986c9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="986c9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="986c9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="986c9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="986c9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





