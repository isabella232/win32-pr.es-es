---
description: Algunas aplicaciones necesitan recibir notificaciones de eventos de conexión, antes del evento, justo después de que se produzca o ambos. Puede crear un archivo DLL para recibir notificaciones de eventos de conexión anticipados y posteriores a los hechos.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Recepción de notificaciones de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539859"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="664c8-104">Recepción de notificaciones de conexión</span><span class="sxs-lookup"><span data-stu-id="664c8-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="664c8-105">Algunas aplicaciones necesitan recibir notificaciones de eventos de conexión, antes del evento, justo después de que se produzca o ambos.</span><span class="sxs-lookup"><span data-stu-id="664c8-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="664c8-106">Puede crear un archivo DLL para recibir notificaciones de eventos de conexión anticipados y posteriores a los hechos.</span><span class="sxs-lookup"><span data-stu-id="664c8-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="664c8-107">Un ejemplo de una aplicación que necesita recibir notificaciones previas de un evento de conexión es el servicio de acceso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="664c8-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="664c8-108">RAS debe ser informado antes de que se establezca una conexión, ya que puede ser necesario establecer una conexión de módem antes de realizar la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="664c8-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="664c8-109">Del mismo modo, es posible que las aplicaciones necesiten limpiar los recursos una vez realizada la conexión, lo que requiere una notificación posterior a la conexión.</span><span class="sxs-lookup"><span data-stu-id="664c8-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="664c8-110">Las aplicaciones interesadas en recibir notificaciones anticipadas y posteriores a los eventos de conexión deben proporcionar un archivo DLL que exporte dos funciones, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) y [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span><span class="sxs-lookup"><span data-stu-id="664c8-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="664c8-111">Después de implementar estas funciones, debe registrar el archivo DLL tal y como se describe en [registrar para recibir notificaciones de conexión](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="664c8-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



