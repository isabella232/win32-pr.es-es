---
title: Win32_RDMSEnvironment (clase)
description: Administra un entorno de Escritorio remoto Management Services (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSEnvironment de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676710"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="67155-105">\_Clase Win32 RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="67155-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="67155-106">Administra un entorno de Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="67155-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="67155-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="67155-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67155-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67155-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="67155-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="67155-109">Members</span></span>

<span data-ttu-id="67155-110">La **clase \_ RDMSEnvironment de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67155-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="67155-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="67155-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67155-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="67155-112">Methods</span></span>

<span data-ttu-id="67155-113">La clase **Win32 \_ RDMSEnvironment** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="67155-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="67155-114">Método</span><span class="sxs-lookup"><span data-stu-id="67155-114">Method</span></span>                                                                   | <span data-ttu-id="67155-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="67155-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67155-116">**GetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="67155-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="67155-117">Recupera el nombre de dominio completo (FQDN) del entorno de RDMS.</span><span class="sxs-lookup"><span data-stu-id="67155-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="67155-118">**GetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="67155-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="67155-119">Recupera el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) del entorno de RDMS.</span><span class="sxs-lookup"><span data-stu-id="67155-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="67155-120">**SetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="67155-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="67155-121">Establece el FQDN del entorno de RDMS en el nodo actual.</span><span class="sxs-lookup"><span data-stu-id="67155-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="67155-122">**SetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="67155-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="67155-123">Actualiza el nombre de DNS RR del entorno de RDMS.</span><span class="sxs-lookup"><span data-stu-id="67155-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="67155-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67155-124">Requirements</span></span>



| <span data-ttu-id="67155-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="67155-125">Requirement</span></span> | <span data-ttu-id="67155-126">Value</span><span class="sxs-lookup"><span data-stu-id="67155-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="67155-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67155-127">Minimum supported client</span></span><br/> | <span data-ttu-id="67155-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="67155-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="67155-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67155-129">Minimum supported server</span></span><br/> | <span data-ttu-id="67155-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67155-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="67155-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67155-131">Namespace</span></span><br/>                | <span data-ttu-id="67155-132">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="67155-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="67155-133">MOF</span><span class="sxs-lookup"><span data-stu-id="67155-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67155-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67155-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="67155-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67155-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67155-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67155-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="67155-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="67155-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67155-138">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="67155-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





