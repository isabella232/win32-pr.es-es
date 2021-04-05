---
description: Utilice el registro de eventos para registrar los errores que se producen en el archivo DLL de rendimiento.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Control de errores en el archivo DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001978"
---
# <a name="error-handling-in-the-dll"></a>Control de errores en el archivo DLL

Utilice el registro de eventos para registrar los errores que se producen en el archivo DLL de rendimiento. El registro de eventos de error ayuda en la solución de problemas de aplicaciones que proporcionan datos de rendimiento durante el desarrollo y después de la instalación. Debe limitar la cantidad de registro de errores que se produce en la función [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) porque la recopilación de datos puede ser frecuente.

El sistema registra los siguientes errores en el registro de eventos si hay problemas con la función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) . Si se produce uno de los siguientes errores, el sistema no vuelve a llamar al archivo DLL de rendimiento. En su lugar, se descarga el archivo DLL.

-   **PERFLIB \_ OPEN \_ proc \_ not \_ found**: se registra cuando el nombre de procedimiento definido en el registro no se pudo encontrar en el archivo dll como una función exportada. Esto suele ocurrir cuando el archivo DLL o el servicio no está instalado correctamente o se ha cambiado el nombre de la función sin actualizar el procedimiento de instalación.
-   **PERFLIB \_ OPEN \_ proc \_ error**: se registra cuando el procedimiento abierto devolvió un estado de error que no es \_ correcto. En caso de que esto suceda, el archivo DLL debe haber especificado también una entrada en el registro de eventos que describe las condiciones que han provocado el error.
-   **PERFLIB \_ OPEN \_ proc \_ Exception**: se registra cuando el procedimiento abierto encuentra una excepción no controlada. Esto suele deberse a una condición de error inesperada detectada por el procedimiento abierto.

 

 
