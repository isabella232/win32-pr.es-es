---
description: Windows Sockets 1,1 presentó el mecanismo de selección asincrónica para proporcionar indicaciones de eventos de red que no implicaban sondeo ni bloqueo.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Mensajes de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715475"
---
# <a name="windows-messages"></a><span data-ttu-id="39007-103">Mensajes de Windows</span><span class="sxs-lookup"><span data-stu-id="39007-103">Windows Messages</span></span>

<span data-ttu-id="39007-104">Windows Sockets 1,1 presentó el mecanismo de selección asincrónica para proporcionar indicaciones de eventos de red que no implicaban sondeo ni bloqueo.</span><span class="sxs-lookup"><span data-stu-id="39007-104">Windows Sockets 1.1 introduced the async-select mechanism to provide network event indications that did not involve either polling or blocking.</span></span> <span data-ttu-id="39007-105">La función [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) se usa para registrar un interés en uno o varios eventos de red, tal y como se indica en el anterior, y proporcionar un identificador de ventana que se usará para la notificación.</span><span class="sxs-lookup"><span data-stu-id="39007-105">The [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) function is used to register an interest in one or more network events as listed in the preceding, and supply a window handle to be used for notification.</span></span> <span data-ttu-id="39007-106">Cuando se produce un evento de red designado, se envía un mensaje de Windows especificado por el cliente a la ventana indicada.</span><span class="sxs-lookup"><span data-stu-id="39007-106">When a nominated network event occurs, a client-specified Windows message is sent to the indicated window.</span></span> <span data-ttu-id="39007-107">El proveedor de servicios debe utilizar la función [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) para lograr esto.</span><span class="sxs-lookup"><span data-stu-id="39007-107">The service provider must use the [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) function to accomplish this.</span></span>

<span data-ttu-id="39007-108">En Windows, es posible que este no sea el mecanismo de notificación más eficaz y que no sea práctico para los demonios y servicios que no quieran abrir ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="39007-108">In Windows, this may not be the most efficient notification mechanism, and is inconvenient for daemons and services that do not want to open any windows.</span></span> <span data-ttu-id="39007-109">El mecanismo de señalización del objeto de evento que se describe en lo siguiente se ha introducido para solucionar este problema.</span><span class="sxs-lookup"><span data-stu-id="39007-109">The event object signaling mechanism described in the following is introduced to solve this problem.</span></span>

 

 
