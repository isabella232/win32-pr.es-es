---
description: Se envía cuando VMR ha seleccionado su mecanismo de representación.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680468"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="fce87-103">EC \_ VMR \_ RENDERDEVICE \_ set</span><span class="sxs-lookup"><span data-stu-id="fce87-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="fce87-104">Se envía cuando VMR ha seleccionado su mecanismo de representación.</span><span class="sxs-lookup"><span data-stu-id="fce87-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="fce87-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fce87-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce87-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fce87-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fce87-107">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="fce87-107">May be one of the following values:</span></span>



| <span data-ttu-id="fce87-108">Value</span><span class="sxs-lookup"><span data-stu-id="fce87-108">Value</span></span>                        | <span data-ttu-id="fce87-109">Significado</span><span class="sxs-lookup"><span data-stu-id="fce87-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="fce87-110">superposición de dispositivo de representación de VMR \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fce87-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="fce87-111">La VMR se representará en la superficie de superposición (solo VMR-7).</span><span class="sxs-lookup"><span data-stu-id="fce87-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="fce87-112">\_VIDMEM de \_ dispositivo de representación VMR \_</span><span class="sxs-lookup"><span data-stu-id="fce87-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="fce87-113">La VMR se representará en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fce87-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="fce87-114">\_SYSMEM de \_ dispositivo de representación VMR \_</span><span class="sxs-lookup"><span data-stu-id="fce87-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="fce87-115">La VMR se representará en la memoria del sistema (solo VMR-7).</span><span class="sxs-lookup"><span data-stu-id="fce87-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="fce87-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fce87-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fce87-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="fce87-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fce87-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fce87-118">Remarks</span></span>

<span data-ttu-id="fce87-119">Este evento lo envían los eventos VMR-7 y VMR-9 y se reenvían a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fce87-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="fce87-120">Tenga en cuenta que VMR-9 solo admite destinos de representación de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fce87-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce87-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce87-121">Requirements</span></span>



| <span data-ttu-id="fce87-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce87-122">Requirement</span></span> | <span data-ttu-id="fce87-123">Value</span><span class="sxs-lookup"><span data-stu-id="fce87-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fce87-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fce87-124">Header</span></span><br/> | <dl> <span data-ttu-id="fce87-125"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce87-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce87-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fce87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce87-127">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="fce87-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="fce87-128">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="fce87-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




