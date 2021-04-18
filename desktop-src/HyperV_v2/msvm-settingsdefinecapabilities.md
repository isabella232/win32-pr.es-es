---
description: Proporciona un vínculo entre la instancia de Capabilities y los valores mínimo, máximo, incremental y predeterminados para un recurso.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687005"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="ab07b-103">MSVM \_ SettingsDefineCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="ab07b-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="ab07b-104">Proporciona un vínculo entre la instancia de Capabilities y los valores mínimo, máximo, incremental y predeterminados para un recurso.</span><span class="sxs-lookup"><span data-stu-id="ab07b-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="ab07b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ab07b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab07b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab07b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="ab07b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab07b-107">Members</span></span>

<span data-ttu-id="ab07b-108">La clase **MSVM \_ SettingsDefineCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab07b-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ab07b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab07b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab07b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab07b-110">Properties</span></span>

<span data-ttu-id="ab07b-111">La clase **MSVM \_ SettingsDefineCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab07b-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab07b-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ab07b-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab07b-113">Tipo de datos: **[ **\_ capacidades de CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ab07b-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="ab07b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab07b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab07b-115">Instancia de Capabilities.</span><span class="sxs-lookup"><span data-stu-id="ab07b-115">The capabilities instance.</span></span> <span data-ttu-id="ab07b-116">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab07b-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab07b-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ab07b-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab07b-118">Tipo de datos: **[ **\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ab07b-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="ab07b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab07b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab07b-120">Un valor de configuración que se usa para definir la instancia de Capabilities asociada.</span><span class="sxs-lookup"><span data-stu-id="ab07b-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="ab07b-121">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab07b-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab07b-122">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="ab07b-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab07b-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab07b-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab07b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab07b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab07b-125">Indica si las propiedades que no son NULL y que no son de clave de la instancia de datos de configuración asociada se tratan de forma independiente o como un conjunto correlacionado.</span><span class="sxs-lookup"><span data-stu-id="ab07b-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="ab07b-126">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)) y siempre está establecida en 0 (independiente).</span><span class="sxs-lookup"><span data-stu-id="ab07b-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="ab07b-127">**SupportStatement**</span><span class="sxs-lookup"><span data-stu-id="ab07b-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab07b-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab07b-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab07b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab07b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab07b-130">Identifica la instrucción de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="ab07b-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="ab07b-131">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ab07b-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="ab07b-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Producción** (0)</span><span class="sxs-lookup"><span data-stu-id="ab07b-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="ab07b-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Versión preliminar** (1)</span><span class="sxs-lookup"><span data-stu-id="ab07b-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="ab07b-134">No era de **producción** en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ab07b-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="ab07b-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ab07b-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab07b-136">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="ab07b-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab07b-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab07b-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab07b-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab07b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab07b-139">Cualquier semántica adicional en la interpretación de todas las propiedades no clave no nulas de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ab07b-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="ab07b-140">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab07b-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab07b-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="ab07b-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab07b-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab07b-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab07b-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab07b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab07b-144">Cualquier semántica adicional en la interpretación de las propiedades no clave no nulas de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ab07b-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="ab07b-145">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab07b-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab07b-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab07b-146">Remarks</span></span>

<span data-ttu-id="ab07b-147">Los valores de las propiedades **ValueRole** y **ValueRange** se usan en los siguientes pares:</span><span class="sxs-lookup"><span data-stu-id="ab07b-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="ab07b-148">Punto/valor predeterminado (0/0)</span><span class="sxs-lookup"><span data-stu-id="ab07b-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="ab07b-149">Mínimos/admitidos (1/3)</span><span class="sxs-lookup"><span data-stu-id="ab07b-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="ab07b-150">Máximos/admitidos (2/3)</span><span class="sxs-lookup"><span data-stu-id="ab07b-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="ab07b-151">Incrementos/admitidos (3/3).</span><span class="sxs-lookup"><span data-stu-id="ab07b-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="ab07b-152">"Point" significa que cada una de las propiedades del objeto **PartComponent** representa el valor predeterminado de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="ab07b-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="ab07b-153">"Mínimo" y "máximo" significan que cada una de las propiedades del objeto **PartComponent** representa los valores posibles más pequeños y más grandes para estas propiedades que son compatibles con la plataforma en función de la configuración actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="ab07b-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="ab07b-154">"Incrementos" indica la granularidad con la que puede aumentar o disminuir la configuración.</span><span class="sxs-lookup"><span data-stu-id="ab07b-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="ab07b-155">El acceso a la clase **MSVM \_ SettingsDefineCapabilities** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ab07b-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ab07b-156">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ab07b-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab07b-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab07b-157">Requirements</span></span>



| <span data-ttu-id="ab07b-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab07b-158">Requirement</span></span> | <span data-ttu-id="ab07b-159">Value</span><span class="sxs-lookup"><span data-stu-id="ab07b-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab07b-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab07b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ab07b-161">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab07b-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab07b-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab07b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ab07b-163">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab07b-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab07b-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab07b-164">Namespace</span></span><br/>                | <span data-ttu-id="ab07b-165">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ab07b-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ab07b-166">MOF</span><span class="sxs-lookup"><span data-stu-id="ab07b-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab07b-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab07b-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab07b-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab07b-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab07b-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab07b-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab07b-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab07b-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab07b-171">**\_SETTINGSDEFINECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="ab07b-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="ab07b-172">[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab07b-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ab07b-173">**MSVM \_ SettingsDefineCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="ab07b-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="ab07b-174">Clases de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="ab07b-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

