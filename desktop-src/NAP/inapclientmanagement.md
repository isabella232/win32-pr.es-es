---
title: Interfaz INapClientManagement (NapManagement. h)
description: Proporciona métodos para la administración del cliente de NAP. | Interfaz INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- Interfaz INapClientManagement NAP
- Interfaz INapClientManagement NAP, descripción
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003660"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="0fff1-106">Interfaz INapClientManagement</span><span class="sxs-lookup"><span data-stu-id="0fff1-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="0fff1-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0fff1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0fff1-108">La interfaz **INapClientManagement** proporciona métodos para la administración del cliente de NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="0fff1-109">[**INapClientManagement2**](inapclientmanagement2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0fff1-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="0fff1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="0fff1-110">Members</span></span>

<span data-ttu-id="0fff1-111">La interfaz **INapClientManagement** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0fff1-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0fff1-112">**INapClientManagement** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0fff1-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="0fff1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="0fff1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0fff1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0fff1-114">Methods</span></span>

<span data-ttu-id="0fff1-115">La interfaz **INapClientManagement** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0fff1-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="0fff1-116">Método</span><span class="sxs-lookup"><span data-stu-id="0fff1-116">Method</span></span>                                                                                                                | <span data-ttu-id="0fff1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fff1-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="0fff1-118">**INapClientManagement::GetNapClientInfo**</span><span class="sxs-lookup"><span data-stu-id="0fff1-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="0fff1-119">Recupera información sobre un cliente de NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="0fff1-120">**INapClientManagement::GetRegisteredEnforcementClients**</span><span class="sxs-lookup"><span data-stu-id="0fff1-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="0fff1-121">Recupera información acerca de los clientes de cumplimiento registrados.</span><span class="sxs-lookup"><span data-stu-id="0fff1-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="0fff1-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span><span class="sxs-lookup"><span data-stu-id="0fff1-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="0fff1-123">Recupera información sobre un SHA registrado.</span><span class="sxs-lookup"><span data-stu-id="0fff1-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="0fff1-124">**INapClientManagement::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="0fff1-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="0fff1-125">Recupera información sobre el estado de aislamiento del cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="0fff1-126">**INapClientManagement::RegisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="0fff1-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="0fff1-127">Registra un cliente de cumplimiento con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="0fff1-128">**INapClientManagement::RegisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="0fff1-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="0fff1-129">Registra un SHA con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="0fff1-130">**INapClientManagement::UnregisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="0fff1-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="0fff1-131">Anula el registro de un cliente de cumplimiento con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="0fff1-132">**INapClientManagement::UnregisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="0fff1-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="0fff1-133">Anula el registro de un SHA con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="0fff1-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="0fff1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fff1-134">Requirements</span></span>



| <span data-ttu-id="0fff1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fff1-135">Requirement</span></span> | <span data-ttu-id="0fff1-136">Value</span><span class="sxs-lookup"><span data-stu-id="0fff1-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fff1-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fff1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0fff1-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fff1-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0fff1-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fff1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0fff1-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fff1-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0fff1-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fff1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fff1-142"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fff1-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fff1-143">IDL</span><span class="sxs-lookup"><span data-stu-id="0fff1-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fff1-144"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fff1-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fff1-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0fff1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fff1-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fff1-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="0fff1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fff1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fff1-148">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="0fff1-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0fff1-149">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="0fff1-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

