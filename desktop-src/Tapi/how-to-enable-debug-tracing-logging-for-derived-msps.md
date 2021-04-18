---
description: En el procedimiento siguiente se describe cómo habilitar el seguimiento y el registro de depuración.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Cómo habilitar el registro y el seguimiento de depuración para los MSP derivados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3883d12c050f245cc58595c9a52586c4f01ba27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687067"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Cómo habilitar el registro y el seguimiento de depuración para los MSP derivados

En primer lugar, asegúrese de que la implementación del MSP derivado ha seguido las instrucciones de la sección anterior con respecto al seguimiento de depuración (definición del símbolo de preprocesador MSPLOG, registro para el seguimiento durante DllMain y uso de la macro de registro para el seguimiento). Averigüe qué nombre usa el MSP al registrarse para el seguimiento (suele ser el nombre del archivo DLL; se hace referencia a continuación como "nombre de &lt; dll &gt; "). Para habilitar el seguimiento, use un editor del registro ("Regedit.exe" o "Regedt32.exe") para buscar la clave "HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Tracing" y haga lo siguiente. Tenga en cuenta que todos los valores que se mencionan a continuación, excepto el valor EnableDebuggerTracing, deben crearse automáticamente después de ejecutar el MSP por primera vez.

-   Para habilitar el seguimiento en depuradores en modo kernel y usuario, establezca el valor **DWORD** <dll name> \\ EnableDebuggerTracing en 1. Opcionalmente, use el  valor DWORD <dll name> \\ ConsoleTracing Mask para habilitar o deshabilitar varios niveles de salida de seguimiento (el valor predeterminado es 0xFFFF0000, que habilita todos los niveles de seguimiento).
-   Para habilitar el seguimiento en un archivo, establezca el valor **DWORD** <dll name> \\ EnableFileTracing en 1. Opcionalmente, utilice el valor de cadena <dll name> \\ FileDirectory para ajustar la ubicación del archivo de registro. Opcionalmente, use el  valor DWORD <dll name> \\ FileTracingMask para habilitar o deshabilitar varios niveles de salida de seguimiento (el valor predeterminado es 0xFFFF0000, que habilita todos los niveles de seguimiento).
-   Para habilitar el seguimiento en una ventana de consola independiente, separada por DLL, establezca el valor **DWORD** EnableConsoleTracing en 1 y establezca el  valor DWORD <dll name> \\ EnableConsoleTracing en 1. Opcionalmente, use el  valor DWORD <dll name> \\ ConsoleTracing Mask para habilitar o deshabilitar varios niveles de salida de seguimiento (el valor predeterminado es 0xFFFF0000, que habilita todos los niveles de seguimiento).

 

 



