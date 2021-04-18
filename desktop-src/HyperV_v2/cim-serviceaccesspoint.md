---
description: Representa un punto de acceso al servicio (SAP), que puede utilizarse o invocar un servicio. SAP indica que un servicio está disponible para que lo usen otras entidades.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: CIM_ServiceAccessPoint (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686900"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="0e12b-104">CIM_ServiceAccessPoint (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0e12b-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="0e12b-105">Representa un punto de acceso al servicio (SAP), que puede utilizarse o invocar un servicio.</span><span class="sxs-lookup"><span data-stu-id="0e12b-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="0e12b-106">SAP indica que un servicio está disponible para que lo usen otras entidades.</span><span class="sxs-lookup"><span data-stu-id="0e12b-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e12b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e12b-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="0e12b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e12b-108">Members</span></span>

<span data-ttu-id="0e12b-109">La clase **CIM \_ punto** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0e12b-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="0e12b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e12b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e12b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e12b-111">Properties</span></span>

<span data-ttu-id="0e12b-112">La clase **CIM \_ punto** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0e12b-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e12b-113">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e12b-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e12b-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e12b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e12b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e12b-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e12b-117">Nombre de clase utilizado para crear una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0e12b-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="0e12b-118">**CreationClassName** se combina con otras propiedades de clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="0e12b-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="0e12b-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0e12b-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e12b-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e12b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e12b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-122">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e12b-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e12b-123">El nombre único de SAP que indica las características admitidas por SAP.</span><span class="sxs-lookup"><span data-stu-id="0e12b-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="0e12b-124">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e12b-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e12b-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e12b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e12b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-127">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="0e12b-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="0e12b-128">Nombre de clase que se usa para crear una instancia del sistema que contiene SAP.</span><span class="sxs-lookup"><span data-stu-id="0e12b-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="0e12b-129">**SystemCreationClassName** se combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="0e12b-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="0e12b-130">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0e12b-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e12b-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0e12b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e12b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e12b-133">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="0e12b-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="0e12b-134">Nombre del sistema que contiene SAP.</span><span class="sxs-lookup"><span data-stu-id="0e12b-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e12b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e12b-135">Requirements</span></span>



| <span data-ttu-id="0e12b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e12b-136">Requirement</span></span> | <span data-ttu-id="0e12b-137">Value</span><span class="sxs-lookup"><span data-stu-id="0e12b-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e12b-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e12b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0e12b-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0e12b-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0e12b-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e12b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0e12b-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e12b-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0e12b-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e12b-142">Namespace</span></span><br/>                | <span data-ttu-id="0e12b-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0e12b-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e12b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0e12b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e12b-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e12b-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e12b-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e12b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e12b-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e12b-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e12b-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e12b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e12b-149">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0e12b-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

