---
title: Proceso de conexión a una estación de ventana
description: Un proceso establece automáticamente una conexión a una estación de ventana y un escritorio cuando llama por primera vez a una función USER32 o GDI32 (distinta de la estación de ventana y las funciones de escritorio).
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421134"
---
# <a name="process-connection-to-a-window-station"></a>Proceso de conexión a una estación de ventana

Un proceso establece automáticamente una conexión a una estación de ventana y un escritorio cuando llama por primera vez a una función USER32 o GDI32 (distinta de la estación de ventana y las funciones de escritorio). El sistema determina la estación de ventana a la que se conecta un proceso según las siguientes reglas:

1.  Si el proceso ha llamado a la función [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) , se conecta a la estación de ventana especificada en esa llamada.
2.  Si el proceso no llama a [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), se conecta a la estación de ventana heredada del proceso primario.
3.  Si el proceso no llama a [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) y no heredó una estación de ventana, el sistema intenta abrir el acceso máximo \_ permitido y se conecta a una estación de ventana de la manera siguiente:
    -   Si se especificó un nombre de estación de ventana en el miembro **lpDesktop** de la estructura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que se usó cuando se creó el proceso, el proceso se conecta a la estación de ventana especificada.
    -   De lo contrario, si el proceso se está ejecutando en la sesión de inicio de sesión del usuario interactivo, el proceso se conecta a la estación de ventana interactiva.
    -   Si el proceso se está ejecutando en una sesión de inicio de sesión no interactiva, el nombre de la estación de ventana se forma basándose en el identificador de la sesión de inicio de sesión y se realiza un intento de abrir esa estación de ventana. Si se produce un error en la operación de apertura porque esta estación de ventana no existe, el sistema intenta crear la estación de ventana y un escritorio predeterminado.

No se puede cerrar la estación de ventana asignada durante este proceso de conexión mediante una llamada a la función [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) .

Cuando un proceso se conecta a una estación de ventana, el sistema busca identificadores heredados en la tabla de identificadores del proceso. El sistema utiliza el primer identificador de la estación de ventana que encuentra. Si desea que un proceso secundario se conecte a una estación de ventana heredada determinada, debe asegurarse de que solo el identificador deseado esté marcado como heredable. Si un proceso secundario hereda varios identificadores de estación de ventana, los resultados de la conexión de la estación de ventana son indefinidos.

Los identificadores de una estación de ventana que el sistema abre mientras se conecta un proceso a una estación de ventana no se pueden heredar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión de subprocesos a un escritorio](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 