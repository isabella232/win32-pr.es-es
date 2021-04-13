---
title: Comunicación entre procesos
description: Las técnicas siguientes se pueden usar para la comunicación entre las aplicaciones de 32 bits y 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- 'comunicación entre procesos: programación de Windows de 64 bits'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421100"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Comunicación entre procesos entre aplicaciones de 32 bits y de 64 bits

Las técnicas siguientes se pueden usar para la comunicación entre las aplicaciones de 32 bits y 64 bits:

-   las versiones de 64 bits de Windows usan identificadores de 32 bits para la interoperabilidad. Al compartir un controlador entre las aplicaciones de 32 bits y de 64 bits, solo los 32 bits inferiores son significativos, por lo que es seguro truncar el identificador (al pasarlo de 64 a 32 bits) o firmar el identificador (al pasarlo de 32 a 64 bits). Entre los identificadores que se pueden compartir se incluyen los identificadores de los objetos de usuario como Windows (**hWnd**), los identificadores de objetos GDI, como lápices y pinceles (**hbrush** y **HPEN**), y los identificadores de objetos con nombre como exclusiones mutuas, semáforos e identificadores de archivo.
-   Se pueden utilizar llamadas a procedimiento remoto (RPC).
-   Los LocalServers COM se pueden usar si se registran archivos dll de proxy/stub de 32 bits y de 64 bits para todas las interfaces utilizadas.
-   Se puede utilizar la memoria compartida si los tipos dependientes del puntero se convierten correctamente (o se evitan).
-   Las funciones [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) y [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pueden iniciar procesos de 32 bits y de 64 bits desde procesos de 32 bits o de 64 bits con ciertas limitaciones.

No se puede iniciar un archivo ejecutable de 64 bits ubicado en% WINDIR% \\ system32 desde un proceso de 32 bits, porque el redirector del sistema de archivos redirige la ruta de acceso. No deshabilite la redirección para lograr esto; Use% WINDIR% \\ Sysnative en su lugar. Para obtener más información, consulte [redirector del sistema de archivos](file-system-redirector.md).

 

 