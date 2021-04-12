---
title: Mensaje de DTM_SETMCFONT (commctrl. h)
description: Establece la fuente que va a usar el control de calendario mensual del control de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro SetMonthCalFont de fecha y hora \_ .
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491824"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="2034c-105">DTM \_ SETMCFONT</span><span class="sxs-lookup"><span data-stu-id="2034c-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="2034c-106">Establece la fuente que va a usar el control de calendario mensual del control de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="2034c-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="2034c-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetMonthCalFont de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="2034c-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2034c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2034c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2034c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2034c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2034c-110">Identificador de la fuente que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="2034c-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="2034c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2034c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2034c-112">Especifica si el control debe volver a dibujarse inmediatamente después de establecer la fuente.</span><span class="sxs-lookup"><span data-stu-id="2034c-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="2034c-113">Establecer este parámetro en **true** hace que el control se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="2034c-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2034c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2034c-114">Return value</span></span>

<span data-ttu-id="2034c-115">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2034c-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2034c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2034c-116">Requirements</span></span>



| <span data-ttu-id="2034c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2034c-117">Requirement</span></span> | <span data-ttu-id="2034c-118">Value</span><span class="sxs-lookup"><span data-stu-id="2034c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2034c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2034c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2034c-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2034c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2034c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2034c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2034c-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2034c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2034c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2034c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2034c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





