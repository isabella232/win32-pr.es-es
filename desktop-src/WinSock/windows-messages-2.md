---
description: Windows Sockets 1.1 introdujo el mecanismo de selección asincrónica para proporcionar indicaciones de eventos de red que no implicaban sondeo o bloqueo.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Mensajes de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bab33ecb4d2898c8f1e363ab19ad425503e9d005bf24229a29f581aadf1788f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993215"
---
# <a name="windows-messages"></a>Mensajes de Windows

Windows Sockets 1.1 introdujo el mecanismo de selección asincrónica para proporcionar indicaciones de eventos de red que no implicaban sondeo o bloqueo. La [**función WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) se usa para registrar un interés en uno o varios eventos de red, como se muestra en el anterior, y proporcionar un identificador de ventana que se usará para la notificación. Cuando se produce un evento de red designado, se envía un mensaje de Windows especificado por el cliente a la ventana indicada. Para ello, el proveedor de servicios debe usar la función [**WPUPostMessage.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage)

En Windows, puede que este no sea el mecanismo de notificación más eficaz y sea inconveniente para los demonios y servicios que no desean abrir ninguna ventana. El mecanismo de señalización de objetos de evento que se describe a continuación se introduce para resolver este problema.

 

 
