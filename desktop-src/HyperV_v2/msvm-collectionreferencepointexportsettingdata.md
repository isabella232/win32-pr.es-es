---
description: Exportar los datos de configuración que se van a pasar al método ExportReferencePoint de la \_ clase CollectionReferencePointService de MSVM.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Msvm_CollectionReferencePointExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688364"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="40eee-103">MSVM \_ CollectionReferencePointExportSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="40eee-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="40eee-104">Exportar los datos de configuración que se van a pasar al método [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) de la clase [**\_ CollectionReferencePointService de MSVM**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="40eee-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="40eee-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="40eee-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40eee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40eee-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="40eee-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="40eee-107">Members</span></span>

<span data-ttu-id="40eee-108">La clase **MSVM \_ CollectionReferencePointExportSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="40eee-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="40eee-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40eee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40eee-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40eee-110">Properties</span></span>

<span data-ttu-id="40eee-111">La clase **MSVM \_ CollectionReferencePointExportSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="40eee-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40eee-112">**BaseReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="40eee-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40eee-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40eee-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40eee-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40eee-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40eee-115">Ruta de acceso a una instancia de [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa la colección de puntos de referencia base que se va a usar para la exportación diferencial.</span><span class="sxs-lookup"><span data-stu-id="40eee-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="40eee-116">**VirtualMachinesToDisksToExport**</span><span class="sxs-lookup"><span data-stu-id="40eee-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40eee-117">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="40eee-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40eee-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40eee-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40eee-119">Calificadores: **HyperVEmbeddedInstance** ("MSVM \_ VirtualMachineToDisks")</span><span class="sxs-lookup"><span data-stu-id="40eee-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="40eee-120">Lista de la información de asignación de "VirtualMachines a DisksToExport" para la que es necesario exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="40eee-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40eee-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40eee-121">Requirements</span></span>



| <span data-ttu-id="40eee-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="40eee-122">Requirement</span></span> | <span data-ttu-id="40eee-123">Value</span><span class="sxs-lookup"><span data-stu-id="40eee-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40eee-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40eee-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40eee-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="40eee-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="40eee-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40eee-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40eee-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="40eee-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="40eee-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40eee-128">Namespace</span></span><br/>                | <span data-ttu-id="40eee-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="40eee-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="40eee-130">MOF</span><span class="sxs-lookup"><span data-stu-id="40eee-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40eee-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40eee-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="40eee-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40eee-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40eee-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40eee-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="40eee-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="40eee-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40eee-135">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="40eee-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




