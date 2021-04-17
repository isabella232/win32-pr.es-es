---
description: Las funciones de configuración de hardware recuperan información como el procesador, el perfil de hardware y la información del teclado.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration (Configuración de hardware)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668447"
---
# <a name="hardware-configuration"></a>Hardware Configuration (Configuración de hardware)

Las funciones de configuración de hardware recuperan información como el procesador, el perfil de hardware y la información del teclado.

La función [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera la información de procesador y de memoria, como el tamaño de página, el identificador del fabricante de equipos originales (OEM), el número y el tipo de procesadores, el intervalo de direcciones de la aplicación, etc. La función [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera información sobre las operaciones de punto flotante y los conjuntos de instrucciones compatibles con el procesador.

La función [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera información sobre el perfil de hardware. El perfil de hardware incluye información como el estado de acoplamiento, el identificador único global (GUID) y el nombre para mostrar del perfil. La función [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera la información como el tipo de teclado y el número de teclas de función en el teclado actual.

 

 
