---
description: Un proveedor es un archivo DLL de rendimiento que proporciona datos de contador a los consumidores.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Crear un archivo DLL de extensión de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ef4509af77bcc1a4016e494a2834d40162305a837349e32a573cbf36d994d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011323"
---
# <a name="creating-a-performance-extension-dll"></a>Crear un archivo DLL de extensión de rendimiento

> [!IMPORTANT]
> Debido a limitaciones significativas de rendimiento y confiabilidad, el método para proporcionar datos de contadores de rendimiento que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en Proporcionar datos de contador mediante la versión [2.0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar también ese método.

Un [proveedor V1 usa](providing-counter-data.md) un archivo DLL de rendimiento que proporciona datos de contador a los consumidores. El archivo DLL de rendimiento debe exportar [**las funciones OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)y [**ClosePerformanceData.**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) Normalmente, se usa un archivo de definición de módulo (.def) para exportar las funciones desde el archivo DLL. El sistema llama a estas funciones cuando un consumidor consulta los datos de rendimiento.

La primera vez que un consumidor llama a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)o si el consumidor usa la función [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) o [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) para abrir , el sistema llama a la función `HKEY_PERFORMANCE_DATA` [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) para cada proveedor registrado en el equipo. [](adding-performance-counters.md) La excepción es si el proveedor especifica la lista de objetos que admite en la `[objects]` sección del .INI archivo. En este caso, el sistema llama al proveedor solo si uno de los objetos consultados coincide con un objeto de la lista.

La [**función OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) proporciona a cada proveedor una oportunidad para inicializar sus estructuras de datos de rendimiento. A continuación, **si la función OpenPerformanceData** se devuelve correctamente, el sistema llama a la función [**CollectPerformanceData del**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) proveedor. Las llamadas posteriores [**a RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) hacen que el sistema llame a la **función CollectPerformanceData.**

Cuando el consumidor termina de recopilar datos de rendimiento, especifica `HKEY_PERFORMANCE_DATA` en una llamada a la función [**RegCloseKey.**](/windows/desktop/api/winreg/nf-winreg-regclosekey) Esto hace que el sistema llame a la [**función ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) para cada proveedor. A continuación, se descargan los proveedores.

Es posible que varios consumidores recopile datos de rendimiento al mismo tiempo. El sistema llama [**a las funciones OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) solo una vez cada vez que se carga o descarga el archivo DLL.

> [!Note]
> Asegúrese de incluir "C" externo en el código de C++ para evitar que el compilador agregue decoración a los nombres de función. De lo contrario, es posible que el sistema no encuentre las funciones.

> [!Note]
> Si se produce un error al cargar el archivo DLL de rendimiento, buscar las funciones o llamar a las funciones, el sistema deshabilitará el proveedor para las recopilaciones posteriores dentro del mismo proceso. Además, si esto ocurre mientras se ejecuta en un proceso con **privilegios,** el sistema agrega un valor Deshabilitar contadores de rendimiento a la clave de rendimiento para evitar que el proveedor se cargue en el futuro. 

Para obtener más información sobre cómo escribir un archivo DLL de rendimiento, vea los temas siguientes:

- [Implementación de la función OpenPerformanceData](implementing-openperformancedata.md)
- [Implementación de la función CollectPerformanceData](implementing-collectperformancedata.md)
- [Control de errores en el archivo DLL](error-handling-in-the-dll.md)
- [Restringir el acceso a los archivos DLL de la extensión de rendimiento](restricting-access-to-performance-extension--dlls.md)
- [Ejemplos de DLL de rendimiento](performance-dll-samples.md)
