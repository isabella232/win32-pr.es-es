---
description: Especifica la marca de tiempo para el paso más reciente del marco.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680442"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="6a215-103">\_hora de limpieza de EC \_</span><span class="sxs-lookup"><span data-stu-id="6a215-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="6a215-104">Especifica la marca de tiempo para el paso más reciente del marco.</span><span class="sxs-lookup"><span data-stu-id="6a215-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a215-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a215-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a215-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6a215-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6a215-107">(**DWORD**) Menos 32 bits de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6a215-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="6a215-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6a215-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6a215-109">(**DWORD**) Los 32 superiores de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6a215-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6a215-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="6a215-110">Default Action</span></span>

<span data-ttu-id="6a215-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a215-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a215-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a215-112">Remarks</span></span>

<span data-ttu-id="6a215-113">El presentador del filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) envía este mensaje a EVR cuando completa un paso de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6a215-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a215-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a215-114">Requirements</span></span>



| <span data-ttu-id="6a215-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a215-115">Requirement</span></span> | <span data-ttu-id="6a215-116">Value</span><span class="sxs-lookup"><span data-stu-id="6a215-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a215-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a215-117">Header</span></span><br/> | <dl> <span data-ttu-id="6a215-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a215-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a215-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a215-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a215-120">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="6a215-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




