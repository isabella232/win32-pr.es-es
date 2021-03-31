---
title: Método INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: Lo usa el cliente de cumplimiento para recuperar una solicitud de SoH para una conexión determinada.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996183"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="b2043-106">INapEnforcementClientBinding:: GetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="b2043-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="b2043-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2043-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b2043-108">El cliente de cumplimiento usa el método **INapEnforcementClientBinding:: GetSoHRequest** para recuperar una solicitud de SOH para una conexión determinada.</span><span class="sxs-lookup"><span data-stu-id="b2043-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2043-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2043-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="b2043-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2043-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2043-111">*conexión* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b2043-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2043-112">Puntero COM a una interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="b2043-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="b2043-113">El NapAgent no conserva las referencias al objeto asociado a esta interfaz una vez que se completa el método.</span><span class="sxs-lookup"><span data-stu-id="b2043-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="b2043-114">*retriggerHint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2043-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2043-115">Un puntero a un **booleano** que indica si se debe volver a desencadenar la conexión.</span><span class="sxs-lookup"><span data-stu-id="b2043-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="b2043-116">Es **true** si [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ha cambiado desde la última vez que se llamó a esta función o si [**ProbationTime**](nap-datatypes.md) ha expirado.</span><span class="sxs-lookup"><span data-stu-id="b2043-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="b2043-117">De lo contrario, se devuelve **false** .</span><span class="sxs-lookup"><span data-stu-id="b2043-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2043-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2043-118">Return value</span></span>

<span data-ttu-id="b2043-119">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="b2043-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b2043-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b2043-120">Return code</span></span>                                                                                             | <span data-ttu-id="b2043-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2043-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2043-122"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="b2043-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2043-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b2043-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="b2043-125">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b2043-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b2043-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="b2043-127">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b2043-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b2043-128"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="b2043-129">El exigidor no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="b2043-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b2043-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2043-130">Remarks</span></span>

<span data-ttu-id="b2043-131">NapAgent establece [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) en el objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="b2043-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="b2043-132">Si un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estaba pendiente en esta conexión, se descartará y se notificará a los Sha de **SoHRequests** huérfanos.</span><span class="sxs-lookup"><span data-stu-id="b2043-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="b2043-133">El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="b2043-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2043-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2043-134">Requirements</span></span>



| <span data-ttu-id="b2043-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2043-135">Requirement</span></span> | <span data-ttu-id="b2043-136">Value</span><span class="sxs-lookup"><span data-stu-id="b2043-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2043-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2043-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b2043-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b2043-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2043-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2043-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b2043-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2043-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2043-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2043-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2043-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2043-143">IDL</span><span class="sxs-lookup"><span data-stu-id="b2043-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2043-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b2043-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2043-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2043-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2043-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b2043-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2043-147">See also</span></span>

<dl> <span data-ttu-id="b2043-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b2043-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b2043-149">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="b2043-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





