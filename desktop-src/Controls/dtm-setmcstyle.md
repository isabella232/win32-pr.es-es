---
title: Mensaje de DTM_SETMCSTYLE (commctrl. h)
description: Establece el estilo de un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro SetMonthCalStyle de fecha y hora \_ .
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150672"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="4404b-105">DTM \_ SETMCSTYLE</span><span class="sxs-lookup"><span data-stu-id="4404b-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="4404b-106">Establece el estilo de un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="4404b-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="4404b-107">Envíe este mensaje explícitamente o mediante la [**macro \_ SetMonthCalStyle de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="4404b-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4404b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4404b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4404b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4404b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4404b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4404b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4404b-111">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4404b-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="4404b-112">Valor de estilo.</span><span class="sxs-lookup"><span data-stu-id="4404b-112">A style value.</span></span> <span data-ttu-id="4404b-113">Para obtener más información, vea <a href="month-calendar-control-styles.md">estilos de control de calendario mensual</a>.</span><span class="sxs-lookup"><span data-stu-id="4404b-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4404b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4404b-114">Return value</span></span>

<span data-ttu-id="4404b-115">Devuelve el valor del estilo anterior.</span><span class="sxs-lookup"><span data-stu-id="4404b-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4404b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4404b-116">Requirements</span></span>



| <span data-ttu-id="4404b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4404b-117">Requirement</span></span> | <span data-ttu-id="4404b-118">Value</span><span class="sxs-lookup"><span data-stu-id="4404b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4404b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4404b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4404b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4404b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4404b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4404b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4404b-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4404b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4404b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4404b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4404b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4404b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





