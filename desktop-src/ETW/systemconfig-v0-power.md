---
description: 'SystemConfig_V0_Power clase : esta clase es la clase de tipo de evento para los eventos de configuración de energía. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power clase
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
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105943"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="c2d84-104">Clase Power SystemConfig \_ V0 \_</span><span class="sxs-lookup"><span data-stu-id="c2d84-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="c2d84-105">Esta clase es la clase de tipo de evento para los eventos de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="c2d84-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="c2d84-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="c2d84-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d84-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2d84-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c2d84-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2d84-108">Members</span></span>

<span data-ttu-id="c2d84-109">La **clase SystemConfig \_ V0 \_ Power** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2d84-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="c2d84-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2d84-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2d84-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2d84-111">Properties</span></span>

<span data-ttu-id="c2d84-112">La **clase SystemConfig \_ V0 \_ Power** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2d84-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2d84-113">Panel1</span><span class="sxs-lookup"><span data-stu-id="c2d84-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-114">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c2d84-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-116">Calificadores: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="c2d84-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2d84-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-118">Panel2</span><span class="sxs-lookup"><span data-stu-id="c2d84-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-119">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c2d84-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-121">Calificadores: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="c2d84-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2d84-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-123">Panel3</span><span class="sxs-lookup"><span data-stu-id="c2d84-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-124">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c2d84-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-126">Calificadores: WmiDataId(8)</span><span class="sxs-lookup"><span data-stu-id="c2d84-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2d84-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-128">s1</span><span class="sxs-lookup"><span data-stu-id="c2d84-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c2d84-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-131">Calificadores: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="c2d84-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-132">True indica que el sistema admite el estado de suspensión S1.</span><span class="sxs-lookup"><span data-stu-id="c2d84-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-133">s2</span><span class="sxs-lookup"><span data-stu-id="c2d84-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c2d84-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-136">Calificadores: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="c2d84-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-137">True indica que el sistema admite el estado de suspensión S2.</span><span class="sxs-lookup"><span data-stu-id="c2d84-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-138">s3</span><span class="sxs-lookup"><span data-stu-id="c2d84-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c2d84-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-141">Calificadores: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="c2d84-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-142">True indica que el sistema admite el estado de suspensión S3.</span><span class="sxs-lookup"><span data-stu-id="c2d84-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-143">s4</span><span class="sxs-lookup"><span data-stu-id="c2d84-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c2d84-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-146">Calificadores: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="c2d84-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-147">True indica que el sistema admite el estado de suspensión S4.</span><span class="sxs-lookup"><span data-stu-id="c2d84-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="c2d84-148">s5</span><span class="sxs-lookup"><span data-stu-id="c2d84-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d84-149">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c2d84-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d84-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d84-151">Calificadores: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="c2d84-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="c2d84-152">True indica que el sistema admite el estado de suspensión S5.</span><span class="sxs-lookup"><span data-stu-id="c2d84-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2d84-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2d84-153">Requirements</span></span>



| <span data-ttu-id="c2d84-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2d84-154">Requirement</span></span> | <span data-ttu-id="c2d84-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c2d84-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c2d84-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2d84-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c2d84-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c2d84-157">None supported</span></span><br/>                            |
| <span data-ttu-id="c2d84-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2d84-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c2d84-159">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2d84-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2d84-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2d84-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d84-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c2d84-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




