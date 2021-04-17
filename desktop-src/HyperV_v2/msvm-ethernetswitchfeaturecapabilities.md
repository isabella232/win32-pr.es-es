---
description: Define los medios por los que un cliente puede detectar el intervalo válido de valores predeterminados para una característica de conmutador Ethernet.
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Msvm_EthernetSwitchFeatureCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670032"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="fb783-103">MSVM \_ EthernetSwitchFeatureCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="fb783-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="fb783-104">Define los medios por los que un cliente puede detectar el intervalo válido de valores predeterminados para una característica de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="fb783-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="fb783-105">Un objeto **MSVM \_ EthernetSwitchFeatureCapabilities** está asociado a cada conmutador Ethernet virtual, para cada característica que admite el conmutador.</span><span class="sxs-lookup"><span data-stu-id="fb783-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="fb783-106">Se asocian cuatro objetos [**\_ EthernetSwitchFeatureSettingData de MSVM**](msvm-ethernetswitchfeaturesettingdata.md) al objeto **MSVM \_ EthernetSwitchFeatureCapabilities** para describir los valores mínimo, máximo, predeterminado e incremental para las funcionalidades de características del conmutador dado.</span><span class="sxs-lookup"><span data-stu-id="fb783-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="fb783-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fb783-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb783-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb783-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="fb783-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb783-109">Members</span></span>

<span data-ttu-id="fb783-110">La clase **MSVM \_ EthernetSwitchFeatureCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fb783-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="fb783-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb783-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb783-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb783-112">Properties</span></span>

<span data-ttu-id="fb783-113">La clase **MSVM \_ EthernetSwitchFeatureCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fb783-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb783-114">**Aplicabilidad**</span><span class="sxs-lookup"><span data-stu-id="fb783-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-115">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb783-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb783-117">Describe si esta característica se aplica a un conmutador Ethernet o a un puerto de conmutador Ethernet determinado.</span><span class="sxs-lookup"><span data-stu-id="fb783-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fb783-118">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fb783-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="fb783-119">**Puerto** (1)</span><span class="sxs-lookup"><span data-stu-id="fb783-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="fb783-120">**Modificador** (2)</span><span class="sxs-lookup"><span data-stu-id="fb783-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fb783-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fb783-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb783-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb783-124">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="fb783-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="fb783-125">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb783-125">A short description of the object.</span></span> <span data-ttu-id="fb783-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fb783-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb783-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb783-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb783-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb783-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb783-130">A description of the object.</span></span> <span data-ttu-id="fb783-131">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fb783-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb783-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fb783-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb783-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb783-135">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb783-135">A display name for the object.</span></span> <span data-ttu-id="fb783-136">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fb783-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb783-137">**FeatureId**</span><span class="sxs-lookup"><span data-stu-id="fb783-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb783-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb783-140">Identificador de la característica para la que este objeto proporciona información de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fb783-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="fb783-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb783-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb783-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb783-144">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="fb783-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fb783-145">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fb783-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fb783-146">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fb783-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb783-147">**Versión**</span><span class="sxs-lookup"><span data-stu-id="fb783-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb783-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb783-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb783-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb783-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb783-150">Versión de la característica en un formato de "Major. minor", por ejemplo "2,0".</span><span class="sxs-lookup"><span data-stu-id="fb783-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb783-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb783-151">Requirements</span></span>



| <span data-ttu-id="fb783-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb783-152">Requirement</span></span> | <span data-ttu-id="fb783-153">Value</span><span class="sxs-lookup"><span data-stu-id="fb783-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb783-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb783-154">Minimum supported client</span></span><br/> | <span data-ttu-id="fb783-155">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb783-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fb783-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb783-156">Minimum supported server</span></span><br/> | <span data-ttu-id="fb783-157">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb783-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb783-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fb783-158">Namespace</span></span><br/>                | <span data-ttu-id="fb783-159">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fb783-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fb783-160">MOF</span><span class="sxs-lookup"><span data-stu-id="fb783-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb783-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb783-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb783-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb783-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb783-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb783-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

