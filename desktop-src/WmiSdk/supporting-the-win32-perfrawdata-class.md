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
# <a name="supporting-the-win32_perfrawdata-class"></a>Compatibilidad con la \_ clase Win32 PerfRawData

Al escribir un proveedor de alto rendimiento que deriva clases de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), debe seguir convenciones específicas para que WMI pueda proporcionar datos a los valores de propiedad.

> [!Note]  
> No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento en ninguna versión del sistema operativo Windows. Para obtener más información, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)y [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md).

 

En el procedimiento siguiente se describe cómo admitir la clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) con el proveedor de alto rendimiento.

**Para admitir la \_ clase Win32 PerfRawData**

1.  Cree la clase en el \\ espacio de nombres root CIMv2.

    La clase se debe derivar [**de \_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y tener el calificador de **HiPerf** establecido en **true**. También puede Agregar clases de datos de rendimiento de WDM (controlador) al \\ espacio de nombres WMI raíz. Para obtener más información acerca de la creación de su propia clase para WMI, consulte [diseño de clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

2.  Especifique el proveedor como "NT5 \_ GenericPerfProvider \_ v1" en el calificador de **proveedor** .
3.  Especifique los siguientes calificadores de nivel de clase:

    -   **HiPerf**
    -   **Configuración regional**
    -   **PerfDetail**
    -   **Proveedor**

    Para obtener más información, vea [**calificadores de clase para las clases de contador de rendimiento**](class-qualifiers-for-performance-counter-classes.md). No defina el calificador **GenericPerfCtr** porque está reservado para el proceso ADAP que transfiere los datos de la biblioteca de rendimiento a clases WMI.

4.  Rellene las propiedades de marca de tiempo y frecuencia apropiadas utilizadas para calcular las fórmulas de tipo de contador.

    Estas propiedades se heredan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y, si está escribiendo un proveedor de alto rendimiento, debe rellenarlos para que la clase se muestre en el monitor de sistema.

5.  Incluya una propiedad de clave denominada **nombre** en la clase (esta propiedad no es necesaria para las clases singleton).

    No debe utilizar ninguna propiedad de clave que no sea **el nombre** de la clase.

6.  Crear propiedades con tipo de datos como **DWORD** (**Uint32**) o **QWord** (**UInt64**). Estas propiedades se convierten en contadores de rendimiento cuando se transfieren a las bibliotecas de rendimiento.
7.  Especifique los siguientes calificadores de nivel de propiedad para todas las propiedades de la clase:

    -   **DisplayName**
    -   **Tipo**
    -   **DefaultScale**
    -   **Descripción**
    -   **PerfDefault**
    -   **PerfDetail**

    Para obtener más información, vea [**calificadores de propiedad para las clases de contador de rendimiento**](property-qualifiers-for-performance-counter-classes.md). Además, el archivo de encabezado WINPERF. h contiene valores que puede especificar para **PerfDetail** y **contratype**.

    WMI usa los calificadores **displayName**, **locale** y **Description** para la localización. Debe agregar calificadores modificados al espacio de \_ nombres MS 409 (Inglés) para que el monitor de sistema pueda mostrar correctamente los datos de clase. Esto significa que se modifica la definición de propiedad agregando un calificador de **Descripción** con texto explicativo y rellenando el valor **displayName** . También debe agregar calificadores modificados a cualquier otro espacio de nombres de configuración regional que admita la clase. Si un usuario solicita datos de una configuración regional para la que no se proporcionan calificadores modificados, WMI toma como valor predeterminado las definiciones especificadas en el \_ espacio de nombres MS 409.

8.  Cree una propiedad base para cualquier propiedad que tenga un tipo de contador que espera un valor base.

    Esta propiedad sigue inmediatamente a la propiedad y se denomina * PropertyName ***\_ base**. Por ejemplo, la propiedad Average **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) requiere una propiedad base denominada **AvgDiskBytesPerRead \_ base** para contar el número de muestras. Para determinar si el tipo de contador que desea utilizar requiere una propiedad base, busque el tipo de contador por nombre o valor decimal en [tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md).

9.  Asegúrese de que el proveedor cumple los [requisitos de rendimiento](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
