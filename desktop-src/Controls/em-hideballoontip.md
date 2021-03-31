---
title: Mensaje de EM_HIDEBALLOONTIP (commctrl. h)
description: Oculta cualquier globo de sugerencias asociado a un control de edición.
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- EM_HIDEBALLOONTIP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996005"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="73d63-104">\_Mensaje HIDEBALLOONTIP em</span><span class="sxs-lookup"><span data-stu-id="73d63-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="73d63-105">Oculta cualquier globo de sugerencias asociado a un control de edición.</span><span class="sxs-lookup"><span data-stu-id="73d63-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="73d63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73d63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73d63-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73d63-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73d63-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="73d63-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="73d63-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73d63-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73d63-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="73d63-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73d63-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73d63-111">Return value</span></span>

<span data-ttu-id="73d63-112">Si el mensaje se realiza correctamente, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="73d63-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="73d63-113">En caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="73d63-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="73d63-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73d63-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73d63-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="73d63-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="73d63-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73d63-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73d63-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73d63-117">Requirements</span></span>



| <span data-ttu-id="73d63-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d63-118">Requirement</span></span> | <span data-ttu-id="73d63-119">Value</span><span class="sxs-lookup"><span data-stu-id="73d63-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73d63-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73d63-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73d63-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73d63-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73d63-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73d63-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73d63-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="73d63-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73d63-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73d63-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73d63-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73d63-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d63-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="73d63-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d63-127">**Editar \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="73d63-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





