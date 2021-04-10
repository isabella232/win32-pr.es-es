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
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="1d3dd-103">Conexión de subprocesos a un escritorio</span><span class="sxs-lookup"><span data-stu-id="1d3dd-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="1d3dd-104">Una vez que un proceso se conecta a una estación de ventana, el sistema asigna un escritorio al subproceso que realiza la conexión.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="1d3dd-105">El sistema determina el escritorio que se va a asignar al subproceso según las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="1d3dd-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="1d3dd-106">Si el subproceso ha llamado a la función [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , se conecta al escritorio especificado.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="1d3dd-107">Si el subproceso no llama a [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), se conecta al escritorio heredado del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="1d3dd-108">Si el subproceso no llama a [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) y no heredó un escritorio, el sistema intenta abrir el acceso máximo \_ permitido y se conecta a un escritorio de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d3dd-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="1d3dd-109">Si se especificó un nombre de escritorio en el miembro **lpDesktop** de la estructura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que se usó cuando se creó el proceso, el subproceso se conecta al escritorio especificado.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="1d3dd-110">De lo contrario, el subproceso se conecta al escritorio predeterminado de la estación de ventana a la que se conecta el proceso.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="1d3dd-111">No se puede cerrar el escritorio asignado durante este proceso de conexión mediante una llamada a la función [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .</span><span class="sxs-lookup"><span data-stu-id="1d3dd-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="1d3dd-112">Cuando un proceso se conecta a un escritorio, el sistema busca identificadores heredados en la tabla de identificadores del proceso.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="1d3dd-113">El sistema utiliza el primer controlador de escritorio que encuentra.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="1d3dd-114">Si desea que un proceso secundario se conecte a un escritorio heredado determinado, debe asegurarse de que solo el identificador deseado esté marcado como heredable.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="1d3dd-115">Si un proceso secundario hereda varios identificadores de escritorio, los resultados de la conexión de escritorio son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="1d3dd-116">Los identificadores de un escritorio que el sistema abre mientras se conecta un proceso a un escritorio no se pueden heredar.</span><span class="sxs-lookup"><span data-stu-id="1d3dd-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d3dd-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d3dd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d3dd-118">Proceso de conexión a una estación de ventana</span><span class="sxs-lookup"><span data-stu-id="1d3dd-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 