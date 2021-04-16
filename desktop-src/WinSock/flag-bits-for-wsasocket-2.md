---
description: En algunos casos, los sockets Unidos a una sesión de Multipoint pueden tener algunas diferencias de comportamiento con los sockets de punto a punto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Marcar bits para WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705623"
---
# <a name="flag-bits-for-wsasocket"></a><span data-ttu-id="aeae3-103">Marcar bits para WSASocket</span><span class="sxs-lookup"><span data-stu-id="aeae3-103">Flag Bits for WSASocket</span></span>

<span data-ttu-id="aeae3-104">En algunos casos, los sockets Unidos a una sesión de Multipoint pueden tener algunas diferencias de comportamiento con los sockets de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="aeae3-104">In some instances sockets joined to a multipoint session may have some differences in behavior from point-to-point sockets.</span></span> <span data-ttu-id="aeae3-105">Por ejemplo, un \_ socket de hoja d en un esquema de plano de datos raíz solo puede enviar información al \_ participante raíz d.</span><span class="sxs-lookup"><span data-stu-id="aeae3-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="aeae3-106">Esto crea una necesidad de que la aplicación pueda indicar el uso previsto de un coincidente de socket con su creación.</span><span class="sxs-lookup"><span data-stu-id="aeae3-106">This creates a need for the application to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="aeae3-107">Esto se hace a través de los cuatro bits de marca que se pueden establecer en el parámetro *dwFlags* en [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span><span class="sxs-lookup"><span data-stu-id="aeae3-107">This is done through four-flag bits that can be set in the *dwFlags* parameter to [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span></span>

-   <span data-ttu-id="aeae3-108">WSA \_ marca \_ \_ \_ la raíz de Multipoint c, para la creación de un socket que actúa como una raíz de c \_ y solo se permite si un plano de control con raíz se indica en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aeae3-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="aeae3-109">WSA \_ marca \_ la hoja Multipoint- \_ c \_ , para la creación de un socket que actúa como hoja de c \_ y solo se permite si XP1 \_ admite \_ Multipoint en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aeae3-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="aeae3-110">WSA \_ marca \_ \_ \_ la raíz de Multipoint d, para la creación de un socket que actúa como \_ raíz d y solo se permite si un plano de datos raíz se indica en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aeae3-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="aeae3-111">WSA \_ marca \_ \_ \_ la hoja multipunto d, para la creación de un socket que actúa como \_ hoja d y solo se permite si XP1 \_ admite \_ Multipoint en la entrada [**de \_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aeae3-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="aeae3-112">Tenga en cuenta que al crear un Multipoint socket, exactamente una de las dos marcas de plano de control y una de las dos marcas de plano de datos debe establecerse en el parámetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="aeae3-112">Note that when creating a multipoint socket, exactly one of the two control-plane flags, and one of the two data-plane flags must be set in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)'s *dwFlags* parameter.</span></span> <span data-ttu-id="aeae3-113">Por lo tanto, las cuatro posibilidades para crear Multipoint Sockets son:</span><span class="sxs-lookup"><span data-stu-id="aeae3-113">Thus, the four possibilities for creating multipoint sockets are:</span></span>

-   <span data-ttu-id="aeae3-114">" \_ raíz raíz/d de c \_ "</span><span class="sxs-lookup"><span data-stu-id="aeae3-114">"c\_root/d\_root"</span></span>
-   <span data-ttu-id="aeae3-115">" \_ hoja raíz/d de c \_ "</span><span class="sxs-lookup"><span data-stu-id="aeae3-115">"c\_root/d\_leaf"</span></span>
-   <span data-ttu-id="aeae3-116">"raíz de c \_ /d \_ "</span><span class="sxs-lookup"><span data-stu-id="aeae3-116">"c\_leaf/d\_root"</span></span>
-   <span data-ttu-id="aeae3-117">" \_ hoja c/d \_ hoja"</span><span class="sxs-lookup"><span data-stu-id="aeae3-117">"c\_leaf /d\_leaf"</span></span>

 

 
