---
description: Una clase abstracta que representa los valores para una instancia determinada de una característica de conmutador Ethernet.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Msvm_EthernetSwitchFeatureSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689589"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="8fb31-103">MSVM \_ EthernetSwitchFeatureSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="8fb31-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="8fb31-104">Una clase abstracta que representa los valores para una instancia determinada de una característica de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8fb31-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="8fb31-105">Características del conmutador Ethernet la clase de administración de configuración debe derivar de esta clase abstracta.</span><span class="sxs-lookup"><span data-stu-id="8fb31-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="8fb31-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8fb31-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fb31-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="8fb31-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8fb31-108">Members</span></span>

<span data-ttu-id="8fb31-109">La clase **MSVM \_ EthernetSwitchFeatureSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8fb31-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8fb31-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fb31-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fb31-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fb31-111">Properties</span></span>

<span data-ttu-id="8fb31-112">La clase **MSVM \_ EthernetSwitchFeatureSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8fb31-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fb31-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8fb31-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb31-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8fb31-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb31-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fb31-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb31-116">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8fb31-116">A short description of the object.</span></span> <span data-ttu-id="8fb31-117">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8fb31-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8fb31-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fb31-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb31-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8fb31-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb31-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fb31-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb31-121">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8fb31-121">A description of the object.</span></span> <span data-ttu-id="8fb31-122">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8fb31-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8fb31-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8fb31-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb31-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8fb31-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb31-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fb31-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb31-126">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="8fb31-126">A display name for the object.</span></span> <span data-ttu-id="8fb31-127">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb31-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8fb31-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8fb31-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb31-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8fb31-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb31-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fb31-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fb31-131">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8fb31-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8fb31-132">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8fb31-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8fb31-133">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb31-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fb31-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fb31-134">Requirements</span></span>



| <span data-ttu-id="8fb31-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb31-135">Requirement</span></span> | <span data-ttu-id="8fb31-136">Value</span><span class="sxs-lookup"><span data-stu-id="8fb31-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb31-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fb31-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb31-138">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fb31-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8fb31-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fb31-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb31-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fb31-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fb31-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8fb31-141">Namespace</span></span><br/>                | <span data-ttu-id="8fb31-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8fb31-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8fb31-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8fb31-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fb31-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fb31-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fb31-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8fb31-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fb31-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8fb31-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

