---
description: 'Evento InkCollector.NewPackets: se produce cuando el recopilador de entrada de lápiz recibe un paquete.'
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Evento InkCollector.NewPackets (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110123"
---
# <a name="inkcollectornewpackets-event"></a><span data-ttu-id="efa94-103">Evento InkCollector.NewPackets</span><span class="sxs-lookup"><span data-stu-id="efa94-103">InkCollector.NewPackets event</span></span>

<span data-ttu-id="efa94-104">Se produce cuando el recopilador de entrada de lápiz recibe un paquete.</span><span class="sxs-lookup"><span data-stu-id="efa94-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efa94-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="efa94-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efa94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efa94-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="efa94-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa94-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento NewInAirPackets.**](inkcollector-newinairpackets.md)</span><span class="sxs-lookup"><span data-stu-id="efa94-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="efa94-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="efa94-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa94-110">Especifica el [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="efa94-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="efa94-111">*PacketCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="efa94-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa94-112">Número de paquetes recibidos para un [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="efa94-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="efa94-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="efa94-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efa94-114">Cuando este método vuelve, contiene una matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="efa94-114">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="efa94-115">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="efa94-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efa94-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efa94-116">Return value</span></span>

<span data-ttu-id="efa94-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="efa94-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efa94-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efa94-118">Remarks</span></span>

<span data-ttu-id="efa94-119">Los paquetes se reciben mientras se recopila un trazo.</span><span class="sxs-lookup"><span data-stu-id="efa94-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="efa94-120">Los eventos de paquetes se producen rápidamente y un controlador de eventos **NewPackets** debe ser rápido o el rendimiento se vería afectado.</span><span class="sxs-lookup"><span data-stu-id="efa94-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="efa94-121">El método de evento TThis se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents con un identificador de DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="efa94-121">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="efa94-122">Este evento debe usarse cuidadosamente, ya que podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="efa94-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="efa94-123">Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto del recopilador de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="efa94-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="efa94-124">La matriz que devuelve *el parámetro PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="efa94-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="efa94-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="efa94-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efa94-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efa94-126">Requirements</span></span>



| <span data-ttu-id="efa94-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="efa94-127">Requirement</span></span> | <span data-ttu-id="efa94-128">Valor</span><span class="sxs-lookup"><span data-stu-id="efa94-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa94-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efa94-129">Minimum supported client</span></span><br/> | <span data-ttu-id="efa94-130">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="efa94-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="efa94-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efa94-131">Minimum supported server</span></span><br/> | <span data-ttu-id="efa94-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="efa94-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="efa94-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efa94-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="efa94-134"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="efa94-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="efa94-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efa94-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="efa94-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efa94-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="efa94-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="efa94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efa94-138">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="efa94-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="efa94-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="efa94-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="efa94-140">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="efa94-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="efa94-141">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="efa94-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




