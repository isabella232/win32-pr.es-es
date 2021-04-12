---
title: Interfaz INapEnforcementClientConnection (NapEnforcementClient. h)
description: Permite la administración de conexiones de cliente. | Interfaz INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Interfaz INapEnforcementClientConnection NAP
- Interfaz INapEnforcementClientConnection NAP, descripción
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279990"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="fd6df-106">Interfaz INapEnforcementClientConnection</span><span class="sxs-lookup"><span data-stu-id="fd6df-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="fd6df-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fd6df-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fd6df-108">**INapEnforcementClientConnection** proporciona métodos que permiten la administración de conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="fd6df-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="fd6df-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="fd6df-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd6df-110">Members</span></span>

<span data-ttu-id="fd6df-111">La interfaz **INapEnforcementClientConnection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fd6df-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fd6df-112">**INapEnforcementClientConnection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fd6df-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="fd6df-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd6df-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fd6df-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd6df-114">Methods</span></span>

<span data-ttu-id="fd6df-115">La interfaz **INapEnforcementClientConnection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fd6df-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="fd6df-116">Método</span><span class="sxs-lookup"><span data-stu-id="fd6df-116">Method</span></span>                                                                                                                           | <span data-ttu-id="fd6df-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd6df-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd6df-118">**INapEnforcementClientConnection:: Getconnectionid (**</span><span class="sxs-lookup"><span data-stu-id="fd6df-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="fd6df-119">Obtiene el identificador de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="fd6df-120">**INapEnforcementClientConnection::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="fd6df-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="fd6df-121">Obtiene el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.</span><span class="sxs-lookup"><span data-stu-id="fd6df-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="fd6df-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="fd6df-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="fd6df-123">Lo utiliza el aplicador para obtener datos privados.</span><span class="sxs-lookup"><span data-stu-id="fd6df-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fd6df-124">**INapEnforcementClientConnection:: GetFlags**</span><span class="sxs-lookup"><span data-stu-id="fd6df-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="fd6df-125">Obtiene el valor de la marca que diferencia las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los imforcedores.</span><span class="sxs-lookup"><span data-stu-id="fd6df-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="fd6df-126">**INapEnforcementClientConnection::GetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="fd6df-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="fd6df-127">Se usa para obtener la información de aislamiento del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="fd6df-128">**INapEnforcementClientConnection::GetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="fd6df-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="fd6df-129">Obtiene el tamaño máximo del paquete SoH para este cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="fd6df-130">**INapEnforcementClientConnection::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="fd6df-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="fd6df-131">Lo usa NapAgent para obtener datos privados.</span><span class="sxs-lookup"><span data-stu-id="fd6df-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fd6df-132">**INapEnforcementClientConnection::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="fd6df-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="fd6df-133">Obtiene la solicitud de SoH.</span><span class="sxs-lookup"><span data-stu-id="fd6df-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="fd6df-134">**INapEnforcementClientConnection::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="fd6df-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="fd6df-135">Obtiene el SoH-Response recibido por el cliente de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="fd6df-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="fd6df-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="fd6df-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="fd6df-137">Obtiene la versión de cadena de CorrelationId.</span><span class="sxs-lookup"><span data-stu-id="fd6df-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="fd6df-138">Se utiliza principalmente para fines de registro.</span><span class="sxs-lookup"><span data-stu-id="fd6df-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="fd6df-139">**INapEnforcementClientConnection:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="fd6df-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="fd6df-140">Inicializa la conexión.</span><span class="sxs-lookup"><span data-stu-id="fd6df-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="fd6df-141">**INapEnforcementClientConnection::SetConnectionId**</span><span class="sxs-lookup"><span data-stu-id="fd6df-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="fd6df-142">Establece el identificador de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="fd6df-143">**INapEnforcementClientConnection::SetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="fd6df-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="fd6df-144">Establece el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.</span><span class="sxs-lookup"><span data-stu-id="fd6df-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="fd6df-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="fd6df-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="fd6df-146">Lo utiliza el aplicador para establecer datos privados.</span><span class="sxs-lookup"><span data-stu-id="fd6df-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fd6df-147">**INapEnforcementClientConnection:: SetFlags**</span><span class="sxs-lookup"><span data-stu-id="fd6df-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="fd6df-148">Establece la marca que diferencia las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los incumplimientos.</span><span class="sxs-lookup"><span data-stu-id="fd6df-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="fd6df-149">**INapEnforcementClientConnection::SetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="fd6df-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="fd6df-150">Lo usa NapAgent para establecer la información de aislamiento del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="fd6df-151">**INapEnforcementClientConnection::SetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="fd6df-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="fd6df-152">Establece el tamaño máximo del paquete SoH para este cliente.</span><span class="sxs-lookup"><span data-stu-id="fd6df-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="fd6df-153">**INapEnforcementClientConnection::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="fd6df-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="fd6df-154">Lo usa NapAgent para establecer datos privados.</span><span class="sxs-lookup"><span data-stu-id="fd6df-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fd6df-155">**INapEnforcementClientConnection::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="fd6df-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="fd6df-156">Establece la solicitud de SoH.</span><span class="sxs-lookup"><span data-stu-id="fd6df-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="fd6df-157">**INapEnforcementClientConnection::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="fd6df-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="fd6df-158">Establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.</span><span class="sxs-lookup"><span data-stu-id="fd6df-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="fd6df-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd6df-159">Requirements</span></span>



| <span data-ttu-id="fd6df-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd6df-160">Requirement</span></span> | <span data-ttu-id="fd6df-161">Value</span><span class="sxs-lookup"><span data-stu-id="fd6df-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6df-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd6df-162">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6df-163">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fd6df-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd6df-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd6df-164">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6df-165">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd6df-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd6df-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd6df-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd6df-167"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6df-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd6df-168">IDL</span><span class="sxs-lookup"><span data-stu-id="fd6df-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd6df-169"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd6df-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fd6df-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd6df-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6df-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6df-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fd6df-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd6df-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6df-173">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="fd6df-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fd6df-174">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="fd6df-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

