---
description: Al escribir un proveedor de alto rendimiento que derive clases de Win32 PerfFormattedData, debe seguir convenciones específicas para que WMI pueda calcular los valores \_ de propiedad.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Compatibilidad con la Win32_PerfFormattedData clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bbed50bde7ef16f6362d28151744cf22d66e5d0f56df253ad48ab469b397d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050133"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Compatibilidad con la clase PerfFormattedData de Win32 \_

Al escribir un proveedor de alto rendimiento que derive clases de [**Win32 \_ PerfFormattedData,**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)debe seguir convenciones específicas para que WMI pueda calcular los valores de propiedad.

> [!Note]  
> No se recomienda escribir un proveedor de alto rendimiento WMI para crear contadores de rendimiento en ninguna versión del Windows operativo. Para obtener más información, vea [Convertir un proveedor de instancias](making-an-instance-provider-into-a-high-performance-provider.md)en un proveedor High-Performance y [bibliotecas de rendimiento y WMI.](performance-libraries-and-wmi.md)

 

En el procedimiento siguiente se describe cómo admitir la clase \_ PerfFormattedData de Win32.

**Para admitir la clase PerfFormattedData de Win32 \_**

1.  Cree la clase en el mismo espacio de nombres que la clase sin formato correspondiente. La clase debe derivarse de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) y tener el calificador **HiPerf** establecido en **TRUE.** Para obtener más información sobre cómo crear su propia clase para WMI, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).
2.  Especifique "HiPerfCooker \_ v1" en el [**calificador Provider.**](class-qualifiers-for-performance-counter-classes.md)
3.  Especifique los siguientes calificadores de nivel de clase además de los calificadores usados para las clases sin formato:

    -   [**AutoCook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ RawClass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cocinado**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Costoso**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dinámica**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Configuración regional**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Proveedor**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > No establezca ningún valor para **GenericPerfCtr,** **PerfIndex** o **HelpIndex** porque lo establecerá el proceso de ADAP. Para obtener más información, vea [**Calificadores de clase para clases de contador de rendimiento**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Incluya una propiedad de clave denominada **Name** en la clase (esta propiedad no es necesaria para las clases singleton).

    El valor de la **propiedad Name** debe ser el mismo que el de la clase sin formato correspondiente. No debe usar ninguna propiedad de clave que no **sea Name** en la clase.

5.  Cree datos de propiedades con el tipo **DWORD** (**uint32**) o **QWORD** (**uint64**).

    Las propiedades deben corresponder a una propiedad de la clase sin formato o a una propiedad de la clase que está creando.

6.  Especifique los siguientes calificadores de nivel de propiedad para todas las propiedades de la clase, además de los calificadores **PerfIndex** y **PerfDetail** usados para las propiedades de clase sin formato:

    -   [**Base**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Tipo de cocina**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Contador**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Para obtener más información, vea [**Calificadores de propiedad para las clases de contador de rendimiento**](property-qualifiers-for-performance-counter-classes.md). Además, el archivo de encabezado Winperf.h contiene valores que puede especificar para **PerfDetail** y **CounterType.**

7.  Asegúrese de que el proveedor cumple los [requisitos de rendimiento.](#performance-requirements)

## <a name="performance-requirements"></a>Requisitos de rendimiento

Al escribir un proveedor de alto rendimiento, su rendimiento debe cumplir los siguientes requisitos:

-   La apertura del archivo DLL de alto rendimiento no puede tardar más de 100 milisegundos. En general, la apertura de cada proveedor de alto rendimiento y la biblioteca de rendimiento no puede superar los 5 segundos.
-   La actualización de datos no puede tardar más de 10 milisegundos por recopilación. En una operación de actualización y recopilación general, todos los proveedores de alto rendimiento no pueden tardar más de 800 milisegundos.
-   La carga total de CPU para todos los proveedores de alto rendimiento no puede superar la sobrecarga de CPU del 6 al 7 % de forma interactiva o del 5 % para el registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Convertir un proveedor de instancias en un High-Performance de recursos](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
