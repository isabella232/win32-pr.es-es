---
title: Método INapEnforcementClientConnection GetCorrelationId (NapEnforcementClient. h)
description: Obtiene el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- Método GetCorrelationId NAP
- Método GetCorrelationId NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82572cc499a61d453a70c47391e48f2004dca24d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079767"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a><span data-ttu-id="b3364-106">INapEnforcementClientConnection:: GetCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="b3364-106">INapEnforcementClientConnection::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="b3364-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3364-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b3364-108">El método **INapEnforcementClientConnection:: GetCorrelationId** obtiene el identificador usado para correlacionar las solicitudes de SOH y las respuestas de SOH.</span><span class="sxs-lookup"><span data-stu-id="b3364-108">The **INapEnforcementClientConnection::GetCorrelationId** method gets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3364-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3364-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="b3364-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3364-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3364-111">*CorrelationId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3364-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3364-112">Una estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica este intercambio de SOH.</span><span class="sxs-lookup"><span data-stu-id="b3364-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3364-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3364-113">Return value</span></span>

<span data-ttu-id="b3364-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="b3364-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b3364-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b3364-115">Return code</span></span>                                                                                     | <span data-ttu-id="b3364-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3364-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3364-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="b3364-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b3364-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3364-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b3364-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b3364-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b3364-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b3364-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b3364-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b3364-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b3364-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b3364-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3364-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3364-123">Remarks</span></span>

<span data-ttu-id="b3364-124">El NapAgent establece el identificador de correlación y se basa en el identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="b3364-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="b3364-125">Este identificador se usa para correlacionar las solicitudes y las respuestas, es decir, describe de forma única un intercambio de SoH y siempre contiene el ID. del SoH más reciente establecido en el objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="b3364-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="b3364-126">Cuando se recibe un SoH-Response, el NapAgent primero asegura que los identificadores coincidan; Si no es así, se devuelve un error y el forzado debe quitar el paquete.</span><span class="sxs-lookup"><span data-stu-id="b3364-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="b3364-127">Consulte [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b3364-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3364-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3364-128">Requirements</span></span>



| <span data-ttu-id="b3364-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3364-129">Requirement</span></span> | <span data-ttu-id="b3364-130">Value</span><span class="sxs-lookup"><span data-stu-id="b3364-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3364-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3364-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b3364-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3364-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b3364-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3364-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b3364-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3364-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b3364-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3364-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3364-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3364-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3364-137">IDL</span><span class="sxs-lookup"><span data-stu-id="b3364-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3364-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3364-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b3364-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3364-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3364-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3364-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b3364-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3364-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3364-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="b3364-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





