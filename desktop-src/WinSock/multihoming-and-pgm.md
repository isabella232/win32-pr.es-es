---
description: Se debe tener en cuenta una consideración especial para los receptores o los remitentes de PGM de host múltiple. En esta página se describen las consideraciones y se proporcionan instrucciones para las mejores prácticas de programación.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Host múltiple y PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659803"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="6da6c-104">Host múltiple y PGM</span><span class="sxs-lookup"><span data-stu-id="6da6c-104">Multihoming and PGM</span></span>

<span data-ttu-id="6da6c-105">Se debe tener en cuenta una consideración especial para los receptores o los remitentes de PGM de host múltiple.</span><span class="sxs-lookup"><span data-stu-id="6da6c-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="6da6c-106">En esta página se describen las consideraciones y se proporcionan instrucciones para las mejores prácticas de programación.</span><span class="sxs-lookup"><span data-stu-id="6da6c-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="6da6c-107">Remitente PGM de host múltiple</span><span class="sxs-lookup"><span data-stu-id="6da6c-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="6da6c-108">Cuando una aplicación no puede especificar una interfaz al llamar a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , se usa la primera interfaz disponible.</span><span class="sxs-lookup"><span data-stu-id="6da6c-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="6da6c-109">Si no hay ninguna interfaz disponible, se produce un error de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="6da6c-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="6da6c-110">Cuando una aplicación especifica una interfaz mediante la opción [RM \_ set \_ send \_ If](socket-options.md) socket, se realiza un intento de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) implícitamente a esa interfaz mediante TCP/IP y se produce un error si TCP/IP produce un error en la solicitud de enlace.</span><span class="sxs-lookup"><span data-stu-id="6da6c-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="6da6c-111">Si la interfaz se establece mediante RM \_ set \_ send \_ si varias veces, solo se aplica la última interfaz establecida correctamente.</span><span class="sxs-lookup"><span data-stu-id="6da6c-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="6da6c-112">Windows Sockets mantiene la interfaz que se establece y, si esa interfaz desaparece, la sesión se desconecta.</span><span class="sxs-lookup"><span data-stu-id="6da6c-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="6da6c-113">Receptor PGM de host múltiple</span><span class="sxs-lookup"><span data-stu-id="6da6c-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="6da6c-114">Cuando una aplicación no puede especificar una interfaz al llamar a la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , se usa la interfaz predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6da6c-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="6da6c-115">Si no hay ninguna interfaz disponible, se produce un error de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="6da6c-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="6da6c-116">Cuando una aplicación especifica una o más interfaces en las que se va a realizar la escucha, mediante el uso de [RM \_ Add \_ Receive \_ si](socket-options.md), Windows Sockets intenta enlazar a la interfaz o interfaces solicitadas mediante TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6da6c-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="6da6c-117">Cualquier error de TCP/IP hace que esta solicitud produzca un error.</span><span class="sxs-lookup"><span data-stu-id="6da6c-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="6da6c-118">A diferencia del caso del remitente PGM, la adición de una interfaz de recepción varias veces da lugar a que se publiquen las escuchas en todas las interfaces agregadas correctamente.</span><span class="sxs-lookup"><span data-stu-id="6da6c-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="6da6c-119">Use la \_ opción de \_ socket de recepción IF de RM \_ para detener la escucha en una interfaz.</span><span class="sxs-lookup"><span data-stu-id="6da6c-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="6da6c-120">Windows Sockets no mantiene el estado de varias interfaces de escucha especificadas y, en su lugar, se basa en TCP/IP para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6da6c-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="6da6c-121">Sin embargo, una vez que una sesión está en curso, Windows Sockets realiza un seguimiento de la interfaz entrante de esa sesión y, si esa interfaz desaparece, Windows Sockets desconecta la sesión.</span><span class="sxs-lookup"><span data-stu-id="6da6c-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



