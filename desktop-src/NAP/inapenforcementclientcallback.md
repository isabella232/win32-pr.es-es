---
title: Interfaz INapEnforcementClientCallback (NapEnforcementClient. h)
description: Los clientes de cumplimiento deben implementar para permitir que NapAgent se comunique con ellos.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- Interfaz INapEnforcementClientCallback NAP
- Interfaz INapEnforcementClientCallback NAP, descripción
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677009"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="6ec86-105">Interfaz INapEnforcementClientCallback</span><span class="sxs-lookup"><span data-stu-id="6ec86-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="6ec86-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6ec86-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6ec86-107">La interfaz **INapEnforcementClientCallback** proporciona métodos de devolución de llamada que los clientes de cumplimiento deben implementar para permitir que NapAgent se comunique con ellos.</span><span class="sxs-lookup"><span data-stu-id="6ec86-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="6ec86-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ec86-108">Members</span></span>

<span data-ttu-id="6ec86-109">La interfaz **INapEnforcementClientCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6ec86-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6ec86-110">**INapEnforcementClientCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ec86-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="6ec86-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ec86-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ec86-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ec86-112">Methods</span></span>

<span data-ttu-id="6ec86-113">La interfaz **INapEnforcementClientCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6ec86-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="6ec86-114">Método</span><span class="sxs-lookup"><span data-stu-id="6ec86-114">Method</span></span>                                                                                                         | <span data-ttu-id="6ec86-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ec86-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="6ec86-116">**INapEnforcementClientCallback::GetConnections**</span><span class="sxs-lookup"><span data-stu-id="6ec86-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="6ec86-117">Lo utiliza el NapAgent para recuperar las conexiones.</span><span class="sxs-lookup"><span data-stu-id="6ec86-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="6ec86-118">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="6ec86-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="6ec86-119">Lo utiliza el NapAgent para informar al cliente de cumplimiento de los cambios de SoH.</span><span class="sxs-lookup"><span data-stu-id="6ec86-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ec86-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec86-120">Requirements</span></span>



| <span data-ttu-id="6ec86-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec86-121">Requirement</span></span> | <span data-ttu-id="6ec86-122">Value</span><span class="sxs-lookup"><span data-stu-id="6ec86-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec86-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec86-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec86-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ec86-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec86-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec86-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ec86-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ec86-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec86-128"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec86-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ec86-129">IDL</span><span class="sxs-lookup"><span data-stu-id="6ec86-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ec86-130"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ec86-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 

