---
description: Proporciona información sobre una instantánea dentro de un archivo de conjunto de VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Msvm_VHDSnapshotInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908309"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="192ed-103">MSVM \_ VHDSnapshotInformation (clase)</span><span class="sxs-lookup"><span data-stu-id="192ed-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="192ed-104">Proporciona información sobre una instantánea dentro de un archivo de conjunto de VHD</span><span class="sxs-lookup"><span data-stu-id="192ed-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="192ed-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="192ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="192ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="192ed-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="192ed-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="192ed-107">Members</span></span>

<span data-ttu-id="192ed-108">La clase **MSVM \_ VHDSnapshotInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="192ed-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="192ed-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="192ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="192ed-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="192ed-110">Properties</span></span>

<span data-ttu-id="192ed-111">La clase **MSVM \_ VHDSnapshotInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="192ed-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="192ed-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="192ed-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="192ed-113">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="192ed-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="192ed-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="192ed-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="192ed-115">Fecha y hora de creación de esta instantánea.</span><span class="sxs-lookup"><span data-stu-id="192ed-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="192ed-116">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="192ed-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="192ed-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="192ed-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="192ed-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="192ed-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="192ed-119">Ruta de acceso del archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="192ed-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="192ed-120">**ParentPathsList**</span><span class="sxs-lookup"><span data-stu-id="192ed-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="192ed-121">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="192ed-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="192ed-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="192ed-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="192ed-123">Una lista de rutas de acceso de archivo que representan todos los archivos de los que depende esta instantánea.</span><span class="sxs-lookup"><span data-stu-id="192ed-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="192ed-124">Este campo estará vacío a menos que se solicite específicamente.</span><span class="sxs-lookup"><span data-stu-id="192ed-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="192ed-125">La primera entrada es el elemento primario inmediato del archivo, donde la última entrada es la raíz.</span><span class="sxs-lookup"><span data-stu-id="192ed-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="192ed-126">**ResilientChangeTrackingId**</span><span class="sxs-lookup"><span data-stu-id="192ed-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="192ed-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="192ed-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="192ed-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="192ed-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="192ed-129">IDENTIFICADOR de seguimiento de cambios resistente, si existe, asociado a esta instantánea.</span><span class="sxs-lookup"><span data-stu-id="192ed-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="192ed-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="192ed-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="192ed-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="192ed-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="192ed-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="192ed-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="192ed-133">GUID que identifica de forma única esta instantánea dentro del archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="192ed-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="192ed-134">**SnapshotPath**</span><span class="sxs-lookup"><span data-stu-id="192ed-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="192ed-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="192ed-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="192ed-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="192ed-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="192ed-137">Ruta de acceso del archivo representado por esta instantánea.</span><span class="sxs-lookup"><span data-stu-id="192ed-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="192ed-138">Este campo puede estar vacío si no hay ningún archivo asociado a esta instantánea.</span><span class="sxs-lookup"><span data-stu-id="192ed-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="192ed-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="192ed-139">Requirements</span></span>



| <span data-ttu-id="192ed-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="192ed-140">Requirement</span></span> | <span data-ttu-id="192ed-141">Value</span><span class="sxs-lookup"><span data-stu-id="192ed-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="192ed-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="192ed-142">Minimum supported client</span></span><br/> | <span data-ttu-id="192ed-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="192ed-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="192ed-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="192ed-144">Minimum supported server</span></span><br/> | <span data-ttu-id="192ed-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="192ed-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="192ed-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="192ed-146">Namespace</span></span><br/>                | <span data-ttu-id="192ed-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="192ed-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="192ed-148">MOF</span><span class="sxs-lookup"><span data-stu-id="192ed-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="192ed-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="192ed-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="192ed-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="192ed-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="192ed-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="192ed-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




