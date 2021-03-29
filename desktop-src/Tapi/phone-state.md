---
description: TAPI envía el \_ mensaje de estado de teléfono a una aplicación cada vez que cambia el estado de un dispositivo de teléfono.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Mensaje de PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678905"
---
# <a name="phone_state-message"></a><span data-ttu-id="7f49b-103">Mensaje de estado de teléfono \_</span><span class="sxs-lookup"><span data-stu-id="7f49b-103">PHONE\_STATE message</span></span>

<span data-ttu-id="7f49b-104">TAPI envía el mensaje de **\_ Estado de teléfono** a una aplicación cada vez que cambia el estado de un dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="7f49b-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7f49b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f49b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f49b-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="7f49b-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="7f49b-107">Identificador del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="7f49b-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="7f49b-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7f49b-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7f49b-109">Instancia de devolución de llamada de la aplicación que se proporciona al abrir el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="7f49b-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="7f49b-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7f49b-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7f49b-111">Estado del teléfono que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7f49b-111">The phone state that has changed.</span></span> <span data-ttu-id="7f49b-112">Este parámetro utiliza una de las [**\_ constantes de PHONESTATE**](phonestate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7f49b-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f49b-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7f49b-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7f49b-114">Información dependiente del estado del teléfono que detalla el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="7f49b-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="7f49b-115">Este parámetro no se utiliza si se establecen varias marcas en *dwParam1*, porque han cambiado varios elementos de estado.</span><span class="sxs-lookup"><span data-stu-id="7f49b-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="7f49b-116">La aplicación debe invocar [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) para obtener un conjunto de información completo.</span><span class="sxs-lookup"><span data-stu-id="7f49b-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="7f49b-117">Si *dwParam1* es PHONESTATE \_ Owner, *dwParam2* contiene el nuevo número de propietarios.</span><span class="sxs-lookup"><span data-stu-id="7f49b-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="7f49b-118">Si *dwParam1* es PHONESTATE \_ supervisa, *dwParam2* contiene el nuevo número de monitores.</span><span class="sxs-lookup"><span data-stu-id="7f49b-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="7f49b-119">Si *dwParam1* es PHONESTATE \_ LAMP, *dwParam2* contiene el identificador de botón o lámpara de la lámpara que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7f49b-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="7f49b-120">Si *dwParam1* es PHONESTATE \_ RINGMODE, *dwParam2* contiene el nuevo modo de anillo.</span><span class="sxs-lookup"><span data-stu-id="7f49b-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="7f49b-121">Si *dwParam1* es PHONESTATE \_ auricular, altavoces o auriculares, *dwParam2* contiene el nuevo modo conmutador de ese dispositivo conmutador.</span><span class="sxs-lookup"><span data-stu-id="7f49b-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="7f49b-122">Este parámetro utiliza una de las [**\_ constantes de PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7f49b-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f49b-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7f49b-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7f49b-124">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="7f49b-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f49b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f49b-125">Return value</span></span>

<span data-ttu-id="7f49b-126">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7f49b-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f49b-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f49b-127">Remarks</span></span>

<span data-ttu-id="7f49b-128">El envío del mensaje de **\_ Estado telefónico** a la aplicación se puede controlar y consultar mediante [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) y [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="7f49b-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="7f49b-129">De forma predeterminada, este mensaje está deshabilitado para todos los cambios de estado excepto PHONESTATE \_ reinit, que no se puede deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="7f49b-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="7f49b-130">Este mensaje se envía a todas las aplicaciones que tienen un identificador al teléfono, incluidos los que llaman a [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con el parámetro *DWPRIVILEGES* establecido en PHONEPRIVILEGE \_ Owner o \_ PHONEPRIVILEGE monitor.</span><span class="sxs-lookup"><span data-stu-id="7f49b-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="7f49b-131">Se envía un mensaje de **\_ Estado de teléfono** con una indicación de propietarios y/o monitores a las aplicaciones que ya tienen un identificador para el teléfono.</span><span class="sxs-lookup"><span data-stu-id="7f49b-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="7f49b-132">Esto puede ser el resultado de que otra aplicación cambie la propiedad o supervise el dispositivo telefónico con [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) o [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span><span class="sxs-lookup"><span data-stu-id="7f49b-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f49b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f49b-133">Requirements</span></span>



| <span data-ttu-id="7f49b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f49b-134">Requirement</span></span> | <span data-ttu-id="7f49b-135">Value</span><span class="sxs-lookup"><span data-stu-id="7f49b-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7f49b-136">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7f49b-136">TAPI version</span></span><br/> | <span data-ttu-id="7f49b-137">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7f49b-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7f49b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f49b-138">Header</span></span><br/>       | <dl> <span data-ttu-id="7f49b-139"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f49b-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f49b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f49b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f49b-141">**\_cerrar teléfono**</span><span class="sxs-lookup"><span data-stu-id="7f49b-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="7f49b-142">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="7f49b-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="7f49b-143">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="7f49b-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="7f49b-144">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="7f49b-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="7f49b-145">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="7f49b-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="7f49b-146">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="7f49b-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="7f49b-147">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="7f49b-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="7f49b-148">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="7f49b-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="7f49b-149">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="7f49b-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="7f49b-150">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="7f49b-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="7f49b-151">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="7f49b-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




