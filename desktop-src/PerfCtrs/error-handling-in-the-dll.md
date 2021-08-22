---
description: Use el registro de eventos para registrar los errores que se producen en el archivo DLL de rendimiento.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Control de errores en el archivo DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a64dcfdf360a1dcc2301b5496d3f4630631cd7bfbc3fffb0e2cd5408120351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517475"
---
# <a name="error-handling-in-the-dll"></a>Control de errores en el archivo DLL

Use el registro de eventos para registrar los errores que se producen en el archivo DLL de rendimiento. El registro de eventos de error ayuda a solucionar problemas de aplicaciones que proporcionan datos de rendimiento durante el desarrollo y después de la instalación. Debe limitar la cantidad de registro de errores que se produce en la función [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) porque la recopilación de datos puede ser frecuente.

El sistema registra los siguientes errores en el registro de eventos si hay problemas con la [**función OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) Si se produce uno de los siguientes errores, el sistema no vuelve a llamar a la DLL de rendimiento. En su lugar, se descarga el archivo DLL.

-   **PERFLIB \_ OPEN \_ PROC \_ NOT \_ FOUND**: se registra cuando el nombre del procedimiento definido en el registro no se encuentra en el archivo DLL como una función exportada. Esto suele ocurrir cuando el archivo DLL o el servicio no están instalados correctamente o se ha cambiado el nombre de la función sin actualizar el procedimiento de instalación.
-   **PERFLIB \_ OPEN \_ PROC \_ FAILURE :** se registra cuando el procedimiento abierto devuelve un estado de error distinto de ERROR \_ SUCCESS. En caso de que esto suceda, el archivo DLL también debería haber escrito una entrada del registro de eventos que describa las condiciones que provocaron el error.
-   **PERFLIB \_ OPEN \_ PROC \_ EXCEPTION :** se registra cuando el procedimiento abierto encuentra una excepción no controlada. Esto suele deberse a una condición de error inesperada detectada por el procedimiento abierto.

 

 
