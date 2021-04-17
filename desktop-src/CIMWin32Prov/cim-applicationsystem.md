---
description: La \_ clase CIM ApplicationSystem representa una aplicación o un sistema de software que admite una determinada función empresarial que se puede administrar como una unidad independiente.
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: CIM_ApplicationSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659657"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="a259e-103">\_Clase ApplicationSystem de CIM</span><span class="sxs-lookup"><span data-stu-id="a259e-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="a259e-104">La clase **CIM \_ ApplicationSystem** representa una aplicación o un sistema de software que admite una determinada función empresarial que se puede administrar como una unidad independiente.</span><span class="sxs-lookup"><span data-stu-id="a259e-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="a259e-105">Este tipo de sistema se puede descomponer en sus componentes funcionales mediante la clase [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="a259e-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="a259e-106">Las características de software de una aplicación o un sistema de software en particular se encuentran mediante la Asociación [**\_ ApplicationSystemSoftwareFeature de CIM**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="a259e-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a259e-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a259e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a259e-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a259e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a259e-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a259e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a259e-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a259e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a259e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a259e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="a259e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="a259e-112">Members</span></span>

<span data-ttu-id="a259e-113">La clase **CIM \_ ApplicationSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a259e-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a259e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a259e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a259e-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a259e-115">Properties</span></span>

<span data-ttu-id="a259e-116">La clase **CIM \_ ApplicationSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a259e-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a259e-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a259e-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a259e-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a259e-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a259e-121">A short textual description of the object.</span></span>

<span data-ttu-id="a259e-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a259e-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-126">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a259e-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a259e-127">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a259e-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a259e-128">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a259e-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a259e-129">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a259e-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-133">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a259e-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a259e-134">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a259e-134">A textual description of the object.</span></span>

<span data-ttu-id="a259e-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a259e-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-137">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a259e-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a259e-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a259e-140">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a259e-140">Indicates when the object was installed.</span></span> <span data-ttu-id="a259e-141">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="a259e-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a259e-142">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-143">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a259e-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a259e-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a259e-147">Define la etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a259e-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="a259e-148">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="a259e-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a259e-152">Identifica cómo se generó el nombre del sistema, mediante la heurística de subclases.</span><span class="sxs-lookup"><span data-stu-id="a259e-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="a259e-153">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-154">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="a259e-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a259e-157">Cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono o la dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="a259e-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="a259e-158">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-159">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="a259e-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-162">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a259e-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a259e-163">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="a259e-163">Name of the primary system owner.</span></span>

<span data-ttu-id="a259e-164">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-165">**Roles**</span><span class="sxs-lookup"><span data-stu-id="a259e-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-166">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a259e-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a259e-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a259e-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a259e-168">Roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="a259e-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="a259e-169">Las subclases del sistema pueden invalidar esta propiedad para definir valores de rol explícitos.</span><span class="sxs-lookup"><span data-stu-id="a259e-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="a259e-170">Como alternativa, un grupo de trabajo puede describir la heurística, las convenciones y las directrices para especificar los roles.</span><span class="sxs-lookup"><span data-stu-id="a259e-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="a259e-171">Por ejemplo, para una instancia de un sistema de red, esta propiedad puede contener la cadena "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="a259e-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="a259e-172">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="a259e-173">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a259e-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a259e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a259e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a259e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a259e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a259e-176">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a259e-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a259e-177">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a259e-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="a259e-178">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="a259e-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a259e-179">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="a259e-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a259e-180">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="a259e-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a259e-181">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a259e-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a259e-182">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a259e-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a259e-183">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a259e-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a259e-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a259e-185">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a259e-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a259e-186">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a259e-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a259e-187">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a259e-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a259e-188">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a259e-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a259e-189">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a259e-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a259e-190">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a259e-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a259e-191">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a259e-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a259e-192">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a259e-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a259e-193">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a259e-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a259e-194">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a259e-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a259e-195">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a259e-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a259e-196">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a259e-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a259e-197">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a259e-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a259e-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a259e-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a259e-199">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a259e-199">Remarks</span></span>

<span data-ttu-id="a259e-200">La clase **CIM \_ ApplicationSystem** se deriva del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="a259e-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="a259e-201">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a259e-201">WMI does not implement this class.</span></span>

<span data-ttu-id="a259e-202">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a259e-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a259e-203">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a259e-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a259e-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a259e-204">Requirements</span></span>



| <span data-ttu-id="a259e-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="a259e-205">Requirement</span></span> | <span data-ttu-id="a259e-206">Value</span><span class="sxs-lookup"><span data-stu-id="a259e-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a259e-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a259e-207">Minimum supported client</span></span><br/> | <span data-ttu-id="a259e-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a259e-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a259e-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a259e-209">Minimum supported server</span></span><br/> | <span data-ttu-id="a259e-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a259e-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a259e-211">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a259e-211">Namespace</span></span><br/>                | <span data-ttu-id="a259e-212">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a259e-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a259e-213">MOF</span><span class="sxs-lookup"><span data-stu-id="a259e-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a259e-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a259e-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a259e-215">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a259e-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a259e-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a259e-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a259e-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="a259e-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a259e-218">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="a259e-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

