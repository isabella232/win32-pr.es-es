---
title: Mensaje EM_SETZOOM (RichEdit. h)
description: Establece la relación de zoom. La relación debe ser un valor entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905359"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="4105c-106">\_Mensaje SETZOOM em</span><span class="sxs-lookup"><span data-stu-id="4105c-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="4105c-107">Establece la relación de zoom para un control de edición de varias líneas o un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4105c-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="4105c-108">La relación debe ser un valor entre 1/64 y 64.</span><span class="sxs-lookup"><span data-stu-id="4105c-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="4105c-109">El control de edición debe tener el conjunto de estilo extendido **es \_ ex \_** para el que este mensaje tiene un efecto, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="4105c-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="4105c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4105c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4105c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4105c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4105c-112">Numerador de la relación de zoom.</span><span class="sxs-lookup"><span data-stu-id="4105c-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="4105c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4105c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4105c-114">Denominador de la relación de zoom.</span><span class="sxs-lookup"><span data-stu-id="4105c-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="4105c-115">Estos parámetros pueden tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4105c-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="4105c-116">Value</span><span class="sxs-lookup"><span data-stu-id="4105c-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="4105c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4105c-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="4105c-118"><dt>**Ambos 0**</dt></span><span class="sxs-lookup"><span data-stu-id="4105c-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="4105c-119">Desactiva el zoom mediante el mensaje **em \_ SETZOOM** (el zoom puede seguir produciendo el uso de [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span><span class="sxs-lookup"><span data-stu-id="4105c-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="4105c-120"><dt>**1/64 < (wParam/lParam) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="4105c-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="4105c-121">Zooms mostrados por el numerador y el denominador de la relación de zoom</span><span class="sxs-lookup"><span data-stu-id="4105c-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4105c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4105c-122">Return value</span></span>

<span data-ttu-id="4105c-123">Si se acepta la nueva configuración de zoom, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="4105c-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="4105c-124">Si no se acepta la nueva configuración de zoom, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="4105c-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4105c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4105c-125">Remarks</span></span>

<span data-ttu-id="4105c-126">**Editar:** Compatible con Windows 10 1809 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4105c-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="4105c-127">El control de edición debe tener el conjunto de estilo extendido **es \_ ex \_** para el que este mensaje tiene un efecto, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="4105c-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="4105c-128">Para obtener información sobre el control de edición, vea [controles de edición](about-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4105c-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4105c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4105c-129">Requirements</span></span>



| <span data-ttu-id="4105c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4105c-130">Requirement</span></span> | <span data-ttu-id="4105c-131">Value</span><span class="sxs-lookup"><span data-stu-id="4105c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4105c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4105c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4105c-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4105c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4105c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4105c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4105c-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4105c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4105c-136">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4105c-136">Redistributable</span></span><br/>          | <span data-ttu-id="4105c-137">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="4105c-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="4105c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4105c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4105c-139"><dt>RichEdit. h/commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4105c-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4105c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4105c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4105c-141">**\_GETZOOM em**</span><span class="sxs-lookup"><span data-stu-id="4105c-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





