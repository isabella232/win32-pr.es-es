---
title: Método INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: El NapAgent llama a para consultar la solicitud de SoH del agente de mantenimiento del sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422402"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="3c3dd-106">INapSystemHealthAgentCallback:: GetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="3c3dd-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="3c3dd-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3c3dd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3c3dd-108">El NapAgent llama al método **INapSystemHealthAgentCallback:: GetSoHRequest** para consultar la solicitud de SOH del agente de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3dd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c3dd-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="3c3dd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c3dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3dd-111">*solicitud* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c3dd-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3dd-112">Puntero COM a un objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica el objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3dd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c3dd-113">Return value</span></span>



| <span data-ttu-id="3c3dd-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3c3dd-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="3c3dd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c3dd-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c3dd-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3c3dd-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="3c3dd-117">Indica que se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="3c3dd-118"><dt>**HRESULT \_ de \_ Win32 ( \_ servidor RPC \_ \_ no disponible)**</dt></span><span class="sxs-lookup"><span data-stu-id="3c3dd-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="3c3dd-119">Si la implementación devuelve este código, NapAgent quita el SHA de la lista Bound-SHA y vacía su entrada de caché.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="3c3dd-120">Cuando la implementación devuelve cualquier valor devuelto (excepto **HRESULT \_ de \_ Win32 ( \_ servidor RPC \_ \_ no disponible)**), el sistema NAP crea y devuelve un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al SHV correspondiente con los siguientes valores y tipos de atributo:</span><span class="sxs-lookup"><span data-stu-id="3c3dd-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="3c3dd-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="3c3dd-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="3c3dd-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="3c3dd-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="3c3dd-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <> código de error</span><span class="sxs-lookup"><span data-stu-id="3c3dd-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="3c3dd-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c3dd-124">Remarks</span></span>

<span data-ttu-id="3c3dd-125">Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="3c3dd-126">Este método debe procesar la solicitud y volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="3c3dd-127">Retrasar la devolución de este método afecta negativamente al rendimiento y la capacidad de respuesta del sistema, y puede provocar que se agote el tiempo de espera de otras partes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="3c3dd-128">La supervisión del estado de mantenimiento no debe realizarse como parte de esta llamada, especialmente si se trata de un proceso intensivo y tarda mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="3c3dd-129">La supervisión del estado de mantenimiento y el cálculo de SoH deben realizarse en un subproceso o servicio independiente.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="3c3dd-130">La única función de este método debe ser establecer el SoH de SHA y devolver.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="3c3dd-131">Si el SHA tarda mucho tiempo en generar un SoH, se debe devolver el SoH almacenado en caché a NapAgent.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="3c3dd-132">Si no hay ningún SoH almacenado en caché para devolver, el SHA debe devolver inmediatamente un SoH con los siguientes valores y tipos de atributo:</span><span class="sxs-lookup"><span data-stu-id="3c3dd-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="3c3dd-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="3c3dd-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="3c3dd-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="3c3dd-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="3c3dd-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  NO se ha [ **\_ \_ \_ almacenado en caché el \_ SOH de NAP E**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="3c3dd-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="3c3dd-136">Cuando se ha generado el SoH, el SHA debe llamar a [**INapSystemHealthAgentBinding:: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para notificar al NapAgent el cambio de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="3c3dd-137">NapAgent llama a este método para consultar el SoHRequest del agente de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="3c3dd-138">SHA puede consultar el objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) pasado en busca de los parámetros que necesita para calcular el SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="3c3dd-139">SHA debe establecer el SoHRequest calculado en el objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="3c3dd-140">SHA no debe contener referencias al objeto de solicitud una vez completada esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="3c3dd-141">Cuando se llama a este método, si hay un SoH en la memoria caché de NapAgent, se establece en el objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="3c3dd-142">SHA puede consultarlo mediante **GetSoHRequest**.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="3c3dd-143">Si el SHA no establece un nuevo SoH, se usa el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="3c3dd-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="3c3dd-144">En el caso de los Sha sin enlazar que se registran con el sistema, el sistema NAP construye y envía un SoHRequest al SHV correspondiente con los siguientes valores y tipos de atributo:</span><span class="sxs-lookup"><span data-stu-id="3c3dd-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="3c3dd-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="3c3dd-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="3c3dd-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="3c3dd-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="3c3dd-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ no \_ inicializado**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="3c3dd-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3dd-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c3dd-148">Requirements</span></span>



| <span data-ttu-id="3c3dd-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c3dd-149">Requirement</span></span> | <span data-ttu-id="3c3dd-150">Value</span><span class="sxs-lookup"><span data-stu-id="3c3dd-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3dd-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c3dd-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3dd-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c3dd-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c3dd-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c3dd-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3dd-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c3dd-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c3dd-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c3dd-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c3dd-156"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3dd-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c3dd-157">IDL</span><span class="sxs-lookup"><span data-stu-id="3c3dd-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c3dd-158"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c3dd-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c3dd-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c3dd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3dd-160">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="3c3dd-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





