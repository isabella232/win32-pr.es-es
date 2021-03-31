---
description: Describe el proceso de una operación de e/s de red en Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descripción de una operación de e/s de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360759"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="47805-103">Descripción de una operación de e/s de red</span><span class="sxs-lookup"><span data-stu-id="47805-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="47805-104">En la ilustración siguiente se muestra el proceso de una operación de e/s de red en Windows.</span><span class="sxs-lookup"><span data-stu-id="47805-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![operación de e/s de red en Windows](images/fig4.png)

<span data-ttu-id="47805-106">Cuando una aplicación llama a una función de e/s de archivo para tener acceso a un archivo en un equipo remoto, se producen los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="47805-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="47805-107">La solicitud de e/s es interceptada por un [redirector de red](network-redirectors.md), también conocido como redirector, en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="47805-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="47805-108">Esto se muestra en la figura anterior mediante la flecha sólida entre la aplicación y el redirector del cliente.</span><span class="sxs-lookup"><span data-stu-id="47805-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="47805-109">El redirector crea un paquete de datos que contiene toda la información sobre la solicitud y lo envía al servidor donde se encuentra el archivo.</span><span class="sxs-lookup"><span data-stu-id="47805-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="47805-110">Esto se muestra en la figura anterior mediante la flecha sólida entre el redirector del cliente y el redirector del servidor.</span><span class="sxs-lookup"><span data-stu-id="47805-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="47805-111">El redirector del servidor recibe el paquete del cliente, autentica el acceso al archivo requerido por la solicitud de e/s y, si se autentica, ejecuta la solicitud en nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="47805-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="47805-112">En caso contrario, devuelve un código de error al Redirector en el cliente.</span><span class="sxs-lookup"><span data-stu-id="47805-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="47805-113">Esto se muestra en la figura anterior por la flecha sólida curvada entre el redirector del servidor y el archivo.</span><span class="sxs-lookup"><span data-stu-id="47805-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="47805-114">Cuando se ha ejecutado la solicitud, el redirector en el servidor envía los datos resultantes de la solicitud de e/s al Redirector en el cliente junto con una notificación de operación correcta.</span><span class="sxs-lookup"><span data-stu-id="47805-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="47805-115">Esto se muestra en la figura anterior por la flecha de puntos entre el servidor y el redirector del cliente.</span><span class="sxs-lookup"><span data-stu-id="47805-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="47805-116">El redirector del cliente recibe el paquete del servidor y pasa los datos del paquete a la aplicación junto con una notificación de éxito.</span><span class="sxs-lookup"><span data-stu-id="47805-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="47805-117">Esto se muestra en la figura anterior por la flecha de puntos entre el redirector de cliente y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="47805-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="47805-118">Windows puede usar una variedad de protocolos de red para realizar una operación de e/s de red, incluidos el [protocolo SMB de Microsoft y la información general sobre el protocolo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) y NFS.</span><span class="sxs-lookup"><span data-stu-id="47805-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="47805-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="47805-119">In this section</span></span>



| <span data-ttu-id="47805-120">Tema</span><span class="sxs-lookup"><span data-stu-id="47805-120">Topic</span></span>                                                                                       | <span data-ttu-id="47805-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="47805-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="47805-122">Diferencias en la e/s local y de red</span><span class="sxs-lookup"><span data-stu-id="47805-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="47805-123">Diferencias entre la e/s local y la e/s de red en Windows.</span><span class="sxs-lookup"><span data-stu-id="47805-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="47805-124">Redirectores de red</span><span class="sxs-lookup"><span data-stu-id="47805-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="47805-125">Describe la funcionalidad de un redirector de red.</span><span class="sxs-lookup"><span data-stu-id="47805-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




