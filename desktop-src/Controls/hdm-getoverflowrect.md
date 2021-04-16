---
title: Mensaje de HDM_GETOVERFLOWRECT (commctrl. h)
description: Obtiene el rectángulo delimitador del botón de desbordamiento cuando el \_ estilo de desbordamiento de HDS se establece en el control de encabezado y el botón de desbordamiento está visible. Envíe este mensaje explícitamente o mediante la \_ macro header GetOverflowRect.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534504"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="9e902-105">HDM \_ GETOVERFLOWRECT</span><span class="sxs-lookup"><span data-stu-id="9e902-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="9e902-106">Obtiene el rectángulo delimitador del botón de desbordamiento cuando el estilo de [**\_ desbordamiento de HDS**](header-control-styles.md) se establece en el control de encabezado y el botón de desbordamiento está visible.</span><span class="sxs-lookup"><span data-stu-id="9e902-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="9e902-107">Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .</span><span class="sxs-lookup"><span data-stu-id="9e902-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e902-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e902-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e902-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e902-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e902-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9e902-110">Not used.</span></span> <span data-ttu-id="9e902-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e902-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e902-112">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e902-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e902-113">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir la información del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="9e902-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="9e902-114">El remitente del mensaje es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="9e902-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="9e902-115">Las coordenadas devueltas en la estructura **Rect** se expresan como coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9e902-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e902-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e902-116">Return value</span></span>

<span data-ttu-id="9e902-117">Devuelve **true si es** correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9e902-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e902-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e902-118">Remarks</span></span>

<span data-ttu-id="9e902-119">El control de encabezado debe tener el estilo **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="9e902-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e902-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e902-120">Requirements</span></span>



| <span data-ttu-id="9e902-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e902-121">Requirement</span></span> | <span data-ttu-id="9e902-122">Value</span><span class="sxs-lookup"><span data-stu-id="9e902-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e902-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e902-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9e902-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e902-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e902-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e902-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9e902-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e902-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e902-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e902-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e902-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e902-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e902-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e902-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e902-130">Acerca de los controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="9e902-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

