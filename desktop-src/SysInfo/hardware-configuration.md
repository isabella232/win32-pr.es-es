---
description: Las funciones de configuración de hardware recuperan información como el procesador, el perfil de hardware y la información del teclado.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration (Configuración de hardware)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e396b2d08b489e92c7a407ca892250135fdd3d174d16de50d0c2d75428a88dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764431"
---
# <a name="hardware-configuration"></a>Hardware Configuration (Configuración de hardware)

Las funciones de configuración de hardware recuperan información como el procesador, el perfil de hardware y la información del teclado.

La [**función GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera información de procesador y memoria, como el tamaño de página, el identificador del fabricante de equipos originales (OEM), el número y el tipo de procesadores, el intervalo de direcciones de la aplicación, entre otros. La [**función IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera información sobre las operaciones de punto flotante y los conjuntos de instrucciones admitidos por el procesador.

La [**función GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera información sobre el perfil de hardware. El perfil de hardware incluye información como el estado de acoplamiento, el identificador único global (GUID) y el nombre para mostrar del perfil. La [**función GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera información como el tipo de teclado y el número de teclas de función en el teclado actual.

 

 
