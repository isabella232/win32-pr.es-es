---
description: El \_ objeto de configuración de CIM permite agrupar los conjuntos de parámetros (definidos en objetos de configuración de CIM \_ ) y las dependencias de uno o más elementos del sistema administrados.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: CIM_Configuration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807603"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="2dc97-103">CIM ( \_ clase de configuración)</span><span class="sxs-lookup"><span data-stu-id="2dc97-103">CIM\_Configuration class</span></span>

<span data-ttu-id="2dc97-104">El objeto de **\_ configuración de CIM** permite agrupar los conjuntos de parámetros (definidos en objetos de [**\_ configuración de CIM**](cim-setting.md) ) y las dependencias de uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="2dc97-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="2dc97-105">Este objeto representa un comportamiento determinado o un estado funcional deseado para los elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="2dc97-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="2dc97-106">Normalmente, el estado funcional deseado está controlado por requisitos externos, como la hora o la ubicación.</span><span class="sxs-lookup"><span data-stu-id="2dc97-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="2dc97-107">Por ejemplo, para conectarse a un sistema de correo desde casa, existe una dependencia de un módem; sin embargo, existe una dependencia de un adaptador de red en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2dc97-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="2dc97-108">Los valores de configuración de los dispositivos lógicos pertinentes (en este ejemplo, módem de POTS y adaptador de red) se pueden definir y agregar mediante la **\_ configuración de CIM**.</span><span class="sxs-lookup"><span data-stu-id="2dc97-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="2dc97-109">Por lo tanto, se pueden definir dos configuraciones de "conectar a correo" agrupando las dependencias pertinentes y los objetos de [**\_ configuración de CIM**](cim-setting.md) .</span><span class="sxs-lookup"><span data-stu-id="2dc97-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2dc97-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc97-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2dc97-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2dc97-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2dc97-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2dc97-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2dc97-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2dc97-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc97-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dc97-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2dc97-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dc97-115">Members</span></span>

<span data-ttu-id="2dc97-116">La clase de **\_ configuración CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2dc97-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="2dc97-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2dc97-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2dc97-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2dc97-118">Properties</span></span>

<span data-ttu-id="2dc97-119">La clase de **\_ configuración CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2dc97-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2dc97-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2dc97-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc97-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc97-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc97-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc97-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc97-123">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2dc97-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2dc97-124">Descripción textual breve del objeto **de \_ configuración de CIM** .</span><span class="sxs-lookup"><span data-stu-id="2dc97-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="2dc97-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dc97-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc97-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc97-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc97-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc97-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2dc97-128">Descripción textual del objeto **de \_ configuración de CIM** .</span><span class="sxs-lookup"><span data-stu-id="2dc97-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="2dc97-129">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2dc97-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc97-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc97-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc97-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc97-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc97-132">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2dc97-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2dc97-133">Etiqueta por la que se conoce el objeto de **\_ configuración de CIM** .</span><span class="sxs-lookup"><span data-stu-id="2dc97-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dc97-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dc97-134">Remarks</span></span>

<span data-ttu-id="2dc97-135">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2dc97-135">WMI does not implement this class.</span></span>

<span data-ttu-id="2dc97-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2dc97-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2dc97-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2dc97-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc97-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dc97-138">Requirements</span></span>



| <span data-ttu-id="2dc97-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dc97-139">Requirement</span></span> | <span data-ttu-id="2dc97-140">Value</span><span class="sxs-lookup"><span data-stu-id="2dc97-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc97-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc97-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc97-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2dc97-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2dc97-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc97-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc97-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2dc97-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2dc97-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2dc97-145">Namespace</span></span><br/>                | <span data-ttu-id="2dc97-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2dc97-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2dc97-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2dc97-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dc97-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2dc97-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2dc97-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2dc97-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dc97-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc97-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

