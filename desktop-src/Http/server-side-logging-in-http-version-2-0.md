---
title: Registro de Server-Side
description: El registro del lado servidor está disponible en un grupo de direcciones URL o una sesión de servidor.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903648"
---
# <a name="server-side-logging"></a><span data-ttu-id="e4e04-103">Registro de Server-Side</span><span class="sxs-lookup"><span data-stu-id="e4e04-103">Server-Side Logging</span></span>

<span data-ttu-id="e4e04-104">El registro del lado servidor está disponible en un grupo de direcciones URL o una sesión de servidor.</span><span class="sxs-lookup"><span data-stu-id="e4e04-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="e4e04-105">Cuando el registro está habilitado en una sesión de servidor, funciona como una forma centralizada de registro para todos los grupos de direcciones URL en la sesión de servidor.</span><span class="sxs-lookup"><span data-stu-id="e4e04-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="e4e04-106">Cuando el registro está habilitado en un grupo de direcciones URL, el registro solo se realiza en las solicitudes que se enrutan al grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e4e04-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="e4e04-107">La API del servidor HTTP admite los siguientes tipos de registro:</span><span class="sxs-lookup"><span data-stu-id="e4e04-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="e4e04-108">[Registro de W3C](w3c-logging.md): disponible en la sesión del servidor y el grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e4e04-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="e4e04-109">[Registro NCSA](ncsa-logging.md): disponible en el grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e4e04-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="e4e04-110">[Registro de IIS](iis-logging.md): disponible en el grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e4e04-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="e4e04-111">[Registro binario centralizado](centralized-binary-logging.md): disponible en la sesión del servidor.</span><span class="sxs-lookup"><span data-stu-id="e4e04-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="e4e04-112">Para aprovechar las ventajas de la característica de registro HTTP, la aplicación habilita y configura un tipo de registro en la sesión de servidor o el grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e4e04-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="e4e04-113">Para obtener más información, vea [configurar y habilitar el registro del lado servidor](configuring-and-enabling-server-side-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e04-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




