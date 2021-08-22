---
description: Windows Sockets 2 sigue siendo compatible con todas las semánticas de Windows Sockets 1.1 y las llamadas de función, excepto las que se enfrentan al pseudobloqueo.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Problemas de compatibilidad de sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3fa7aba32ed74f04b04d717e0b2897dc92e0c78079d2a8c20e2c3bcdd85191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051473"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Problemas de compatibilidad de sockets

Windows Sockets 2 sigue siendo compatible con todas las semánticas de Windows Sockets 1.1 y las llamadas de función, excepto las que se enfrentan al pseudobloqueo. Puesto Windows Sockets 2 se ejecuta solo en entornos programados de forma preferente de 32 bits, no es necesario implementar el pseudobloqueo que se encuentra en Windows Sockets 1.1. Esto significa que el código de error WSAEINPROGRESS nunca se indicará y que las siguientes funciones de sockets de Windows 1.1 no están disponibles para las aplicaciones Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows Los programas sockets 1.1 que se escriben para utilizar el pseudobloqueo seguirán funcionando correctamente, ya que se vinculan a Winsock.dll o Wsock32.dll. Ambos siguen siendo compatibles con el conjunto completo de Windows sockets 1.1. Para que los programas se conviertan en Windows Sockets 2, debe producirse alguna modificación del código. En la mayoría de los casos, el uso de subprocesos se puede sustituir para dar cabida al procesamiento que se estaba logrando con una función de enlace de bloqueo.

 

 



