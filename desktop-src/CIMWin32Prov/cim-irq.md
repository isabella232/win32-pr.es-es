---
description: La \_ clase de IRQ CIM representa una línea de solicitud de interrupción (IRQ) de arquitectura Intel.
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: CIM_IRQ (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907289"
---
# <a name="cim_irq-class"></a><span data-ttu-id="7c0b5-103">CIM ( \_ clase)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-103">CIM\_IRQ class</span></span>

<span data-ttu-id="7c0b5-104">La clase de **\_ IRQ CIM** representa una línea de solicitud de interrupción (IRQ) de arquitectura Intel.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c0b5-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c0b5-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7c0b5-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7c0b5-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0b5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c0b5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="7c0b5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c0b5-110">Members</span></span>

<span data-ttu-id="7c0b5-111">La clase de **\_ IRQ CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7c0b5-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="7c0b5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c0b5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c0b5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c0b5-113">Properties</span></span>

<span data-ttu-id="7c0b5-114">La clase de **\_ IRQ CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c0b5-115">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|IRQ DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-119">Disponibilidad de la IRQ.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c0b5-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c0b5-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="7c0b5-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="7c0b5-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En uso/no disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="7c0b5-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En uso y disponible/compartible** (5)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7c0b5-125">En uso y disponible/compartible</span><span class="sxs-lookup"><span data-stu-id="7c0b5-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7c0b5-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-129">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-130">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-130">A short textual description of the object.</span></span>

<span data-ttu-id="7c0b5-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-135">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-136">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7c0b5-137">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-141">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-142">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-146">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-147">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-148">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-151">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-152">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-152">A textual description of the object.</span></span>

<span data-ttu-id="7c0b5-153">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-155">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-157">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-158">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-158">Indicates when the object was installed.</span></span> <span data-ttu-id="7c0b5-159">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7c0b5-160">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-161">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-164">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,1 "), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-165">Parte del valor de clave del objeto, número de IRQ.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-166">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-169">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-170">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-170">Label by which the object is known.</span></span> <span data-ttu-id="7c0b5-171">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7c0b5-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-173">**Compartible**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-174">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-176">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|IRQ DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-177">Si **es true**, se puede compartir la IRQ.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="7c0b5-178">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-181">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-182">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="7c0b5-183">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7c0b5-184">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="7c0b5-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7c0b5-185">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7c0b5-186">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7c0b5-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7c0b5-187">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7c0b5-188">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7c0b5-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7c0b5-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7c0b5-190">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7c0b5-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7c0b5-191">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7c0b5-192">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7c0b5-193">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c0b5-194">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7c0b5-195">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7c0b5-196">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7c0b5-197">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7c0b5-198">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7c0b5-199">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7c0b5-200">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7c0b5-201">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7c0b5-202">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c0b5-203">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-204">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-206">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información de IRQ del recurso del sistema DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-207">Indica si la interrupción se desencadena por la señal de hardware que va a ser alta o baja.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c0b5-208">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c0b5-209">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="7c0b5-210">**Bajo activo** (3)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="7c0b5-211">**Activo alto** (4)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c0b5-212">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0b5-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c0b5-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0b5-215">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,3 "," MIF. \|Información de IRQ del recurso del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="7c0b5-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="7c0b5-216">Tipo de interrupción que se puede producir.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c0b5-217">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c0b5-218">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="7c0b5-219">**Nivel** (3)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="7c0b5-220">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="7c0b5-220">**Edge** (4)</span></span>


<span data-ttu-id="7c0b5-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7c0b5-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7c0b5-222">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c0b5-222">Remarks</span></span>

<span data-ttu-id="7c0b5-223">La clase de **\_ IRQ CIM** se deriva de [**CIM \_ SystemResource**](cim-systemresource.md). WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="7c0b5-224">Vea [clases Win32](win32-provider.md) para las clases derivadas de la **\_ IRQ CIM**.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="7c0b5-225">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c0b5-226">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7c0b5-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0b5-227">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c0b5-227">Requirements</span></span>



| <span data-ttu-id="7c0b5-228">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c0b5-228">Requirement</span></span> | <span data-ttu-id="7c0b5-229">Value</span><span class="sxs-lookup"><span data-stu-id="7c0b5-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0b5-230">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c0b5-230">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0b5-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c0b5-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c0b5-232">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c0b5-232">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0b5-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c0b5-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c0b5-234">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c0b5-234">Namespace</span></span><br/>                | <span data-ttu-id="7c0b5-235">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7c0b5-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c0b5-236">MOF</span><span class="sxs-lookup"><span data-stu-id="7c0b5-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c0b5-237"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c0b5-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c0b5-238">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c0b5-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c0b5-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c0b5-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c0b5-240">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c0b5-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0b5-241">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="7c0b5-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

