---
description: Al escribir un proveedor de alto rendimiento que deriva clases de Win32 PerfRawData, debe seguir convenciones específicas para que WMI pueda proporcionar datos a los valores \_ de propiedad.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Compatibilidad con la Win32_PerfRawData clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c9899c88849c70265b019c1d73021c61cae4758c41f462349537bd2e806ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050123"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>Compatibilidad con la clase PerfRawData de Win32 \_

Al escribir un proveedor de alto rendimiento que deriva clases de [**Win32 \_ PerfRawData,**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)debe seguir convenciones específicas para que WMI pueda proporcionar datos a los valores de propiedad.

> [!Note]  
> No se recomienda escribir un proveedor de alto rendimiento WMI para crear contadores de rendimiento en ninguna versión del Windows operativo. Para obtener más información, vea [Convertir un proveedor de instancias en](making-an-instance-provider-into-a-high-performance-provider.md)un proveedor de High-Performance y [bibliotecas de rendimiento y WMI.](performance-libraries-and-wmi.md)

 

En el procedimiento siguiente se describe cómo admitir la clase [**\_ PerfRawData win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) con el proveedor de alto rendimiento.

**Para admitir la clase PerfRawData de Win32 \_**

1.  Cree la clase en el espacio de nombres \\ CIMv2 raíz.

    La clase debe derivarse de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y tener el calificador **Hiperf** establecido en **TRUE.** También puede agregar clases de datos de rendimiento de WDM (controlador) al espacio de \\ nombres wmi raíz. Para obtener más información sobre cómo crear su propia clase para WMI, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).

2.  Especifique el proveedor como "NT5 \_ GenericPerfProvider \_ V1" en el **calificador Provider.**
3.  Especifique los siguientes calificadores de nivel de clase:

    -   **HiPerf**
    -   **Configuración regional**
    -   **PerfDetail**
    -   **Proveedor**

    Para obtener más información, vea [**Calificadores de clase para clases de contador de rendimiento**](class-qualifiers-for-performance-counter-classes.md). No defina el calificador **GenericPerfCtr** porque está reservado para el proceso de ADAP que transfiere los datos de la biblioteca de rendimiento a clases WMI.

4.  Rellene las propiedades de marca de tiempo y frecuencia adecuadas que se usan para calcular fórmulas de tipo de contador.

    Estas propiedades se heredan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y, si escribe un proveedor de alto rendimiento, debe rellenar estas propiedades para que la clase se muestre en el Monitor de sistema.

5.  Incluya una propiedad de clave denominada **Name** en la clase (esta propiedad no es necesaria para las clases singleton).

    No debe usar ninguna propiedad de clave que no **sea Name** en la clase.

6.  Cree propiedades con tipo de datos **como DWORD** (**uint32**) o **QWORD** (**uint64**). Estas propiedades se convierten en contadores de rendimiento cuando se transfieren a las bibliotecas de rendimiento.
7.  Especifique los siguientes calificadores de nivel de propiedad para todas las propiedades de la clase:

    -   **DisplayName**
    -   **CounterType**
    -   **DefaultScale**
    -   **Descripción**
    -   **PerfDefault**
    -   **PerfDetail**

    Para obtener más información, vea [**Calificadores de propiedad para clases de contadores de rendimiento.**](property-qualifiers-for-performance-counter-classes.md) Además, el archivo de encabezado Winperf.h contiene valores que puede especificar para **PerfDetail** y **CounterType**.

    WMI usa los **calificadores DisplayName**, **Locale** **y Description** para la localización. Debe agregar calificadores modificados al espacio de nombres MS 409 (inglés) para que el Monitor de sistema pueda mostrar correctamente \_ los datos de clase. Esto significa que modifica la definición de propiedad agregando un calificador **Description** con texto explicativo y rellenando el **valor DisplayName.** También debe agregar calificadores modificados a cualquier otro espacio de nombres de configuración regional que admita la clase . Si un usuario solicita datos de una configuración regional para la que no se proporcionan calificadores modificados, WMI tiene como valor predeterminado las definiciones especificadas en el espacio de nombres MS \_ 409.

8.  Cree una propiedad base para cualquier propiedad que tenga un tipo de contador que espere un valor base.

    Esta propiedad sigue inmediatamente a la propiedad y se denomina *propertyname***\_ Base**. Por ejemplo, la propiedad promedio **AvgDiskBytesPerRead** de la clase [**\_ \_ \_ LogicalDisk PerfRawData PerfDisk de Win32**](./retrieving-raw-and-formatted-performance-data.md) requiere una propiedad base denominada **AvgDiskBytesPerRead \_ Base** para contar el número de muestras. Para determinar si el tipo de contador que desea usar requiere una propiedad base, busque el tipo de contador por nombre o valor decimal en Tipos de [contadores de](wmi-performance-counter-types.md)rendimiento WMI .

9.  Asegúrese de que el proveedor cumple los [requisitos de rendimiento.](supporting-the-win32-perfformatteddata-class.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Convertir un proveedor de instancias en un High-Performance personalizado](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
