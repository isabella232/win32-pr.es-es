---
description: Windows Sockets 2 es un conjunto de funciones que estandariza el modo en que las aplicaciones tienen acceso a los diversos servicios de nombres de red y los usan.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registro y resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706109"
---
# <a name="registration-and-name-resolution"></a><span data-ttu-id="9f484-103">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="9f484-103">Registration and Name Resolution</span></span>

<span data-ttu-id="9f484-104">Windows Sockets 2 es un conjunto de funciones que estandariza el modo en que las aplicaciones tienen acceso a los diversos servicios de nombres de red y los usan.</span><span class="sxs-lookup"><span data-stu-id="9f484-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="9f484-105">Cuando se usan estas funciones, las aplicaciones no necesitan distinguir los protocolos que difieren ampliamente de los asociados a los servicios de nombres como DNS, NIS, X. 500, SAP, etc. Para mantener la compatibilidad completa con versiones anteriores de Windows Sockets 1,1, las funciones de búsqueda de base de datos **getXbyY** y asincrónica **WSAAsyncGetXbyY** se siguen admitiendo, pero se implementan en la interfaz del proveedor de servicios de Windows Sockets en cuanto a las nuevas capacidades de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9f484-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="9f484-106">Para obtener más información, vea las funciones [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) y [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) .</span><span class="sxs-lookup"><span data-stu-id="9f484-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="9f484-107">Además, consulte [resolución de nombres compatible para TCP/IP en Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span><span class="sxs-lookup"><span data-stu-id="9f484-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="9f484-108">En esta sección se describen las capacidades de registro y resolución de nombres disponibles para los desarrolladores de Winsock.</span><span class="sxs-lookup"><span data-stu-id="9f484-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="9f484-109">En la lista siguiente se describen los temas de esta sección:</span><span class="sxs-lookup"><span data-stu-id="9f484-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="9f484-110">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="9f484-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="9f484-111">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="9f484-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="9f484-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f484-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f484-113">Acerca de Winsock</span><span class="sxs-lookup"><span data-stu-id="9f484-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="9f484-114">Usar WinSock</span><span class="sxs-lookup"><span data-stu-id="9f484-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



