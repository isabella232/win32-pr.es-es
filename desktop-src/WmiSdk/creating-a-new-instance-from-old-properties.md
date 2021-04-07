---
description: Una clase de vista de combinación contiene propiedades de las instancias de clase de origen conectadas por un valor de propiedad común, como Class1. Prop1 = clase2. Prop2. Cada instancia de una clase de vista de combinación se compone de partes de diferentes instancias de clase.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Crear una nueva instancia a partir de las propiedades anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002829"
---
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="9e6c1-104">Crear una nueva instancia a partir de las propiedades anteriores</span><span class="sxs-lookup"><span data-stu-id="9e6c1-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="9e6c1-105">Una clase de vista de combinación contiene propiedades de las instancias de clase de origen conectadas por un valor de propiedad común, como **Class1. Prop1**  =  **clase2. Prop2**.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="9e6c1-106">Cada instancia de una clase de vista de combinación se compone de partes de diferentes instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="9e6c1-107">Puede basar una clase de vista de combinación en la desigualdad de los valores de propiedad, como **Class1. Prop1**  <>  **clase2. Prop2** , donde **Prop1** y **Prop2** no están asignados a la misma propiedad en la clase de vista.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="9e6c1-108">Una clase de vista de combinación es útil cuando la información que busca está contenida en clases independientes pero relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="9e6c1-109">Por ejemplo, si desea obtener información acerca de una impresora y de la configuración de la impresora, puede crear una clase de vista de combinación que contenga algunas de las propiedades de la clase [**\_ Printer de Win32**](/windows/desktop/CIMWin32Prov/win32-printer) y algunas de las propiedades de la clase [**\_ PrinterConfiguration de Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="9e6c1-110">Sin el proveedor de vistas, debe recuperar y combinar las propiedades de las instancias independientes para obtener la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="9e6c1-111">En el procedimiento siguiente se describe cómo crear una clase de vista de combinación.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="9e6c1-112">**Para crear una clase de vista de combinación**</span><span class="sxs-lookup"><span data-stu-id="9e6c1-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="9e6c1-113">Comience una definición de clase con el calificador de cadena [**joinon**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="9e6c1-114">Los calificadores [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** y **Union** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="9e6c1-115">Si es necesario, filtre las instancias que desee en la clase de combinación aplicando el calificador [**PostJoinFilter**](postjoinfilter-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="9e6c1-116">El proveedor [**PostJoinFilter**](postjoinfilter-qualifier.md) permite restringir las instancias de una clase de vista a instancias que cumplen condiciones específicas.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="9e6c1-117">Cree las consultas que definen las instancias de origen de la clase de vista con el calificador [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="9e6c1-118">Defina los nombres y las ubicaciones de los espacios de nombres donde se encuentran las instancias de origen con el calificador [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="9e6c1-119">Defina las propiedades que desee en una clase de vista de combinación con el calificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="9e6c1-120">Cuando las propiedades se agregan a la vista de combinación en función de la igualdad, las dos propiedades de origen deben asignarse en un calificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="9e6c1-121">En el ejemplo de código siguiente se muestran dos propiedades que se asignan en un calificador **PropertySources** .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="9e6c1-122">Con el calificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , puede etiquetar las propiedades que pertenecen a una clase de origen.</span><span class="sxs-lookup"><span data-stu-id="9e6c1-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="9e6c1-123">En el ejemplo de código siguiente se muestra una clase de vista de combinación creada a partir de las clases de proveedor del monitor de rendimiento [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) y [**Win32 \_ PerfRawData \_ PerfProc \_ Thread**](/previous-versions//aa394325(v=vs.85)) con propiedades de las dos clases Unidas por la propiedad **ProcessId** .</span><span class="sxs-lookup"><span data-stu-id="9e6c1-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
