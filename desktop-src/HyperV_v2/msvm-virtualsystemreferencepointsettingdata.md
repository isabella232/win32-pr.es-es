---
description: Proporciona información adicional que se va a usar con el método CreateReferencePoint de la \_ clase VirtualSystemReferencePointService de MSVM.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Msvm_VirtualSystemReferencePointSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670055"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="a849c-103">MSVM \_ VirtualSystemReferencePointSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="a849c-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="a849c-104">Proporciona información adicional que se va a usar con el método [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) de la clase [**\_ VirtualSystemReferencePointService de MSVM**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a849c-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="a849c-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a849c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a849c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a849c-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="a849c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a849c-107">Members</span></span>

<span data-ttu-id="a849c-108">La clase **MSVM \_ VirtualSystemReferencePointSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a849c-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a849c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a849c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a849c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a849c-110">Properties</span></span>

<span data-ttu-id="a849c-111">La clase **MSVM \_ VirtualSystemReferencePointSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a849c-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a849c-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="a849c-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a849c-113">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a849c-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a849c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a849c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a849c-115">El nivel de coherencia del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="a849c-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a849c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a849c-116">Requirements</span></span>



| <span data-ttu-id="a849c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a849c-117">Requirement</span></span> | <span data-ttu-id="a849c-118">Value</span><span class="sxs-lookup"><span data-stu-id="a849c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a849c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a849c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a849c-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a849c-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a849c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a849c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a849c-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a849c-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a849c-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a849c-123">Namespace</span></span><br/>                | <span data-ttu-id="a849c-124">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a849c-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a849c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="a849c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a849c-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a849c-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a849c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a849c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a849c-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a849c-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a849c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a849c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a849c-130">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a849c-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




