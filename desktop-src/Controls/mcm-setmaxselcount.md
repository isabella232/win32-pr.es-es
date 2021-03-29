---
title: Mensaje de MCM_SETMAXSELCOUNT (commctrl. h)
description: Establece el número máximo de días que se pueden seleccionar en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetMaxSelCount.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- MCM_SETMAXSELCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905593"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="1803f-105">Mensaje de MCM \_ SETMAXSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="1803f-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="1803f-106">Establece el número máximo de días que se pueden seleccionar en un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="1803f-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="1803f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="1803f-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1803f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1803f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1803f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1803f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1803f-110">Valor de tipo **int** que se establecerá para representar el número máximo de días que se pueden seleccionar.</span><span class="sxs-lookup"><span data-stu-id="1803f-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="1803f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1803f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1803f-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1803f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1803f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1803f-113">Return value</span></span>

<span data-ttu-id="1803f-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="1803f-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="1803f-115">Se producirá un error en este mensaje si se aplica a un control de calendario mensual que no use el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1803f-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="1803f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1803f-116">Requirements</span></span>



| <span data-ttu-id="1803f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1803f-117">Requirement</span></span> | <span data-ttu-id="1803f-118">Value</span><span class="sxs-lookup"><span data-stu-id="1803f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1803f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1803f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1803f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1803f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1803f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1803f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1803f-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1803f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1803f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1803f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1803f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1803f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





