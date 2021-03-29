---
title: Uso del administrador de reinicio con un instalador principal
description: En el procedimiento siguiente se describe cómo usar el administrador de reinicio para cerrar y reiniciar aplicaciones y servicios. Al usar el administrador de reinicio con un solo instalador, este instalador es también el instalador principal que controla la interfaz de usuario.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38956ee8d04bc377809e93579080d9b767c3da3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994054"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Uso del administrador de reinicio con un instalador principal

En el procedimiento siguiente se describe cómo usar el administrador de reinicio para cerrar y reiniciar aplicaciones y servicios. Al usar el administrador de reinicio con un solo instalador, este instalador es también el instalador principal que controla la interfaz de usuario.

**Para usar el administrador de reinicio con un instalador principal**

1.  El instalador llama a la función [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) para iniciar la sesión del administrador de reinicio y obtener un identificador de sesión y una clave.
2.  El instalador llama a la función [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) para registrar los recursos. El administrador de reinicio solo puede usar recursos registrados para determinar qué aplicaciones y servicios deben cerrarse y reiniciarse. Todos los recursos que pueden verse afectados por la instalación deben registrarse con la sesión. Los recursos se pueden identificar mediante el nombre de archivo, el nombre corto de servicio o una estructura de [**\_ \_ proceso único de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .
3.  El instalador llama a la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obtener una matriz de estructuras de [**información del \_ proceso \_ de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) que enumera todas las aplicaciones y servicios que deben cerrarse y reiniciarse.

    Si el valor del parámetro *lpdwRebootReason* devuelto por la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) es distinto de cero, el administrador de reinicio no puede liberar un recurso registrado por el cierre de una aplicación o servicio. En este caso, es necesario apagar y reiniciar el sistema para continuar con la instalación. El instalador debe solicitar al usuario una acción, detener programas o servicios, o programar un cierre del sistema y reiniciarlo.

    Si el valor del parámetro *lpdwRebootReason* devuelto por la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) es cero, el instalador debe llamar a la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) . Esto cierra los servicios y aplicaciones que usan recursos registrados. Después, el instalador debe realizar las modificaciones del sistema necesarias para completar la instalación. Por último, el instalador debe llamar a la función [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) para que el administrador de reinicio pueda reiniciar las aplicaciones que se han cerrado y que se han registrado para un reinicio.

4.  El instalador puede usar la función [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) para evitar que las aplicaciones y los servicios especificados se cierren o reinicien con las operaciones del administrador de reinicio. La función [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) devuelve una lista de las aplicaciones y los servicios que se van a filtrar del apagado y el reinicio. La función [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) quita un filtro.
5.  El instalador llama a la función [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) para cerrar la sesión del administrador de reinicio.

Para obtener un fragmento de código de ejemplo que muestra el inicio y el uso de una sesión del administrador de reinicio mediante un instalador principal y la Unión a un instalador secundario a la sesión existente, consulte [uso del administrador de reinicio con un instalador secundario](using-restart-manager-with-a-secondary-installer.md).

 

 




