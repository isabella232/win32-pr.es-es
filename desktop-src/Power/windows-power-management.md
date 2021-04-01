---
description: La administración de energía de Windows hace que los equipos estén accesibles al instante a los usuarios al tocar un botón o una tecla.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Administración de energía de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abb3a040f8da8e2deb242a2aa607a9448d31c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909682"
---
# <a name="windows-power-management"></a>Administración de energía de Windows

La administración de energía de Windows hace que los equipos estén accesibles al instante a los usuarios al tocar un botón o una tecla. También garantiza que todos los elementos del sistema (aplicaciones, dispositivos e interfaz de usuario) pueden aprovechar las grandes mejoras en la tecnología de administración de energía y las capacidades.

El sistema operativo Windows usa hardware de administración de energía para poner el equipo en un estado de *suspensión* de bajo consumo en lugar de cerrarse completamente, de modo que el sistema pueda reanudar rápidamente el trabajo. El sistema operativo entrará automáticamente en estado de suspensión cuando el equipo esté inactivo o cuando el usuario presione un botón para indicar que la sesión de trabajo actual ha superado. Para el usuario, el sistema parece estar desactivado. En el estado de suspensión, el procesador del equipo no está ejecutando código y no se realiza ningún trabajo para el usuario. Sin embargo, los eventos del sistema de los dispositivos de hardware y del reloj en tiempo real pueden estar habilitados para que el sistema salga del estado de suspensión (es decir, "reactivación") y vuelva rápidamente al estado de funcionamiento.

Cuando el equipo se encuentra en estado de suspensión, el hardware del equipo, el sistema y las aplicaciones que se ejecutan en el equipo deben ser capaces de responder inmediatamente al conmutador de energía, los eventos de comunicaciones y otras acciones. Si todas las aplicaciones controlan las transiciones de estado de energía correctamente, el usuario percibirá un sistema más elegante e integrado. Se puede producir un error en las aplicaciones que no controlan estas transiciones cuando la alimentación está apagada y después en, debido a la pérdida de datos o a una dependencia en un dispositivo que puede haberse quitado.

A continuación se muestran las ventajas de la administración de energía de Windows:

-   Elimina los retrasos de inicio y cierre. No es necesario que el equipo realice un arranque completo del sistema al salir del estado de suspensión o un cierre completo del sistema cuando el usuario inicia el estado de suspensión.
-   Permite que las tareas automatizadas se ejecuten mientras el equipo está en estado de suspensión. La Programador de tareas permite al usuario programar aplicaciones para que se ejecuten. los eventos programados se pueden ejecutar incluso cuando el sistema se encuentra en estado de suspensión. El Programador de tareas utiliza [temporizadores que esperan](/windows/desktop/Sync/waitable-timer-objects) para asegurarse de que el sistema está listo cuando la aplicación está programada para ejecutarse. Para obtener más información, vea el archivo de ayuda incluido en el Programador de tareas.
-   Habilita la administración de energía de cada dispositivo. Los dispositivos que no están en uso pueden ahorrar energía si entran en estado de suspensión.
-   Mejora la eficacia de la energía. La eficiencia energética es especialmente importante en los equipos portátiles. Reducir el consumo de energía del sistema se traduce directamente en costos energéticos más bajos y una mayor duración de la batería.
-   Permite a los usuarios crear [planes de energía](power-schemes.md), establecer alarmas y especificar opciones de batería a través de la aplicación opciones de energía del panel de control. El sistema operativo coordina todas las actividades de administración de energía en función de la configuración de la Directiva de energía. Para obtener más información, vea el archivo de ayuda que se incluye con la aplicación Power Options.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
