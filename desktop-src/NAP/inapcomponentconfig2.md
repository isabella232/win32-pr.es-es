---
title: Interfaz INapComponentConfig2 (NapCommon. h)
description: Proporciona métodos de configuración del sistema NAP para validadores de mantenimiento del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de redes (NPS) de forma remota.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- Interfaz INapComponentConfig2 NAP
- Interfaz INapComponentConfig2 NAP, descripción
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665955"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="2e5d0-105">Interfaz INapComponentConfig2</span><span class="sxs-lookup"><span data-stu-id="2e5d0-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="2e5d0-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2e5d0-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2e5d0-107">La interfaz **INapComponentConfig2** proporciona métodos de configuración del sistema NAP para los validadores de mantenimiento del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de redes (NPS) de forma remota.</span><span class="sxs-lookup"><span data-stu-id="2e5d0-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="2e5d0-108">Esta interfaz hereda todos los métodos de [**INapComponentConfig**](inapcomponentconfig.md) y se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2e5d0-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="2e5d0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e5d0-109">Members</span></span>

<span data-ttu-id="2e5d0-110">La interfaz **INapComponentConfig2** hereda de [**INapComponentConfig**](inapcomponentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="2e5d0-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="2e5d0-111">**INapComponentConfig2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e5d0-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="2e5d0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e5d0-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e5d0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e5d0-113">Methods</span></span>

<span data-ttu-id="2e5d0-114">La interfaz **INapComponentConfig2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2e5d0-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="2e5d0-115">Método</span><span class="sxs-lookup"><span data-stu-id="2e5d0-115">Method</span></span>                                                                                                | <span data-ttu-id="2e5d0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e5d0-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e5d0-117">**INapComponentConfig2::InvokeUIForMachine**</span><span class="sxs-lookup"><span data-stu-id="2e5d0-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="2e5d0-118">Implementado por SHV según sea necesario para administrar la configuración remota directamente en el equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e5d0-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="2e5d0-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="2e5d0-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="2e5d0-120">Implementado por SHV según sea necesario para cargar la configuración del equipo remoto en la memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="2e5d0-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="2e5d0-121">**INapComponentConfig2::IsRemoteConfigSupported**</span><span class="sxs-lookup"><span data-stu-id="2e5d0-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="2e5d0-122">Implementado por SHV para indicar si se admite la configuración remota.</span><span class="sxs-lookup"><span data-stu-id="2e5d0-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="2e5d0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e5d0-123">Remarks</span></span>

<span data-ttu-id="2e5d0-124">Esta interfaz no debe ser implementada por los agentes de mantenimiento del sistema (SHA) o los clientes de aplicación de cuarentena (QECs).</span><span class="sxs-lookup"><span data-stu-id="2e5d0-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e5d0-125">Requirements</span></span>



| <span data-ttu-id="2e5d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5d0-126">Requirement</span></span> | <span data-ttu-id="2e5d0-127">Value</span><span class="sxs-lookup"><span data-stu-id="2e5d0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5d0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e5d0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5d0-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e5d0-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2e5d0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e5d0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5d0-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e5d0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e5d0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e5d0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e5d0-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5d0-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e5d0-134">IDL</span><span class="sxs-lookup"><span data-stu-id="2e5d0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e5d0-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e5d0-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e5d0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e5d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5d0-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="2e5d0-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="2e5d0-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="2e5d0-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2e5d0-139">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="2e5d0-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





