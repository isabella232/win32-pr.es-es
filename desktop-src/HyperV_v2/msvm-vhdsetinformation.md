---
description: Proporciona información sobre un archivo de conjunto de VHD.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687112"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="dd8a9-103">MSVM \_ VHDSetInformation (clase)</span><span class="sxs-lookup"><span data-stu-id="dd8a9-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="dd8a9-104">Proporciona información sobre un archivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="dd8a9-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd8a9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd8a9-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="dd8a9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd8a9-107">Members</span></span>

<span data-ttu-id="dd8a9-108">La clase **MSVM \_ VHDSetInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd8a9-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="dd8a9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd8a9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd8a9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd8a9-110">Properties</span></span>

<span data-ttu-id="dd8a9-111">La clase **MSVM \_ VHDSetInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd8a9-112">**AllPaths**</span><span class="sxs-lookup"><span data-stu-id="dd8a9-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd8a9-113">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="dd8a9-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd8a9-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd8a9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd8a9-115">Una lista de todos los archivos englobados por el archivo de VHD Set, incluidos los archivos sin referencia y los elementos primarios del disco duro virtual raíz.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="dd8a9-116">Todos los archivos enumerados después del disco duro virtual raíz no están administrados por este archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="dd8a9-117">Este campo puede estar vacío si no se ha solicitado específicamente esta información.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="dd8a9-118">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="dd8a9-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd8a9-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd8a9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd8a9-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd8a9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd8a9-121">Ruta de acceso del archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="dd8a9-122">**SnapshotIdList**</span><span class="sxs-lookup"><span data-stu-id="dd8a9-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd8a9-123">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="dd8a9-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd8a9-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd8a9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd8a9-125">Una lista de GUID que representa todas las instantáneas que contiene este archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="dd8a9-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd8a9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd8a9-126">Requirements</span></span>



| <span data-ttu-id="dd8a9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd8a9-127">Requirement</span></span> | <span data-ttu-id="dd8a9-128">Value</span><span class="sxs-lookup"><span data-stu-id="dd8a9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8a9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd8a9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd8a9-130">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd8a9-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dd8a9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd8a9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd8a9-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dd8a9-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dd8a9-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd8a9-133">Namespace</span></span><br/>                | <span data-ttu-id="dd8a9-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dd8a9-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd8a9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dd8a9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd8a9-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd8a9-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd8a9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd8a9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd8a9-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd8a9-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




