---
description: Al escribir un proveedor de alto rendimiento que deriva clases de Win32 \_ PerfRawData, debe seguir convenciones específicas para que WMI pueda proporcionar datos a los valores de propiedad.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Compatibilidad con la clase Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652545"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="d6a23-103">Compatibilidad con la \_ clase Win32 PerfRawData</span><span class="sxs-lookup"><span data-stu-id="d6a23-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="d6a23-104">Al escribir un proveedor de alto rendimiento que deriva clases de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), debe seguir convenciones específicas para que WMI pueda proporcionar datos a los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d6a23-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="d6a23-105">No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento en ninguna versión del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a23-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="d6a23-106">Para obtener más información, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)y [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d6a23-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="d6a23-107">En el procedimiento siguiente se describe cómo admitir la clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) con el proveedor de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d6a23-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="d6a23-108">**Para admitir la \_ clase Win32 PerfRawData**</span><span class="sxs-lookup"><span data-stu-id="d6a23-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="d6a23-109">Cree la clase en el \\ espacio de nombres root CIMv2.</span><span class="sxs-lookup"><span data-stu-id="d6a23-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="d6a23-110">La clase se debe derivar [**de \_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y tener el calificador de **HiPerf** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="d6a23-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="d6a23-111">También puede Agregar clases de datos de rendimiento de WDM (controlador) al \\ espacio de nombres WMI raíz.</span><span class="sxs-lookup"><span data-stu-id="d6a23-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="d6a23-112">Para obtener más información acerca de la creación de su propia clase para WMI, consulte [diseño de clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="d6a23-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="d6a23-113">Especifique el proveedor como "NT5 \_ GenericPerfProvider \_ v1" en el calificador de **proveedor** .</span><span class="sxs-lookup"><span data-stu-id="d6a23-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="d6a23-114">Especifique los siguientes calificadores de nivel de clase:</span><span class="sxs-lookup"><span data-stu-id="d6a23-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="d6a23-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="d6a23-115">**HiPerf**</span></span>
    -   <span data-ttu-id="d6a23-116">**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="d6a23-116">**Locale**</span></span>
    -   <span data-ttu-id="d6a23-117">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="d6a23-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="d6a23-118">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="d6a23-118">**Provider**</span></span>

    <span data-ttu-id="d6a23-119">Para obtener más información, vea [**calificadores de clase para las clases de contador de rendimiento**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d6a23-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="d6a23-120">No defina el calificador **GenericPerfCtr** porque está reservado para el proceso ADAP que transfiere los datos de la biblioteca de rendimiento a clases WMI.</span><span class="sxs-lookup"><span data-stu-id="d6a23-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="d6a23-121">Rellene las propiedades de marca de tiempo y frecuencia apropiadas utilizadas para calcular las fórmulas de tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="d6a23-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="d6a23-122">Estas propiedades se heredan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y, si está escribiendo un proveedor de alto rendimiento, debe rellenarlos para que la clase se muestre en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="d6a23-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="d6a23-123">Incluya una propiedad de clave denominada **nombre** en la clase (esta propiedad no es necesaria para las clases singleton).</span><span class="sxs-lookup"><span data-stu-id="d6a23-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="d6a23-124">No debe utilizar ninguna propiedad de clave que no sea **el nombre** de la clase.</span><span class="sxs-lookup"><span data-stu-id="d6a23-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="d6a23-125">Crear propiedades con tipo de datos como **DWORD** (**Uint32**) o **QWord** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="d6a23-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="d6a23-126">Estas propiedades se convierten en contadores de rendimiento cuando se transfieren a las bibliotecas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d6a23-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="d6a23-127">Especifique los siguientes calificadores de nivel de propiedad para todas las propiedades de la clase:</span><span class="sxs-lookup"><span data-stu-id="d6a23-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="d6a23-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d6a23-128">**DisplayName**</span></span>
    -   <span data-ttu-id="d6a23-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d6a23-129">**CounterType**</span></span>
    -   <span data-ttu-id="d6a23-130">**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="d6a23-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="d6a23-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6a23-131">**Description**</span></span>
    -   <span data-ttu-id="d6a23-132">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="d6a23-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="d6a23-133">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="d6a23-133">**PerfDetail**</span></span>

    <span data-ttu-id="d6a23-134">Para obtener más información, vea [**calificadores de propiedad para las clases de contador de rendimiento**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d6a23-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="d6a23-135">Además, el archivo de encabezado WINPERF. h contiene valores que puede especificar para **PerfDetail** y **contratype**.</span><span class="sxs-lookup"><span data-stu-id="d6a23-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="d6a23-136">WMI usa los calificadores **displayName**, **locale** y **Description** para la localización.</span><span class="sxs-lookup"><span data-stu-id="d6a23-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="d6a23-137">Debe agregar calificadores modificados al espacio de \_ nombres MS 409 (Inglés) para que el monitor de sistema pueda mostrar correctamente los datos de clase.</span><span class="sxs-lookup"><span data-stu-id="d6a23-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="d6a23-138">Esto significa que se modifica la definición de propiedad agregando un calificador de **Descripción** con texto explicativo y rellenando el valor **displayName** .</span><span class="sxs-lookup"><span data-stu-id="d6a23-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="d6a23-139">También debe agregar calificadores modificados a cualquier otro espacio de nombres de configuración regional que admita la clase.</span><span class="sxs-lookup"><span data-stu-id="d6a23-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="d6a23-140">Si un usuario solicita datos de una configuración regional para la que no se proporcionan calificadores modificados, WMI toma como valor predeterminado las definiciones especificadas en el \_ espacio de nombres MS 409.</span><span class="sxs-lookup"><span data-stu-id="d6a23-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="d6a23-141">Cree una propiedad base para cualquier propiedad que tenga un tipo de contador que espera un valor base.</span><span class="sxs-lookup"><span data-stu-id="d6a23-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="d6a23-142">Esta propiedad sigue inmediatamente a la propiedad y se denomina \* PropertyName \***\_ base**.</span><span class="sxs-lookup"><span data-stu-id="d6a23-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="d6a23-143">Por ejemplo, la propiedad Average **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) requiere una propiedad base denominada **AvgDiskBytesPerRead \_ base** para contar el número de muestras.</span><span class="sxs-lookup"><span data-stu-id="d6a23-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="d6a23-144">Para determinar si el tipo de contador que desea utilizar requiere una propiedad base, busque el tipo de contador por nombre o valor decimal en [tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="d6a23-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="d6a23-145">Asegúrese de que el proveedor cumple los [requisitos de rendimiento](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="d6a23-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6a23-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6a23-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6a23-147">Crear un proveedor de instancias en un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="d6a23-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
