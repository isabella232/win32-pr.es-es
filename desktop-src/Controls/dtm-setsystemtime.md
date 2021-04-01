---
title: Mensaje de DTM_SETSYSTEMTIME (commctrl. h)
description: Establece la hora en un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro SetSystemtime de fecha y hora \_ .
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996864"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="5852e-105">DTM \_ SETSYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="5852e-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="5852e-106">Establece la hora en un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="5852e-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="5852e-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetSystemtime de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="5852e-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5852e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5852e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5852e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5852e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5852e-110">Valor que especifica la acción que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="5852e-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="5852e-111">Este valor debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5852e-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="5852e-112">Value</span><span class="sxs-lookup"><span data-stu-id="5852e-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="5852e-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5852e-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="5852e-114"><dt>**GDT \_ válido**</dt></span><span class="sxs-lookup"><span data-stu-id="5852e-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="5852e-115">Establezca el control de DTP según los datos de la estructura a la que se dirige *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5852e-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="5852e-116"><dt>**GDT \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="5852e-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="5852e-117">Establezca el control de DTP en "sin fecha" y desactive su casilla.</span><span class="sxs-lookup"><span data-stu-id="5852e-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="5852e-118">Cuando se especifica esta marca, se omite *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5852e-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="5852e-119">Esta marca solo se aplica a los controles de DTP que se establecen en el estilo [**\_ SHOWNONE de DTS**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5852e-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="5852e-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5852e-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5852e-121">Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la hora del sistema utilizada para establecer el control de DTP.</span><span class="sxs-lookup"><span data-stu-id="5852e-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5852e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5852e-122">Return value</span></span>

<span data-ttu-id="5852e-123">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5852e-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5852e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5852e-124">Requirements</span></span>



| <span data-ttu-id="5852e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5852e-125">Requirement</span></span> | <span data-ttu-id="5852e-126">Value</span><span class="sxs-lookup"><span data-stu-id="5852e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5852e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5852e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5852e-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5852e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5852e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5852e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5852e-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5852e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5852e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5852e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5852e-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5852e-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

