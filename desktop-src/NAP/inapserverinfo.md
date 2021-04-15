---
title: Interfaz INapServerInfo (NapServerManagement. h)
description: Los clientes de administración (por ejemplo, proveedores WMI o herramientas de línea de comandos) usan para consultar el estado del sistema del servidor NAP.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- Interfaz INapServerInfo NAP
- Interfaz INapServerInfo NAP, descripción
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676792"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="2c974-105">Interfaz INapServerInfo</span><span class="sxs-lookup"><span data-stu-id="2c974-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="2c974-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c974-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2c974-107">**INapServerInfo** proporciona métodos que los clientes de administración (por ejemplo, proveedores WMI o herramientas de línea de comandos) usan para consultar el estado del sistema del servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="2c974-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="2c974-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c974-108">Members</span></span>

<span data-ttu-id="2c974-109">La interfaz **INapServerInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2c974-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2c974-110">**INapServerInfo** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2c974-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="2c974-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c974-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2c974-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c974-112">Methods</span></span>

<span data-ttu-id="2c974-113">La interfaz **INapServerInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2c974-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="2c974-114">Método</span><span class="sxs-lookup"><span data-stu-id="2c974-114">Method</span></span>                                                                                                                   | <span data-ttu-id="2c974-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c974-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="2c974-116">**INapServerInfo::GetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="2c974-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="2c974-117">Recupera las asignaciones de categorías de error para un SHV especificado.</span><span class="sxs-lookup"><span data-stu-id="2c974-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="2c974-118">**INapServerInfo::GetNapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="2c974-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="2c974-119">Recupera información acerca del servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="2c974-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="2c974-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span><span class="sxs-lookup"><span data-stu-id="2c974-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="2c974-121">Recupera una lista de SHV registrados.</span><span class="sxs-lookup"><span data-stu-id="2c974-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2c974-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c974-122">Remarks</span></span>

<span data-ttu-id="2c974-123">Estos métodos proporcionan solo información estática sobre el servidor NAP y sus componentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2c974-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c974-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c974-124">Requirements</span></span>



| <span data-ttu-id="2c974-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c974-125">Requirement</span></span> | <span data-ttu-id="2c974-126">Value</span><span class="sxs-lookup"><span data-stu-id="2c974-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c974-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c974-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c974-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2c974-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="2c974-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c974-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c974-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c974-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c974-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c974-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c974-132"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c974-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c974-133">IDL</span><span class="sxs-lookup"><span data-stu-id="2c974-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c974-134"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c974-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2c974-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c974-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c974-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c974-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="2c974-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c974-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c974-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="2c974-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2c974-139">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="2c974-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

