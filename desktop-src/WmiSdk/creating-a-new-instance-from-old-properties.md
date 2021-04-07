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
# <a name="creating-a-new-instance-from-old-properties"></a>Crear una nueva instancia a partir de las propiedades anteriores

Una clase de vista de combinación contiene propiedades de las instancias de clase de origen conectadas por un valor de propiedad común, como **Class1. Prop1**  =  **clase2. Prop2**. Cada instancia de una clase de vista de combinación se compone de partes de diferentes instancias de clase.

Puede basar una clase de vista de combinación en la desigualdad de los valores de propiedad, como **Class1. Prop1**  <>  **clase2. Prop2** , donde **Prop1** y **Prop2** no están asignados a la misma propiedad en la clase de vista.

Una clase de vista de combinación es útil cuando la información que busca está contenida en clases independientes pero relacionadas. Por ejemplo, si desea obtener información acerca de una impresora y de la configuración de la impresora, puede crear una clase de vista de combinación que contenga algunas de las propiedades de la clase [**\_ Printer de Win32**](/windows/desktop/CIMWin32Prov/win32-printer) y algunas de las propiedades de la clase [**\_ PrinterConfiguration de Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) . Sin el proveedor de vistas, debe recuperar y combinar las propiedades de las instancias independientes para obtener la información que necesita.

En el procedimiento siguiente se describe cómo crear una clase de vista de combinación.

**Para crear una clase de vista de combinación**

1.  Comience una definición de clase con el calificador de cadena [**joinon**](qualifiers-specific-to-the-view-provider.md) .

    Los calificadores [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** y **Union** se excluyen mutuamente.

2.  Si es necesario, filtre las instancias que desee en la clase de combinación aplicando el calificador [**PostJoinFilter**](postjoinfilter-qualifier.md) .

    El proveedor [**PostJoinFilter**](postjoinfilter-qualifier.md) permite restringir las instancias de una clase de vista a instancias que cumplen condiciones específicas.

3.  Cree las consultas que definen las instancias de origen de la clase de vista con el calificador [**ViewSources**](viewsources-qualifier.md) .
4.  Defina los nombres y las ubicaciones de los espacios de nombres donde se encuentran las instancias de origen con el calificador [**ViewSpaces**](viewspaces-qualifier.md) .
5.  Defina las propiedades que desee en una clase de vista de combinación con el calificador [**PropertySources**](propertysources-qualifier.md) .

    Cuando las propiedades se agregan a la vista de combinación en función de la igualdad, las dos propiedades de origen deben asignarse en un calificador [**PropertySources**](propertysources-qualifier.md) .

    En el ejemplo de código siguiente se muestran dos propiedades que se asignan en un calificador **PropertySources** .

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    Con el calificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , puede etiquetar las propiedades que pertenecen a una clase de origen.

En el ejemplo de código siguiente se muestra una clase de vista de combinación creada a partir de las clases de proveedor del monitor de rendimiento [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) y [**Win32 \_ PerfRawData \_ PerfProc \_ Thread**](/previous-versions//aa394325(v=vs.85)) con propiedades de las dos clases Unidas por la propiedad **ProcessId** .

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

 

 
