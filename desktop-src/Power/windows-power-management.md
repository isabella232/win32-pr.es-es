---
description: Windows administración de energía permite que los usuarios puedan acceder al instante a los equipos con solo tocar un botón o una tecla.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Windows Administración de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7335b521b22b762468d2b542ea3c4fdbfcacb798860d4997f4a512d8135bcf46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032725"
---
# <a name="windows-power-management"></a>Windows Administración de energía

Windows administración de energía permite que los usuarios puedan acceder al instante a los equipos con solo tocar un botón o una tecla. También garantiza que todos los elementos del sistema (aplicaciones, dispositivos e interfaz de usuario) puedan aprovechar las enormes mejoras en las funcionalidades y la tecnología de administración de energía.

El Windows operativo usa hardware de administración de energía para poner  el equipo en estado de suspensión de bajo consumo en lugar de apagarse completamente, de modo que el sistema pueda reanudar rápidamente el trabajo. El sistema operativo entrará automáticamente en estado de suspensión cuando el equipo esté inactivo o cuando el usuario presione un botón para indicar que la sesión de trabajo actual ha terminado. Para el usuario, el sistema parece estar desactivado. Mientras está en estado de suspensión, el procesador del equipo no está ejecutando código y no se está realizando ningún trabajo para el usuario. Sin embargo, los eventos del sistema de los dispositivos de hardware y el reloj en tiempo real se pueden habilitar para que el sistema salga del estado de suspensión (es decir, "reactivación") y vuelva rápidamente al estado de funcionamiento.

Cuando el equipo está en estado de suspensión, el hardware del equipo, el sistema y las aplicaciones que se ejecutan en el equipo deben ser capaces de responder inmediatamente al conmutador de alimentación, los eventos de comunicaciones y otras acciones. Si todas las aplicaciones controlan correctamente las transiciones de estado de energía, el usuario percibirá un sistema más elegante e integrado. Las aplicaciones que no controlan estas transiciones pueden producir un error cuando la alimentación está apagada y, a continuación, activada, debido a la pérdida de datos o a una dependencia de un dispositivo que se haya quitado.

Estas son las ventajas de la administración Windows energía:

-   Elimina los retrasos de inicio y apagado. El equipo no necesita realizar un arranque completo del sistema al salir del estado de suspensión o un apagado completo del sistema cuando el usuario inicia el estado de suspensión.
-   Permite que las tareas automatizadas se ejecuten mientras el equipo está en estado de suspensión. El Programador de tareas permite al usuario programar la ejecución de aplicaciones; los eventos programados se pueden ejecutar incluso cuando el sistema está en estado de suspensión. El Programador de tareas usa [temporizadores que se](/windows/desktop/Sync/waitable-timer-objects) pueden esperar para asegurarse de que el sistema está listo cuando la aplicación está programada para ejecutarse. Para obtener más información, vea el archivo de ayuda incluido con el Programador de tareas.
-   Habilita la administración de energía por dispositivo. Los dispositivos que no están en uso pueden ahorrar energía si entran en estado de suspensión.
-   Mejora la eficacia de la energía. La eficiencia energética es especialmente importante en los equipos portátiles. La reducción del consumo de energía del sistema se traduce directamente en menores costos de energía y una mayor duración de la batería.
-   Permite a los usuarios [crear esquemas de energía,](power-schemes.md)establecer alarmas y especificar opciones de batería a través de Opciones de energía aplicación en Panel de control. El sistema operativo coordina todas las actividades de administración de energía, en función de la configuración de la directiva de energía. Para obtener más información, vea el archivo de ayuda incluido con la Opciones de energía aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
