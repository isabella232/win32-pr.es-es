---
title: Mensaje de DTM_GETSYSTEMTIME (commctrl. h)
description: Obtiene la hora actualmente seleccionada de un control de selector de fecha y hora (DTP) y lo coloca en una estructura SYSTEMTIME especificada. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetSystemtime de DateTime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150673"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="b41f9-105">DTM \_ GETSYSTEMTIME Message</span><span class="sxs-lookup"><span data-stu-id="b41f9-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="b41f9-106">Obtiene la hora actualmente seleccionada de un control de selector de fecha y hora (DTP) y lo coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada.</span><span class="sxs-lookup"><span data-stu-id="b41f9-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="b41f9-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetSystemtime de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="b41f9-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b41f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b41f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b41f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b41f9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b41f9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b41f9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b41f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b41f9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f9-112">Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="b41f9-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="b41f9-113">Si **DTM \_ GETSYSTEMTIME** devuelve GDT \_ Valid, esta estructura contendrá la hora seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="b41f9-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="b41f9-114">De lo contrario, no contendrá información válida.</span><span class="sxs-lookup"><span data-stu-id="b41f9-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="b41f9-115">Este parámetro debe ser un puntero válido; no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b41f9-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b41f9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b41f9-116">Return value</span></span>

<span data-ttu-id="b41f9-117">Devuelve GDT \_ válido si la información de hora se colocó correctamente en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b41f9-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="b41f9-118">Devuelve GDT \_ None si el control se estableció en el estilo [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) y no se activó la casilla Control.</span><span class="sxs-lookup"><span data-stu-id="b41f9-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="b41f9-119">Devuelve \_ un error de GDT si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b41f9-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b41f9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b41f9-120">Requirements</span></span>



| <span data-ttu-id="b41f9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b41f9-121">Requirement</span></span> | <span data-ttu-id="b41f9-122">Value</span><span class="sxs-lookup"><span data-stu-id="b41f9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b41f9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b41f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b41f9-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b41f9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b41f9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b41f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b41f9-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b41f9-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b41f9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b41f9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b41f9-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b41f9-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

