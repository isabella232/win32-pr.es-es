---
title: Método Initialize INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Inicializa el agente de mantenimiento del sistema (SHA) y enlaza el SHA al servicio NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359676"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="d51c9-106">INapSystemHealthAgentBinding:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="d51c9-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="d51c9-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d51c9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d51c9-108">El método **INapSystemHealthAgentBinding:: Initialize** inicializa el agente de mantenimiento del sistema (SHA) y enlaza el Sha con el servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="d51c9-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="d51c9-109">Se debe llamar a este método antes de llamar a cualquier otro método en la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="d51c9-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51c9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d51c9-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="d51c9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d51c9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d51c9-112">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d51c9-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d51c9-113">Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del Sha que se está enlazando al servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="d51c9-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="d51c9-114">*devolución de llamada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d51c9-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d51c9-115">Puntero COM a una interfaz [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) que usa NapAgent para devolver una llamada al agente de mantenimiento con una notificación/proceso.</span><span class="sxs-lookup"><span data-stu-id="d51c9-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="d51c9-116">NapAgent contiene una referencia al objeto asociado a esta interfaz hasta que se llama a [**UnInitialize**](inapsystemhealthagentbinding-uninitialize-method.md) .</span><span class="sxs-lookup"><span data-stu-id="d51c9-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d51c9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d51c9-117">Return value</span></span>

<span data-ttu-id="d51c9-118">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="d51c9-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d51c9-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d51c9-119">Return code</span></span>                                                                                                | <span data-ttu-id="d51c9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d51c9-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d51c9-121"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="d51c9-122">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d51c9-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="d51c9-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="d51c9-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d51c9-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="d51c9-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="d51c9-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="d51c9-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="d51c9-127"><dt>**ERROR \_ ya \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="d51c9-128">Si se ha inicializado SHA previamente, se devuelve este error.</span><span class="sxs-lookup"><span data-stu-id="d51c9-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="d51c9-129"><dt>**NAP \_ E \_ no \_ registrado**</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="d51c9-130">Si el SHA no se ha registrado anteriormente, se devuelve este error.</span><span class="sxs-lookup"><span data-stu-id="d51c9-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="d51c9-131"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="d51c9-132">NapAgent se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="d51c9-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="d51c9-133">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="d51c9-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d51c9-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d51c9-134">Remarks</span></span>

<span data-ttu-id="d51c9-135">NapAgent no desencadena un intercambio de SoH como resultado de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="d51c9-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="d51c9-136">Un agente de mantenimiento del sistema debe llamar a [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para solicitar un intercambio de paquetes de SOH después de inicializarse con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="d51c9-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d51c9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d51c9-137">Requirements</span></span>



| <span data-ttu-id="d51c9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d51c9-138">Requirement</span></span> | <span data-ttu-id="d51c9-139">Value</span><span class="sxs-lookup"><span data-stu-id="d51c9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51c9-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d51c9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d51c9-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d51c9-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d51c9-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d51c9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d51c9-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d51c9-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d51c9-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d51c9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d51c9-145"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="d51c9-146">IDL</span><span class="sxs-lookup"><span data-stu-id="d51c9-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d51c9-147"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="d51c9-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d51c9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d51c9-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d51c9-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d51c9-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="d51c9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51c9-151">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="d51c9-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





