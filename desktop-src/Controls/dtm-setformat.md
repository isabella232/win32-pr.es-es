---
title: Mensaje de DTM_SETFORMAT (commctrl. h)
description: Establece la presentación de un control de selector de fecha y hora (DTP) basándose en una cadena de formato determinada. Puede enviar este mensaje explícitamente o utilizar la macro SetFormat de fecha y hora \_ .
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079573"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="28173-105">DTM \_ SETFORMAT</span><span class="sxs-lookup"><span data-stu-id="28173-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="28173-106">Establece la presentación de un control de selector de fecha y hora (DTP) basándose en una cadena de formato determinada.</span><span class="sxs-lookup"><span data-stu-id="28173-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="28173-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetFormat de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .</span><span class="sxs-lookup"><span data-stu-id="28173-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="28173-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28173-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28173-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28173-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="28173-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="28173-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="28173-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28173-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28173-112">Puntero a una [cadena de formato](date-and-time-picker-controls.md) terminada en cero que define la presentación deseada.</span><span class="sxs-lookup"><span data-stu-id="28173-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="28173-113">Si se establece este parámetro en **null** , se restablecerá el control en la cadena de formato predeterminada para el estilo actual.</span><span class="sxs-lookup"><span data-stu-id="28173-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28173-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28173-114">Return value</span></span>

<span data-ttu-id="28173-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="28173-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="28173-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28173-116">Remarks</span></span>

<span data-ttu-id="28173-117">Es aceptable incluir caracteres adicionales en la cadena de formato para generar una pantalla más enriquecida.</span><span class="sxs-lookup"><span data-stu-id="28173-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="28173-118">Sin embargo, los caracteres que no sean de formato deben encerrarse entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="28173-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="28173-119">Por ejemplo, la cadena de formato "' hoy es: ' HH ': ' m ': ddddMMMdd ', ' yyy" produciría una salida como "hoy es: 04:22:31 martes, 23, 1996".</span><span class="sxs-lookup"><span data-stu-id="28173-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="28173-120">Un control de DTP realiza un seguimiento de los cambios de la configuración regional cuando se usa la cadena de formato predeterminada.</span><span class="sxs-lookup"><span data-stu-id="28173-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="28173-121">Si establece una cadena de formato personalizado, no se actualizará en respuesta a los cambios de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="28173-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28173-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28173-122">Requirements</span></span>



| <span data-ttu-id="28173-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="28173-123">Requirement</span></span> | <span data-ttu-id="28173-124">Value</span><span class="sxs-lookup"><span data-stu-id="28173-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28173-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28173-125">Minimum supported client</span></span><br/> | <span data-ttu-id="28173-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="28173-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28173-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28173-127">Minimum supported server</span></span><br/> | <span data-ttu-id="28173-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="28173-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28173-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28173-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="28173-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28173-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="28173-131">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="28173-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="28173-132">**DTM \_ SETFORMATW** (Unicode) y **DTM \_ SETFORMATA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="28173-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 





