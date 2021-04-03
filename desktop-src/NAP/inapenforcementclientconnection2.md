---
title: Interfaz INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Permite la administración de conexiones de cliente. | Interfaz INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- Interfaz INapEnforcementClientConnection2 NAP
- Interfaz INapEnforcementClientConnection2 NAP, descripción
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914361"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="a8727-106">Interfaz INapEnforcementClientConnection2</span><span class="sxs-lookup"><span data-stu-id="a8727-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="a8727-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a8727-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a8727-108">**INapEnforcementClientConnection2** proporciona métodos que permiten la administración de conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="a8727-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="a8727-109">Esta interfaz hereda todos los métodos de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) y se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a8727-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="a8727-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8727-110">Members</span></span>

<span data-ttu-id="a8727-111">La interfaz **INapEnforcementClientConnection2** hereda de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a8727-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="a8727-112">**INapEnforcementClientConnection2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a8727-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="a8727-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8727-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8727-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8727-114">Methods</span></span>

<span data-ttu-id="a8727-115">La interfaz **INapEnforcementClientConnection2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a8727-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="a8727-116">Método</span><span class="sxs-lookup"><span data-stu-id="a8727-116">Method</span></span>                                                                                                              | <span data-ttu-id="a8727-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8727-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="a8727-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="a8727-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="a8727-119">Se usa para obtener los identificadores de los SHV instalados para el cliente.</span><span class="sxs-lookup"><span data-stu-id="a8727-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="a8727-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="a8727-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="a8727-121">Se utiliza para obtener la información de aislamiento para el cliente.</span><span class="sxs-lookup"><span data-stu-id="a8727-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="a8727-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="a8727-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="a8727-123">Lo usa NapAgent para establecer los identificadores de SHV instalados para el cliente.</span><span class="sxs-lookup"><span data-stu-id="a8727-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="a8727-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="a8727-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="a8727-125">Lo usa NapAgent para establecer la información de aislamiento para el cliente.</span><span class="sxs-lookup"><span data-stu-id="a8727-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8727-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8727-126">Requirements</span></span>



| <span data-ttu-id="a8727-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8727-127">Requirement</span></span> | <span data-ttu-id="a8727-128">Value</span><span class="sxs-lookup"><span data-stu-id="a8727-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8727-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8727-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8727-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8727-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8727-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8727-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8727-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8727-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8727-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8727-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8727-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8727-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8727-135">IDL</span><span class="sxs-lookup"><span data-stu-id="a8727-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8727-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8727-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8727-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8727-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8727-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8727-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a8727-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8727-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8727-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a8727-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="a8727-141">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="a8727-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a8727-142">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="a8727-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





