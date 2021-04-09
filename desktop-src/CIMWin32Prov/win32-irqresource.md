---
description: Win32 \_ IRQResource &\# 160; La clase WMI representa un número de línea de solicitud de interrupción (IRQ) en un equipo que ejecuta Windows.
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Win32_IRQResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152914"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="b6e0e-103">\_Clase Win32 IRQResource</span><span class="sxs-lookup"><span data-stu-id="b6e0e-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="b6e0e-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ IRQResource de Win32** representa un número de línea de solicitud de interrupción (IRQ) en un equipo que ejecuta Windows.  </span><span class="sxs-lookup"><span data-stu-id="b6e0e-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="b6e0e-105">Una solicitud de interrupción es una señal enviada a la CPU por un dispositivo o programa para eventos críticos en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="b6e0e-106">La IRQ puede estar basada en hardware o en software.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="b6e0e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b6e0e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e0e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6e0e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="b6e0e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6e0e-110">Members</span></span>

<span data-ttu-id="b6e0e-111">La **clase \_ IRQResource de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6e0e-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="b6e0e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6e0e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6e0e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6e0e-113">Properties</span></span>

<span data-ttu-id="b6e0e-114">La **clase \_ IRQResource de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6e0e-115">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|IRQ DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-119">Disponibilidad de la IRQ.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-119">Availability of the IRQ.</span></span>

<span data-ttu-id="b6e0e-120">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b6e0e-121"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b6e0e-122">Otros</span><span class="sxs-lookup"><span data-stu-id="b6e0e-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b6e0e-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b6e0e-124">Unknown</span><span class="sxs-lookup"><span data-stu-id="b6e0e-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6e0e-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b6e0e-126">Disponible</span><span class="sxs-lookup"><span data-stu-id="b6e0e-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="b6e0e-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b6e0e-128">En uso o no disponible</span><span class="sxs-lookup"><span data-stu-id="b6e0e-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="b6e0e-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En uso/no disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b6e0e-130">En uso y disponible o compartible</span><span class="sxs-lookup"><span data-stu-id="b6e0e-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="b6e0e-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En uso y disponible/compartible** (5)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b6e0e-132">En uso y disponible/compartible</span><span class="sxs-lookup"><span data-stu-id="b6e0e-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6e0e-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-136">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-137">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b6e0e-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-139">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-142">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-143">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b6e0e-144">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b6e0e-145">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-146">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-149">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-150">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="b6e0e-151">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-155">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-156">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="b6e0e-157">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-161">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-162">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-162">Textual description of the object.</span></span>

<span data-ttu-id="b6e0e-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-164">**Hardware**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-165">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-167">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| System Structures \| \_ descriptor \| InterfaceType")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-168">Si es **true**, la interrupción se basa en hardware o software.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="b6e0e-169">Una IRQ de hardware es una conexión física desde el periférico al chip del controlador programable de interrupciones (PIC) a través de la cual se puede notificar a la CPU de eventos críticos en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="b6e0e-170">Algunas líneas IRQ están reservadas para dispositivos estándar, como el teclado, las unidades de disquete y el reloj del sistema.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="b6e0e-171">Una interrupción de software permite a las aplicaciones obtener la atención del procesador.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-173">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-175">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-176">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-176">Date and time the object was installed.</span></span> <span data-ttu-id="b6e0e-177">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b6e0e-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-179">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-180">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-182">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,1 "), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-183">Parte del valor de clave del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-183">Part of the object's key value.</span></span>

<span data-ttu-id="b6e0e-184">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-185">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-188">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-189">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-189">Label by which the object is known.</span></span> <span data-ttu-id="b6e0e-190">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b6e0e-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-192">**Compartible**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-193">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-195">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|IRQ DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-196">Si **es true**, se puede compartir la IRQ.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="b6e0e-197">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e0e-198">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-201">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-202">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-202">Current status of the object.</span></span> <span data-ttu-id="b6e0e-203">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b6e0e-204">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b6e0e-205">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b6e0e-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b6e0e-206">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b6e0e-207">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b6e0e-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b6e0e-209">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6e0e-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b6e0e-210">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b6e0e-211">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b6e0e-212">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6e0e-213">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b6e0e-214">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b6e0e-215">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b6e0e-216">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b6e0e-217">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b6e0e-218">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b6e0e-219">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b6e0e-220">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b6e0e-221">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6e0e-222">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-225">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información de IRQ del recurso del sistema DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-226">Nivel de desencadenador de IRQ que indica si la interrupción se desencadena por la señal de hardware que va a ser alta (4) o baja (3).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="b6e0e-227">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b6e0e-228">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6e0e-229">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="b6e0e-230">**Bajo activo** (3)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="b6e0e-231">**Activo alto** (4)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6e0e-232">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-233">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-235">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,3 "," MIF. \|Información de IRQ del recurso del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-236">Tipo de desencadenador de IRQ que indica si se producen interrupciones desencadenadas por el borde (4) o por el nivel (3).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="b6e0e-237">Esta propiedad se hereda de [**la \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b6e0e-238">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6e0e-239">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="b6e0e-240">**Nivel** (3)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="b6e0e-241">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6e0e-242">**Vector**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e0e-243">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6e0e-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e0e-245">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| nivel de interrupción del \| [**\_ \_ \_ descriptor de recursos parciales**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)de inesperados win32api de estructuras del sistema \| \| ")</span><span class="sxs-lookup"><span data-stu-id="b6e0e-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="b6e0e-246">Vector del recurso de IRQ de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="b6e0e-247">Un vector contiene la dirección de memoria de la función que se ejecutará una vez que la CPU confirme la solicitud de interrupción.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e0e-248">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6e0e-248">Remarks</span></span>

<span data-ttu-id="b6e0e-249">La **clase \_ IRQResource de Win32** se deriva de la [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b6e0e-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e0e-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e0e-250">Requirements</span></span>



| <span data-ttu-id="b6e0e-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e0e-251">Requirement</span></span> | <span data-ttu-id="b6e0e-252">Value</span><span class="sxs-lookup"><span data-stu-id="b6e0e-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e0e-253">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6e0e-253">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e0e-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6e0e-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6e0e-255">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6e0e-255">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e0e-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6e0e-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6e0e-257">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6e0e-257">Namespace</span></span><br/>                | <span data-ttu-id="b6e0e-258">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b6e0e-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6e0e-259">MOF</span><span class="sxs-lookup"><span data-stu-id="b6e0e-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6e0e-260"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6e0e-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6e0e-261">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6e0e-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6e0e-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6e0e-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e0e-263">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6e0e-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e0e-264">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="b6e0e-265">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="b6e0e-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

