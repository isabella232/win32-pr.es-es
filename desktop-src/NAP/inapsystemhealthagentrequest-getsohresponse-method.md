---
title: Método INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: Lo usa el agente de mantenimiento para recuperar su BLOB de SoHResponse cuando NapAgent llama a INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150100"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="3c441-106">INapSystemHealthAgentRequest:: GetSoHResponse (método)</span><span class="sxs-lookup"><span data-stu-id="3c441-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="3c441-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3c441-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3c441-108">El agente de mantenimiento usa el método **INapSystemHealthAgentRequest:: GetSoHResponse** para recuperar su BLOB de SoHResponse cuando el NapAgent llama a [**INapSystemHealthAgentCallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span><span class="sxs-lookup"><span data-stu-id="3c441-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c441-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c441-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="3c441-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c441-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c441-111">*sohResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c441-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c441-112">Un puntero a un puntero a un paquete [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="3c441-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="3c441-113">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c441-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c441-114">Un puntero a una marca que habilita la corrección del SHA si se establece el bit [**shaFixup**](nap-type-constants.md) ; de lo contrario, se deshabilita la corrección.</span><span class="sxs-lookup"><span data-stu-id="3c441-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="3c441-115">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="3c441-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="3c441-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3c441-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="3c441-117"><dt>**shaFixup**</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="3c441-118">Se espera que SHA realice la corrección basada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c441-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="3c441-119">Si no se establece esta marca, SHA no debe realizar ninguna corrección, aunque el [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indica que está en mal estado.</span><span class="sxs-lookup"><span data-stu-id="3c441-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c441-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c441-120">Return value</span></span>

<span data-ttu-id="3c441-121">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="3c441-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3c441-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3c441-122">Return code</span></span>                                                                                     | <span data-ttu-id="3c441-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c441-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c441-124"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3c441-125">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c441-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3c441-126"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3c441-127">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="3c441-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3c441-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3c441-129">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3c441-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3c441-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c441-130">Requirements</span></span>



| <span data-ttu-id="3c441-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c441-131">Requirement</span></span> | <span data-ttu-id="3c441-132">Value</span><span class="sxs-lookup"><span data-stu-id="3c441-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c441-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c441-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3c441-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c441-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c441-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c441-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3c441-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c441-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c441-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c441-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c441-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c441-139">IDL</span><span class="sxs-lookup"><span data-stu-id="3c441-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c441-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="3c441-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c441-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c441-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c441-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="3c441-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c441-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c441-144">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="3c441-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





