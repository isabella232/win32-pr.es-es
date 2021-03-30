---
title: Interfaz INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Se usan para admitir validadores de mantenimiento del sistema definidos por el desarrollador de la aplicación.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- Interfaz INapSystemHealthValidationRequest NAP
- Interfaz INapSystemHealthValidationRequest NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803800"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="60895-105">Interfaz INapSystemHealthValidationRequest</span><span class="sxs-lookup"><span data-stu-id="60895-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="60895-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="60895-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="60895-107">La interfaz **INapSystemHealthValidationRequest** proporciona métodos que se usan para admitir los validadores de mantenimiento del sistema definidos por el desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60895-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="60895-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="60895-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="60895-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="60895-109">Members</span></span>

<span data-ttu-id="60895-110">La interfaz **INapSystemHealthValidationRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="60895-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="60895-111">**INapSystemHealthValidationRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60895-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="60895-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="60895-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60895-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="60895-113">Methods</span></span>

<span data-ttu-id="60895-114">La interfaz **INapSystemHealthValidationRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="60895-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="60895-115">Método</span><span class="sxs-lookup"><span data-stu-id="60895-115">Method</span></span>                                                                                                                               | <span data-ttu-id="60895-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="60895-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60895-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="60895-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="60895-118">Lo usan los validadores para recuperar el identificador de correlación.</span><span class="sxs-lookup"><span data-stu-id="60895-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="60895-119">Después, el validador debe registrar esta información.</span><span class="sxs-lookup"><span data-stu-id="60895-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="60895-120">**INapSystemHealthValidationRequest::GetMachineName**</span><span class="sxs-lookup"><span data-stu-id="60895-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="60895-121">Lo usan los validadores para recuperar el nombre de la máquina.</span><span class="sxs-lookup"><span data-stu-id="60895-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="60895-122">Después, el validador debe registrar esta información.</span><span class="sxs-lookup"><span data-stu-id="60895-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="60895-123">**INapSystemHealthValidationRequest::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="60895-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="60895-124">Permite que NapServer recupere información de estado.</span><span class="sxs-lookup"><span data-stu-id="60895-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="60895-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="60895-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="60895-126">Permite que los validadores recuperen y validen la información de SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="60895-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="60895-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="60895-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="60895-128">Obtiene el objeto SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="60895-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="60895-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="60895-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="60895-130">Lo usan los validadores para recuperar un identificador único de Exchange.</span><span class="sxs-lookup"><span data-stu-id="60895-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="60895-131">Después, el validador debe registrar esta información.</span><span class="sxs-lookup"><span data-stu-id="60895-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="60895-132">**INapSystemHealthValidationRequest::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="60895-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="60895-133">Permite que NapServer almacene información de estado.</span><span class="sxs-lookup"><span data-stu-id="60895-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="60895-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="60895-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="60895-135">Permite a los validadores establecer SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="60895-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="60895-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60895-136">Requirements</span></span>



| <span data-ttu-id="60895-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="60895-137">Requirement</span></span> | <span data-ttu-id="60895-138">Value</span><span class="sxs-lookup"><span data-stu-id="60895-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60895-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60895-139">Minimum supported client</span></span><br/> | <span data-ttu-id="60895-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60895-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="60895-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60895-141">Minimum supported server</span></span><br/> | <span data-ttu-id="60895-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="60895-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60895-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60895-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="60895-144"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="60895-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="60895-145">IDL</span><span class="sxs-lookup"><span data-stu-id="60895-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60895-146"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60895-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="60895-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60895-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60895-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60895-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="60895-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="60895-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60895-150">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="60895-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="60895-151">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="60895-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

