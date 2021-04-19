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
# <a name="supporting-the-win32_perfformatteddata-class"></a>Compatibilidad con la \_ clase Win32 PerfFormattedData

Al escribir un proveedor de alto rendimiento que deriva clases de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), debe seguir convenciones específicas para que WMI pueda calcular los valores de propiedad.

> [!Note]  
> No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento en ninguna versión del sistema operativo Windows. Para obtener más información, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)y [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).

 

En el procedimiento siguiente se describe cómo admitir la \_ clase Win32 PerfFormattedData.

**Para admitir la \_ clase Win32 PerfFormattedData**

1.  Cree la clase en el mismo espacio de nombres que la clase sin formato correspondiente. La clase se debe derivar [**de \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) y tener el calificador de **HiPerf** establecido en **true**. Para obtener más información acerca de la creación de su propia clase para WMI, consulte [diseño de clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).
2.  Especifique "HiPerfCooker \_ v1" en el calificador de [**proveedor**](class-qualifiers-for-performance-counter-classes.md) .
3.  Especifique los siguientes calificadores de nivel de clase además de los calificadores que se usan para las clases sin formato:

    -   [**Autocook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ RawClass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cocida**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Costoso**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dinámica**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Configuración regional**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Proveedor**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Simple**](standard-wmi-qualifiers.md)

    > [!Note]  
    > No establezca ningún valor para **GenericPerfCtr**, **PerfIndex** o **HelpIndex** , ya que lo establecerá el proceso ADAP. Para obtener más información, vea [**calificadores de clase para las clases de contador de rendimiento**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Incluya una propiedad de clave denominada **nombre** en la clase (esta propiedad no es necesaria para las clases singleton).

    El valor de la propiedad **Name** debe ser el mismo que el de la clase sin formato correspondiente. No debe utilizar ninguna propiedad de clave que no sea **el nombre** de la clase.

5.  Cree los datos de las propiedades con el tipo **DWORD** (**Uint32**) o **QWord** (**UInt64**).

    Las propiedades deben corresponder a una propiedad de la clase sin formato o a una propiedad de la clase que se va a crear.

6.  Especifique los siguientes calificadores de nivel de propiedad para todas las propiedades de la clase además de los calificadores **PerfIndex** y **PerfDetail** que se usan para las propiedades de la clase sin formato:

    -   [**Básica**](property-qualifiers-for-performance-counter-classes.md)
    -   [**CookingType**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Contador**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Para obtener más información, vea [**calificadores de propiedad para las clases de contador de rendimiento**](property-qualifiers-for-performance-counter-classes.md). Además, el archivo de encabezado WINPERF. h contiene valores que puede especificar para **PerfDetail** y **contratype**.

7.  Asegúrese de que el proveedor cumple los [requisitos de rendimiento](#performance-requirements).

## <a name="performance-requirements"></a>Requisitos de rendimiento

Al escribir un proveedor de alto rendimiento, su rendimiento debe cumplir los siguientes requisitos:

-   Abrir el archivo DLL de alto rendimiento no puede tardar más de 100 milisegundos. En general, abrir cada proveedor de alto rendimiento y la biblioteca de rendimiento no puede superar los 5 segundos.
-   La actualización de datos no puede tardar más de 10 milisegundos por recopilación. En una operación de actualización y recopilación general, todos los proveedores de alto rendimiento juntos no pueden tardar más de 800 milisegundos.
-   La carga general de la CPU para todos los proveedores de alto rendimiento no puede superar la sobrecarga de CPU del 6-7% de forma interactiva o el 5% para el registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
