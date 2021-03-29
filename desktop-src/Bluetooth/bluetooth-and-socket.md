---
title: Bluetooth y socket
description: Crea un socket para las conexiones entrantes o salientes.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Bluetooth de socket
- Bluetooth y Socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791889"
---
# <a name="bluetooth-and-socket"></a><span data-ttu-id="9aea8-106">Bluetooth y socket</span><span class="sxs-lookup"><span data-stu-id="9aea8-106">Bluetooth and socket</span></span>

<span data-ttu-id="9aea8-107">La función [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket para las conexiones entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="9aea8-107">The [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function creates a socket for incoming or outgoing connections.:</span></span>

<span data-ttu-id="9aea8-108">Para crear un socket mediante Bluetooth, utilice la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="9aea8-108">To create a socket using Bluetooth, use the following settings:</span></span>

-   <span data-ttu-id="9aea8-109">El parámetro *AF* de la función [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) siempre se establece en **AF \_ BTH** para los sockets Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9aea8-109">The *af* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always set to **AF\_BTH** for Bluetooth sockets.</span></span>
-   <span data-ttu-id="9aea8-110">El parámetro de *tipo* de la función de [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) siempre es **sock \_ Stream**; **Sock \_** Los sockets DGRAM no son compatibles con Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9aea8-110">The *type* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always **SOCK\_STREAM**; **SOCK\_DGRAM** sockets are not supported by Bluetooth.</span></span>
-   <span data-ttu-id="9aea8-111">En el caso del parámetro *Protocol* , **BTHPROTO \_ RFCOMM** es el protocolo admitido.</span><span class="sxs-lookup"><span data-stu-id="9aea8-111">For the *protocol* parameter, **BTHPROTO\_RFCOMM** is the supported protocol.</span></span>

<span data-ttu-id="9aea8-112">Para obtener más información, consulte [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span><span class="sxs-lookup"><span data-stu-id="9aea8-112">For more information, see [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9aea8-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9aea8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aea8-114">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="9aea8-114">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="9aea8-115">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="9aea8-115">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 