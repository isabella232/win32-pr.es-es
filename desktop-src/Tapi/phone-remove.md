---
description: Se envía el mensaje de eliminación del teléfono TAPI \_ para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo telefónico.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Mensaje de PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690400"
---
# <a name="phone_remove-message"></a><span data-ttu-id="99297-103">TELÉFONO- \_ quitar mensaje</span><span class="sxs-lookup"><span data-stu-id="99297-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="99297-104">Se envía el mensaje de eliminación del **teléfono \_** TAPI para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="99297-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="99297-105">Por lo general, esto no se utiliza para las eliminaciones temporales, como la extracción de dispositivos PCMCIA, sino solo para las eliminaciones permanentes en las que el proveedor de servicios ya no debe informar del dispositivo si se reinicializara TAPI.</span><span class="sxs-lookup"><span data-stu-id="99297-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="99297-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99297-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="99297-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="99297-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="99297-108">Reserved.</span></span> <span data-ttu-id="99297-109">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="99297-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="99297-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="99297-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="99297-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="99297-111">Reserved.</span></span> <span data-ttu-id="99297-112">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="99297-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="99297-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="99297-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="99297-114">Identificador del dispositivo telefónico que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="99297-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="99297-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="99297-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="99297-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="99297-116">Reserved.</span></span> <span data-ttu-id="99297-117">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="99297-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="99297-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="99297-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="99297-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="99297-119">Reserved.</span></span> <span data-ttu-id="99297-120">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="99297-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99297-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99297-121">Return value</span></span>

<span data-ttu-id="99297-122">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="99297-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99297-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99297-123">Remarks</span></span>

<span data-ttu-id="99297-124">Las aplicaciones TAPI versión 2,0 o posterior se envían un mensaje para **\_ quitar un teléfono** .</span><span class="sxs-lookup"><span data-stu-id="99297-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="99297-125">Esto les informa de que el dispositivo se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="99297-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="99297-126">El mensaje para **\_ quitar el teléfono** está precedido por un mensaje de [**\_ cierre**](phone-close.md) de teléfono en cada identificador de teléfono, si la aplicación tenía el teléfono abierto.</span><span class="sxs-lookup"><span data-stu-id="99297-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="99297-127">Este mensaje se envía a todas las aplicaciones que admiten la versión 2,0 o posterior de TAPI que han llamado a [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), incluidos los que no tienen dispositivos de teléfono abiertos en este momento.</span><span class="sxs-lookup"><span data-stu-id="99297-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="99297-128">A las aplicaciones anteriores (que negociaron la versión 1,4 o anterior de TAPI) se les envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) que especifica PHONESTATE \_ quitado, seguido de un mensaje de [**\_ cierre de teléfono**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="99297-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="99297-129">Sin embargo, a diferencia del mensaje para **\_ quitar el teléfono** , estas aplicaciones antiguas solo pueden recibir estos mensajes si tienen el teléfono abierto cuando se quita.</span><span class="sxs-lookup"><span data-stu-id="99297-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="99297-130">Si no tienen el teléfono abierto, su única indicación de que el dispositivo se ha quitado recibirá un PHONEERR \_ Device cuando intente obtener acceso al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99297-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="99297-131">Una vez que se ha quitado un dispositivo, cualquier intento de acceder al dispositivo por su identificador de dispositivo produce un \_ error PHONEERR Device.</span><span class="sxs-lookup"><span data-stu-id="99297-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="99297-132">Una vez que se han cerrado todas las aplicaciones TAPI para que TAPI pueda reiniciarse y, cuando se reinicialice TAPI, el dispositivo que se ha quitado ya no ocupa un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99297-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="99297-133">Implementación: es TAPI que devuelve este \_ mensaje de PHONEERR Device después \_ de recibir un mensaje de eliminación de teléfono de un proveedor de servicios; no se realizan más llamadas a ese proveedor de servicios con ese identificador de dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="99297-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99297-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99297-134">Requirements</span></span>



| <span data-ttu-id="99297-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="99297-135">Requirement</span></span> | <span data-ttu-id="99297-136">Value</span><span class="sxs-lookup"><span data-stu-id="99297-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="99297-137">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="99297-137">TAPI version</span></span><br/> | <span data-ttu-id="99297-138">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="99297-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="99297-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99297-139">Header</span></span><br/>       | <dl> <span data-ttu-id="99297-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="99297-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99297-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="99297-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99297-142">**\_cerrar teléfono**</span><span class="sxs-lookup"><span data-stu-id="99297-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="99297-143">**Estado del teléfono \_**</span><span class="sxs-lookup"><span data-stu-id="99297-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="99297-144">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="99297-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="99297-145">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="99297-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




