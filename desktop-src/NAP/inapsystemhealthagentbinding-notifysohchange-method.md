---
title: Método INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: Sha usa cuando cambia el SoH.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535332"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="c39cd-106">INapSystemHealthAgentBinding:: NotifySoHChange (método)</span><span class="sxs-lookup"><span data-stu-id="c39cd-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="c39cd-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c39cd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c39cd-108">Sha usa el método **INapSystemHealthAgentBinding:: NotifySoHChange** cuando su SOH cambia.</span><span class="sxs-lookup"><span data-stu-id="c39cd-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c39cd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c39cd-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="c39cd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c39cd-110">Parameters</span></span>

<span data-ttu-id="c39cd-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c39cd-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c39cd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c39cd-112">Return value</span></span>

<span data-ttu-id="c39cd-113">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="c39cd-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c39cd-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c39cd-114">Return code</span></span>                                                                                             | <span data-ttu-id="c39cd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c39cd-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c39cd-116"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="c39cd-117">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c39cd-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c39cd-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="c39cd-119">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c39cd-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="c39cd-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="c39cd-121">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c39cd-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c39cd-122"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="c39cd-123">SHA no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="c39cd-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="c39cd-124"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="c39cd-125">NapAgent se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="c39cd-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="c39cd-126">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="c39cd-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c39cd-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c39cd-127">Remarks</span></span>

<span data-ttu-id="c39cd-128">Los Sha no deben llamar a esta API speculatively, ya que se produce un intercambio de SoH en la conexión.</span><span class="sxs-lookup"><span data-stu-id="c39cd-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="c39cd-129">Las llamadas a esta API solo deben realizarse cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c39cd-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="c39cd-130">NapAgent no contiene este subproceso para procesar el cambio de SoH.</span><span class="sxs-lookup"><span data-stu-id="c39cd-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="c39cd-131">En su lugar, devuelve inmediatamente y procesa el cambio de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c39cd-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="c39cd-132">SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="c39cd-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c39cd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c39cd-133">Requirements</span></span>



| <span data-ttu-id="c39cd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c39cd-134">Requirement</span></span> | <span data-ttu-id="c39cd-135">Value</span><span class="sxs-lookup"><span data-stu-id="c39cd-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c39cd-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c39cd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c39cd-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c39cd-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c39cd-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c39cd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c39cd-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c39cd-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c39cd-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c39cd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c39cd-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c39cd-142">IDL</span><span class="sxs-lookup"><span data-stu-id="c39cd-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c39cd-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="c39cd-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c39cd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c39cd-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c39cd-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c39cd-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="c39cd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c39cd-147">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="c39cd-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





