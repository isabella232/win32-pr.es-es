---
description: 'Evento InkPicture.NewInAirPackets: se produce cuando se ve un paquete en el aire.'
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: Evento InkPicture.NewInAirPackets (Ms inkut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0de8f2423817bada84f83b63de1517393740db4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086563"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="aa20c-103">Evento InkPicture.NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="aa20c-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="aa20c-104">Se produce cuando se ve un paquete en el aire.</span><span class="sxs-lookup"><span data-stu-id="aa20c-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa20c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa20c-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="aa20c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa20c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa20c-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aa20c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa20c-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento NewInAirPackets.**</span><span class="sxs-lookup"><span data-stu-id="aa20c-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="aa20c-109">*PacketCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aa20c-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa20c-110">Número de paquetes en el aire recibidos.</span><span class="sxs-lookup"><span data-stu-id="aa20c-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="aa20c-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa20c-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa20c-112">Matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="aa20c-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="aa20c-113">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="aa20c-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa20c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa20c-114">Return value</span></span>

<span data-ttu-id="aa20c-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="aa20c-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa20c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa20c-116">Remarks</span></span>

<span data-ttu-id="aa20c-117">Se crea un paquete en el aire cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto del recopilador de entrada de lápiz o el usuario mueve un mouse dentro de la ventana asociada del objeto del recopilador de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="aa20c-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="aa20c-118">**Los eventos NewInAirPackets** se generan rápidamente y el controlador de eventos debe ser rápido o el rendimiento se puede ver afectado.</span><span class="sxs-lookup"><span data-stu-id="aa20c-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="aa20c-119">Este método de evento se define en las interfaces de solo envío (dispinterfaces) **\_ de IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="aa20c-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="aa20c-120">El **evento NewInAirPackets** se desencadena incluso en el modo de selección o borrado, no solo al insertar entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="aa20c-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="aa20c-121">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="aa20c-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="aa20c-122">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="aa20c-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="aa20c-123">Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) del objeto del recopilador de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="aa20c-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="aa20c-124">La matriz que devuelve *el parámetro PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa20c-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="aa20c-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="aa20c-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa20c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa20c-126">Requirements</span></span>



| <span data-ttu-id="aa20c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa20c-127">Requirement</span></span> | <span data-ttu-id="aa20c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="aa20c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa20c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa20c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aa20c-130">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="aa20c-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="aa20c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa20c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aa20c-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aa20c-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="aa20c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa20c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa20c-134"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="aa20c-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aa20c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa20c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa20c-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa20c-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="aa20c-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aa20c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa20c-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="aa20c-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="aa20c-139">**Propiedad DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="aa20c-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="aa20c-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="aa20c-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="aa20c-141">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="aa20c-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




