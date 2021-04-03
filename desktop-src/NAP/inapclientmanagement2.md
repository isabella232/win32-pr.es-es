---
title: Interfaz INapClientManagement2 (NapManagement. h)
description: Proporciona métodos para la administración del cliente de NAP. | Interfaz INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- Interfaz INapClientManagement2 NAP
- Interfaz INapClientManagement2 NAP, descripción
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083678"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="7206a-106">Interfaz INapClientManagement2</span><span class="sxs-lookup"><span data-stu-id="7206a-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="7206a-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7206a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7206a-108">La interfaz **INapClientManagement2** proporciona métodos para la administración del cliente de NAP.</span><span class="sxs-lookup"><span data-stu-id="7206a-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="7206a-109">Esta interfaz hereda todos los métodos de [**INapClientManagement**](inapclientmanagement.md) y se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7206a-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="7206a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7206a-110">Members</span></span>

<span data-ttu-id="7206a-111">La interfaz **INapClientManagement2** hereda de [**INapClientManagement**](inapclientmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="7206a-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="7206a-112">**INapClientManagement2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7206a-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="7206a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="7206a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7206a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="7206a-114">Methods</span></span>

<span data-ttu-id="7206a-115">La interfaz **INapClientManagement2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7206a-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="7206a-116">Método</span><span class="sxs-lookup"><span data-stu-id="7206a-116">Method</span></span>                                                                                                    | <span data-ttu-id="7206a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7206a-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7206a-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="7206a-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="7206a-119">Recupera información sobre el estado de aislamiento y el estado de aislamiento extendido del cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="7206a-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7206a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7206a-120">Requirements</span></span>



| <span data-ttu-id="7206a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7206a-121">Requirement</span></span> | <span data-ttu-id="7206a-122">Value</span><span class="sxs-lookup"><span data-stu-id="7206a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7206a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7206a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7206a-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7206a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7206a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7206a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7206a-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7206a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7206a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7206a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7206a-128"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="7206a-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="7206a-129">IDL</span><span class="sxs-lookup"><span data-stu-id="7206a-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7206a-130"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7206a-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="7206a-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7206a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7206a-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7206a-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="7206a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7206a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7206a-134">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="7206a-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="7206a-135">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="7206a-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7206a-136">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="7206a-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





