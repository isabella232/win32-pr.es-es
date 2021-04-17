---
description: Win32 \_ QuickFixEngineering&\# 8194; La clase WMI representa una pequeña actualización en todo el sistema, a la que se suele hacer referencia como una actualización de ingeniería de corrección rápida (QFE), que se aplica al sistema operativo actual.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Win32_QuickFixEngineering (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652333"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="b7760-103">\_Clase Win32 QuickFixEngineering</span><span class="sxs-lookup"><span data-stu-id="b7760-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="b7760-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ QuickFixEngineering de Win32** representa una pequeña actualización en todo el sistema, a la que se suele hacer referencia como una actualización de ingeniería de corrección rápida (QFE), que se aplica al sistema operativo actual.</span><span class="sxs-lookup"><span data-stu-id="b7760-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="b7760-105">Esta clase devuelve solo las actualizaciones proporcionadas por el servicio basado en componentes (CBS).</span><span class="sxs-lookup"><span data-stu-id="b7760-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="b7760-106">Estas actualizaciones no aparecen en el registro.</span><span class="sxs-lookup"><span data-stu-id="b7760-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="b7760-107">Las actualizaciones proporcionadas por Microsoft Windows Installer (MSI) o el sitio de Windows Update ( [https://update.microsoft.com](https://update.microsoft.com/) ) no son devueltas por **\_ QuickFixEngineering de Win32**.</span><span class="sxs-lookup"><span data-stu-id="b7760-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="b7760-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b7760-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b7760-109">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b7760-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7760-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7760-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="b7760-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7760-111">Members</span></span>

<span data-ttu-id="b7760-112">La **clase \_ QuickFixEngineering de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b7760-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="b7760-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7760-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7760-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7760-114">Properties</span></span>

<span data-ttu-id="b7760-115">La **clase \_ QuickFixEngineering de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b7760-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7760-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b7760-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-119">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b7760-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-120">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7760-120">A short textual description of the object.</span></span>

<span data-ttu-id="b7760-121">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7760-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7760-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b7760-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-125">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ")</span><span class="sxs-lookup"><span data-stu-id="b7760-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-126">Nombre local del equipo.</span><span class="sxs-lookup"><span data-stu-id="b7760-126">Local name of the computer system.</span></span> <span data-ttu-id="b7760-127">El valor de esta propiedad procede de la clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="b7760-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b7760-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7760-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-131">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b7760-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-132">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7760-132">A textual description of the object.</span></span>

<span data-ttu-id="b7760-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7760-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7760-134">**FixComments**</span><span class="sxs-lookup"><span data-stu-id="b7760-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-137">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="b7760-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-138">Comentarios adicionales relacionados con la actualización.</span><span class="sxs-lookup"><span data-stu-id="b7760-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="b7760-139">**HotFixID**</span><span class="sxs-lookup"><span data-stu-id="b7760-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-142">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="b7760-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-143">Identificador único asociado a una actualización determinada.</span><span class="sxs-lookup"><span data-stu-id="b7760-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="b7760-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b7760-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-145">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7760-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-147">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b7760-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-148">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b7760-148">Indicates when the object was installed.</span></span> <span data-ttu-id="b7760-149">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="b7760-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b7760-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7760-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7760-151">**InstalledBy**</span><span class="sxs-lookup"><span data-stu-id="b7760-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-154">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="b7760-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-155">Persona que instaló la actualización.</span><span class="sxs-lookup"><span data-stu-id="b7760-155">Person who installed the update.</span></span> <span data-ttu-id="b7760-156">Si no se conoce este valor, la propiedad está vacía.</span><span class="sxs-lookup"><span data-stu-id="b7760-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="b7760-157">**InstalledOn**</span><span class="sxs-lookup"><span data-stu-id="b7760-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-160">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="b7760-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-161">Fecha en que se instaló la actualización.</span><span class="sxs-lookup"><span data-stu-id="b7760-161">Date that the update was installed.</span></span> <span data-ttu-id="b7760-162">Si no se conoce este valor, la propiedad está vacía.</span><span class="sxs-lookup"><span data-stu-id="b7760-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="b7760-163">Esta propiedad puede usar formatos diferentes, dependiendo de Cuándo se haya instalado QuickFix.</span><span class="sxs-lookup"><span data-stu-id="b7760-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="b7760-164">La mayoría de los sistemas utilizan un formato de fecha estándar, como "23-10-2013".</span><span class="sxs-lookup"><span data-stu-id="b7760-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="b7760-165">Sin embargo, algunos sistemas pueden devolver un valor hexadecimal de 64 bits en el formato [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) de Win32.</span><span class="sxs-lookup"><span data-stu-id="b7760-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="b7760-166">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b7760-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-169">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b7760-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-170">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b7760-170">Label by which the object is known.</span></span> <span data-ttu-id="b7760-171">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b7760-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b7760-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7760-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7760-173">**ServicePackInEffect**</span><span class="sxs-lookup"><span data-stu-id="b7760-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-176">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="b7760-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-177">Service Pack en vigor cuando se aplicó la actualización.</span><span class="sxs-lookup"><span data-stu-id="b7760-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="b7760-178">Si no se ha aplicado ningún Service Pack, la propiedad toma el valor SP0.</span><span class="sxs-lookup"><span data-stu-id="b7760-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="b7760-179">Si no se puede determinar qué Service Pack estaba en vigor, esta propiedad es **null**.</span><span class="sxs-lookup"><span data-stu-id="b7760-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b7760-180">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b7760-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7760-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7760-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7760-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7760-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7760-183">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b7760-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b7760-184">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7760-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="b7760-185">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="b7760-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b7760-186">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="b7760-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b7760-187">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="b7760-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b7760-188">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b7760-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b7760-189">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b7760-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b7760-190">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b7760-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b7760-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7760-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b7760-192">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7760-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b7760-193">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b7760-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b7760-194">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b7760-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b7760-195">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b7760-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7760-196">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b7760-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b7760-197">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b7760-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b7760-198">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b7760-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b7760-199">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b7760-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b7760-200">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b7760-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b7760-201">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b7760-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b7760-202">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b7760-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b7760-203">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b7760-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b7760-204">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b7760-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b7760-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b7760-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b7760-206">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7760-206">Remarks</span></span>

<span data-ttu-id="b7760-207">La **clase \_ QuickFixEngineering de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7760-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b7760-208">Dado que las actualizaciones se almacenan en dos lugares, una enumeración de esta clase puede producir duplicados.</span><span class="sxs-lookup"><span data-stu-id="b7760-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="b7760-209">Una corrección urgente es una revisión del sistema operativo temporal creada por el grupo de ingeniería de corrección rápida en Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7760-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="b7760-210">Al igual que los Service Pack, las correcciones activas representan cambios que se han realizado en una versión de Windows una vez que se ha publicado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b7760-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="b7760-211">A diferencia de los Service Pack, las correcciones urgentes no están destinadas a la instalación global en todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="b7760-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="b7760-212">En su lugar, se desarrollan para solucionar problemas muy concretos, a menudo para configuraciones específicas de equipos.</span><span class="sxs-lookup"><span data-stu-id="b7760-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="b7760-213">Además, las revisiones de acceso frecuente representan instalaciones independientes que no dependen de otras correcciones activas publicadas.</span><span class="sxs-lookup"><span data-stu-id="b7760-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="b7760-214">Por ejemplo, una solución de acceso frecuente hipotética no incluiría las correcciones de errores y la funcionalidad incluida en las revisiones 1, 2 y 3.</span><span class="sxs-lookup"><span data-stu-id="b7760-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="b7760-215">En la mayoría de los casos, tampoco sería necesario instalar las revisiones de acceso rápido 1, 2 y 3 antes de instalar la revisión 4.</span><span class="sxs-lookup"><span data-stu-id="b7760-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="b7760-216">Esto hace que la enumeración de las correcciones urgentes individuales sea una tarea administrativa importante: para conocer la configuración exacta de un equipo, necesita saber no solo los Service Packs que se han instalado sino también qué revisiones individuales se han instalado.</span><span class="sxs-lookup"><span data-stu-id="b7760-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="b7760-217">La **clase \_ QuickFixEngineering de Win32** permite enumerar todas las revisiones activas que se han instalado en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b7760-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="b7760-218">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b7760-218">Examples</span></span>

<span data-ttu-id="b7760-219">En el ejemplo de PowerShell de [obtener programas instalados](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) se devuelve una lista completa de los programas instalados.</span><span class="sxs-lookup"><span data-stu-id="b7760-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="b7760-220">En el siguiente ejemplo de VBScript se enumeran las revisiones instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b7760-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="b7760-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7760-221">Requirements</span></span>



| <span data-ttu-id="b7760-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7760-222">Requirement</span></span> | <span data-ttu-id="b7760-223">Value</span><span class="sxs-lookup"><span data-stu-id="b7760-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7760-224">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7760-224">Minimum supported client</span></span><br/> | <span data-ttu-id="b7760-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7760-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7760-226">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7760-226">Minimum supported server</span></span><br/> | <span data-ttu-id="b7760-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7760-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7760-228">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7760-228">Namespace</span></span><br/>                | <span data-ttu-id="b7760-229">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b7760-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7760-230">MOF</span><span class="sxs-lookup"><span data-stu-id="b7760-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7760-231"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7760-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7760-232">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7760-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7760-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7760-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7760-234">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7760-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7760-235">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b7760-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="b7760-236">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b7760-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b7760-237">Tareas WMI: sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="b7760-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
