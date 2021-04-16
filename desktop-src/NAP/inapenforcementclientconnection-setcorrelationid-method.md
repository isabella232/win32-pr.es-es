---
title: Método INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient. h)
description: Establece el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Método SetCorrelationId NAP
- Método SetCorrelationId NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533963"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="4cf75-106">INapEnforcementClientConnection:: SetCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="4cf75-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="4cf75-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="4cf75-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4cf75-108">El método **INapEnforcementClientConnection:: SetCorrelationId** establece el identificador usado para correlacionar las solicitudes de SOH y las respuestas de SOH.</span><span class="sxs-lookup"><span data-stu-id="4cf75-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf75-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cf75-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="4cf75-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cf75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf75-111">*CorrelationId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4cf75-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf75-112">Una estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica un intercambio de SOH específico.</span><span class="sxs-lookup"><span data-stu-id="4cf75-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf75-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cf75-113">Return value</span></span>

<span data-ttu-id="4cf75-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="4cf75-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4cf75-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4cf75-115">Return code</span></span>                                                                                     | <span data-ttu-id="4cf75-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cf75-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cf75-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf75-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4cf75-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="4cf75-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4cf75-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf75-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4cf75-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4cf75-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4cf75-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf75-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4cf75-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4cf75-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cf75-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cf75-123">Remarks</span></span>

<span data-ttu-id="4cf75-124">El NapAgent establece el identificador de correlación y se basa en el identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="4cf75-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="4cf75-125">Este identificador se usa para correlacionar las solicitudes y las respuestas, es decir, describe de forma única un intercambio de SoH y siempre contiene el ID. del SoH más reciente establecido en el objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="4cf75-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="4cf75-126">Cuando se recibe un SoH-Response, el NapAgent primero asegura que los identificadores coincidan; Si no es así, se devuelve un error y el forzado debe quitar el paquete.</span><span class="sxs-lookup"><span data-stu-id="4cf75-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="4cf75-127">Consulte [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4cf75-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf75-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cf75-128">Requirements</span></span>



| <span data-ttu-id="4cf75-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf75-129">Requirement</span></span> | <span data-ttu-id="4cf75-130">Value</span><span class="sxs-lookup"><span data-stu-id="4cf75-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf75-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cf75-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf75-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4cf75-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4cf75-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cf75-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf75-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4cf75-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4cf75-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cf75-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf75-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf75-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cf75-137">IDL</span><span class="sxs-lookup"><span data-stu-id="4cf75-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4cf75-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cf75-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4cf75-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4cf75-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf75-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf75-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4cf75-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cf75-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf75-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="4cf75-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





