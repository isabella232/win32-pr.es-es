---
title: Método INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Permite que los validadores de mantenimiento del sistema (SHV) establezcan el SoHResponse que se va a enviar a su homólogo del agente de mantenimiento del sistema (SHA) en el lado cliente.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Método SetSoHResponse NAP
- Método SetSoHResponse NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422511"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="143a3-106">INapSystemHealthValidationRequest:: SetSoHResponse (método)</span><span class="sxs-lookup"><span data-stu-id="143a3-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="143a3-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="143a3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="143a3-108">El método **INapSystemHealthValidationRequest:: SetSoHResponse** permite que los validadores de mantenimiento del sistema (SHV) establezcan el [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) que se enviará a su homólogo del agente de mantenimiento del sistema (SHA) en el lado del cliente.</span><span class="sxs-lookup"><span data-stu-id="143a3-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="143a3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="143a3-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="143a3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="143a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="143a3-111">*sohResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="143a3-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="143a3-112">Puntero a una estructura [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="143a3-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="143a3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="143a3-113">Return value</span></span>

<span data-ttu-id="143a3-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="143a3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="143a3-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="143a3-115">Return code</span></span>                                                                                     | <span data-ttu-id="143a3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="143a3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="143a3-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="143a3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="143a3-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="143a3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="143a3-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="143a3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="143a3-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="143a3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="143a3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="143a3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="143a3-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="143a3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="143a3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="143a3-123">Requirements</span></span>



| <span data-ttu-id="143a3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="143a3-124">Requirement</span></span> | <span data-ttu-id="143a3-125">Value</span><span class="sxs-lookup"><span data-stu-id="143a3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143a3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="143a3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="143a3-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="143a3-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="143a3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="143a3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="143a3-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="143a3-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="143a3-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="143a3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="143a3-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="143a3-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="143a3-132">IDL</span><span class="sxs-lookup"><span data-stu-id="143a3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="143a3-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="143a3-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="143a3-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="143a3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="143a3-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="143a3-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="143a3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="143a3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143a3-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="143a3-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





