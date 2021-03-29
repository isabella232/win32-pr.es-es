---
description: Una clase abstracta que representa la configuración para una característica específica de un sistema o componente.
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Msvm_FeatureSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540339"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="d1234-103">MSVM \_ FeatureSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="d1234-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="d1234-104">Una clase abstracta que representa la configuración para una característica específica de un sistema o componente.</span><span class="sxs-lookup"><span data-stu-id="d1234-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="d1234-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d1234-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1234-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1234-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="d1234-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1234-107">Members</span></span>

<span data-ttu-id="d1234-108">La clase **MSVM \_ FeatureSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1234-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d1234-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1234-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1234-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1234-110">Properties</span></span>

<span data-ttu-id="d1234-111">La clase **MSVM \_ FeatureSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1234-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1234-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1234-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1234-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1234-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1234-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1234-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1234-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1234-115">A short description of the object.</span></span> <span data-ttu-id="d1234-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d1234-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1234-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1234-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1234-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1234-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1234-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1234-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1234-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1234-120">A description of the object.</span></span> <span data-ttu-id="d1234-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d1234-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1234-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d1234-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1234-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1234-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1234-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1234-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1234-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1234-125">A display name for the object.</span></span> <span data-ttu-id="d1234-126">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1234-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d1234-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1234-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1234-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1234-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1234-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1234-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1234-130">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d1234-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d1234-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d1234-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d1234-132">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1234-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1234-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1234-133">Requirements</span></span>



| <span data-ttu-id="d1234-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1234-134">Requirement</span></span> | <span data-ttu-id="d1234-135">Value</span><span class="sxs-lookup"><span data-stu-id="d1234-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1234-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1234-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1234-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1234-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1234-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1234-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1234-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1234-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1234-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1234-140">Namespace</span></span><br/>                | <span data-ttu-id="d1234-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d1234-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1234-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d1234-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1234-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1234-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1234-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1234-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1234-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1234-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

