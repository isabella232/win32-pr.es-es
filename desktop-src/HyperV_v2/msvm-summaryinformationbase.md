---
description: Se usa en el método GetSummaryInformation de la \_ clase MSVM VirtualSystemManagementService para recuperar rápidamente información común relacionada con un sistema virtual o una instantánea.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652513"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="5e034-103">MSVM \_ SummaryInformationBase (clase)</span><span class="sxs-lookup"><span data-stu-id="5e034-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="5e034-104">Se usa en el método [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rápidamente información común relacionada con un sistema virtual o una instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="5e034-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5e034-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e034-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e034-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="5e034-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e034-107">Members</span></span>

<span data-ttu-id="5e034-108">La clase **MSVM \_ SummaryInformationBase** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e034-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="5e034-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e034-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e034-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e034-110">Properties</span></span>

<span data-ttu-id="5e034-111">La clase **MSVM \_ SummaryInformationBase** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e034-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e034-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="5e034-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-113">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e034-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-115">La hora a la que se creó el sistema virtual o la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5e034-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement. ElementName")</span><span class="sxs-lookup"><span data-stu-id="5e034-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="5e034-120">Nombre descriptivo del sistema virtual o de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5e034-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e034-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-124">Estado actual del sistema virtual o de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-125">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="5e034-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e034-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-128">Indica si el host permite o no conexiones en modo mejorado y, si se permiten, si están disponibles para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="5e034-129">**Permitido y disponible** (2)</span><span class="sxs-lookup"><span data-stu-id="5e034-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="5e034-130">**No permitido** (3)</span><span class="sxs-lookup"><span data-stu-id="5e034-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="5e034-131">**Permitido pero no disponible** (6)</span><span class="sxs-lookup"><span data-stu-id="5e034-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e034-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5e034-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e034-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-135">El estado de mantenimiento actual del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-135">The current health state for the virtual system.</span></span> <span data-ttu-id="5e034-136">Esta propiedad no es válida para las instancias de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) que representan una instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-137">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="5e034-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-140">Nombre del equipo que hospeda esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5e034-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-144">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement. InstanceId"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5e034-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5e034-145">InstanceID es una propiedad opcional que se puede usar para identificar de forma opaca y única una instancia de esta clase dentro del ámbito del espacio de nombres de la instancia.</span><span class="sxs-lookup"><span data-stu-id="5e034-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="5e034-146">Varias subclases de esta clase pueden invalidar esta propiedad para que sea necesaria, o una clave.</span><span class="sxs-lookup"><span data-stu-id="5e034-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="5e034-147">Estas subclases también pueden modificar los algoritmos preferidos para garantizar la exclusividad que se definen a continuación.</span><span class="sxs-lookup"><span data-stu-id="5e034-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="5e034-148">Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido":</span><span class="sxs-lookup"><span data-stu-id="5e034-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="5e034-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="5e034-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="5e034-150">Donde <OrgID> y <LocalID> se separan con dos puntos (:), donde <OrgID> debe incluir un nombre de propiedad intelectual, marca registrada o de otro tipo, que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un identificador registrado asignado a la entidad empresarial por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="5e034-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="5e034-151">(Este requisito es similar al <Schema Name> \_ <Class Name> estructura de los nombres de clase de esquema.) Además, para garantizar la exclusividad, <OrgID> no debe contener un signo de dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="5e034-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="5e034-152">Al utilizar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre <OrgID> y <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="5e034-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="5e034-153"><LocalID> la entidad de negocio elige y no se debe reutilizar para identificar distintos elementos subyacentes (del mundo real).</span><span class="sxs-lookup"><span data-stu-id="5e034-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="5e034-154">Si no es NULL y no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs generado por este u otros proveedores para el espacio de nombres de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="5e034-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="5e034-155">Si no se establece en null para las instancias definidas por DMTF, se debe usar el algoritmo "preferido" con el <OrgID> establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="5e034-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-156">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5e034-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-159">Nombre único del sistema virtual o de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-160">**Notas**</span><span class="sxs-lookup"><span data-stu-id="5e034-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-163">Notas asociadas al sistema virtual o a la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="5e034-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e034-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-167">El número total de procesadores virtuales asignados al sistema virtual o a la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5e034-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5e034-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-169">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e034-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e034-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-171">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="5e034-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5e034-172">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="5e034-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-173">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5e034-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-176">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="5e034-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="5e034-177">Esta propiedad debe establecerse en NULL cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="5e034-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-178">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5e034-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-179">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5e034-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e034-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-181">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="5e034-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5e034-182">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5e034-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-183">**Actividad**</span><span class="sxs-lookup"><span data-stu-id="5e034-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-184">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e034-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-186">La cantidad de tiempo transcurrido desde el último arranque del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="5e034-187">Esta propiedad no es válida para las instancias de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) que representan una instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-188">**Versión**</span><span class="sxs-lookup"><span data-stu-id="5e034-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-191">La versión del sistema virtual en un formato de "Major. minor"; por ejemplo, "2,0".</span><span class="sxs-lookup"><span data-stu-id="5e034-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="5e034-192">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="5e034-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-193">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5e034-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e034-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e034-195">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="5e034-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5e034-196">Cadenas que muestran los nombres descriptivos de los conmutadores virtuales a los que está conectada la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="5e034-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="5e034-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e034-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e034-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e034-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e034-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e034-200">Subtipo del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5e034-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="5e034-201">**Microsoft: Hyper-v: subtipo: 1** ("Microsoft: Hyper-v: SubType: 1")</span><span class="sxs-lookup"><span data-stu-id="5e034-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="5e034-202">**Microsoft: Hyper-v: subtipo: 2** ("Microsoft: Hyper-v: SubType: 2")</span><span class="sxs-lookup"><span data-stu-id="5e034-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="5e034-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5e034-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5e034-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e034-204">Requirements</span></span>



| <span data-ttu-id="5e034-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e034-205">Requirement</span></span> | <span data-ttu-id="5e034-206">Value</span><span class="sxs-lookup"><span data-stu-id="5e034-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e034-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e034-207">Minimum supported client</span></span><br/> | <span data-ttu-id="5e034-208">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e034-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e034-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e034-209">Minimum supported server</span></span><br/> | <span data-ttu-id="5e034-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5e034-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5e034-211">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e034-211">Namespace</span></span><br/>                | <span data-ttu-id="5e034-212">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5e034-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5e034-213">MOF</span><span class="sxs-lookup"><span data-stu-id="5e034-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e034-214"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e034-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e034-215">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e034-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e034-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e034-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e034-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e034-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e034-218">**\_Vista CIM**</span><span class="sxs-lookup"><span data-stu-id="5e034-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

