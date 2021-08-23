---
description: La función OutputDebugString envía una cadena del proceso que se depura al depurador generando un evento de depuración OUTPUT \_ DEBUG \_ STRING \_ EVENT. Un proceso puede detectar si se está depurando llamando a la función IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicación con el depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee4d78fc2b0cef1df9f0597a816966585d00e1041711d4712d1a1fa66639e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692065"
---
# <a name="communicating-with-the-debugger"></a>Comunicación con el depurador

La [**función OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envía una cadena del proceso que se depura al depurador generando un evento de depuración OUTPUT \_ DEBUG STRING \_ \_ EVENT. Un proceso puede detectar si se está depurando llamando a la [**función IsDebuggerPresent.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)

La [**función DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) produce una excepción de punto de interrupción en el proceso actual. Un punto de interrupción es una ubicación de un programa en la que la ejecución se detiene para permitir al desarrollador examinar el código, las variables y registrar los valores del programa y, según sea necesario, realizar cambios, continuar la ejecución o finalizar la ejecución.

La [**función FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) finaliza el proceso actual y proporciona control de ejecución al depurador, pero, a diferencia de [**DebugBreak,**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)no genera una excepción. Esta función solo debe usarse como último recurso, ya que no siempre libera la memoria del proceso ni cierra sus archivos.

 

 
