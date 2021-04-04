---
description: La \_ clase SettingContext de CIM asocia objetos de configuración con objetos de configuración.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: CIM_SettingContext (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998193"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="10df9-103">\_Clase SettingContext de CIM</span><span class="sxs-lookup"><span data-stu-id="10df9-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="10df9-104">La **clase \_ SettingContext de CIM** asocia objetos de configuración con objetos de configuración.</span><span class="sxs-lookup"><span data-stu-id="10df9-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="10df9-105">Por ejemplo, la configuración de un adaptador de red podría cambiar en función del sitio o la red a la que está conectado su equipo host.</span><span class="sxs-lookup"><span data-stu-id="10df9-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="10df9-106">En ese caso, el sistema informático tendría dos objetos de configuración diferentes, correspondientes a las diferencias en la configuración de red para los dos segmentos de red.</span><span class="sxs-lookup"><span data-stu-id="10df9-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="10df9-107">Una configuración agregaría un objeto de configuración para el adaptador de red al operar en un segmento; mientras que la otra configuración agregaría un objeto de configuración de adaptador de red diferente, específico de otro segmento.</span><span class="sxs-lookup"><span data-stu-id="10df9-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="10df9-108">Tenga en cuenta que muchos valores de configuración del equipo son independientes de la configuración de red.</span><span class="sxs-lookup"><span data-stu-id="10df9-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="10df9-109">Por ejemplo, ambas configuraciones agregarían el mismo objeto de configuración para la resolución del monitor del equipo.</span><span class="sxs-lookup"><span data-stu-id="10df9-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10df9-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="10df9-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10df9-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="10df9-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10df9-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="10df9-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="10df9-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="10df9-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10df9-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10df9-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="10df9-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="10df9-115">Members</span></span>

<span data-ttu-id="10df9-116">La clase **CIM \_ SettingContext** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="10df9-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="10df9-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10df9-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10df9-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10df9-118">Properties</span></span>

<span data-ttu-id="10df9-119">La clase **CIM \_ SettingContext** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="10df9-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10df9-120">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="10df9-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10df9-121">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="10df9-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="10df9-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10df9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10df9-123">Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10df9-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10df9-124">Referencia al objeto de configuración que agrega el valor.</span><span class="sxs-lookup"><span data-stu-id="10df9-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="10df9-125">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="10df9-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10df9-126">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="10df9-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="10df9-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10df9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10df9-128">Referencia a una configuración agregada.</span><span class="sxs-lookup"><span data-stu-id="10df9-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10df9-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10df9-129">Remarks</span></span>

<span data-ttu-id="10df9-130">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="10df9-130">WMI does not implement this class.</span></span>

<span data-ttu-id="10df9-131">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="10df9-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="10df9-132">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="10df9-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10df9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10df9-133">Requirements</span></span>



| <span data-ttu-id="10df9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="10df9-134">Requirement</span></span> | <span data-ttu-id="10df9-135">Value</span><span class="sxs-lookup"><span data-stu-id="10df9-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10df9-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10df9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="10df9-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10df9-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10df9-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10df9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="10df9-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10df9-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10df9-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10df9-140">Namespace</span></span><br/>                | <span data-ttu-id="10df9-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="10df9-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10df9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="10df9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10df9-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10df9-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10df9-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10df9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10df9-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10df9-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

