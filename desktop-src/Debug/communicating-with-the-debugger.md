---
description: La función OutputDebugString envía una cadena desde el proceso que se está depurando al depurador generando un evento de depuración de \_ eventos de cadena de depuración de salida \_ \_ . Un proceso puede detectar si se está depurando llamando a la función IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicarse con el depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906932"
---
# <a name="communicating-with-the-debugger"></a>Comunicarse con el depurador

La función [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envía una cadena desde el proceso que se está depurando al depurador generando un evento de depuración de \_ eventos de cadena de depuración de salida \_ \_ . Un proceso puede detectar si se está depurando llamando a la función [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .

La función [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) produce una excepción de punto de interrupción en el proceso actual. Un punto de interrupción es una ubicación en un programa donde la ejecución se detiene para permitir al desarrollador examinar el código, las variables y los valores de registro del programa y, si es necesario, realizar cambios, continuar la ejecución o finalizar la ejecución.

La función [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) finaliza el proceso actual y proporciona el control de ejecución al depurador, pero a diferencia de [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), no genera una excepción. Esta función solo se debe usar como último recurso, ya que no siempre libera la memoria del proceso ni cierra sus archivos.

 

 
