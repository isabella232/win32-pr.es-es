---
title: Mensaje de PBM_GETBKCOLOR (commctrl. h)
description: Obtiene el color de fondo de la barra de progreso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905424"
---
# <a name="pbm_getbkcolor-message"></a><span data-ttu-id="e58f3-104">Mensaje de GETBKCOLOR de PBM \_</span><span class="sxs-lookup"><span data-stu-id="e58f3-104">PBM\_GETBKCOLOR message</span></span>

<span data-ttu-id="e58f3-105">Obtiene el color de fondo de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="e58f3-105">Gets the background color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e58f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e58f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58f3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e58f3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e58f3-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e58f3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e58f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e58f3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e58f3-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e58f3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e58f3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e58f3-111">Return value</span></span>

<span data-ttu-id="e58f3-112">Devuelve el color de fondo de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="e58f3-112">Returns the background color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="e58f3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e58f3-113">Remarks</span></span>

<span data-ttu-id="e58f3-114">Este es el color establecido por el mensaje de [**\_ SETBKCOLOR de PBM**](pbm-setbkcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="e58f3-114">This is the color set by the [**PBM\_SETBKCOLOR**](pbm-setbkcolor.md) message.</span></span> <span data-ttu-id="e58f3-115">El valor predeterminado es CLR \_ predeterminado, que se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="e58f3-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="e58f3-116">Esta función solo afecta al modo clásico, no a cualquier estilo visual.</span><span class="sxs-lookup"><span data-stu-id="e58f3-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58f3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e58f3-117">Requirements</span></span>



| <span data-ttu-id="e58f3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e58f3-118">Requirement</span></span> | <span data-ttu-id="e58f3-119">Value</span><span class="sxs-lookup"><span data-stu-id="e58f3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e58f3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e58f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e58f3-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e58f3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e58f3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e58f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e58f3-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e58f3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e58f3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e58f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58f3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e58f3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





