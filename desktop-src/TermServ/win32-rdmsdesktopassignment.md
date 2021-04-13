---
title: Win32_RDMSDesktopAssignment (clase)
description: Describe la asignación de escritorio de usuario de la colección de RD.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSDesktopAssignment de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359729"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="df611-105">\_Clase Win32 RDMSDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="df611-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="df611-106">Describe la asignación de escritorio de usuario de la colección de RD.</span><span class="sxs-lookup"><span data-stu-id="df611-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="df611-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="df611-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df611-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df611-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="df611-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="df611-109">Members</span></span>

<span data-ttu-id="df611-110">La **clase \_ RDMSDesktopAssignment de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="df611-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="df611-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="df611-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="df611-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df611-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df611-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="df611-113">Methods</span></span>

<span data-ttu-id="df611-114">La clase **Win32 \_ RDMSDesktopAssignment** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="df611-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="df611-115">Método</span><span class="sxs-lookup"><span data-stu-id="df611-115">Method</span></span>                                                                                 | <span data-ttu-id="df611-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="df611-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="df611-117">**AddDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="df611-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="df611-118">Agrega una asignación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="df611-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="df611-119">**RemoveDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="df611-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="df611-120">Quita una asignación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="df611-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df611-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df611-121">Properties</span></span>

<span data-ttu-id="df611-122">La **clase \_ RDMSDesktopAssignment de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="df611-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df611-123">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="df611-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df611-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="df611-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df611-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="df611-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="df611-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df611-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="df611-127">Alias de la colección.</span><span class="sxs-lookup"><span data-stu-id="df611-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="df611-128">**DesktopName**</span><span class="sxs-lookup"><span data-stu-id="df611-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df611-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="df611-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df611-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="df611-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="df611-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df611-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="df611-132">Nombre del escritorio.</span><span class="sxs-lookup"><span data-stu-id="df611-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="df611-133">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="df611-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df611-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="df611-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df611-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="df611-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="df611-136">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df611-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="df611-137">El nombre de dominio de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="df611-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="df611-138">**UserName**</span><span class="sxs-lookup"><span data-stu-id="df611-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df611-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="df611-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df611-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="df611-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="df611-141">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df611-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="df611-142">El nombre de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="df611-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df611-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df611-143">Requirements</span></span>



| <span data-ttu-id="df611-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="df611-144">Requirement</span></span> | <span data-ttu-id="df611-145">Value</span><span class="sxs-lookup"><span data-stu-id="df611-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="df611-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df611-146">Minimum supported client</span></span><br/> | <span data-ttu-id="df611-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="df611-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="df611-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df611-148">Minimum supported server</span></span><br/> | <span data-ttu-id="df611-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="df611-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="df611-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df611-150">Namespace</span></span><br/>                | <span data-ttu-id="df611-151">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="df611-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="df611-152">MOF</span><span class="sxs-lookup"><span data-stu-id="df611-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df611-153"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df611-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="df611-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df611-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df611-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df611-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

