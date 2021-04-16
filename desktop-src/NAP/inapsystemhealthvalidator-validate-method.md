---
title: Método Validate de INapSystemHealthValidator (NapSystemHealthValidator. h)
description: El sistema NAP para validar el SoHRequest recibido de un cliente.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validar el método NAP
- Método Validate NAP, interfaz INapSystemHealthValidator
- Interfaz INapSystemHealthValidator NAP, método Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676696"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="c9e02-106">INapSystemHealthValidator:: Validate (método)</span><span class="sxs-lookup"><span data-stu-id="c9e02-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="c9e02-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c9e02-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c9e02-108">El método **INapSystemHealthValidator:: Validate** lo define el desarrollador de SHV y el sistema NAP lo llama para validar el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recibido de un cliente.</span><span class="sxs-lookup"><span data-stu-id="c9e02-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e02-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9e02-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="c9e02-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9e02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e02-111">*solicitud* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c9e02-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e02-112">Puntero COM a un objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que identifica el objeto de solicitud de validación.</span><span class="sxs-lookup"><span data-stu-id="c9e02-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="c9e02-113">*hintTimeOutInMsec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9e02-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e02-114">La duración, en milisegundos, del período de tiempo de espera de la comunicación.</span><span class="sxs-lookup"><span data-stu-id="c9e02-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="c9e02-115">El validador de mantenimiento del sistema (SHV) debe responder en este período de tiempo; de lo contrario, se quita la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9e02-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="c9e02-116">El tiempo de espera predeterminado para todos los SHV es de 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c9e02-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="c9e02-117">Si usa un valor distinto del predeterminado, se cambiará el tiempo de espera de todos los SHV registrados.</span><span class="sxs-lookup"><span data-stu-id="c9e02-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="c9e02-118">*devolución de llamada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9e02-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e02-119">Un puntero al objeto de devolución de llamada [**INapServerCallback**](inapservercallback.md).</span><span class="sxs-lookup"><span data-stu-id="c9e02-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="c9e02-120">Los SHV usan este puntero de devolución de llamada cuando devuelven **E \_ pendientes** de la llamada a **INapSystemHealthValidator:: Validate**.</span><span class="sxs-lookup"><span data-stu-id="c9e02-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="c9e02-121">Se utiliza para la validación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c9e02-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="c9e02-122">Se espera que los SHV respondan dentro del tiempo de *hintTimeOutInMsec* o, de lo contrario, se quitará la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9e02-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e02-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9e02-123">Return value</span></span>

<span data-ttu-id="c9e02-124">Si se devuelve cualquier otro código de error, el sistema asume que se ha producido un error de serverComponent y se ha realizado la asignación adecuada a Pass/Fail.</span><span class="sxs-lookup"><span data-stu-id="c9e02-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="c9e02-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c9e02-125">Return code</span></span>                                                                                                | <span data-ttu-id="c9e02-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9e02-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9e02-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e02-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c9e02-128">Indica que el validador ha establecido SoHResponse en el objeto ' request '.</span><span class="sxs-lookup"><span data-stu-id="c9e02-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="c9e02-129"><dt>**E \_ pendientes**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e02-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="c9e02-130">Indica que se llamará a alcomplete () en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="c9e02-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c9e02-131"><dt>**el \_ servidor RPC S \_ \_ no está disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e02-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="c9e02-132">Indica que el proceso de validador de mantenimiento del sistema (SHV) terminó sin que el NapServer realmente haya liberado una referencia a él.</span><span class="sxs-lookup"><span data-stu-id="c9e02-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="c9e02-133">NapServer intentará volver a crear una nueva referencia al SHV y volverá a ejecutar la llamada de validación una vez.</span><span class="sxs-lookup"><span data-stu-id="c9e02-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="c9e02-134">Si se produce un error en la creación del objeto o la validación que se ha vuelto a ejecutar, el SHV se quita de la lista de SHV cargados.</span><span class="sxs-lookup"><span data-stu-id="c9e02-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="c9e02-135">La única forma en que se puede recargar ahora este SHV es anular el registro y volver a registrar el SHV, o bien cuando se reinicie NapServer</span><span class="sxs-lookup"><span data-stu-id="c9e02-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9e02-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9e02-136">Remarks</span></span>

<span data-ttu-id="c9e02-137">Con el fin de admitir la detección de intrusiones, se pedirá a los SHV que validen el equipo cliente, independientemente de si el cliente envió un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado al SHV.</span><span class="sxs-lookup"><span data-stu-id="c9e02-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="c9e02-138">El SHV debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c9e02-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="c9e02-139">Recupere el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) de la *solicitud* mediante una llamada a la [**solicitud. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="c9e02-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="c9e02-140">Si el paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) es NULL:</span><span class="sxs-lookup"><span data-stu-id="c9e02-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="c9e02-141">Si el SHV es un sistema de detección de intrusiones, rellene un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con el [**código de error NAP**](nap-error-constants.md) adecuado en cuanto a la razón por la que el equipo cliente es malintencionado.</span><span class="sxs-lookup"><span data-stu-id="c9e02-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="c9e02-142">Todos los demás SHV deben rellenar un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con un código de error [**NAP \_ E \_ Missing \_ SOH**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c9e02-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="c9e02-143">Si *napSystemGenerated* es **true** desde la llamada a la [**solicitud. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), el SHV debería esperar un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) con los 3 TLVs siguientes: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="c9e02-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="c9e02-144">Este **SoHRequest** lo genera NapAgent en nombre del agente de mantenimiento del sistema (SHA), ya que se produjo un error al recuperar un paquete de solicitud del Sha.</span><span class="sxs-lookup"><span data-stu-id="c9e02-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="c9e02-145">Valide el paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="c9e02-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="c9e02-146">Si el formato de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) es incorrecto, construya un paquete **SoHResponse** con código de error [**NAP \_ E \_ \_ paquete no válido**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c9e02-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="c9e02-147">Si el SHV solo usa información almacenada en caché para validar el paquete de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (es decir, no se realiza ninguna e/s), puede construir el **SoHResponse**, establecerlo en el objeto en la *solicitud* y devolver **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c9e02-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="c9e02-148">Si el SHV está realizando e/s para comunicarse con los servidores back-end para validar el estado del cliente, debe poner en cola la e/s y devolver esta función con **E \_ pendiente**.</span><span class="sxs-lookup"><span data-stu-id="c9e02-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="c9e02-149">En este caso, el SHV debe llamar a [**callback. Alcompletar ()**](inapservercallback-oncomplete-method.md) en un subproceso independiente dentro del período de tiempo de espera, *hintTimeOutInMsec*.</span><span class="sxs-lookup"><span data-stu-id="c9e02-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="c9e02-150">De lo contrario, se quitará la respuesta de SHV.</span><span class="sxs-lookup"><span data-stu-id="c9e02-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="c9e02-151">No devuelva ningún otro error distinto de los enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c9e02-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="c9e02-152">Si el SHV devuelve cualquier otro código de error (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="c9e02-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="c9e02-153">error del sistema), se descartará el paquete.</span><span class="sxs-lookup"><span data-stu-id="c9e02-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="c9e02-154">Un SHV debe devolver un TLV de **sohAttributeTypeComplianceResultCodes** o **SohAttributeTypeFailureCategory** en su [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="c9e02-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="c9e02-155">[**TLV de sohAttributeTypeComplianceResultCodes**](sohattributetype-enum.md): Si el SHV podría validar el estado del cliente (es decir, correcto o incorrecto), se devuelve este TLV.</span><span class="sxs-lookup"><span data-stu-id="c9e02-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="c9e02-156">[**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md): si se produjo algún error de componente o de comunicación en el cliente o servidor, debe indicarse mediante este TLV.</span><span class="sxs-lookup"><span data-stu-id="c9e02-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="c9e02-157">Este TLV se asignará a un estado correcto o incorrecto en función de la configuración de SHV.</span><span class="sxs-lookup"><span data-stu-id="c9e02-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="c9e02-158">Para obtener más información, vea la interfaz [**INapServerManagement**](inapservermanagement.md) y la estructura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="c9e02-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="c9e02-159">El SHV no debe contener referencias a *request* o *callback* una vez que se complete la llamada asyncronous.</span><span class="sxs-lookup"><span data-stu-id="c9e02-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e02-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9e02-160">Requirements</span></span>



| <span data-ttu-id="c9e02-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9e02-161">Requirement</span></span> | <span data-ttu-id="c9e02-162">Value</span><span class="sxs-lookup"><span data-stu-id="c9e02-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e02-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9e02-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c9e02-164">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c9e02-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="c9e02-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9e02-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c9e02-166">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9e02-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9e02-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9e02-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9e02-168"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9e02-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9e02-169">IDL</span><span class="sxs-lookup"><span data-stu-id="c9e02-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9e02-170"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9e02-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9e02-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9e02-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e02-172">**INapSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="c9e02-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





