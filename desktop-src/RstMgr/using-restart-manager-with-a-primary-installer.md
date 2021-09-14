---
title: Usar el Administrador de reinicio con un instalador principal
description: En el procedimiento siguiente se describe cómo usar el Administrador de reinicio para apagar y reiniciar aplicaciones y servicios. Cuando se usa el Administrador de reinicio con un solo instalador, este instalador también es el instalador principal que controla la interfaz de usuario.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38956ee8d04bc377809e93579080d9b767c3da3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169006"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Usar el Administrador de reinicio con un instalador principal

En el procedimiento siguiente se describe cómo usar el Administrador de reinicio para apagar y reiniciar aplicaciones y servicios. Cuando se usa el Administrador de reinicio con un solo instalador, este instalador también es el instalador principal que controla la interfaz de usuario.

**Para usar el Administrador de reinicio con un instalador principal**

1.  El instalador llama a la [**función RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) para iniciar la sesión de Restart Manager y obtener un identificador de sesión y una clave.
2.  El instalador llama a la [**función RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) para registrar los recursos. El Administrador de reinicio solo puede usar recursos registrados para determinar qué aplicaciones y servicios deben apagarse y reiniciarse. Todos los recursos que pueden verse afectados por la instalación deben registrarse con la sesión. Los recursos se pueden identificar por nombre de archivo, nombre corto del servicio o una [**estructura \_ RM UNIQUE \_ PROCESS.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process)
3.  El instalador llama a la [**función RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obtener una matriz de estructuras [**DE RM PROCESS \_ \_ INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) que enumera todas las aplicaciones y servicios que se deben apagar y reiniciar.

    Si el valor del parámetro *lpdwRebootReason* devuelto por la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) es distinto de cero, el Administrador de reinicio no puede liberar un recurso registrado al apagar una aplicación o un servicio. En este caso, se requiere un apagado y reinicio del sistema para continuar con la instalación. El instalador debe solicitar al usuario una acción, detener programas o servicios, o programar un apagado y reinicio del sistema.

    Si el valor del parámetro *lpdwRebootReason* devuelto por la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) es cero, el instalador debe llamar a la [**función RmShutdown.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) Esto cierra los servicios y las aplicaciones que usan recursos registrados. A continuación, el instalador debe realizar las modificaciones del sistema necesarias para completar la instalación. Por último, el instalador debe llamar a la función [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) para que el Administrador de reinicio pueda reiniciar las aplicaciones que ha apagado y que se han registrado para un reinicio.

4.  El instalador puede usar la [**función RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) para evitar que las operaciones de Restart Manager apaguen o reinicien las aplicaciones y servicios especificados. La [**función RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) devuelve una lista de las aplicaciones y servicios que se filtrarán desde el apagado y el reinicio. La [**función RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) quita un filtro.
5.  El instalador llama a la [**función RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) para cerrar la sesión del Administrador de reinicio.

Para obtener un fragmento de código de ejemplo que muestra cómo iniciar y usar una sesión de Restart Manager mediante un instalador principal y, a continuación, unir un instalador secundario a la sesión existente, vea [Using Restart Manager with a Secondary Installer](using-restart-manager-with-a-secondary-installer.md).

 

 




