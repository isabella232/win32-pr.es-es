---
description: Una de las responsabilidades más importantes de un proveedor de servicios de transporte de datos es que proporciona indicaciones al cliente cuando se han producido determinados eventos de red.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notificación de eventos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907940"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="2d8e2-103">Notificación de eventos de red</span><span class="sxs-lookup"><span data-stu-id="2d8e2-103">Notification of Network Events</span></span>

<span data-ttu-id="2d8e2-104">Una de las responsabilidades más importantes de un proveedor de servicios de transporte de datos es que proporciona indicaciones al cliente cuando se han producido determinados eventos de red.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="2d8e2-105">La lista de eventos de red definidos consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2d8e2-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="2d8e2-106">**FD \_ CONECTAR**: se ha completado una conexión a un host remoto o a una sesión de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="2d8e2-107">**FD \_ ACEPTAR**: un host remoto está realizando una solicitud de conexión.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="2d8e2-108">**FD \_ LECTURA**: los datos de red llegaron a estar disponibles para su lectura.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="2d8e2-109">**FD \_ ESCRITURA**: el espacio está disponible en los búferes del proveedor de servicios para que ahora se puedan enviar datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="2d8e2-110">**FD \_ OOB**: los datos fuera de banda están disponibles para su lectura.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="2d8e2-111">**FD \_ CERRAR**: el host remoto ha cerrado la conexión.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="2d8e2-112">**FD \_ QOS**: se ha producido un cambio en los niveles de QoS negociados.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="2d8e2-113">**FD \_ \_QoS de grupo**: reservado.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="2d8e2-114">**FD \_ \_ \_ Cambio** de la interfaz de enrutamiento: una interfaz local que se debe usar para alcanzar el destino especificado en la **interfaz de enrutamiento de SiO el cambio de \_ \_ \_ ioctl** ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="2d8e2-115">**FD \_ \_ \_ Cambio** en la lista de direcciones: la lista de direcciones locales a la que se puede enlazar la aplicación ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="2d8e2-116">El conjunto de eventos de red enumerados anteriormente se denomina a veces eventos **FD \_ XXX** .</span><span class="sxs-lookup"><span data-stu-id="2d8e2-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="2d8e2-117">La indicación de que se produzcan uno o varios de estos eventos de red se puede proporcionar de varias maneras, dependiendo de cómo el cliente solicite la notificación.</span><span class="sxs-lookup"><span data-stu-id="2d8e2-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



