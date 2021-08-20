---
title: Conexión de subprocesos a un escritorio
description: Una vez que un proceso se conecta a una estación de ventana, el sistema asigna un escritorio al subproceso que realiza la conexión.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb6f57debd0ed85953ee458d7235acee0aa0b4b274b70670a46dedfb7be03d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030597"
---
# <a name="thread-connection-to-a-desktop"></a>Conexión de subprocesos a un escritorio

Una vez que un proceso se conecta a una estación de ventana, el sistema asigna un escritorio al subproceso que realiza la conexión. El sistema determina el escritorio que se asignará al subproceso según las reglas siguientes:

1.  Si el subproceso ha llamado a [**la función SetThreadDesktop,**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) se conecta al escritorio especificado.
2.  Si el subproceso no llamó a [**SetThreadDesktop,**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)se conecta al escritorio heredado del proceso primario.
3.  Si el subproceso no llamó a [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) y no heredó un escritorio, el sistema intenta abrirse para el acceso MÁXIMO PERMITIDO y conectarse a un escritorio de la \_ siguiente manera:
    -   Si se especificó un nombre de escritorio en el miembro **lpDesktop** de la estructura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que se usó cuando se creó el proceso, el subproceso se conecta al escritorio especificado.
    -   De lo contrario, el subproceso se conecta al escritorio predeterminado de la estación de ventana a la que se conectó el proceso.

El escritorio asignado durante este proceso de conexión no se puede cerrar mediante una llamada a la [**función CloseDesktop.**](/windows/win32/api/winuser/nf-winuser-closedesktop)

Cuando un proceso se conecta a un escritorio, el sistema busca identificadores heredados en la tabla de identificadores del proceso. El sistema usa el primer identificador de escritorio que encuentra. Si desea que un proceso secundario se conecte a un escritorio heredado determinado, debe asegurarse de que el único identificador deseado se marca como heredable. Si un proceso secundario hereda varios identificadores de escritorio, los resultados de la conexión de escritorio no están definidos.

Los identificadores de un escritorio que el sistema abre al conectar un proceso a un escritorio no son heredables.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesar conexión a una estación de ventana](process-connection-to-a-window-station.md)
</dt> </dl>

 

 