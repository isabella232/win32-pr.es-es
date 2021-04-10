---
title: Conexión de subprocesos a un escritorio
description: Una vez que un proceso se conecta a una estación de ventana, el sistema asigna un escritorio al subproceso que realiza la conexión.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271266"
---
# <a name="thread-connection-to-a-desktop"></a>Conexión de subprocesos a un escritorio

Una vez que un proceso se conecta a una estación de ventana, el sistema asigna un escritorio al subproceso que realiza la conexión. El sistema determina el escritorio que se va a asignar al subproceso según las siguientes reglas:

1.  Si el subproceso ha llamado a la función [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , se conecta al escritorio especificado.
2.  Si el subproceso no llama a [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), se conecta al escritorio heredado del proceso primario.
3.  Si el subproceso no llama a [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) y no heredó un escritorio, el sistema intenta abrir el acceso máximo \_ permitido y se conecta a un escritorio de la manera siguiente:
    -   Si se especificó un nombre de escritorio en el miembro **lpDesktop** de la estructura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que se usó cuando se creó el proceso, el subproceso se conecta al escritorio especificado.
    -   De lo contrario, el subproceso se conecta al escritorio predeterminado de la estación de ventana a la que se conecta el proceso.

No se puede cerrar el escritorio asignado durante este proceso de conexión mediante una llamada a la función [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .

Cuando un proceso se conecta a un escritorio, el sistema busca identificadores heredados en la tabla de identificadores del proceso. El sistema utiliza el primer controlador de escritorio que encuentra. Si desea que un proceso secundario se conecte a un escritorio heredado determinado, debe asegurarse de que solo el identificador deseado esté marcado como heredable. Si un proceso secundario hereda varios identificadores de escritorio, los resultados de la conexión de escritorio son indefinidos.

Los identificadores de un escritorio que el sistema abre mientras se conecta un proceso a un escritorio no se pueden heredar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proceso de conexión a una estación de ventana](process-connection-to-a-window-station.md)
</dt> </dl>

 

 