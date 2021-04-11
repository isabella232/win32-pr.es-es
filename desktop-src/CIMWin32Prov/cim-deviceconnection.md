---
description: La clase de Asociación de CIM \_ DeviceConnection representa dos o más dispositivos conectados.
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: CIM_DeviceConnection (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275000"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="c6a14-103">CIM_DeviceConnection (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c6a14-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c6a14-104">La clase de Asociación de **CIM \_ DeviceConnection** representa dos o más dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="c6a14-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6a14-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c6a14-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c6a14-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c6a14-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c6a14-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c6a14-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c6a14-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c6a14-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a14-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6a14-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="c6a14-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6a14-110">Members</span></span>

<span data-ttu-id="c6a14-111">La **clase \_ de CIM de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c6a14-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="c6a14-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6a14-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6a14-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6a14-113">Properties</span></span>

<span data-ttu-id="c6a14-114">La **clase \_ DeviceConnection de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c6a14-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6a14-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c6a14-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a14-116">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="c6a14-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6a14-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="c6a14-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c6a14-119">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c6a14-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="c6a14-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="c6a14-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a14-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="c6a14-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6a14-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="c6a14-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c6a14-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe un segundo dispositivo lógico conectado al dispositivo antecedente.</span><span class="sxs-lookup"><span data-stu-id="c6a14-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="c6a14-125">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="c6a14-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a14-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6a14-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6a14-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-128">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="c6a14-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c6a14-129">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c6a14-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="c6a14-130">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="c6a14-130">Data width is specified in bits.</span></span> <span data-ttu-id="c6a14-131">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c6a14-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="c6a14-132">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="c6a14-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a14-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6a14-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6a14-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a14-135">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="c6a14-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="c6a14-136">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c6a14-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="c6a14-137">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c6a14-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="c6a14-138">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c6a14-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="c6a14-139">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c6a14-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6a14-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6a14-140">Remarks</span></span>

<span data-ttu-id="c6a14-141">La clase derivada de **CIM \_** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c6a14-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c6a14-142">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c6a14-142">WMI does not implement this class.</span></span> <span data-ttu-id="c6a14-143">Para obtener más información sobre las clases que se derivan de **CIM \_ DeviceConnection**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6a14-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c6a14-144">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c6a14-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6a14-145">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c6a14-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a14-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6a14-146">Requirements</span></span>



| <span data-ttu-id="c6a14-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a14-147">Requirement</span></span> | <span data-ttu-id="c6a14-148">Value</span><span class="sxs-lookup"><span data-stu-id="c6a14-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a14-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6a14-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a14-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6a14-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6a14-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6a14-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a14-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6a14-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6a14-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c6a14-153">Namespace</span></span><br/>                | <span data-ttu-id="c6a14-154">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c6a14-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6a14-155">MOF</span><span class="sxs-lookup"><span data-stu-id="c6a14-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6a14-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6a14-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6a14-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6a14-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6a14-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6a14-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a14-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6a14-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a14-160">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c6a14-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

