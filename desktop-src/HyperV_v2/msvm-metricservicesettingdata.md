---
description: Representa la configuración para el servicio de métricas. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al método ModifyServiceSettings para modificar cualquiera de estas propiedades.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Msvm_MetricServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687269"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="d82bc-105">MSVM \_ MetricServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="d82bc-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="d82bc-106">Representa la configuración para el servicio de métricas.</span><span class="sxs-lookup"><span data-stu-id="d82bc-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="d82bc-107">Las propiedades de esta clase no se pueden modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="d82bc-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="d82bc-108">El cliente debe llamar al método [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) para modificar cualquiera de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d82bc-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="d82bc-109">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d82bc-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d82bc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d82bc-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="d82bc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d82bc-111">Members</span></span>

<span data-ttu-id="d82bc-112">La clase **MSVM \_ MetricServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d82bc-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d82bc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d82bc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d82bc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d82bc-114">Properties</span></span>

<span data-ttu-id="d82bc-115">La clase **MSVM \_ MetricServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d82bc-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d82bc-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d82bc-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d82bc-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d82bc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d82bc-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d82bc-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d82bc-119">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d82bc-119">A short description of the object.</span></span> <span data-ttu-id="d82bc-120">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="d82bc-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d82bc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d82bc-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d82bc-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d82bc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d82bc-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d82bc-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d82bc-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d82bc-124">A description of the object.</span></span> <span data-ttu-id="d82bc-125">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "define la configuración del servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="d82bc-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d82bc-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d82bc-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d82bc-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d82bc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d82bc-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d82bc-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d82bc-129">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d82bc-129">A display name for the object.</span></span> <span data-ttu-id="d82bc-130">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="d82bc-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d82bc-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d82bc-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d82bc-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d82bc-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d82bc-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d82bc-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d82bc-134">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d82bc-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d82bc-135">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d82bc-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d82bc-136">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d82bc-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d82bc-137">**MetricsFlushInterval**</span><span class="sxs-lookup"><span data-stu-id="d82bc-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d82bc-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d82bc-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d82bc-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d82bc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d82bc-140">Define el intervalo en el que las métricas se deben vaciar en el disco.</span><span class="sxs-lookup"><span data-stu-id="d82bc-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d82bc-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d82bc-141">Requirements</span></span>



| <span data-ttu-id="d82bc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d82bc-142">Requirement</span></span> | <span data-ttu-id="d82bc-143">Value</span><span class="sxs-lookup"><span data-stu-id="d82bc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d82bc-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d82bc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d82bc-145">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d82bc-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d82bc-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d82bc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d82bc-147">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d82bc-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d82bc-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d82bc-148">Namespace</span></span><br/>                | <span data-ttu-id="d82bc-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d82bc-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d82bc-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d82bc-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d82bc-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d82bc-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d82bc-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d82bc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d82bc-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d82bc-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d82bc-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="d82bc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82bc-155">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d82bc-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="d82bc-156">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="d82bc-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

