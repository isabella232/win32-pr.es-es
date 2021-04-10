---
description: La \_ Asociación PackageAlarm de CIM representa la relación en la que un dispositivo de alarma se instala como parte de un paquete. La instalación de indica problemas con el entorno del paquete&\# 8212, su estado de seguridad o su estado general.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: CIM_PackageAlarm (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152877"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="2b293-104">\_Clase PackageAlarm de CIM</span><span class="sxs-lookup"><span data-stu-id="2b293-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="2b293-105">La [**Asociación \_ PackageAlarm de CIM**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa la relación en la que un dispositivo de alarma se instala como parte de un paquete.</span><span class="sxs-lookup"><span data-stu-id="2b293-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="2b293-106">La instalación de indica problemas con el entorno del paquete con su estado de seguridad o con su estado general.</span><span class="sxs-lookup"><span data-stu-id="2b293-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b293-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2b293-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2b293-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2b293-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2b293-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2b293-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2b293-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2b293-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b293-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b293-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2b293-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b293-112">Members</span></span>

<span data-ttu-id="2b293-113">La clase **CIM \_ PackageAlarm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2b293-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="2b293-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b293-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b293-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b293-115">Properties</span></span>

<span data-ttu-id="2b293-116">La clase **CIM \_ PackageAlarm** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2b293-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b293-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2b293-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b293-118">Tipo de datos: **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="2b293-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2b293-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b293-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b293-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2b293-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2b293-121">Un [**\_ AlarmDevice de CIM**](cim-alarmdevice.md) que describe el dispositivo de alarma para el paquete.</span><span class="sxs-lookup"><span data-stu-id="2b293-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="2b293-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2b293-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b293-123">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="2b293-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="2b293-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b293-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b293-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="2b293-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2b293-126">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico cuyo estado, seguridad, entorno, etc. se pone en alarma.</span><span class="sxs-lookup"><span data-stu-id="2b293-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b293-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b293-127">Remarks</span></span>

<span data-ttu-id="2b293-128">**CIM \_ PackageAlarm** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="2b293-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2b293-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2b293-129">WMI does not implement this class.</span></span>

<span data-ttu-id="2b293-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2b293-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2b293-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2b293-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b293-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b293-132">Requirements</span></span>



| <span data-ttu-id="2b293-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b293-133">Requirement</span></span> | <span data-ttu-id="2b293-134">Value</span><span class="sxs-lookup"><span data-stu-id="2b293-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b293-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b293-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2b293-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b293-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b293-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b293-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2b293-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b293-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b293-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b293-139">Namespace</span></span><br/>                | <span data-ttu-id="2b293-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2b293-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b293-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2b293-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b293-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b293-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b293-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b293-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b293-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b293-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b293-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b293-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b293-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2b293-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

