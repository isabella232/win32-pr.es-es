---
title: Mensaje de DTM_GETMCFONT (commctrl. h)
description: Obtiene la fuente que está usando actualmente el control de calendario mensual del control de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro GetMonthCalFont de fecha y hora \_ .
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905528"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="6f927-105">DTM \_ GETMCFONT</span><span class="sxs-lookup"><span data-stu-id="6f927-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="6f927-106">Obtiene la fuente que está usando actualmente el control de calendario mensual del control de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="6f927-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="6f927-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCalFont de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="6f927-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f927-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f927-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f927-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f927-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f927-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6f927-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f927-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f927-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6f927-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6f927-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f927-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f927-113">Return value</span></span>

<span data-ttu-id="6f927-114">Devuelve un valor de HFONT que es el identificador de la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="6f927-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f927-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f927-115">Requirements</span></span>



| <span data-ttu-id="6f927-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f927-116">Requirement</span></span> | <span data-ttu-id="6f927-117">Value</span><span class="sxs-lookup"><span data-stu-id="6f927-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f927-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f927-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f927-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f927-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f927-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f927-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f927-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f927-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f927-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f927-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f927-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f927-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





