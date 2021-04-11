---
description: Se produce cuando el recopilador de entradas de lápiz rreceives un paquete.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: Evento InkOverlay. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43743b47d007b44d4f2460266e7198266c36afd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278855"
---
# <a name="inkoverlaynewpackets-event"></a><span data-ttu-id="5fc49-103">Evento InkOverlay. NewPackets</span><span class="sxs-lookup"><span data-stu-id="5fc49-103">InkOverlay.NewPackets event</span></span>

<span data-ttu-id="5fc49-104">Se produce cuando el recopilador de entradas de lápiz rreceives un paquete</span><span class="sxs-lookup"><span data-stu-id="5fc49-104">Occurs when the ink collecto rreceives a packet</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fc49-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="5fc49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fc49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc49-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5fc49-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc49-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="5fc49-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="5fc49-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5fc49-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc49-110">Especifica el objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="5fc49-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5fc49-111">*PacketCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5fc49-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc49-112">El número de paquetes recibidos para un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="5fc49-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5fc49-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5fc49-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc49-114">Una matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="5fc49-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="5fc49-115">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="5fc49-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc49-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fc49-116">Return value</span></span>

<span data-ttu-id="5fc49-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5fc49-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc49-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fc49-118">Remarks</span></span>

<span data-ttu-id="5fc49-119">Los paquetes se reciben mientras se recopila un trazo.</span><span class="sxs-lookup"><span data-stu-id="5fc49-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="5fc49-120">Los eventos de paquetes se producen rápidamente y un controlador de eventos [**NewPackets**](inkcollector-newpackets.md) debe ser rápido o se ve afectado por el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5fc49-120">Packet events occur rapidly, and a [**NewPackets**](inkcollector-newpackets.md) event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="5fc49-121">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="5fc49-121">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="5fc49-122">Este evento debe usarse con cuidado, ya que podría tener un efecto adverso en el rendimiento de la tinta si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="5fc49-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="5fc49-123">Para establecer qué propiedades están contenidas en esta matriz, use la propiedad [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="5fc49-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="5fc49-124">La matriz que devuelve el parámetro *PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5fc49-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="5fc49-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="5fc49-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5fc49-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc49-126">Requirements</span></span>



| <span data-ttu-id="5fc49-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc49-127">Requirement</span></span> | <span data-ttu-id="5fc49-128">Value</span><span class="sxs-lookup"><span data-stu-id="5fc49-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc49-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc49-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc49-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5fc49-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5fc49-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc49-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc49-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5fc49-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5fc49-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fc49-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc49-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc49-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5fc49-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fc49-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fc49-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fc49-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5fc49-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fc49-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc49-138">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="5fc49-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5fc49-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="5fc49-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="5fc49-140">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="5fc49-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5fc49-141">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="5fc49-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




