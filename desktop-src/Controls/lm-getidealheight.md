---
title: Mensaje de LM_GETIDEALHEIGHT (commctrl. h)
description: Recupera el alto preferido de un vínculo para el ancho actual del control.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a92f24d63cc8f58e260d79dafd0555429d65d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905009"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="f8497-104">\_Mensaje GETIDEALHEIGHT de LM</span><span class="sxs-lookup"><span data-stu-id="f8497-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="f8497-105">Recupera el alto preferido de un vínculo para el ancho actual del control.</span><span class="sxs-lookup"><span data-stu-id="f8497-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8497-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8497-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8497-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8497-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f8497-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8497-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8497-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f8497-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f8497-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8497-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8497-111">Return value</span></span>

<span data-ttu-id="f8497-112">Entero que representa el alto preferido del texto del vínculo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f8497-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8497-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8497-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8497-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f8497-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f8497-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8497-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8497-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8497-116">Requirements</span></span>



| <span data-ttu-id="f8497-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8497-117">Requirement</span></span> | <span data-ttu-id="f8497-118">Value</span><span class="sxs-lookup"><span data-stu-id="f8497-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8497-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8497-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f8497-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8497-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8497-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8497-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f8497-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8497-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8497-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8497-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8497-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8497-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





