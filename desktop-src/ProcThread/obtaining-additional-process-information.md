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
# <a name="obtaining-additional-process-information"></a>Obtención de información de proceso adicional

Hay una variedad de funciones para obtener información acerca de los procesos. Algunas de estas funciones solo se pueden usar para el proceso de llamada, ya que no toman un identificador de proceso como parámetro. Puede usar funciones que toman un identificador de proceso para obtener información sobre otros procesos.

-   Para obtener la cadena de línea de comandos para el proceso actual, utilice la función [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .
-   Para recuperar la estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especificada al crear el proceso actual, utilice la función [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .
-   Para obtener la información de versión del encabezado ejecutable, utilice la función [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .
-   Para obtener la ruta de acceso completa y el nombre de archivo del archivo ejecutable que contiene el código de proceso, utilice la función [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .
-   Para obtener el recuento de identificadores de los objetos de la interfaz gráfica de usuario (GUI) en uso, utilice la función [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .
-   Para determinar si se está depurando un proceso, utilice la función [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .
-   Para recuperar información de cuentas para todas las operaciones de e/s realizadas por el proceso, utilice la función [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .

 

 
