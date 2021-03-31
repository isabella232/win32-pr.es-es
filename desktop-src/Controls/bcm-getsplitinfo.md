---
title: Mensaje de BCM_GETSPLITINFO (commctrl. h)
description: Obtiene información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la \_ macro Button GetSplitInfo.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996468"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="ea998-105">\_Mensaje GETSPLITINFO de BCM</span><span class="sxs-lookup"><span data-stu-id="ea998-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="ea998-106">Obtiene información de un control de botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="ea998-106">Gets information for a split button control.</span></span> <span data-ttu-id="ea998-107">Envíe este mensaje explícitamente o mediante la macro [**Button \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) .</span><span class="sxs-lookup"><span data-stu-id="ea998-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea998-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea998-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea998-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea998-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea998-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ea998-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea998-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ea998-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea998-112">Un puntero a una [**estructura \_ SPLITINFO de botón**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) para recibir información sobre el botón.</span><span class="sxs-lookup"><span data-stu-id="ea998-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="ea998-113">El autor de la llamada es responsable de asignar la memoria para la estructura.</span><span class="sxs-lookup"><span data-stu-id="ea998-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="ea998-114">Establezca el miembro de **máscara** de esta estructura para determinar la información que se va a recibir.</span><span class="sxs-lookup"><span data-stu-id="ea998-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea998-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea998-115">Return value</span></span>

<span data-ttu-id="ea998-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ea998-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea998-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea998-117">Remarks</span></span>

<span data-ttu-id="ea998-118">Use este mensaje solo con los estilos de botón [**BS \_ SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ea998-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea998-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea998-119">Requirements</span></span>



| <span data-ttu-id="ea998-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea998-120">Requirement</span></span> | <span data-ttu-id="ea998-121">Value</span><span class="sxs-lookup"><span data-stu-id="ea998-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea998-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea998-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea998-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea998-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea998-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea998-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea998-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea998-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea998-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea998-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea998-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea998-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea998-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea998-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea998-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ea998-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea998-130">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="ea998-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="ea998-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ea998-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea998-132">Tipos de botón</span><span class="sxs-lookup"><span data-stu-id="ea998-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





