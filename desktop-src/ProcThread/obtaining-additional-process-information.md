---
description: Hay una variedad de funciones para obtener información acerca de los procesos.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtención de información de proceso adicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545478"
---
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="ff50d-103">Obtención de información de proceso adicional</span><span class="sxs-lookup"><span data-stu-id="ff50d-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="ff50d-104">Hay una variedad de funciones para obtener información acerca de los procesos.</span><span class="sxs-lookup"><span data-stu-id="ff50d-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="ff50d-105">Algunas de estas funciones solo se pueden usar para el proceso de llamada, ya que no toman un identificador de proceso como parámetro.</span><span class="sxs-lookup"><span data-stu-id="ff50d-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="ff50d-106">Puede usar funciones que toman un identificador de proceso para obtener información sobre otros procesos.</span><span class="sxs-lookup"><span data-stu-id="ff50d-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="ff50d-107">Para obtener la cadena de línea de comandos para el proceso actual, utilice la función [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="ff50d-108">Para recuperar la estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especificada al crear el proceso actual, utilice la función [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="ff50d-109">Para obtener la información de versión del encabezado ejecutable, utilice la función [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="ff50d-110">Para obtener la ruta de acceso completa y el nombre de archivo del archivo ejecutable que contiene el código de proceso, utilice la función [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="ff50d-111">Para obtener el recuento de identificadores de los objetos de la interfaz gráfica de usuario (GUI) en uso, utilice la función [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="ff50d-112">Para determinar si se está depurando un proceso, utilice la función [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="ff50d-113">Para recuperar información de cuentas para todas las operaciones de e/s realizadas por el proceso, utilice la función [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .</span><span class="sxs-lookup"><span data-stu-id="ff50d-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 
