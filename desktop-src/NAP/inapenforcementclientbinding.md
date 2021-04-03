---
title: Interfaz INapEnforcementClientBinding (NapEnforcementClient. h)
description: Los clientes de cumplimiento utilizan para comunicarse con el NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- Interfaz INapEnforcementClientBinding NAP
- Interfaz INapEnforcementClientBinding NAP, descripción
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905636"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="b1f6d-105">Interfaz INapEnforcementClientBinding</span><span class="sxs-lookup"><span data-stu-id="b1f6d-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="b1f6d-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b1f6d-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b1f6d-107">**INapEnforcementClientBinding** proporciona métodos que los clientes de cumplimiento usan para comunicarse con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="b1f6d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1f6d-108">Members</span></span>

<span data-ttu-id="b1f6d-109">La interfaz **INapEnforcementClientBinding** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b1f6d-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b1f6d-110">**INapEnforcementClientBinding** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b1f6d-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="b1f6d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1f6d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1f6d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1f6d-112">Methods</span></span>

<span data-ttu-id="b1f6d-113">La interfaz **INapEnforcementClientBinding** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="b1f6d-114">Método</span><span class="sxs-lookup"><span data-stu-id="b1f6d-114">Method</span></span>                                                                                                                           | <span data-ttu-id="b1f6d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1f6d-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1f6d-116">**INapEnforcementClientBinding:: CreateConnection**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="b1f6d-117">Lo usan los exigidos para crear objetos de conexión.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="b1f6d-118">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="b1f6d-119">Lo usa el cliente de cumplimiento cuando necesita una solicitud de SoH para una conexión determinada.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="b1f6d-120">**INapEnforcementClientBinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="b1f6d-121">Inicia el servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="b1f6d-122">El cliente de cumplimiento debe llamar a este método antes de llamar a cualquier otro método de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="b1f6d-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="b1f6d-124">Se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha dejado de funcionar.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="b1f6d-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="b1f6d-126">Lo usa el cliente de cumplimiento para informar a NapAgent de que no pudo procesar un [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="b1f6d-127">**INapEnforcementClientBinding::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="b1f6d-128">Lo usan los clientes de cumplimiento siempre que obtienen un BLOB de datos SoH-Response del servidor de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="b1f6d-129">**INapEnforcementClientBinding:: UnInitialize**</span><span class="sxs-lookup"><span data-stu-id="b1f6d-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="b1f6d-130">Concluye el servicio NapAgent para esta conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b1f6d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1f6d-131">Remarks</span></span>

<span data-ttu-id="b1f6d-132">Todas las API de esta interfaz devolverán RPC \_ E \_ desconectadas si NapAgent está detenido.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="b1f6d-133">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="b1f6d-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f6d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f6d-134">Requirements</span></span>



| <span data-ttu-id="b1f6d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f6d-135">Requirement</span></span> | <span data-ttu-id="b1f6d-136">Value</span><span class="sxs-lookup"><span data-stu-id="b1f6d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f6d-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1f6d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f6d-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b1f6d-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1f6d-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1f6d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f6d-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1f6d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b1f6d-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1f6d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f6d-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f6d-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1f6d-143">IDL</span><span class="sxs-lookup"><span data-stu-id="b1f6d-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1f6d-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1f6d-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1f6d-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1f6d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f6d-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1f6d-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b1f6d-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1f6d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f6d-148">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="b1f6d-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b1f6d-149">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="b1f6d-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

