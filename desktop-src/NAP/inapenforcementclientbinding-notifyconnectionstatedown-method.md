---
title: Método INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: Se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha dejado de funcionar.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Método NotifyConnectionStateDown NAP
- Método NotifyConnectionStateDown NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método NotifyConnectionStateDown
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535608"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="2a55a-106">INapEnforcementClientBinding:: NotifyConnectionStateDown (método)</span><span class="sxs-lookup"><span data-stu-id="2a55a-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="2a55a-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2a55a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2a55a-108">El método **INapEnforcementClientBinding:: NotifyConnectionStateDown** se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha dejado de funcionar.</span><span class="sxs-lookup"><span data-stu-id="2a55a-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a55a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a55a-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="2a55a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a55a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a55a-111">*downCxn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a55a-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a55a-112">Puntero COM a la interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la conexión hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="2a55a-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a55a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a55a-113">Return value</span></span>

<span data-ttu-id="2a55a-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="2a55a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2a55a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a55a-115">Return code</span></span>                                                                                             | <span data-ttu-id="2a55a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a55a-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a55a-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="2a55a-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a55a-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="2a55a-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="2a55a-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="2a55a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2a55a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="2a55a-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2a55a-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a55a-123"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="2a55a-124">El exigidor no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="2a55a-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="2a55a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a55a-125">Remarks</span></span>

<span data-ttu-id="2a55a-126">Cuando cualquiera de las conexiones establecidas por un cliente de cumplimiento se desactive, el cliente de cumplimiento debe quitar la conexión de su lista activa e informar a NapAgent mediante este método.</span><span class="sxs-lookup"><span data-stu-id="2a55a-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="2a55a-127">En cuanto se devuelve esta llamada, el objeto de conexión se puede liberar y liberar.</span><span class="sxs-lookup"><span data-stu-id="2a55a-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="2a55a-128">NapAgent no conservará las referencias al objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="2a55a-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="2a55a-129">Como resultado de esta notificación, el NapAgent actualiza su estado NAP del sistema según corresponda.</span><span class="sxs-lookup"><span data-stu-id="2a55a-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="2a55a-130">El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="2a55a-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a55a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a55a-131">Requirements</span></span>



| <span data-ttu-id="2a55a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a55a-132">Requirement</span></span> | <span data-ttu-id="2a55a-133">Value</span><span class="sxs-lookup"><span data-stu-id="2a55a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a55a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a55a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2a55a-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a55a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2a55a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a55a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2a55a-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a55a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2a55a-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a55a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a55a-139"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a55a-140">IDL</span><span class="sxs-lookup"><span data-stu-id="2a55a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a55a-141"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a55a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a55a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a55a-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2a55a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a55a-144">See also</span></span>

<dl> <span data-ttu-id="2a55a-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2a55a-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="2a55a-146">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="2a55a-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





