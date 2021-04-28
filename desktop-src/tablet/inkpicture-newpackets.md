---
description: 'Evento InkPicture.NewPackets: se produce cuando el recopilador de entrada de lápiz recibe un paquete.'
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Evento InkPicture.NewPackets (Msasisut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086483"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="ee3f8-103">Evento InkPicture.NewPackets</span><span class="sxs-lookup"><span data-stu-id="ee3f8-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="ee3f8-104">Se produce cuando el recopilador de entrada de lápiz recibe un paquete.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee3f8-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="ee3f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee3f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee3f8-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee3f8-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee3f8-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento NewInAirPackets.**](inkpicture-newinairpackets.md)</span><span class="sxs-lookup"><span data-stu-id="ee3f8-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="ee3f8-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee3f8-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee3f8-110">Objeto [**IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="ee3f8-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="ee3f8-111">*PacketCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee3f8-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee3f8-112">Número de paquetes recibidos para un [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="ee3f8-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="ee3f8-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ee3f8-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee3f8-114">Matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="ee3f8-115">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f8-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee3f8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee3f8-116">Return value</span></span>

<span data-ttu-id="ee3f8-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee3f8-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee3f8-118">Remarks</span></span>

<span data-ttu-id="ee3f8-119">Los paquetes se reciben mientras se recopila un trazo.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="ee3f8-120">Los eventos de paquetes se producen rápidamente y un controlador de eventos **NewPackets** debe ser rápido o el rendimiento sufra.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="ee3f8-121">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) de **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="ee3f8-122">Este evento debe usarse cuidadosamente, ya que podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="ee3f8-123">Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de lápiz.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="ee3f8-124">La matriz que devuelve el parámetro *PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="ee3f8-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee3f8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee3f8-126">Requirements</span></span>



| <span data-ttu-id="ee3f8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee3f8-127">Requirement</span></span> | <span data-ttu-id="ee3f8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ee3f8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3f8-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee3f8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3f8-130">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="ee3f8-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ee3f8-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee3f8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3f8-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee3f8-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ee3f8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee3f8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee3f8-134"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee3f8-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee3f8-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee3f8-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee3f8-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee3f8-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ee3f8-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee3f8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3f8-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="ee3f8-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ee3f8-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="ee3f8-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="ee3f8-140">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="ee3f8-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="ee3f8-141">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="ee3f8-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




