---
title: Método INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: Lo utilizan los agentes de mantenimiento para escribir su solicitud de SoH resultante de la llamada a INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651392"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="bbb4e-106">INapSystemHealthAgentRequest:: SetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="bbb4e-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="bbb4e-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bbb4e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bbb4e-108">Los agentes de mantenimiento usan el método **INapSystemHealthAgentRequest:: SetSoHRequest** para escribir su solicitud de SOH resultante de la llamada a [**INapSystemHealthAgentCallback:: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="bbb4e-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb4e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbb4e-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="bbb4e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbb4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbb4e-111">*sohRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bbb4e-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb4e-112">Un puntero a un paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="bbb4e-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="bbb4e-113">*cacheSohForLaterUse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bbb4e-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb4e-114">Valor **booleano** que es **true** si NapAgent debe almacenar en caché el [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bbb4e-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbb4e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbb4e-115">Return value</span></span>

<span data-ttu-id="bbb4e-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="bbb4e-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bbb4e-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bbb4e-117">Return code</span></span>                                                                                     | <span data-ttu-id="bbb4e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbb4e-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbb4e-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="bbb4e-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bbb4e-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="bbb4e-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bbb4e-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bbb4e-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bbb4e-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="bbb4e-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bbb4e-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bbb4e-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bbb4e-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bbb4e-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bbb4e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbb4e-125">Requirements</span></span>



| <span data-ttu-id="bbb4e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbb4e-126">Requirement</span></span> | <span data-ttu-id="bbb4e-127">Value</span><span class="sxs-lookup"><span data-stu-id="bbb4e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb4e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbb4e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bbb4e-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bbb4e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bbb4e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbb4e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bbb4e-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbb4e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bbb4e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbb4e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbb4e-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbb4e-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbb4e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="bbb4e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbb4e-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbb4e-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbb4e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbb4e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbb4e-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbb4e-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="bbb4e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbb4e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb4e-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="bbb4e-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





