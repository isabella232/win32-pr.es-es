---
description: Define la configuración para la migración del sistema virtual administrada por una instancia de la \_ clase VirtualSystemMigrationService de CIM.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813387"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="bbfc1-103">\_Clase VirtualSystemMigrationSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="bbfc1-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="bbfc1-104">Define la configuración para la migración del sistema virtual administrada por una instancia de la clase [**\_ VirtualSystemMigrationService de CIM**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="bbfc1-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfc1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbfc1-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="bbfc1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbfc1-106">Members</span></span>

<span data-ttu-id="bbfc1-107">La clase **CIM \_ VirtualSystemMigrationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bbfc1-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="bbfc1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbfc1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbfc1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbfc1-109">Properties</span></span>

<span data-ttu-id="bbfc1-110">La clase **CIM \_ VirtualSystemMigrationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbfc1-111">**Ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbfc1-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbfc1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-114">Calificadores: [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span><span class="sxs-lookup"><span data-stu-id="bbfc1-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="bbfc1-115">Ancho de banda asignado a o solicitado para una operación de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="bbfc1-116">"0" es el ancho de banda predeterminado para las solicitudes de migración.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="bbfc1-117">Las propiedades de **ancho de banda** y **prioridad** se pueden usar conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="bbfc1-118">Los procesos de migración que tienen los valores de **prioridad** más altos comparten el ancho de banda disponible según el ancho de banda solicitado.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="bbfc1-119">Si este conjunto de procesos no consume todo el ancho de banda, los procesos de migración con los valores de **prioridad** inferior siguientes comparten el ancho de banda restante.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="bbfc1-120">Si se mantiene más ancho de banda, se tienen en cuenta los procesos de migración con los siguientes valores de **prioridad** inferiores.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="bbfc1-121">La unidad usada en la propiedad **ancho de banda** se especifica mediante el valor de la propiedad **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="bbfc1-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="bbfc1-122">Si el valor de la propiedad **BandwidthUnit** es "Percent", se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="bbfc1-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="bbfc1-123">El valor de la propiedad de **ancho de banda** debe estar entre "0" y "100", con valores más altos que indiquen un ancho de banda mayor.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="bbfc1-124">Un valor de "100" indica todo el ancho de banda disponible para realizar operaciones de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="bbfc1-125">Los valores entre "1" y "100" se correlacionan linealmente con el intervalo de ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="bbfc1-126">Por ejemplo, un valor de 50 solicita la mitad del ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="bbfc1-127">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbfc1-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbfc1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-130">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Ancho de banda**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="bbfc1-131">Unidad usada por la propiedad de **ancho de banda** .</span><span class="sxs-lookup"><span data-stu-id="bbfc1-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="bbfc1-132">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación definido en el Apéndice C. 1 de DSP0004 V 2.4 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="bbfc1-133">Los perfiles como DMTF DSP1081 definen cómo los clientes pueden detectar el conjunto de unidades admitidas por una implementación, y intervalos e incrementos para los valores de la propiedad de **ancho de banda** .</span><span class="sxs-lookup"><span data-stu-id="bbfc1-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="bbfc1-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbfc1-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbfc1-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbfc1-137">Tipo de operación de migración que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbfc1-138">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bbfc1-139">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="bbfc1-140">**Live** (2)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="bbfc1-141">**Reanudar** (3)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="bbfc1-142">**Reiniciar** (4)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbfc1-143">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbfc1-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbfc1-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-146">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")</span><span class="sxs-lookup"><span data-stu-id="bbfc1-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="bbfc1-147">Tipo de transporte que se va a aplicar si el valor de **TransportType** es "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="bbfc1-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="bbfc1-148">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbfc1-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbfc1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbfc1-151">Importancia de la migración relativa que la implementación de la migración del sistema virtual puede usar para ordenar o asignar preferencias entre varias solicitudes de migración pendientes.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="bbfc1-152">Cuanto menor sea el valor, mayor será la prioridad.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="bbfc1-153">"0" es el ancho de banda predeterminado para las solicitudes de migración.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="bbfc1-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbfc1-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbfc1-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbfc1-157">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")</span><span class="sxs-lookup"><span data-stu-id="bbfc1-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="bbfc1-158">El tipo de transporte que se va a aplicar a una operación de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbfc1-159">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bbfc1-160">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="bbfc1-161">**Ssh** (2)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="bbfc1-162">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="bbfc1-163">**TLS STRICT** (4)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="bbfc1-164">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="bbfc1-165">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bbfc1-166">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bbfc1-167">**Proveedor reservado** (32768...)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="bbfc1-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bbfc1-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bbfc1-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbfc1-169">Requirements</span></span>



| <span data-ttu-id="bbfc1-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbfc1-170">Requirement</span></span> | <span data-ttu-id="bbfc1-171">Value</span><span class="sxs-lookup"><span data-stu-id="bbfc1-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfc1-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbfc1-172">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfc1-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bbfc1-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bbfc1-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbfc1-174">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfc1-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bbfc1-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bbfc1-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bbfc1-176">Namespace</span></span><br/>                | <span data-ttu-id="bbfc1-177">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bbfc1-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bbfc1-178">MOF</span><span class="sxs-lookup"><span data-stu-id="bbfc1-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbfc1-179"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbfc1-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbfc1-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbfc1-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbfc1-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bbfc1-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bbfc1-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbfc1-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbfc1-183">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

