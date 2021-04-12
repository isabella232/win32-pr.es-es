---
title: Mensaje de DTM_GETDATETIMEPICKERINFO (commctrl. h)
description: Obtiene información sobre un control de selector de fecha y hora (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489298"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="16489-104">DTM \_ GETDATETIMEPICKERINFO</span><span class="sxs-lookup"><span data-stu-id="16489-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="16489-105">Obtiene información sobre un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="16489-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="16489-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16489-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16489-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16489-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="16489-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="16489-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16489-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="16489-110">Puntero a <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> para recibir la información.</span><span class="sxs-lookup"><span data-stu-id="16489-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="16489-111">El autor de la llamada es responsable de asignar la memoria para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="16489-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="16489-112">Establezca el miembro **cbSize** de la estructura en SIZEOF (DATETIMEPICKERINFO) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="16489-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16489-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16489-113">Return value</span></span>

<span data-ttu-id="16489-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="16489-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="16489-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16489-115">Requirements</span></span>



| <span data-ttu-id="16489-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="16489-116">Requirement</span></span> | <span data-ttu-id="16489-117">Value</span><span class="sxs-lookup"><span data-stu-id="16489-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16489-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16489-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16489-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="16489-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16489-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16489-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16489-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="16489-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16489-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16489-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16489-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16489-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





