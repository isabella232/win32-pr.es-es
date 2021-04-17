---
description: Se envía el mensaje de eliminación de línea TAPI \_ para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo de línea.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Mensaje de LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680364"
---
# <a name="line_remove-message"></a><span data-ttu-id="fac78-103">Mensaje de eliminación de línea \_</span><span class="sxs-lookup"><span data-stu-id="fac78-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="fac78-104">Se envía el mensaje de eliminación de **línea \_** TAPI para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="fac78-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="fac78-105">Por lo general, esto no se utiliza para las eliminaciones temporales, como la extracción de dispositivos PCMCIA, sino solo para las eliminaciones permanentes en las que el proveedor de servicios ya no debe informar del dispositivo si se reinicializara TAPI.</span><span class="sxs-lookup"><span data-stu-id="fac78-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="fac78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fac78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac78-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="fac78-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="fac78-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fac78-108">Reserved.</span></span> <span data-ttu-id="fac78-109">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="fac78-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fac78-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="fac78-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="fac78-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fac78-111">Reserved.</span></span> <span data-ttu-id="fac78-112">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="fac78-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fac78-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="fac78-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="fac78-114">Identificador del dispositivo de línea que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="fac78-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="fac78-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="fac78-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="fac78-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fac78-116">Reserved.</span></span> <span data-ttu-id="fac78-117">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="fac78-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fac78-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="fac78-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="fac78-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fac78-119">Reserved.</span></span> <span data-ttu-id="fac78-120">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="fac78-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac78-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fac78-121">Return value</span></span>

<span data-ttu-id="fac78-122">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fac78-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac78-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fac78-123">Remarks</span></span>

<span data-ttu-id="fac78-124">Las aplicaciones que admiten la versión 2,0 o posterior de TAPI recibirán un mensaje de **\_ eliminación de línea** .</span><span class="sxs-lookup"><span data-stu-id="fac78-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="fac78-125">Esto les informa de que el dispositivo se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="fac78-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="fac78-126">El mensaje de **\_ eliminación de línea** está precedido por un mensaje de [**\_ cierre de línea**](line-close.md) en cada identificador de línea, si la aplicación tenía abierta la línea.</span><span class="sxs-lookup"><span data-stu-id="fac78-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="fac78-127">Este mensaje se envía a todas las aplicaciones que admiten la versión 2,0 o posterior de TAPI que han llamado a [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluidos los que no tienen dispositivos de línea abiertos en este momento.</span><span class="sxs-lookup"><span data-stu-id="fac78-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="fac78-128">A las aplicaciones anteriores se les envía un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que especifica LINEDEVSTATE \_ quitado, seguido de un mensaje de cierre de línea \_ .</span><span class="sxs-lookup"><span data-stu-id="fac78-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="fac78-129">Sin embargo, a diferencia del mensaje de **\_ eliminación de línea** , estas aplicaciones antiguas solo pueden recibir estos mensajes si tienen la línea abierta cuando se quita.</span><span class="sxs-lookup"><span data-stu-id="fac78-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="fac78-130">Si no tienen abierta la línea, su única indicación de que el dispositivo se ha quitado recibirá un \_ error LINEERR Device al intentar acceder al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fac78-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="fac78-131">Una vez que se ha quitado un dispositivo, cualquier intento de acceder al dispositivo por su identificador de dispositivo produce un \_ error LINEERR Device.</span><span class="sxs-lookup"><span data-stu-id="fac78-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="fac78-132">Una vez que se han cerrado todas las aplicaciones TAPI para que TAPI pueda reiniciarse y, cuando se reinicialice TAPI, el dispositivo que se ha quitado ya no ocupa un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fac78-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="fac78-133">Implementación: es TAPI que devuelve este LINEERR \_ Device; una vez que se recibe un mensaje de **\_ eliminación de línea** de un proveedor de servicios; no se realizan más llamadas a ese proveedor de servicios con ese identificador de dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="fac78-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fac78-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac78-134">Requirements</span></span>



| <span data-ttu-id="fac78-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac78-135">Requirement</span></span> | <span data-ttu-id="fac78-136">Value</span><span class="sxs-lookup"><span data-stu-id="fac78-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fac78-137">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="fac78-137">TAPI version</span></span><br/> | <span data-ttu-id="fac78-138">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fac78-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fac78-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fac78-139">Header</span></span><br/>       | <dl> <span data-ttu-id="fac78-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fac78-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac78-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="fac78-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac78-142">**cierre de línea \_**</span><span class="sxs-lookup"><span data-stu-id="fac78-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="fac78-143">**LÍNEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="fac78-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="fac78-144">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="fac78-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




