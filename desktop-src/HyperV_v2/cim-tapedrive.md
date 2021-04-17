---
description: Representa las capacidades y la administración de una unidad de cinta.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: CIM_TapeDrive (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666908"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="ae516-103">CIM_TapeDrive (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ae516-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="ae516-104">Representa las capacidades y la administración de una unidad de cinta.</span><span class="sxs-lookup"><span data-stu-id="ae516-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae516-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae516-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="ae516-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae516-106">Members</span></span>

<span data-ttu-id="ae516-107">La clase **CIM \_ TapeDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ae516-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="ae516-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae516-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae516-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae516-109">Properties</span></span>

<span data-ttu-id="ae516-110">La clase **CIM \_ TapeDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ae516-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae516-111">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="ae516-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae516-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae516-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae516-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae516-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae516-114">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="ae516-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="ae516-115">Tamaño, en bytes, del área designada como "final de la cinta".</span><span class="sxs-lookup"><span data-stu-id="ae516-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="ae516-116">El acceso en esta área genera una advertencia de "final de cinta".</span><span class="sxs-lookup"><span data-stu-id="ae516-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="ae516-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="ae516-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae516-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae516-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae516-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae516-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae516-120">Número máximo de particiones para la unidad de cinta.</span><span class="sxs-lookup"><span data-stu-id="ae516-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="ae516-121">**MaxRewindTime**</span><span class="sxs-lookup"><span data-stu-id="ae516-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae516-122">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae516-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae516-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae516-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae516-124">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos"), **punitivo** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="ae516-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="ae516-125">Tiempo, en milisegundos, que se va a pasar desde el punto más alejado físicamente de la cinta al principio.</span><span class="sxs-lookup"><span data-stu-id="ae516-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="ae516-126">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="ae516-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae516-127">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae516-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae516-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae516-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae516-129">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="ae516-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="ae516-130">Número de bytes insertados entre bloques en un medio de cinta.</span><span class="sxs-lookup"><span data-stu-id="ae516-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae516-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae516-131">Requirements</span></span>



| <span data-ttu-id="ae516-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae516-132">Requirement</span></span> | <span data-ttu-id="ae516-133">Value</span><span class="sxs-lookup"><span data-stu-id="ae516-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae516-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae516-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ae516-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ae516-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ae516-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae516-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ae516-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ae516-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ae516-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae516-138">Namespace</span></span><br/>                | <span data-ttu-id="ae516-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ae516-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae516-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ae516-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae516-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae516-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae516-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae516-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae516-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae516-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae516-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae516-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae516-145">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ae516-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

