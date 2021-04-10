---
title: Mensaje de TTM_POPUP (commctrl. h)
description: Hace que la información sobre herramientas se muestre en las coordenadas del último mensaje del mouse.
ms.assetid: 6b7b430b-4f59-49f9-bd3f-70099485fac8
keywords:
- TTM_POPUP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_POPUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabcbf710b57cdb110eb349a928bdceaf389dbb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150301"
---
# <a name="ttm_popup-message"></a><span data-ttu-id="2a96f-104">\_Mensaje emergente de TTM</span><span class="sxs-lookup"><span data-stu-id="2a96f-104">TTM\_POPUP message</span></span>

<span data-ttu-id="2a96f-105">Hace que la información sobre herramientas se muestre en las coordenadas del último mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="2a96f-105">Causes the tooltip to display at the coordinates of the last mouse message.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a96f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a96f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a96f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a96f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a96f-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2a96f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a96f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a96f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a96f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2a96f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a96f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a96f-111">Return value</span></span>

<span data-ttu-id="2a96f-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2a96f-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a96f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a96f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2a96f-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="2a96f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2a96f-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2a96f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a96f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a96f-116">Requirements</span></span>



| <span data-ttu-id="2a96f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a96f-117">Requirement</span></span> | <span data-ttu-id="2a96f-118">Value</span><span class="sxs-lookup"><span data-stu-id="2a96f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a96f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a96f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a96f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a96f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a96f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a96f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a96f-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a96f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a96f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a96f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a96f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a96f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





