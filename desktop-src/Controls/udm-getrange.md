---
title: Mensaje de UDM_GETRANGE (commctrl. h)
description: Recupera las posiciones mínima y máxima (intervalo) de un control de flechas.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274556"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="15ca0-104">\_Mensaje GETRANGE UDM</span><span class="sxs-lookup"><span data-stu-id="15ca0-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="15ca0-105">Recupera las posiciones mínima y máxima (intervalo) de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="15ca0-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="15ca0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15ca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ca0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15ca0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="15ca0-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="15ca0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="15ca0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15ca0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="15ca0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="15ca0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ca0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15ca0-111">Return value</span></span>

<span data-ttu-id="15ca0-112">El valor devuelto es un valor de 32 bits que contiene las posiciones mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="15ca0-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="15ca0-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es la posición máxima del control y el valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es la posición mínima.</span><span class="sxs-lookup"><span data-stu-id="15ca0-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ca0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ca0-114">Requirements</span></span>



| <span data-ttu-id="15ca0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ca0-115">Requirement</span></span> | <span data-ttu-id="15ca0-116">Value</span><span class="sxs-lookup"><span data-stu-id="15ca0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15ca0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15ca0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15ca0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15ca0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15ca0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15ca0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15ca0-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15ca0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15ca0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15ca0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ca0-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15ca0-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

