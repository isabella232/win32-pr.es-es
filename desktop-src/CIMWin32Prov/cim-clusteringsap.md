---
description: La \_ clase CIM ClusteringSAP representa los puntos de acceso de un servicio de agrupación en clústeres.
ms.assetid: 7a95f4b0-b9fc-4dba-ad2d-1b6db1539a57
ms.tgt_platform: multiple
title: CIM_ClusteringSAP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringSAP
- CIM_ClusteringSAP.Caption
- CIM_ClusteringSAP.Description
- CIM_ClusteringSAP.InstallDate
- CIM_ClusteringSAP.Status
- CIM_ClusteringSAP.CreationClassName
- CIM_ClusteringSAP.Name
- CIM_ClusteringSAP.SystemCreationClassName
- CIM_ClusteringSAP.SystemName
- CIM_ClusteringSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc2d0296201e06382563cc3a0c34fec4d668cd58
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275016"
---
# <a name="cim_clusteringsap-class"></a><span data-ttu-id="15a0e-103">\_Clase ClusteringSAP de CIM</span><span class="sxs-lookup"><span data-stu-id="15a0e-103">CIM\_ClusteringSAP class</span></span>

<span data-ttu-id="15a0e-104">La clase **CIM \_ ClusteringSAP** representa los puntos de acceso de un servicio de agrupación en clústeres.</span><span class="sxs-lookup"><span data-stu-id="15a0e-104">The **CIM\_ClusteringSAP** class represents the access points of a clustering service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15a0e-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="15a0e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15a0e-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15a0e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="15a0e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="15a0e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="15a0e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="15a0e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a0e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15a0e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2bb2b772-ffed-4aa6-b1b3-3d0cb74fc613}"), AMENDMENT]
class CIM_ClusteringSAP : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="15a0e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="15a0e-110">Members</span></span>

<span data-ttu-id="15a0e-111">La clase **CIM \_ ClusteringSAP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15a0e-111">The **CIM\_ClusteringSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="15a0e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15a0e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15a0e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15a0e-113">Properties</span></span>

<span data-ttu-id="15a0e-114">La clase **CIM \_ ClusteringSAP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15a0e-114">The **CIM\_ClusteringSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15a0e-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="15a0e-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="15a0e-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="15a0e-119">A short textual description of the object.</span></span>

<span data-ttu-id="15a0e-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="15a0e-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-124">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="15a0e-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-125">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="15a0e-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="15a0e-126">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="15a0e-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="15a0e-127">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15a0e-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-131">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="15a0e-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-132">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="15a0e-132">A textual description of the object.</span></span>

<span data-ttu-id="15a0e-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="15a0e-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-135">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15a0e-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="15a0e-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-138">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="15a0e-138">Indicates when the object was installed.</span></span> <span data-ttu-id="15a0e-139">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="15a0e-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="15a0e-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="15a0e-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-144">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="15a0e-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-145">Identifica de forma única el punto de acceso al servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="15a0e-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="15a0e-146">Esta funcionalidad se describe con más detalle en la propiedad Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="15a0e-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="15a0e-147">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-148">**Estado**</span><span class="sxs-lookup"><span data-stu-id="15a0e-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="15a0e-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-152">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="15a0e-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="15a0e-153">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="15a0e-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="15a0e-154">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="15a0e-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="15a0e-155">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="15a0e-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="15a0e-156">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="15a0e-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="15a0e-157">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="15a0e-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="15a0e-158">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="15a0e-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="15a0e-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="15a0e-160">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="15a0e-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="15a0e-161">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="15a0e-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="15a0e-162">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="15a0e-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="15a0e-163">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="15a0e-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15a0e-164">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="15a0e-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="15a0e-165">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="15a0e-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="15a0e-166">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="15a0e-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="15a0e-167">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="15a0e-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="15a0e-168">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="15a0e-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="15a0e-169">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="15a0e-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="15a0e-170">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="15a0e-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="15a0e-171">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="15a0e-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="15a0e-172">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="15a0e-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15a0e-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="15a0e-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-176">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="15a0e-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-177">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="15a0e-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="15a0e-178">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="15a0e-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15a0e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-182">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="15a0e-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-183">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="15a0e-183">The scoping system's name.</span></span>

<span data-ttu-id="15a0e-184">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="15a0e-185">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="15a0e-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15a0e-186">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15a0e-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15a0e-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15a0e-188">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="15a0e-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="15a0e-189">Tipo de SAP, como adjuntado o redirigido.</span><span class="sxs-lookup"><span data-stu-id="15a0e-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="15a0e-190">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="15a0e-191">**Escritura** (1)</span><span class="sxs-lookup"><span data-stu-id="15a0e-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="15a0e-192">**Lectura** (2)</span><span class="sxs-lookup"><span data-stu-id="15a0e-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="15a0e-193">**Redirigido** (4)</span><span class="sxs-lookup"><span data-stu-id="15a0e-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="15a0e-194">**Net \_ Adjunta** (8)</span><span class="sxs-lookup"><span data-stu-id="15a0e-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15a0e-195">**desconocido** (16)</span><span class="sxs-lookup"><span data-stu-id="15a0e-195">**unknown** (16)</span></span>


<span data-ttu-id="15a0e-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="15a0e-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="15a0e-197">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15a0e-197">Remarks</span></span>

<span data-ttu-id="15a0e-198">La clase **CIM \_ ClusteringSAP** se deriva de [**\_ punto de CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="15a0e-198">The **CIM\_ClusteringSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="15a0e-199">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="15a0e-199">WMI does not implement this class.</span></span>

<span data-ttu-id="15a0e-200">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="15a0e-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15a0e-201">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="15a0e-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a0e-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15a0e-202">Requirements</span></span>



| <span data-ttu-id="15a0e-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="15a0e-203">Requirement</span></span> | <span data-ttu-id="15a0e-204">Value</span><span class="sxs-lookup"><span data-stu-id="15a0e-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15a0e-205">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15a0e-205">Minimum supported client</span></span><br/> | <span data-ttu-id="15a0e-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15a0e-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15a0e-207">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15a0e-207">Minimum supported server</span></span><br/> | <span data-ttu-id="15a0e-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15a0e-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15a0e-209">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15a0e-209">Namespace</span></span><br/>                | <span data-ttu-id="15a0e-210">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="15a0e-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15a0e-211">MOF</span><span class="sxs-lookup"><span data-stu-id="15a0e-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15a0e-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15a0e-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15a0e-213">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15a0e-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15a0e-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15a0e-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a0e-215">Vea también</span><span class="sxs-lookup"><span data-stu-id="15a0e-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a0e-216">**\_Punto CIM**</span><span class="sxs-lookup"><span data-stu-id="15a0e-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

