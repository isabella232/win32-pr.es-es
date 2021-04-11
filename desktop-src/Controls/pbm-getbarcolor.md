---
title: Mensaje de PBM_GETBARCOLOR (commctrl. h)
description: Obtiene el color de la barra de progreso.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150659"
---
# <a name="pbm_getbarcolor-message"></a><span data-ttu-id="6326c-104">Mensaje de GETBARCOLOR de PBM \_</span><span class="sxs-lookup"><span data-stu-id="6326c-104">PBM\_GETBARCOLOR message</span></span>

<span data-ttu-id="6326c-105">Obtiene el color de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="6326c-105">Gets the color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6326c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6326c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6326c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6326c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6326c-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6326c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6326c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6326c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6326c-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6326c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6326c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6326c-111">Return value</span></span>

<span data-ttu-id="6326c-112">Devuelve el color de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="6326c-112">Returns the color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="6326c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6326c-113">Remarks</span></span>

<span data-ttu-id="6326c-114">Este es el color establecido por el mensaje de [**\_ SETBARCOLOR de PBM**](pbm-setbarcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="6326c-114">This is the color set by the [**PBM\_SETBARCOLOR**](pbm-setbarcolor.md) message.</span></span> <span data-ttu-id="6326c-115">El valor predeterminado es CLR \_ predeterminado, que se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="6326c-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="6326c-116">Esta función solo afecta al modo clásico, no a cualquier estilo visual.</span><span class="sxs-lookup"><span data-stu-id="6326c-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6326c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6326c-117">Requirements</span></span>



| <span data-ttu-id="6326c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6326c-118">Requirement</span></span> | <span data-ttu-id="6326c-119">Value</span><span class="sxs-lookup"><span data-stu-id="6326c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6326c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6326c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6326c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6326c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6326c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6326c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6326c-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6326c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6326c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6326c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6326c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6326c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





