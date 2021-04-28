---
description: 'SystemConfig_Power clase : esta clase es la clase de tipo de evento para los eventos de configuración de energía. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: SystemConfig_Power clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106073"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="f3dd5-104">SystemConfig \_ Power (clase)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="f3dd5-105">Esta clase es la clase de tipo de evento para los eventos de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="f3dd5-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3dd5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3dd5-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="f3dd5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3dd5-108">Members</span></span>

<span data-ttu-id="f3dd5-109">La **clase SystemConfig \_ Power** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f3dd5-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="f3dd5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3dd5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3dd5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3dd5-111">Properties</span></span>

<span data-ttu-id="f3dd5-112">La **clase SystemConfig \_ Power** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3dd5-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="f3dd5-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-114">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-116">Calificadores: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="f3dd5-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-119">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-121">Calificadores: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="f3dd5-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-124">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-126">Calificadores: WmiDataId(8)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-127">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-128">s1</span><span class="sxs-lookup"><span data-stu-id="f3dd5-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-129">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-131">Calificadores: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-132">True indica que el sistema admite el estado de suspensión S1.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-133">s2</span><span class="sxs-lookup"><span data-stu-id="f3dd5-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-134">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-136">Calificadores: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-137">True indica que el sistema admite el estado de suspensión S2.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-138">s3</span><span class="sxs-lookup"><span data-stu-id="f3dd5-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-139">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-141">Calificadores: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-142">True indica que el sistema admite el estado de suspensión S3.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-143">s4</span><span class="sxs-lookup"><span data-stu-id="f3dd5-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-144">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-146">Calificadores: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-147">True indica que el sistema admite el estado de suspensión S4.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="f3dd5-148">s5</span><span class="sxs-lookup"><span data-stu-id="f3dd5-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3dd5-149">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3dd5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3dd5-151">Calificadores: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="f3dd5-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="f3dd5-152">True indica que el sistema admite el estado de suspensión S5.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3dd5-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3dd5-153">Requirements</span></span>



| <span data-ttu-id="f3dd5-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3dd5-154">Requirement</span></span> | <span data-ttu-id="f3dd5-155">Valor</span><span class="sxs-lookup"><span data-stu-id="f3dd5-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3dd5-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3dd5-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f3dd5-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3dd5-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3dd5-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3dd5-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f3dd5-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3dd5-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3dd5-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f3dd5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3dd5-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dd5-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




