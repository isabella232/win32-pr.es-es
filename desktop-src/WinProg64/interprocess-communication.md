---
title: Comunicación entre procesos
description: Las técnicas siguientes se pueden usar para la comunicación entre aplicaciones de 32 y 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- Comunicación entre procesos de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5089440caf6ac537a314e7e920796fadeac5817220ba91f283c297bd0451b705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734125"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Comunicación entre procesos entre aplicaciones de 32 y 64 bits

Las técnicas siguientes se pueden usar para la comunicación entre aplicaciones de 32 y 64 bits:

-   Las versiones de 64 bits de Windows usan identificadores de 32 bits para la interoperabilidad. Al compartir un identificador entre aplicaciones de 32 y 64 bits, solo los 32 bits inferiores son significativos, por lo que es seguro truncar el identificador (al pasarlo de 64 bits a 32 bits) o firmar la extensión del identificador (al pasarlo de 32 bits a 64 bits). Los identificadores que se pueden compartir incluyen identificadores para objetos de usuario como ventanas **(HWND),** identificadores para objetos GDI como lápices y pinceles **(HBRUSH** y **HPEN)** y identificadores para objetos con nombre, como exclusiones mutuas, semáforos y identificadores de archivo.
-   Se pueden usar llamadas a procedimiento remoto (RPC).
-   Los servidores locales COM se pueden usar si se registran archivos DLL de proxy o stub de 32 y 64 bits para todas las interfaces usadas.
-   La memoria compartida se puede usar si los tipos dependientes del puntero se convierten correctamente (o se evitan).
-   Las [**funciones CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) y [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pueden iniciar procesos de 32 y 64 bits desde procesos de 32 o 64 bits con ciertas limitaciones.

Un archivo ejecutable de 64 bits ubicado en %windir% System32 no se puede iniciar desde un proceso de 32 bits, porque el redireccionamiento del sistema de archivos redirige la ruta \\ de acceso. No deshabilite el redireccionamiento para lograr esto; use %windir% \\ Sysnative en su lugar. Para obtener más información, vea [Redirección del sistema de archivos](file-system-redirector.md).

 

 