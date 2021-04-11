---
title: Mensaje de EM_SHOWBALLOONTIP (commctrl. h)
description: El \_ mensaje SHOWBALLOONTIP em muestra un globo de sugerencias asociado a un control de edición.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150461"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="6a53d-104">\_Mensaje SHOWBALLOONTIP em</span><span class="sxs-lookup"><span data-stu-id="6a53d-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="6a53d-105">El **mensaje \_ SHOWBALLOONTIP em** muestra un globo de sugerencias asociado a un control de edición.</span><span class="sxs-lookup"><span data-stu-id="6a53d-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a53d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a53d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a53d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a53d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a53d-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6a53d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6a53d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a53d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a53d-110">Puntero a una estructura [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) que contiene información sobre el globo de sugerencias que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="6a53d-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a53d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a53d-111">Return value</span></span>

<span data-ttu-id="6a53d-112">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="6a53d-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="6a53d-113">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="6a53d-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a53d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a53d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a53d-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="6a53d-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6a53d-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6a53d-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a53d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a53d-117">Requirements</span></span>



| <span data-ttu-id="6a53d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a53d-118">Requirement</span></span> | <span data-ttu-id="6a53d-119">Value</span><span class="sxs-lookup"><span data-stu-id="6a53d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a53d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a53d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a53d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a53d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a53d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a53d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a53d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a53d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a53d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a53d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a53d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a53d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a53d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a53d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a53d-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6a53d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6a53d-128">**EDITBALLOONTIP**</span><span class="sxs-lookup"><span data-stu-id="6a53d-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="6a53d-129">**Editar \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="6a53d-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





