---
description: Representa la asociación entre un trabajo y los elementos administrados que pueden verse afectados por su ejecución.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Msvm_AffectedStorageJobElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666232"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="0a34e-103">MSVM \_ AffectedStorageJobElement (clase)</span><span class="sxs-lookup"><span data-stu-id="0a34e-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="0a34e-104">Representa la asociación entre un trabajo y los elementos administrados que pueden verse afectados por su ejecución.</span><span class="sxs-lookup"><span data-stu-id="0a34e-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="0a34e-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0a34e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a34e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a34e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="0a34e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0a34e-107">Members</span></span>

<span data-ttu-id="0a34e-108">La clase **MSVM \_ AffectedStorageJobElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0a34e-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="0a34e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a34e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a34e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a34e-110">Properties</span></span>

<span data-ttu-id="0a34e-111">La clase **MSVM \_ AffectedStorageJobElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0a34e-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a34e-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="0a34e-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a34e-113">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0a34e-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a34e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-115">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="0a34e-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0a34e-116">Elemento administrado que se ve afectado por la ejecución del trabajo.</span><span class="sxs-lookup"><span data-stu-id="0a34e-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="0a34e-117">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a34e-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0a34e-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="0a34e-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a34e-119">Tipo de datos: **[ **MSVM \_ StorageJob**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="0a34e-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a34e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. AffectingElement")</span><span class="sxs-lookup"><span data-stu-id="0a34e-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="0a34e-122">El trabajo que está afectando al elemento afectado.</span><span class="sxs-lookup"><span data-stu-id="0a34e-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="0a34e-123">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a34e-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0a34e-124">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="0a34e-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a34e-125">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a34e-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a34e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a34e-127">Una enumeración que describe el efecto en el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="0a34e-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="0a34e-128">Esta matriz corresponde a la matriz de propiedades **OtherElementEffectsDescriptions** , donde la última proporciona detalles relacionados con los efectos de alto nivel enumerados por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0a34e-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="0a34e-129">Se requiere detalle adicional si la matriz de la propiedad **ElementEffects** contiene el valor 1, (otro).</span><span class="sxs-lookup"><span data-stu-id="0a34e-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="0a34e-130">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a34e-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0a34e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0a34e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0a34e-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Uso exclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="0a34e-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Impacto** en el rendimiento (3)</span><span class="sxs-lookup"><span data-stu-id="0a34e-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Integridad de elementos** (4)</span><span class="sxs-lookup"><span data-stu-id="0a34e-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0a34e-136">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0a34e-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a34e-137">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0a34e-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0a34e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a34e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a34e-139">Proporciona detalles sobre el efecto en la posición de la matriz correspondiente en la matriz de propiedades **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="0a34e-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="0a34e-140">Esta información es necesaria siempre que el elemento correspondiente en la matriz de la propiedad **ElementEffects** contiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="0a34e-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="0a34e-141">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a34e-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a34e-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a34e-142">Remarks</span></span>

<span data-ttu-id="0a34e-143">El acceso a la clase **MSVM \_ AffectedStorageJobElement** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="0a34e-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0a34e-144">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0a34e-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a34e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a34e-145">Requirements</span></span>



| <span data-ttu-id="0a34e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a34e-146">Requirement</span></span> | <span data-ttu-id="0a34e-147">Value</span><span class="sxs-lookup"><span data-stu-id="0a34e-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a34e-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a34e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0a34e-149">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a34e-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0a34e-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a34e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0a34e-151">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a34e-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a34e-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0a34e-152">Namespace</span></span><br/>                | <span data-ttu-id="0a34e-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0a34e-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0a34e-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0a34e-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a34e-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a34e-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a34e-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a34e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a34e-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a34e-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a34e-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a34e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a34e-159">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0a34e-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="0a34e-160">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a34e-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0a34e-161">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="0a34e-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

