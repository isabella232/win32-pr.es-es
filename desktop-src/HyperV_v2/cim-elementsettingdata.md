---
description: Representa una asociación entre un elemento administrado y sus datos de configuración asociados. Esta asociación también describe si se trata de una configuración predeterminada o actual.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: CIM_ElementSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667576"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="6f367-104">\_Clase ElementSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="6f367-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="6f367-105">Representa una asociación entre un elemento administrado y sus datos de configuración asociados.</span><span class="sxs-lookup"><span data-stu-id="6f367-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="6f367-106">Esta asociación también describe si se trata de una configuración predeterminada o actual.</span><span class="sxs-lookup"><span data-stu-id="6f367-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f367-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f367-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="6f367-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f367-108">Members</span></span>

<span data-ttu-id="6f367-109">La clase **CIM \_ ElementSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6f367-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6f367-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f367-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f367-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f367-111">Properties</span></span>

<span data-ttu-id="6f367-112">La clase **CIM \_ ElementSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6f367-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f367-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="6f367-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f367-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f367-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f367-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f367-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f367-116">Indica si el elemento está usando actualmente la configuración a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="6f367-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f367-117">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f367-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="6f367-118">**Es actual** (1)</span><span class="sxs-lookup"><span data-stu-id="6f367-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="6f367-119">**No es actual** (2)</span><span class="sxs-lookup"><span data-stu-id="6f367-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f367-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="6f367-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f367-121">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f367-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f367-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f367-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f367-123">Que indica si el valor es un valor predeterminado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="6f367-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f367-124">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f367-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="6f367-125">**Es el valor predeterminado** (1)</span><span class="sxs-lookup"><span data-stu-id="6f367-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="6f367-126">**No es el valor predeterminado** (2)</span><span class="sxs-lookup"><span data-stu-id="6f367-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f367-127">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="6f367-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f367-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f367-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f367-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f367-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f367-130">Marca que indica cuándo y con qué frecuencia se aplica la configuración.</span><span class="sxs-lookup"><span data-stu-id="6f367-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="6f367-131">Por ejemplo, la configuración se puede aplicar en una solicitud de reinicialización, restablecimiento y reconfiguración.</span><span class="sxs-lookup"><span data-stu-id="6f367-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="6f367-132">Puede ser un valor de configuración permanente o una configuración usada solo una vez, como indica la marca.</span><span class="sxs-lookup"><span data-stu-id="6f367-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="6f367-133">Si se trata de una configuración permanente, se aplica la configuración cada vez que se reinicializa el elemento administrado, hasta que esta marca se restablece manualmente.</span><span class="sxs-lookup"><span data-stu-id="6f367-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="6f367-134">Sin embargo, si es de uso único, la marca se borra automáticamente después de aplicar la configuración.</span><span class="sxs-lookup"><span data-stu-id="6f367-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="6f367-135">Además, si esta marca se establece en un valor distinto de 0 (desconocido), esto tiene prioridad sobre una propiedad **SettingData** establecida en "default".</span><span class="sxs-lookup"><span data-stu-id="6f367-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="6f367-136">Si el elemento administrado es un sistema informático y el valor de esta marca es "es siguiente", el valor será efectivo la próxima vez que se restablezca el sistema.</span><span class="sxs-lookup"><span data-stu-id="6f367-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="6f367-137">Y, a menos que se cambie esta marca, se conservará para los restablecimientos del sistema posteriores.</span><span class="sxs-lookup"><span data-stu-id="6f367-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="6f367-138">Sin embargo, si esta marca se establece en "es siguiente para uso único", esta configuración solo se utilizará una vez y la marca se restablecerá después de la 2 (no es siguiente).</span><span class="sxs-lookup"><span data-stu-id="6f367-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="6f367-139">Por lo tanto, en el ejemplo anterior, si el sistema se reinicia en una sucesión rápida, la configuración no se utilizará en el segundo reinicio.</span><span class="sxs-lookup"><span data-stu-id="6f367-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f367-140">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f367-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="6f367-141">**Es Next** (1)</span><span class="sxs-lookup"><span data-stu-id="6f367-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="6f367-142">**No es Next** (2)</span><span class="sxs-lookup"><span data-stu-id="6f367-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="6f367-143">**Siguiente para uso único** (3)</span><span class="sxs-lookup"><span data-stu-id="6f367-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f367-144">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6f367-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f367-145">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6f367-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="6f367-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f367-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f367-147">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f367-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f367-148">Elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="6f367-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="6f367-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="6f367-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f367-150">Tipo de datos **: \_ SettingData de CIM**</span><span class="sxs-lookup"><span data-stu-id="6f367-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="6f367-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f367-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f367-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f367-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f367-153">Los datos de configuración asociados al elemento.</span><span class="sxs-lookup"><span data-stu-id="6f367-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f367-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f367-154">Requirements</span></span>



| <span data-ttu-id="6f367-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f367-155">Requirement</span></span> | <span data-ttu-id="6f367-156">Value</span><span class="sxs-lookup"><span data-stu-id="6f367-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f367-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f367-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6f367-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6f367-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6f367-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f367-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6f367-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f367-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6f367-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f367-161">Namespace</span></span><br/>                | <span data-ttu-id="6f367-162">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f367-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6f367-163">MOF</span><span class="sxs-lookup"><span data-stu-id="6f367-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f367-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f367-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f367-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f367-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f367-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f367-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

