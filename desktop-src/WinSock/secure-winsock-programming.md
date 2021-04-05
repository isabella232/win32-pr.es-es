---
description: La siguiente es una guía para proteger la programación de Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programación de Winsock segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812457"
---
# <a name="secure-winsock-programming"></a><span data-ttu-id="dda27-103">Programación de Winsock segura</span><span class="sxs-lookup"><span data-stu-id="dda27-103">Secure Winsock Programming</span></span>

<span data-ttu-id="dda27-104">La siguiente es una guía para proteger la programación de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="dda27-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="dda27-105">Está diseñado para proporcionar una descripción de la seguridad de Winsock y las opciones disponibles para el desarrollador de aplicaciones de red segura.</span><span class="sxs-lookup"><span data-stu-id="dda27-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="dda27-106">Usar SO \_ REUSEADDR y so \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="dda27-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="dda27-107">Extensiones Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="dda27-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="dda27-108">Las comunicaciones que usan Sockets también se pueden cifrar mediante los estándares SSL/TLS mediante el canal seguro, también conocido como tecnología Schannel.</span><span class="sxs-lookup"><span data-stu-id="dda27-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="dda27-109">Schannel es un proveedor de compatibilidad para seguridad (SSP) que contiene un conjunto de protocolos de seguridad que proporcionan autenticación de identidad y comunicación privada segura a través del cifrado.</span><span class="sxs-lookup"><span data-stu-id="dda27-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="dda27-110">Schannel se usa principalmente para aplicaciones de Internet que requieren comunicaciones del protocolo seguro de transferencia de hipertexto (HTTP).</span><span class="sxs-lookup"><span data-stu-id="dda27-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="dda27-111">Para obtener más información, consulte [canal seguro](../secauthn/secure-channel.md).</span><span class="sxs-lookup"><span data-stu-id="dda27-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dda27-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dda27-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dda27-113">Canal seguro</span><span class="sxs-lookup"><span data-stu-id="dda27-113">Secure Channel</span></span>](../secauthn/secure-channel.md)
</dt> </dl>

 

 
