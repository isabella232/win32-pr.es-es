---
description: Proporciona información adicional que se va a usar con el método ExportReferencePoint de la \_ clase VirtualSystemReferencePointService de MSVM.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Msvm_VirtualSystemReferencePointExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083570"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="4e7ab-103">MSVM \_ VirtualSystemReferencePointExportSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="4e7ab-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="4e7ab-104">Proporciona información adicional que se va a usar con el método [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) de la clase [**\_ VirtualSystemReferencePointService de MSVM**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4e7ab-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="4e7ab-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4e7ab-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7ab-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e7ab-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="4e7ab-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e7ab-107">Members</span></span>

<span data-ttu-id="4e7ab-108">La clase **MSVM \_ VirtualSystemReferencePointExportSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4e7ab-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4e7ab-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e7ab-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e7ab-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e7ab-110">Properties</span></span>

<span data-ttu-id="4e7ab-111">La clase **MSVM \_ VirtualSystemReferencePointExportSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e7ab-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e7ab-112">**BaseReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="4e7ab-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e7ab-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e7ab-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4e7ab-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e7ab-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e7ab-115">Ruta de acceso del punto de referencia base con respecto a la exportación que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="4e7ab-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="4e7ab-116">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="4e7ab-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e7ab-117">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4e7ab-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="4e7ab-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e7ab-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e7ab-119">Identificadores de instancia de WMI de los discos para los que se deben exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="4e7ab-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e7ab-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e7ab-120">Requirements</span></span>



| <span data-ttu-id="4e7ab-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e7ab-121">Requirement</span></span> | <span data-ttu-id="4e7ab-122">Value</span><span class="sxs-lookup"><span data-stu-id="4e7ab-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7ab-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e7ab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e7ab-124">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e7ab-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4e7ab-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e7ab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e7ab-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4e7ab-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4e7ab-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e7ab-127">Namespace</span></span><br/>                | <span data-ttu-id="4e7ab-128">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4e7ab-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4e7ab-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4e7ab-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e7ab-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e7ab-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e7ab-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e7ab-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e7ab-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e7ab-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e7ab-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e7ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7ab-134">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4e7ab-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




