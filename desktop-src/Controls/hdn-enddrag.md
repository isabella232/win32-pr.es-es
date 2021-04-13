---
title: Código de notificación de HDN_ENDDRAG (commctrl. h)
description: Lo envía un control de encabezado cuando una operación de arrastrar ha finalizado en uno de sus elementos. Este código de notificación se envía como un mensaje de notificación de WM \_ . Solo los controles de encabezado que se establecen en el \_ estilo HDS DRAGDROP envían este código de notificación.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493342"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="cb56c-106">Código de notificación de ENDDRAG de HDN \_</span><span class="sxs-lookup"><span data-stu-id="cb56c-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="cb56c-107">Lo envía un control de encabezado cuando una operación de arrastrar ha finalizado en uno de sus elementos.</span><span class="sxs-lookup"><span data-stu-id="cb56c-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="cb56c-108">Este código de notificación se envía como un mensaje de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cb56c-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="cb56c-109">Solo los controles de encabezado que se establecen en el estilo [**HDS \_ DRAGDROP**](header-control-styles.md) envían este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="cb56c-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cb56c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb56c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb56c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb56c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb56c-112">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el elemento de encabezado que se estaba arrastrando.</span><span class="sxs-lookup"><span data-stu-id="cb56c-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb56c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb56c-113">Return value</span></span>

<span data-ttu-id="cb56c-114">Para permitir que el control Coloque y reordene automáticamente el elemento, devuelva **false**.</span><span class="sxs-lookup"><span data-stu-id="cb56c-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="cb56c-115">Para evitar que se coloque el elemento, devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="cb56c-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb56c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb56c-116">Remarks</span></span>

<span data-ttu-id="cb56c-117">Si el propietario está realizando la administración externa de arrastrar y colocar (manual), debe devolver el valor **false**.</span><span class="sxs-lookup"><span data-stu-id="cb56c-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="cb56c-118">Después, el propietario debe reordenar los elementos de encabezado manualmente mediante el envío de [**HDM \_ SETITEM**](hdm-setitem.md) o [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).</span><span class="sxs-lookup"><span data-stu-id="cb56c-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb56c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb56c-119">Requirements</span></span>



| <span data-ttu-id="cb56c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb56c-120">Requirement</span></span> | <span data-ttu-id="cb56c-121">Value</span><span class="sxs-lookup"><span data-stu-id="cb56c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb56c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb56c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb56c-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb56c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb56c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb56c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb56c-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb56c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb56c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb56c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb56c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb56c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





