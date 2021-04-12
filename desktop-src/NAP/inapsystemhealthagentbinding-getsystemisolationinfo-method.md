---
title: Método INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent. h)
description: Los Sha llaman para determinar el estado de aislamiento del sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Método GetSystemIsolationInfo NAP
- Método GetSystemIsolationInfo NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492940"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="fe624-106">INapSystemHealthAgentBinding:: GetSystemIsolationInfo (método)</span><span class="sxs-lookup"><span data-stu-id="fe624-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="fe624-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe624-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fe624-108">Sha llama al método **INapSystemHealthAgentBinding:: GetSystemIsolationInfo** para determinar el estado de aislamiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="fe624-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="fe624-109">Use [**INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) para determinar el estado de aislamiento extendido del sistema.</span><span class="sxs-lookup"><span data-stu-id="fe624-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe624-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe624-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="fe624-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe624-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe624-112">*isolationInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fe624-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe624-113">Un puntero a un puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene el estado de aislamiento del sistema para las conexiones conocidas.</span><span class="sxs-lookup"><span data-stu-id="fe624-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="fe624-114">*isolationInfoindicates* si el sistema está en un estado de acceso restringido, período de prueba o acceso sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="fe624-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="fe624-115">*unknownConnections* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fe624-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe624-116">Un puntero a un valor **booleano** que es **true** si alguna conexión tiene un estado desconocido y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fe624-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe624-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe624-117">Return value</span></span>

<span data-ttu-id="fe624-118">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="fe624-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fe624-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fe624-119">Return code</span></span>                                                                                             | <span data-ttu-id="fe624-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe624-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe624-121"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="fe624-122">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe624-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="fe624-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="fe624-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fe624-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="fe624-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="fe624-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fe624-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="fe624-127"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="fe624-128">SHA no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="fe624-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="fe624-129"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="fe624-130">NapAgent se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="fe624-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="fe624-131">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="fe624-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe624-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe624-132">Remarks</span></span>

<span data-ttu-id="fe624-133">SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="fe624-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe624-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe624-134">Requirements</span></span>



| <span data-ttu-id="fe624-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe624-135">Requirement</span></span> | <span data-ttu-id="fe624-136">Value</span><span class="sxs-lookup"><span data-stu-id="fe624-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe624-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe624-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fe624-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fe624-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe624-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe624-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fe624-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe624-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe624-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe624-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe624-142"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe624-143">IDL</span><span class="sxs-lookup"><span data-stu-id="fe624-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe624-144"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="fe624-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe624-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe624-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe624-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fe624-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe624-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe624-148">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="fe624-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





