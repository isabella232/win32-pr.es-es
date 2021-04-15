---
title: Método INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: Los Sha llaman para determinar el estado de aislamiento del sistema y el estado de aislamiento extendido.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interfaz INapSystemHealthAgentBinding2
- Interfaz INapSystemHealthAgentBinding2 NAP, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534318"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="e4c8a-106">INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx (método)</span><span class="sxs-lookup"><span data-stu-id="e4c8a-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="e4c8a-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4c8a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e4c8a-108">Sha llama al método **INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx** para determinar el estado de aislamiento del sistema y el estado de aislamiento extendido.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="e4c8a-109">Use [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) para determinar solo el estado de aislamiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e4c8a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4c8a-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="e4c8a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4c8a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c8a-112">*isolationInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e4c8a-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c8a-113">Un puntero a un puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene el estado de aislamiento extendido del sistema para las conexiones conocidas.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="e4c8a-114">*isolationInfo* indica si el sistema está en un estado de acceso restringido, período de prueba o acceso no restringido, así como información de [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .</span><span class="sxs-lookup"><span data-stu-id="e4c8a-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="e4c8a-115">*unknownConnections* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e4c8a-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c8a-116">Un puntero a un valor **booleano** que es **true** si alguna conexión tiene un estado desconocido y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c8a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4c8a-117">Return value</span></span>

<span data-ttu-id="e4c8a-118">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e4c8a-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e4c8a-119">Return code</span></span>                                                                                             | <span data-ttu-id="e4c8a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4c8a-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4c8a-121"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="e4c8a-122">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e4c8a-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="e4c8a-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e4c8a-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="e4c8a-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e4c8a-127"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="e4c8a-128">SHA no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="e4c8a-129"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="e4c8a-130">NapAgent se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="e4c8a-131">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4c8a-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4c8a-132">Remarks</span></span>

<span data-ttu-id="e4c8a-133">SHA debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando a [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="e4c8a-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="e4c8a-134">SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="e4c8a-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c8a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4c8a-135">Requirements</span></span>



| <span data-ttu-id="e4c8a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c8a-136">Requirement</span></span> | <span data-ttu-id="e4c8a-137">Value</span><span class="sxs-lookup"><span data-stu-id="e4c8a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c8a-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4c8a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c8a-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4c8a-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4c8a-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4c8a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c8a-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4c8a-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4c8a-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4c8a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c8a-143"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4c8a-144">IDL</span><span class="sxs-lookup"><span data-stu-id="e4c8a-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4c8a-145"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4c8a-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4c8a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c8a-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c8a-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e4c8a-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4c8a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c8a-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="e4c8a-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





