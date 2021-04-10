---
description: En el ejemplo siguiente, el código de ensamblado de x86 obtiene el ID. de sesión de Terminal Services asociado al proceso actual.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obtener el ID. de sesión del proceso actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153035"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Obtener el ID. de sesión del proceso actual

\[Las direcciones de memoria especificadas por este código de ejemplo pueden cambiar en futuras versiones de Windows. Para asegurarse de que la aplicación se siga ejecutando correctamente en el futuro, la aplicación debe llamar a [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) y, a continuación, a [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) en lugar de al siguiente código de ejemplo.\]

En el ejemplo siguiente, el código de ensamblado de x86 obtiene el ID. de sesión de Terminal Services asociado al proceso actual.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
