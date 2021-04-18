---
description: Se produce cuando el recopilador de tinta recibe un paquete.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Evento InkPicture. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0b3e1df0df2ba051150550daa60772e2a068df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716305"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="71cad-103">Evento InkPicture. NewPackets</span><span class="sxs-lookup"><span data-stu-id="71cad-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="71cad-104">Se produce cuando el recopilador de tinta recibe un paquete.</span><span class="sxs-lookup"><span data-stu-id="71cad-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="71cad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71cad-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="71cad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cad-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="71cad-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cad-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**NewInAirPackets**](inkpicture-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="71cad-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="71cad-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="71cad-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cad-110">El objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="71cad-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="71cad-111">*PacketCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71cad-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cad-112">El número de paquetes recibidos para un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="71cad-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="71cad-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="71cad-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="71cad-114">Una matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="71cad-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="71cad-115">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="71cad-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71cad-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71cad-116">Return value</span></span>

<span data-ttu-id="71cad-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="71cad-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71cad-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71cad-118">Remarks</span></span>

<span data-ttu-id="71cad-119">Los paquetes se reciben mientras se recopila un trazo.</span><span class="sxs-lookup"><span data-stu-id="71cad-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="71cad-120">Los eventos de paquetes se producen rápidamente y un controlador de eventos **NewPackets** debe ser rápido o se ve afectado por el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71cad-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="71cad-121">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="71cad-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="71cad-122">Este evento debe usarse con cuidado, ya que podría tener un efecto adverso en el rendimiento de la tinta si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="71cad-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="71cad-123">Para establecer qué propiedades están contenidas en esta matriz, use la propiedad [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de tinta.</span><span class="sxs-lookup"><span data-stu-id="71cad-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="71cad-124">La matriz que devuelve el parámetro *PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="71cad-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="71cad-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="71cad-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71cad-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71cad-126">Requirements</span></span>



| <span data-ttu-id="71cad-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="71cad-127">Requirement</span></span> | <span data-ttu-id="71cad-128">Value</span><span class="sxs-lookup"><span data-stu-id="71cad-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cad-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71cad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71cad-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="71cad-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="71cad-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71cad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71cad-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="71cad-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="71cad-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71cad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="71cad-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="71cad-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="71cad-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71cad-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="71cad-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71cad-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="71cad-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="71cad-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cad-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="71cad-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="71cad-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="71cad-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="71cad-140">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="71cad-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="71cad-141">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="71cad-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




