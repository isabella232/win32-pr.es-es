---
description: Un proveedor es un archivo DLL de rendimiento que proporciona datos de contador a los consumidores.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Crear un archivo DLL de extensión de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d397f1581454aca1b25c447b35f250eefd215f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909742"
---
# <a name="creating-a-performance-extension-dll"></a>Crear un archivo DLL de extensión de rendimiento

> [!IMPORTANT]
> Debido a las limitaciones de rendimiento y confiabilidad significativas, el método para proporcionar los datos del contador de rendimiento que se describen en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método también.

Un [proveedor v1](providing-counter-data.md) usa un archivo dll de rendimiento que proporciona datos de contador a los consumidores. El archivo DLL de rendimiento debe exportar las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)y [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) . Normalmente, se usa un archivo de definición de módulo (. def) para exportar las funciones del archivo DLL. El sistema llama a estas funciones cuando un consumidor consulta los datos de rendimiento.

La primera vez que un consumidor llama a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa), o si el consumidor usa la función [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) o [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) para abrir `HKEY_PERFORMANCE_DATA` , el sistema llama a la función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) para cada proveedor [registrado](adding-performance-counters.md) en el equipo. La excepción es si el proveedor especifica la lista de objetos que admite en la `[objects]` sección de. Archivo INI. En este caso, el sistema llama al proveedor solo si uno de los objetos consultados coincide con un objeto de la lista.

La función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) proporciona a cada proveedor una oportunidad de inicializar sus estructuras de datos de rendimiento. Después, si la función **OpenPerformanceData** se devuelve correctamente, el sistema llama a la función [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) del proveedor. Las llamadas posteriores a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) hacen que el sistema llame a la función **CollectPerformanceData** .

Cuando el consumidor termina de recopilar datos de rendimiento, especifica `HKEY_PERFORMANCE_DATA` en una llamada a la función [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) . Esto hace que el sistema llame a la función [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) para cada proveedor. A continuación, se descargan los proveedores.

Es posible que varios consumidores recopilen datos de rendimiento al mismo tiempo. El sistema llama a las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) solo una vez cada vez que se carga o descarga el archivo dll.

> [!Note]
> Asegúrese de incluir extern "C" en el código de C++ para evitar que el compilador agregue decoraciones a los nombres de función; de lo contrario, es posible que el sistema no pueda encontrar las funciones.

> [!Note]
> Si se produce un error mientras se carga el archivo DLL de rendimiento, se buscan las funciones o se llama a las funciones, el sistema deshabilitará el proveedor para las colecciones posteriores en el mismo proceso. Además, si esto ocurre durante la ejecución en un proceso con privilegios, el sistema agrega un valor **deshabilitar contadores de rendimiento** a la clave de **rendimiento** para evitar que el proveedor se cargue en el futuro.

Para obtener más información sobre cómo escribir un archivo DLL de rendimiento, vea los temas siguientes:

- [Implementación de la función OpenPerformanceData](implementing-openperformancedata.md)
- [Implementación de la función CollectPerformanceData](implementing-collectperformancedata.md)
- [Control de errores en el archivo DLL](error-handling-in-the-dll.md)
- [Restringir el acceso a los archivos dll de extensión de rendimiento](restricting-access-to-performance-extension--dlls.md)
- [Ejemplos de DLL de rendimiento](performance-dll-samples.md)
