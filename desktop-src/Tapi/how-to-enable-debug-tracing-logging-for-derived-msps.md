---
description: En el procedimiento siguiente se describe cómo habilitar el seguimiento y el registro de depuración.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Cómo habilitar el seguimiento y el registro de depuración para los MSP derivados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565b66055a43edbe7556e640f8e368aab84fab206bced431c22578a7e21a94ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140528"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Cómo habilitar el seguimiento y el registro de depuración para los MSP derivados

En primer lugar, asegúrese de que la implementación del MSP derivado ha seguido las directrices de la sección anterior con respecto al seguimiento de depuración (definición del símbolo de preprocesador MSPLOG, registro para el seguimiento durante DllMain y uso de la macro LOG para el seguimiento). Descubra qué nombre usa el MSP al registrarse para el seguimiento (normalmente debe ser el nombre del archivo DLL; a continuación se hace referencia a él como &lt; "nombre de &gt; dll"). Para habilitar el seguimiento, use un editor del Registro ("Regedit.exe" o "Regedt32.exe") para buscar la clave "HKEY LOCAL MACHINE Software Microsoft Tracing" y haga \_ \_ lo \\ \\ \\ siguiente. Tenga en cuenta que todos los valores mencionados a continuación, excepto el valor EnableDebuggerTracing, deben crearse automáticamente después de ejecutar el MSP por primera vez.

-   Para habilitar el seguimiento en depuradores en modo de usuario y kernel, establezca el valor **DWORD** <dll name> \\ EnableDebuggerTracing en 1. Opcionalmente, use el valor **DWORD** ConsoleTracing Mask para habilitar o deshabilitar varios niveles de salida de seguimiento (el valor predeterminado es 0xFFFF0000, que habilita todos los niveles <dll name> \\ de seguimiento).
-   Para habilitar el seguimiento en un archivo, establezca el **valor DWORD** <dll name> \\ EnableFileTracing en 1. Opcionalmente, use el valor de cadena <dll name> \\ FileDirectory para ajustar la ubicación del archivo de registro. Opcionalmente, use el valor **DWORD** <dll name> FileTracingMask para habilitar o deshabilitar varios niveles de salida de seguimiento (el valor predeterminado es 0xFFFF0000, que habilita todos los niveles de \\ seguimiento).
-   Para habilitar el seguimiento en una ventana de consola independiente, separada por DLL, establezca el valor **DWORD** EnableConsoleTracing en 1 y establezca TAMBIÉN el valor **DWORD** <dll name> \\ EnableConsoleTracing en 1. Opcionalmente, use el valor **DWORD** ConsoleTracing Mask para habilitar o deshabilitar varios niveles de salida de seguimiento (el valor predeterminado es 0xFFFF0000, que habilita todos los niveles <dll name> \\ de seguimiento).

 

 



