---
description: La \_ clase CIM StorageError representa bloques de medios o espacio de memoria que se asignan sin usar debido a errores. La clave de la clase es la propiedad StartingAddress de los bytes con error.
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: CIM_StorageError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659440"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="44391-104">\_Clase StorageError de CIM</span><span class="sxs-lookup"><span data-stu-id="44391-104">CIM\_StorageError class</span></span>

<span data-ttu-id="44391-105">La clase **CIM \_ StorageError** representa bloques de medios o espacio de memoria que se asignan sin usar debido a errores.</span><span class="sxs-lookup"><span data-stu-id="44391-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="44391-106">La clave de la clase es la propiedad **StartingAddress** de los bytes con error.</span><span class="sxs-lookup"><span data-stu-id="44391-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44391-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="44391-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="44391-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="44391-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="44391-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="44391-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="44391-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="44391-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44391-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44391-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="44391-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="44391-112">Members</span></span>

<span data-ttu-id="44391-113">La clase **CIM \_ StorageError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="44391-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="44391-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44391-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44391-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44391-115">Properties</span></span>

<span data-ttu-id="44391-116">La clase **CIM \_ StorageError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="44391-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44391-117">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="44391-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44391-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44391-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44391-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44391-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44391-120">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="44391-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="44391-121">Ámbito del nombre de la clase de creación de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="44391-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="44391-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="44391-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44391-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44391-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44391-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44391-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44391-125">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**DeviceID**")</span><span class="sxs-lookup"><span data-stu-id="44391-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="44391-126">Ámbito del identificador de dispositivo de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="44391-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="44391-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="44391-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44391-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44391-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44391-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44391-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44391-130">Dirección final de los bytes con errores.</span><span class="sxs-lookup"><span data-stu-id="44391-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="44391-131">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44391-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="44391-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="44391-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44391-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44391-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44391-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44391-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44391-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44391-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44391-136">Dirección de inicio de los bytes con errores.</span><span class="sxs-lookup"><span data-stu-id="44391-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="44391-137">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44391-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="44391-138">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="44391-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44391-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44391-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44391-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44391-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44391-141">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="44391-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="44391-142">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="44391-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="44391-143">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="44391-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44391-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44391-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44391-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44391-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44391-146">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemName**")</span><span class="sxs-lookup"><span data-stu-id="44391-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="44391-147">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="44391-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44391-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44391-148">Remarks</span></span>

<span data-ttu-id="44391-149">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="44391-149">WMI does not implement this class.</span></span>

<span data-ttu-id="44391-150">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="44391-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="44391-151">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="44391-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44391-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44391-152">Requirements</span></span>



| <span data-ttu-id="44391-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="44391-153">Requirement</span></span> | <span data-ttu-id="44391-154">Value</span><span class="sxs-lookup"><span data-stu-id="44391-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44391-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44391-155">Minimum supported client</span></span><br/> | <span data-ttu-id="44391-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44391-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44391-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44391-157">Minimum supported server</span></span><br/> | <span data-ttu-id="44391-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44391-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44391-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44391-159">Namespace</span></span><br/>                | <span data-ttu-id="44391-160">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="44391-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44391-161">MOF</span><span class="sxs-lookup"><span data-stu-id="44391-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44391-162"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44391-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44391-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44391-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44391-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44391-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

