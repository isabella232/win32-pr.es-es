---
title: Win32_RDMSManagementData (clase)
description: Sincroniza los datos de publicación para Escritorio remoto Management Services (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSManagementData de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078964"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="c408c-105">\_Clase Win32 RDMSManagementData</span><span class="sxs-lookup"><span data-stu-id="c408c-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="c408c-106">Sincroniza los datos de publicación para Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="c408c-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="c408c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c408c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c408c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c408c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="c408c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c408c-109">Members</span></span>

<span data-ttu-id="c408c-110">La **clase \_ RDMSManagementData de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c408c-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="c408c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c408c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c408c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c408c-112">Methods</span></span>

<span data-ttu-id="c408c-113">La clase **Win32 \_ RDMSManagementData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c408c-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="c408c-114">Método</span><span class="sxs-lookup"><span data-stu-id="c408c-114">Method</span></span>                                                                                        | <span data-ttu-id="c408c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c408c-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="c408c-116">**SynchronizeAllPublishingData**</span><span class="sxs-lookup"><span data-stu-id="c408c-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="c408c-117">Sincroniza todos los datos de publicación para RDMS.</span><span class="sxs-lookup"><span data-stu-id="c408c-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="c408c-118">**SynchronizePublishingData**</span><span class="sxs-lookup"><span data-stu-id="c408c-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="c408c-119">Sincroniza el conjunto especificado de datos de publicación para RDMS.</span><span class="sxs-lookup"><span data-stu-id="c408c-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c408c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c408c-120">Requirements</span></span>



| <span data-ttu-id="c408c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c408c-121">Requirement</span></span> | <span data-ttu-id="c408c-122">Value</span><span class="sxs-lookup"><span data-stu-id="c408c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c408c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c408c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c408c-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c408c-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c408c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c408c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c408c-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c408c-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c408c-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c408c-127">Namespace</span></span><br/>                | <span data-ttu-id="c408c-128">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="c408c-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c408c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c408c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c408c-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c408c-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c408c-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c408c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c408c-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c408c-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c408c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c408c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c408c-134">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c408c-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





