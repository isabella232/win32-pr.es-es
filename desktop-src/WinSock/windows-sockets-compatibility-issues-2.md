---
description: Windows Sockets 2 sigue admitiendo todas las llamadas a funciones y semánticas de Windows Sockets 1,1, a excepción de las que se ocupan de los pseudo bloqueos.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problemas de compatibilidad de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275795"
---
# <a name="windows-sockets-compatibility-issues"></a>Problemas de compatibilidad de Windows Sockets

Windows Sockets 2 sigue admitiendo todas las llamadas a funciones y semánticas de Windows Sockets 1,1, a excepción de las que se ocupan de los pseudo bloqueos. Dado que Windows Sockets 2 solo se ejecuta en entornos programados de 32 de forma preventiva, no es necesario implementar el pseudo bloqueo que se encuentra en Windows Sockets 1,1. Esto significa que nunca se indicará el código de error WSAEINPROGRESS y que las siguientes funciones de Windows Sockets 1,1 no están disponibles para las aplicaciones de Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Los programas de Windows Sockets 1,1 que se escriben para utilizar el pseudo-bloqueo seguirán funcionando correctamente, ya que se vinculan a Winsock.dll o Wsock32.dll. Ambos continúan admitiendo el conjunto completo de funciones 1,1 de Windows Sockets. Para que los programas se conviertan en aplicaciones de Windows Sockets 2, se debe modificar el código. En la mayoría de los casos, el uso prudente de los subprocesos se puede sustituir para acomodar el procesamiento que se estaba llevando a cabo con una función de enlace de bloqueo.

 

 



