---
title: Interfaz INapServerManagement (NapServerManagement. h)
description: Se usan para administrar el servidor NAP.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- Interfaz INapServerManagement NAP
- Interfaz INapServerManagement NAP, descripción
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150441"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="be543-105">Interfaz INapServerManagement</span><span class="sxs-lookup"><span data-stu-id="be543-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="be543-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="be543-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="be543-107">**INapServerManagement** proporciona métodos que se usan para administrar el servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="be543-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="be543-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="be543-108">Members</span></span>

<span data-ttu-id="be543-109">La interfaz **INapServerManagement** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be543-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be543-110">**INapServerManagement** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="be543-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="be543-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="be543-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be543-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="be543-112">Methods</span></span>

<span data-ttu-id="be543-113">La interfaz **INapServerManagement** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="be543-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="be543-114">Método</span><span class="sxs-lookup"><span data-stu-id="be543-114">Method</span></span>                                                                                                                       | <span data-ttu-id="be543-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="be543-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="be543-116">**INapServerManagement::RegisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="be543-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="be543-117">Registra un SHV.</span><span class="sxs-lookup"><span data-stu-id="be543-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="be543-118">**INapServerManagement::SetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="be543-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="be543-119">Establece las asignaciones de categorías de error de SHV.</span><span class="sxs-lookup"><span data-stu-id="be543-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="be543-120">**INapServerManagement::UnregisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="be543-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="be543-121">Anula el registro de un SHV del servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="be543-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="be543-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be543-122">Requirements</span></span>



| <span data-ttu-id="be543-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be543-123">Requirement</span></span> | <span data-ttu-id="be543-124">Value</span><span class="sxs-lookup"><span data-stu-id="be543-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be543-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be543-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be543-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="be543-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="be543-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be543-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be543-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="be543-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be543-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be543-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be543-130"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="be543-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="be543-131">IDL</span><span class="sxs-lookup"><span data-stu-id="be543-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be543-132"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be543-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="be543-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be543-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be543-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be543-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="be543-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="be543-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be543-136">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="be543-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="be543-137">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="be543-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

