---
title: COM y paquetes de seguridad
description: Windows admite NTLMSSP (proveedor de compatibilidad de seguridad de LAN Manager), el protocolo de autenticación de Kerberos V5 y el paquete de seguridad de Schannel, que proporciona los protocolos PCT 1,0, SSL 2,0, SSL 3,0 y TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714147"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="5d132-103">COM y paquetes de seguridad</span><span class="sxs-lookup"><span data-stu-id="5d132-103">COM and Security Packages</span></span>

<span data-ttu-id="5d132-104">Windows admite NTLMSSP (proveedor de compatibilidad de seguridad de LAN Manager), el protocolo de autenticación de Kerberos V5 y el paquete de seguridad de Schannel, que proporciona los protocolos PCT 1,0, SSL 2,0, SSL 3,0 y TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="5d132-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="5d132-105">También se admite Snego, que comprueba los paquetes de seguridad disponibles y selecciona el más apropiado.</span><span class="sxs-lookup"><span data-stu-id="5d132-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="5d132-106">En la tabla siguiente se muestran los niveles de autenticación que admiten los distintos paquetes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5d132-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="5d132-107">Autenticación de servidor/cliente</span><span class="sxs-lookup"><span data-stu-id="5d132-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="5d132-108">Compatibilidad con paquetes de seguridad</span><span class="sxs-lookup"><span data-stu-id="5d132-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5d132-109">Ninguno de ellos puede obtener el nombre del otro.</span><span class="sxs-lookup"><span data-stu-id="5d132-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="5d132-110">None</span><span class="sxs-lookup"><span data-stu-id="5d132-110">None</span></span><br/>                                                  |
| <span data-ttu-id="5d132-111">El cliente puede autenticar el servidor, pero no viceversa.</span><span class="sxs-lookup"><span data-stu-id="5d132-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="5d132-112">Schannel</span><span class="sxs-lookup"><span data-stu-id="5d132-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="5d132-113">El cliente no puede detectar el servidor, pero el servidor puede obtener el identificador de usuario del cliente.</span><span class="sxs-lookup"><span data-stu-id="5d132-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="5d132-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="5d132-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="5d132-115">Autenticación mutua: el cliente y el servidor pueden conocer el nombre del otro si se concede el permiso.</span><span class="sxs-lookup"><span data-stu-id="5d132-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="5d132-116">NTLMSSP (localmente), protocolo Kerberos V5 y Schannel</span><span class="sxs-lookup"><span data-stu-id="5d132-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="5d132-117">Para obtener más información acerca de estos paquetes de seguridad, vea los temas siguientes en esta sección:</span><span class="sxs-lookup"><span data-stu-id="5d132-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="5d132-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="5d132-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="5d132-119">Protocolo Kerberos V5</span><span class="sxs-lookup"><span data-stu-id="5d132-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="5d132-120">Schannel</span><span class="sxs-lookup"><span data-stu-id="5d132-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="5d132-121">Snego</span><span class="sxs-lookup"><span data-stu-id="5d132-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="5d132-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d132-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d132-123">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="5d132-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





