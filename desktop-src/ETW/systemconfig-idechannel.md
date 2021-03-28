---
description: Esta clase es la clase de tipo de evento para eventos del canal IDE. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541867"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="96b9e-104">SystemConfig \_ IDEChannel (clase)</span><span class="sxs-lookup"><span data-stu-id="96b9e-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="96b9e-105">Esta clase es la clase de tipo de evento para eventos del canal IDE.</span><span class="sxs-lookup"><span data-stu-id="96b9e-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="96b9e-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="96b9e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b9e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96b9e-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="96b9e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="96b9e-108">Members</span></span>

<span data-ttu-id="96b9e-109">La clase **SystemConfig \_ IDEChannel** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="96b9e-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="96b9e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96b9e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96b9e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96b9e-111">Properties</span></span>

<span data-ttu-id="96b9e-112">La clase **SystemConfig \_ IDEChannel** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="96b9e-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96b9e-113">**DeviceTimingMode**</span><span class="sxs-lookup"><span data-stu-id="96b9e-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96b9e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96b9e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b9e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-116">Calificadores: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="96b9e-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96b9e-117">Modo en el que el IDE podría funcionar.</span><span class="sxs-lookup"><span data-stu-id="96b9e-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="96b9e-118">Los posibles valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="96b9e-118">The following are the possible values:</span></span>

-   <span data-ttu-id="96b9e-119">PIO \_ MODE0 (0x1)</span><span class="sxs-lookup"><span data-stu-id="96b9e-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="96b9e-120">PIO \_ MODE1 (0X2)</span><span class="sxs-lookup"><span data-stu-id="96b9e-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="96b9e-121">PIO \_ Mode2 (0x4)</span><span class="sxs-lookup"><span data-stu-id="96b9e-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="96b9e-122">PIO \_ MODE3 (0x8)</span><span class="sxs-lookup"><span data-stu-id="96b9e-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="96b9e-123">PIO \_ MODE4 (0x10)</span><span class="sxs-lookup"><span data-stu-id="96b9e-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="96b9e-124">SWDMA \_ MODE0 (0x20)</span><span class="sxs-lookup"><span data-stu-id="96b9e-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="96b9e-125">SWDMA \_ MODE1 (0x40)</span><span class="sxs-lookup"><span data-stu-id="96b9e-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="96b9e-126">SWDMA \_ Mode2 (0x80)</span><span class="sxs-lookup"><span data-stu-id="96b9e-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="96b9e-127">MWDMA \_ MODE0 (0x100)</span><span class="sxs-lookup"><span data-stu-id="96b9e-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="96b9e-128">MWDMA \_ Mode2 (0x200)</span><span class="sxs-lookup"><span data-stu-id="96b9e-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="96b9e-129">MWDMA \_ MODE3 (0x400)</span><span class="sxs-lookup"><span data-stu-id="96b9e-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="96b9e-130">UDMA \_ MODE0 (0x800)</span><span class="sxs-lookup"><span data-stu-id="96b9e-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="96b9e-131">UDMA \_ MODE1 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="96b9e-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="96b9e-132">UDMA \_ Mode2 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="96b9e-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="96b9e-133">UDMA \_ MODE3 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="96b9e-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="96b9e-134">UDMA \_ MODE4 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="96b9e-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="96b9e-135">UDMA \_ MODE5 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="96b9e-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="96b9e-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="96b9e-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96b9e-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96b9e-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b9e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-139">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="96b9e-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="96b9e-140">El tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96b9e-140">The device type.</span></span> <span data-ttu-id="96b9e-141">Los posibles valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="96b9e-141">The following are the possible values:</span></span>

-   <span data-ttu-id="96b9e-142">ATA (1)</span><span class="sxs-lookup"><span data-stu-id="96b9e-142">ATA (1)</span></span>
-   <span data-ttu-id="96b9e-143">ATAPI (2)</span><span class="sxs-lookup"><span data-stu-id="96b9e-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="96b9e-144">**LocationInformation**</span><span class="sxs-lookup"><span data-stu-id="96b9e-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96b9e-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="96b9e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b9e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-147">Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="96b9e-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="96b9e-148">Canal IDE (por ejemplo, canal principal, canal secundario, etc.).</span><span class="sxs-lookup"><span data-stu-id="96b9e-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="96b9e-149">**LocationInformationLen**</span><span class="sxs-lookup"><span data-stu-id="96b9e-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96b9e-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96b9e-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b9e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-152">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="96b9e-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="96b9e-153">Longitud de la cadena **LocationInformation** .</span><span class="sxs-lookup"><span data-stu-id="96b9e-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="96b9e-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="96b9e-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96b9e-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96b9e-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b9e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96b9e-157">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="96b9e-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="96b9e-158">Identificador del disco.</span><span class="sxs-lookup"><span data-stu-id="96b9e-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96b9e-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96b9e-159">Requirements</span></span>



| <span data-ttu-id="96b9e-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="96b9e-160">Requirement</span></span> | <span data-ttu-id="96b9e-161">Value</span><span class="sxs-lookup"><span data-stu-id="96b9e-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96b9e-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96b9e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="96b9e-163">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96b9e-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96b9e-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96b9e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="96b9e-165">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96b9e-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96b9e-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="96b9e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b9e-167">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="96b9e-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




