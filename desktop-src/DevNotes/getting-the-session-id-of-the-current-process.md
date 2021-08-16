---
description: El código de ensamblado x86 de ejemplo siguiente obtiene el identificador de sesión de Terminal Services asociado al proceso actual.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obtención del identificador de sesión del proceso actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955984"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Obtención del identificador de sesión del proceso actual

\[Las direcciones de memoria especificadas por este código de ejemplo pueden cambiar en futuras versiones de Windows. Para asegurarse de que la aplicación seguirá funcionando correctamente en el futuro, la aplicación debe llamar a [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) y, a continuación, [**a ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) en lugar del siguiente código de ejemplo.\]

El código de ensamblado x86 de ejemplo siguiente obtiene el identificador de sesión de Terminal Services asociado al proceso actual.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
