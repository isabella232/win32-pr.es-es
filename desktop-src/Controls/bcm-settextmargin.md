---
title: Mensaje de BCM_SETTEXTMARGIN (commctrl. h)
description: El \_ mensaje SETTEXTMARGIN de BCM establece los márgenes para dibujar texto en un control de botón.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- BCM_SETTEXTMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490552"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="49dcc-104">\_Mensaje SETTEXTMARGIN de BCM</span><span class="sxs-lookup"><span data-stu-id="49dcc-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="49dcc-105">El **mensaje \_ SETTEXTMARGIN de BCM** establece los márgenes para dibujar texto en un control de botón.</span><span class="sxs-lookup"><span data-stu-id="49dcc-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="49dcc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49dcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49dcc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49dcc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49dcc-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="49dcc-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49dcc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49dcc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49dcc-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica los márgenes que se van a usar para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="49dcc-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49dcc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49dcc-111">Return value</span></span>

<span data-ttu-id="49dcc-112">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="49dcc-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="49dcc-113">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="49dcc-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49dcc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49dcc-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49dcc-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="49dcc-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="49dcc-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="49dcc-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49dcc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49dcc-117">Requirements</span></span>



| <span data-ttu-id="49dcc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49dcc-118">Requirement</span></span> | <span data-ttu-id="49dcc-119">Value</span><span class="sxs-lookup"><span data-stu-id="49dcc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49dcc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49dcc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49dcc-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49dcc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49dcc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49dcc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49dcc-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="49dcc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49dcc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49dcc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49dcc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49dcc-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49dcc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="49dcc-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="49dcc-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="49dcc-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49dcc-128">**Botón \_ SetTextMargin**</span><span class="sxs-lookup"><span data-stu-id="49dcc-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="49dcc-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="49dcc-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="49dcc-130">Botones</span><span class="sxs-lookup"><span data-stu-id="49dcc-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

