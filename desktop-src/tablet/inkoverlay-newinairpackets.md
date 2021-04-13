---
description: Se produce cuando se detecta un paquete en el aire.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac030a2e32ecf662d811a3c91ccdc2dd3c5fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278484"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="46c1d-103">Evento InkOverlay. NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="46c1d-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="46c1d-104">Se produce cuando se detecta un paquete en el aire.</span><span class="sxs-lookup"><span data-stu-id="46c1d-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46c1d-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="46c1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46c1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c1d-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="46c1d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c1d-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="46c1d-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="46c1d-109">*PacketCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46c1d-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c1d-110">El número de paquetes en Air recibidos.</span><span class="sxs-lookup"><span data-stu-id="46c1d-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="46c1d-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="46c1d-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46c1d-112">Una matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="46c1d-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="46c1d-113">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="46c1d-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c1d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46c1d-114">Return value</span></span>

<span data-ttu-id="46c1d-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="46c1d-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46c1d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46c1d-116">Remarks</span></span>

<span data-ttu-id="46c1d-117">Se crea un paquete en el aire cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto del recopilador de tinta o el usuario mueve un mouse dentro de la ventana asociada del objeto del recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="46c1d-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="46c1d-118">Los eventos [**NewInAirPackets**](inkcollector-newinairpackets.md) se generan rápidamente y el controlador de eventos debe ser rápido o se ve afectado por el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="46c1d-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="46c1d-119">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="46c1d-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="46c1d-120">El evento [**NewInAirPackets**](inkcollector-newinairpackets.md) se desencadena incluso cuando está en modo de selección o borrado, no solo cuando se inserta una entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="46c1d-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="46c1d-121">Esto requiere que supervise el modo de edición (que es responsable de establecer) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="46c1d-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="46c1d-122">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="46c1d-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="46c1d-123">Para establecer qué propiedades están contenidas en esta matriz, use la propiedad [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="46c1d-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="46c1d-124">La matriz que devuelve el parámetro *PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="46c1d-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="46c1d-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="46c1d-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46c1d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46c1d-126">Requirements</span></span>



| <span data-ttu-id="46c1d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c1d-127">Requirement</span></span> | <span data-ttu-id="46c1d-128">Value</span><span class="sxs-lookup"><span data-stu-id="46c1d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c1d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46c1d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="46c1d-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="46c1d-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="46c1d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46c1d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="46c1d-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="46c1d-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="46c1d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46c1d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c1d-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="46c1d-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="46c1d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46c1d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="46c1d-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c1d-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="46c1d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c1d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c1d-138">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="46c1d-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="46c1d-139">**Propiedad DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="46c1d-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="46c1d-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="46c1d-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="46c1d-141">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="46c1d-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




