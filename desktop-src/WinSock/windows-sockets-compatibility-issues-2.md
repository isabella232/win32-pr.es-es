---
description: Windows Sockets 2 sigue siendo compatible con todas las semánticas Windows Sockets 1.1 y las llamadas de función, excepto las que se tratan con pseudobloqueo.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Problemas de compatibilidad de sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967288"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Problemas de compatibilidad de sockets

Windows Sockets 2 sigue siendo compatible con todas las semánticas Windows Sockets 1.1 y las llamadas de función, excepto las que se tratan con pseudobloqueo. Dado Windows Sockets 2 solo se ejecuta en entornos de 32 bits programados de forma preferente, no es necesario implementar el pseudobloqueo encontrado en Windows Sockets 1.1. Esto significa que el código de error WSAEINPROGRESS nunca se indicará y que las siguientes funciones de sockets de Windows 1.1 no están disponibles para las aplicaciones Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows Los programas sockets 1.1 que se escriben para utilizar el pseudobloqueo seguirán funcionando correctamente, ya que se vinculan a Winsock.dll o Wsock32.dll. Ambos siguen siendo compatibles con el conjunto completo de Windows sockets 1.1. Para que los programas se conviertan en Windows sockets 2, debe producirse alguna modificación del código. En la mayoría de los casos, se puede sustituir el uso judicio de subprocesos para dar cabida al procesamiento que se estaba logrando con una función de enlace de bloqueo.

 

 



