---
description: Al escribir un proveedor de alto rendimiento que deriva clases de Win32 \_ PerfFormattedData, debe seguir convenciones específicas para que WMI pueda calcular los valores de propiedad.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Compatibilidad con la clase Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707091"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="48c21-103">Compatibilidad con la \_ clase Win32 PerfFormattedData</span><span class="sxs-lookup"><span data-stu-id="48c21-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="48c21-104">Al escribir un proveedor de alto rendimiento que deriva clases de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), debe seguir convenciones específicas para que WMI pueda calcular los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="48c21-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="48c21-105">No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento en ninguna versión del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="48c21-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="48c21-106">Para obtener más información, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)y [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="48c21-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="48c21-107">En el procedimiento siguiente se describe cómo admitir la \_ clase Win32 PerfFormattedData.</span><span class="sxs-lookup"><span data-stu-id="48c21-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="48c21-108">**Para admitir la \_ clase Win32 PerfFormattedData**</span><span class="sxs-lookup"><span data-stu-id="48c21-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="48c21-109">Cree la clase en el mismo espacio de nombres que la clase sin formato correspondiente.</span><span class="sxs-lookup"><span data-stu-id="48c21-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="48c21-110">La clase se debe derivar [**de \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) y tener el calificador de **HiPerf** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="48c21-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="48c21-111">Para obtener más información acerca de la creación de su propia clase para WMI, consulte [diseño de clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="48c21-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="48c21-112">Especifique "HiPerfCooker \_ v1" en el calificador de [**proveedor**](class-qualifiers-for-performance-counter-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="48c21-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="48c21-113">Especifique los siguientes calificadores de nivel de clase además de los calificadores que se usan para las clases sin formato:</span><span class="sxs-lookup"><span data-stu-id="48c21-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="48c21-114">**Autocook**</span><span class="sxs-lookup"><span data-stu-id="48c21-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-115">**Autocook \_ RawClass**</span><span class="sxs-lookup"><span data-stu-id="48c21-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-116">**Cocida**</span><span class="sxs-lookup"><span data-stu-id="48c21-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-117">**Costoso**</span><span class="sxs-lookup"><span data-stu-id="48c21-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-118">**Dinámica**</span><span class="sxs-lookup"><span data-stu-id="48c21-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="48c21-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="48c21-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-120">**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="48c21-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-121">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="48c21-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-122">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="48c21-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-123">**Simple**</span><span class="sxs-lookup"><span data-stu-id="48c21-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="48c21-124">No establezca ningún valor para **GenericPerfCtr**, **PerfIndex** o **HelpIndex** , ya que lo establecerá el proceso ADAP.</span><span class="sxs-lookup"><span data-stu-id="48c21-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="48c21-125">Para obtener más información, vea [**calificadores de clase para las clases de contador de rendimiento**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="48c21-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="48c21-126">Incluya una propiedad de clave denominada **nombre** en la clase (esta propiedad no es necesaria para las clases singleton).</span><span class="sxs-lookup"><span data-stu-id="48c21-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="48c21-127">El valor de la propiedad **Name** debe ser el mismo que el de la clase sin formato correspondiente.</span><span class="sxs-lookup"><span data-stu-id="48c21-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="48c21-128">No debe utilizar ninguna propiedad de clave que no sea **el nombre** de la clase.</span><span class="sxs-lookup"><span data-stu-id="48c21-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="48c21-129">Cree los datos de las propiedades con el tipo **DWORD** (**Uint32**) o **QWord** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="48c21-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="48c21-130">Las propiedades deben corresponder a una propiedad de la clase sin formato o a una propiedad de la clase que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="48c21-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="48c21-131">Especifique los siguientes calificadores de nivel de propiedad para todas las propiedades de la clase además de los calificadores **PerfIndex** y **PerfDetail** que se usan para las propiedades de la clase sin formato:</span><span class="sxs-lookup"><span data-stu-id="48c21-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="48c21-132">**Básica**</span><span class="sxs-lookup"><span data-stu-id="48c21-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-133">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="48c21-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-134">**Contador**</span><span class="sxs-lookup"><span data-stu-id="48c21-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-135">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="48c21-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-136">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="48c21-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="48c21-137">**SampleWindow**</span><span class="sxs-lookup"><span data-stu-id="48c21-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="48c21-138">Para obtener más información, vea [**calificadores de propiedad para las clases de contador de rendimiento**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="48c21-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="48c21-139">Además, el archivo de encabezado WINPERF. h contiene valores que puede especificar para **PerfDetail** y **contratype**.</span><span class="sxs-lookup"><span data-stu-id="48c21-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="48c21-140">Asegúrese de que el proveedor cumple los [requisitos de rendimiento](#performance-requirements).</span><span class="sxs-lookup"><span data-stu-id="48c21-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="48c21-141">Requisitos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="48c21-141">Performance Requirements</span></span>

<span data-ttu-id="48c21-142">Al escribir un proveedor de alto rendimiento, su rendimiento debe cumplir los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="48c21-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="48c21-143">Abrir el archivo DLL de alto rendimiento no puede tardar más de 100 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="48c21-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="48c21-144">En general, abrir cada proveedor de alto rendimiento y la biblioteca de rendimiento no puede superar los 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="48c21-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="48c21-145">La actualización de datos no puede tardar más de 10 milisegundos por recopilación.</span><span class="sxs-lookup"><span data-stu-id="48c21-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="48c21-146">En una operación de actualización y recopilación general, todos los proveedores de alto rendimiento juntos no pueden tardar más de 800 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="48c21-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="48c21-147">La carga general de la CPU para todos los proveedores de alto rendimiento no puede superar la sobrecarga de CPU del 6-7% de forma interactiva o el 5% para el registro.</span><span class="sxs-lookup"><span data-stu-id="48c21-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48c21-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48c21-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48c21-149">Crear un proveedor de instancias en un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="48c21-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
