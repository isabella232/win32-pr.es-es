---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de energía. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984394"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="0322f-104">\_ \_ Clase Power de SystemConfig v0</span><span class="sxs-lookup"><span data-stu-id="0322f-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="0322f-105">Esta clase es la clase de tipo de evento para los eventos de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="0322f-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="0322f-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="0322f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0322f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0322f-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="0322f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0322f-108">Members</span></span>

<span data-ttu-id="0322f-109">La **clase \_ \_ Power de SystemConfig V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0322f-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="0322f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0322f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0322f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0322f-111">Properties</span></span>

<span data-ttu-id="0322f-112">La **clase \_ \_ Power de SystemConfig V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0322f-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0322f-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="0322f-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-114">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0322f-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-116">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="0322f-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0322f-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="0322f-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-119">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0322f-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-121">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="0322f-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0322f-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="0322f-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-124">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0322f-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-126">Calificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="0322f-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0322f-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-128">s1</span><span class="sxs-lookup"><span data-stu-id="0322f-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0322f-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-131">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="0322f-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-132">True indica que el sistema admite el estado de suspensión S1.</span><span class="sxs-lookup"><span data-stu-id="0322f-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-133">s2</span><span class="sxs-lookup"><span data-stu-id="0322f-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0322f-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-136">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="0322f-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-137">True indica que el sistema admite el estado de suspensión S2.</span><span class="sxs-lookup"><span data-stu-id="0322f-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-138">s3</span><span class="sxs-lookup"><span data-stu-id="0322f-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0322f-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-141">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="0322f-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-142">True indica que el sistema admite el estado de suspensión S3.</span><span class="sxs-lookup"><span data-stu-id="0322f-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-143">S4</span><span class="sxs-lookup"><span data-stu-id="0322f-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0322f-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-146">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="0322f-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-147">True indica que el sistema admite el estado de suspensión S4.</span><span class="sxs-lookup"><span data-stu-id="0322f-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="0322f-148">S5</span><span class="sxs-lookup"><span data-stu-id="0322f-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0322f-149">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0322f-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0322f-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0322f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0322f-151">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="0322f-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="0322f-152">True indica que el sistema admite el estado de suspensión S5.</span><span class="sxs-lookup"><span data-stu-id="0322f-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0322f-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0322f-153">Requirements</span></span>



| <span data-ttu-id="0322f-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="0322f-154">Requirement</span></span> | <span data-ttu-id="0322f-155">Value</span><span class="sxs-lookup"><span data-stu-id="0322f-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0322f-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0322f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0322f-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0322f-157">None supported</span></span><br/>                            |
| <span data-ttu-id="0322f-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0322f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0322f-159">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0322f-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0322f-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="0322f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0322f-161">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0322f-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




