---
description: Hay una variedad de funciones para obtener información sobre los procesos.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtener información adicional del proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375015"
---
# <a name="obtaining-additional-process-information"></a>Obtener información adicional del proceso

Hay una variedad de funciones para obtener información sobre los procesos. Algunas de estas funciones solo se pueden usar para el proceso de llamada, porque no toman un identificador de proceso como parámetro. Puede usar funciones que toman un identificador de proceso para obtener información sobre otros procesos.

-   Para obtener la cadena de línea de comandos para el proceso actual, use la [**función GetCommandLine.**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)
-   Para recuperar la [**estructura STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especificada cuando se creó el proceso actual, use la [**función GetStartupInfo.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)
-   Para obtener la información de versión del encabezado ejecutable, use la [**función GetProcessVersion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)
-   Para obtener la ruta de acceso completa y el nombre de archivo para el archivo ejecutable que contiene el código de proceso, use la [**función GetModuleFileName.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
-   Para obtener el recuento de identificadores para los objetos de interfaz gráfica de usuario (GUI) en uso, use la [**función GetGuiResources.**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)
-   Para determinar si un proceso se está depurando, use la [**función IsDebuggerPresent.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
-   Para recuperar información de contabilidad de todas las operaciones de E/S realizadas por el proceso, use la [**función GetProcessIoCounters.**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)

 

 
