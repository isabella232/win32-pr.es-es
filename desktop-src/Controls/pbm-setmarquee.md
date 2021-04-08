---
title: Mensaje de PBM_SETMARQUEE (commctrl. h)
description: Establece la barra de progreso en el modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996735"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="d2a7f-105">Mensaje de SETMARQUEE de PBM \_</span><span class="sxs-lookup"><span data-stu-id="d2a7f-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="d2a7f-106">Establece la barra de progreso en el modo de marquesina.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="d2a7f-107">Esto hace que la barra de progreso se mueva como una marquesina.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2a7f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2a7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a7f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2a7f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a7f-110">Indica si se activa o desactiva el modo de marquesina.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="d2a7f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2a7f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2a7f-112">Tiempo, en milisegundos, entre actualizaciones de animaciones de marquesina.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="d2a7f-113">Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a7f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2a7f-114">Return value</span></span>

<span data-ttu-id="d2a7f-115">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a7f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2a7f-116">Remarks</span></span>

<span data-ttu-id="d2a7f-117">Use este mensaje si no conoce la cantidad de progreso hasta la finalización, pero quiere indicar que se está realizando el progreso.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="d2a7f-118">Envíe el mensaje de **PBM \_ SETMARQUEE** para iniciar o detener la animación.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="d2a7f-119">Debe establecer el estilo de control en [**la \_ marquesina de PBS**](progress-bar-control-styles.md) antes de intentar iniciar la animación.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2a7f-120">Este mensaje requiere ComCtl32.dll versión 6,00 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d2a7f-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2a7f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2a7f-121">Requirements</span></span>



| <span data-ttu-id="d2a7f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a7f-122">Requirement</span></span> | <span data-ttu-id="d2a7f-123">Value</span><span class="sxs-lookup"><span data-stu-id="d2a7f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a7f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a7f-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d2a7f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2a7f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a7f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a7f-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2a7f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2a7f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2a7f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a7f-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a7f-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





