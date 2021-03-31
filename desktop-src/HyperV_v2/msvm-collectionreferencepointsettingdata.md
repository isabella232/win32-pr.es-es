---
description: Proporciona información adicional que se va a usar con el método CreateReferencePoint de la \_ clase CollectionReferencePointService de MSVM.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Msvm_CollectionReferencePointSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155544"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="2f059-103">MSVM \_ CollectionReferencePointSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="2f059-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="2f059-104">Proporciona información adicional que se va a usar con el método [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) de la clase [**\_ CollectionReferencePointService de MSVM**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="2f059-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="2f059-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2f059-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f059-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f059-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="2f059-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f059-107">Members</span></span>

<span data-ttu-id="2f059-108">La clase **MSVM \_ CollectionReferencePointSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2f059-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2f059-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f059-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f059-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f059-110">Properties</span></span>

<span data-ttu-id="2f059-111">La clase **MSVM \_ CollectionReferencePointSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2f059-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f059-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="2f059-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f059-113">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2f059-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2f059-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2f059-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f059-115">Nivel de coherencia del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="2f059-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f059-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2f059-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="2f059-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente** con la aplicación (1)</span><span class="sxs-lookup"><span data-stu-id="2f059-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2f059-118">El punto de referencia indica un punto en el tiempo en el que el sistema virtual se encontraba en un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="2f059-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="2f059-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherencia de bloqueos** (2)</span><span class="sxs-lookup"><span data-stu-id="2f059-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2f059-120">El punto de referencia indica un punto en el tiempo en el que el sistema virtual estuvo en un estado coherente con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f059-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f059-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f059-121">Requirements</span></span>



| <span data-ttu-id="2f059-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f059-122">Requirement</span></span> | <span data-ttu-id="2f059-123">Value</span><span class="sxs-lookup"><span data-stu-id="2f059-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f059-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f059-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2f059-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f059-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2f059-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f059-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2f059-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2f059-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2f059-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f059-128">Namespace</span></span><br/>                | <span data-ttu-id="2f059-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2f059-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2f059-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2f059-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f059-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f059-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f059-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f059-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f059-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f059-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f059-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f059-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f059-135">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2f059-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




