---
description: Clase base abstracta para las clases que representan la configuración de una característica de puerto de conmutador Ethernet.
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Msvm_EthernetSwitchPortFeatureSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360811"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="c1c5c-103">MSVM \_ EthernetSwitchPortFeatureSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="c1c5c-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="c1c5c-104">Clase base abstracta para las clases que representan la configuración de una característica de puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="c1c5c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c5c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1c5c-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="c1c5c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1c5c-107">Members</span></span>

<span data-ttu-id="c1c5c-108">La clase **MSVM \_ EthernetSwitchPortFeatureSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c1c5c-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c1c5c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1c5c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1c5c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1c5c-110">Properties</span></span>

<span data-ttu-id="c1c5c-111">La clase **MSVM \_ EthernetSwitchPortFeatureSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1c5c-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c5c-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c5c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c1c5c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1c5c-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-115">A short description of the object.</span></span> <span data-ttu-id="c1c5c-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c1c5c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1c5c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c5c-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c5c-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c1c5c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1c5c-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-120">A description of the object.</span></span> <span data-ttu-id="c1c5c-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c1c5c-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1c5c-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c5c-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c5c-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c1c5c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1c5c-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-125">A display name for the object.</span></span> <span data-ttu-id="c1c5c-126">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1c5c-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c1c5c-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c5c-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c5c-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c1c5c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c5c-130">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c1c5c-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c1c5c-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c1c5c-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c1c5c-132">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c1c5c-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1c5c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1c5c-133">Requirements</span></span>



| <span data-ttu-id="c1c5c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1c5c-134">Requirement</span></span> | <span data-ttu-id="c1c5c-135">Value</span><span class="sxs-lookup"><span data-stu-id="c1c5c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c5c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1c5c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c5c-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1c5c-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1c5c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1c5c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c5c-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1c5c-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1c5c-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1c5c-140">Namespace</span></span><br/>                | <span data-ttu-id="c1c5c-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c1c5c-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1c5c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c1c5c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1c5c-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1c5c-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1c5c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1c5c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c5c-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1c5c-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

