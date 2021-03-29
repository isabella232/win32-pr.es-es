---
description: La \_ clase CIM DeviceErrorCounts es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico. Los tipos de errores se definen mediante CCITt (REC X. 733) e ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: CIM_DeviceErrorCounts (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000693"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="858af-104">\_Clase DeviceErrorCounts de CIM</span><span class="sxs-lookup"><span data-stu-id="858af-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="858af-105">La clase **CIM \_ DeviceErrorCounts** es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="858af-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="858af-106">Los tipos de errores se definen mediante CCITt (REC X. 733) e ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="858af-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="858af-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="858af-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="858af-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="858af-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="858af-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="858af-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="858af-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="858af-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="858af-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="858af-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="858af-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="858af-112">Members</span></span>

<span data-ttu-id="858af-113">La clase **CIM \_ DeviceErrorCounts** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="858af-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="858af-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="858af-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="858af-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="858af-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="858af-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="858af-116">Methods</span></span>

<span data-ttu-id="858af-117">La clase **CIM \_ DeviceErrorCounts** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="858af-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="858af-118">Método</span><span class="sxs-lookup"><span data-stu-id="858af-118">Method</span></span>                                                                     | <span data-ttu-id="858af-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="858af-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="858af-120">**ResetCounter**</span><span class="sxs-lookup"><span data-stu-id="858af-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="858af-121">Restablece los contadores de error y ADVERTENCIA.</span><span class="sxs-lookup"><span data-stu-id="858af-121">Resets the error and warning counters.</span></span> <span data-ttu-id="858af-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="858af-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="858af-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="858af-123">Properties</span></span>

<span data-ttu-id="858af-124">La clase **CIM \_ DeviceErrorCounts** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="858af-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="858af-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="858af-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-128">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="858af-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="858af-129">Breve descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="858af-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="858af-130">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="858af-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="858af-131">**CriticalErrorCount**</span><span class="sxs-lookup"><span data-stu-id="858af-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-132">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="858af-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="858af-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-134">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="858af-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="858af-135">Recuento de los errores críticos.</span><span class="sxs-lookup"><span data-stu-id="858af-135">Count of the critical errors.</span></span>

<span data-ttu-id="858af-136">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="858af-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="858af-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="858af-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="858af-140">Descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="858af-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="858af-141">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="858af-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="858af-142">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="858af-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-145">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**CreationClassName**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="858af-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="858af-146">Propiedad **CreationClassName** del dispositivo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="858af-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="858af-147">**ID**</span><span class="sxs-lookup"><span data-stu-id="858af-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-150">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**DeviceID**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="858af-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="858af-151">Identificador del dispositivo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="858af-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="858af-152">**IndeterminateErrorCount**</span><span class="sxs-lookup"><span data-stu-id="858af-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-153">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="858af-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="858af-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="858af-155">Recuento de los errores indeterminados.</span><span class="sxs-lookup"><span data-stu-id="858af-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="858af-156">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="858af-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="858af-157">**MajorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="858af-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-158">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="858af-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="858af-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-160">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="858af-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="858af-161">Recuento de los errores principales.</span><span class="sxs-lookup"><span data-stu-id="858af-161">Count of the major errors.</span></span>

<span data-ttu-id="858af-162">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="858af-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="858af-163">**MinorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="858af-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-164">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="858af-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="858af-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="858af-166">Recuento de los errores menores.</span><span class="sxs-lookup"><span data-stu-id="858af-166">Count of the minor errors.</span></span>

<span data-ttu-id="858af-167">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="858af-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="858af-168">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="858af-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-171">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="858af-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="858af-172">La propiedad de nombre heredado sirve como parte de la clave de la instancia de **\_ DeviceErrorCounts de CIM** .</span><span class="sxs-lookup"><span data-stu-id="858af-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="858af-173">El ámbito del objeto es el dispositivo lógico al que se aplican las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="858af-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="858af-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="858af-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-177">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**SystemCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="858af-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="858af-178">El ámbito de **CreationClassName** del sistema.</span><span class="sxs-lookup"><span data-stu-id="858af-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="858af-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="858af-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="858af-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="858af-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-182">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**SystemName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="858af-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="858af-183">Propiedad de **nombre** del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="858af-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="858af-184">**WarningCount**</span><span class="sxs-lookup"><span data-stu-id="858af-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="858af-185">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="858af-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="858af-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="858af-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="858af-187">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="858af-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="858af-188">Recuento de las advertencias.</span><span class="sxs-lookup"><span data-stu-id="858af-188">Count of the warnings.</span></span>

<span data-ttu-id="858af-189">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="858af-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="858af-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="858af-190">Remarks</span></span>

<span data-ttu-id="858af-191">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="858af-191">WMI does not implement this class.</span></span>

<span data-ttu-id="858af-192">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="858af-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="858af-193">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="858af-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="858af-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="858af-194">Requirements</span></span>



| <span data-ttu-id="858af-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="858af-195">Requirement</span></span> | <span data-ttu-id="858af-196">Value</span><span class="sxs-lookup"><span data-stu-id="858af-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="858af-197">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="858af-197">Minimum supported client</span></span><br/> | <span data-ttu-id="858af-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="858af-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="858af-199">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="858af-199">Minimum supported server</span></span><br/> | <span data-ttu-id="858af-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="858af-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="858af-201">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="858af-201">Namespace</span></span><br/>                | <span data-ttu-id="858af-202">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="858af-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="858af-203">MOF</span><span class="sxs-lookup"><span data-stu-id="858af-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="858af-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="858af-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="858af-205">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="858af-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="858af-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="858af-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="858af-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="858af-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="858af-208">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="858af-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

