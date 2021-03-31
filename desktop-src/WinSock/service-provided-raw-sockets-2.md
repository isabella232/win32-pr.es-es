---
description: Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. El uso de sockets sin formato al migrar aplicaciones a Winsock no se recomienda por varias razones.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Sockets sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155869"
---
# <a name="raw-sockets"></a><span data-ttu-id="52328-104">Sockets sin formato</span><span class="sxs-lookup"><span data-stu-id="52328-104">Raw Sockets</span></span>

<span data-ttu-id="52328-105">Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="52328-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="52328-106">El uso de sockets sin formato al migrar aplicaciones a Winsock no se recomienda por varias razones.</span><span class="sxs-lookup"><span data-stu-id="52328-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="52328-107">La especificación de Windows Sockets no exige que un proveedor de servicios Winsock admita Sockets sin formato, es decir, sockets de tipo **sock \_ raw**.</span><span class="sxs-lookup"><span data-stu-id="52328-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="52328-108">Sin embargo, se recomienda que los proveedores de servicios proporcionen compatibilidad con sockets sin formato.</span><span class="sxs-lookup"><span data-stu-id="52328-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="52328-109">Una aplicación compatible con Windows Sockets que desee usar sockets sin formato debe intentar abrir el socket con la llamada de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , y si se produce un error al intentar usar otro tipo de socket o indicar el error al usuario.</span><span class="sxs-lookup"><span data-stu-id="52328-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="52328-110">En Windows 7, Windows Server 2008 R2, Windows Vista y Windows XP con Service Pack 2 (SP2), la capacidad de enviar tráfico a través de sockets sin formato se ha restringido de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="52328-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="52328-111">Para obtener más información, consulte [Sockets sin formato de TCP/IP](tcp-ip-raw-sockets-2.md).</span><span class="sxs-lookup"><span data-stu-id="52328-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52328-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52328-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52328-113">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="52328-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="52328-114">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="52328-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="52328-115">Sockets sin formato de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="52328-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="52328-116">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="52328-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



