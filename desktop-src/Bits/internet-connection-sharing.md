---
title: Conexión compartida a Internet
description: BITS puede forzar una conexión de acceso telefónico para las redes domésticas que usan conexión compartida a Internet de Microsoft si la conexión compartida está configurada para marcar cuando los equipos de la red acceden a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773375"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="fb4ef-103">Conexión compartida a Internet</span><span class="sxs-lookup"><span data-stu-id="fb4ef-103">Internet Connection Sharing</span></span>

<span data-ttu-id="fb4ef-104">BITS puede forzar una conexión de acceso telefónico para las redes domésticas que usan conexión compartida a Internet de Microsoft si la conexión compartida está configurada para marcar cuando los equipos de la red acceden a Internet.</span><span class="sxs-lookup"><span data-stu-id="fb4ef-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="fb4ef-105">Para evitar una conexión de acceso telefónico forzada, deshabilite la opción **establecer una conexión de acceso telefónico cada vez que un equipo en la red intente tener acceso a Internet** en el equipo host de conexión compartida que comparte su conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="fb4ef-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="fb4ef-106">Los equipos conectados al equipo host de conexión compartida suponen que tienen una conexión de red, por lo que BITS intentará transferir los archivos.</span><span class="sxs-lookup"><span data-stu-id="fb4ef-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="fb4ef-107">Si la opción de acceso telefónico está deshabilitada en el equipo host y el equipo host no tiene una conexión activa, se producirá un error transitorio en las transferencias.</span><span class="sxs-lookup"><span data-stu-id="fb4ef-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="fb4ef-108">BITS reintentará las transferencias periódicamente.</span><span class="sxs-lookup"><span data-stu-id="fb4ef-108">BITS will retry the transfers periodically.</span></span>

 

 




