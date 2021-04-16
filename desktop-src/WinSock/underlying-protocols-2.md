---
description: Algunos protocolos de los que depende la aplicación para determinados servicios, como la llamada a procedimiento remoto (RPC), pueden tener estructuras y funciones dependientes de la versión de IP que requieren que se modifique la aplicación en función de su uso.
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: Protocolos subyacentes para aplicaciones Winsock de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88789a5f4cd557111c6e1aee8c51ba00eed25e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275391"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a><span data-ttu-id="365ca-103">Protocolos subyacentes para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="365ca-103">Underlying Protocols for IPv6 Winsock Applications</span></span>

<span data-ttu-id="365ca-104">Algunos protocolos de los que depende la aplicación para determinados servicios, como la llamada a procedimiento remoto (RPC), pueden tener estructuras y funciones dependientes de la versión de IP que requieren que se modifique la aplicación en función de su uso.</span><span class="sxs-lookup"><span data-stu-id="365ca-104">Some protocols that your application depends on for certain services, such as Remote Procedure Call (RPC), may have IP-version dependent functions and structures that require you to modify your application in terms of their usage.</span></span>

<span data-ttu-id="365ca-105">Parte del proceso para modificar el código de forma que admita IPv6 debe incluir la determinación de si el uso de los protocolos subyacentes (desde la perspectiva de la pila, estos protocolos se consideran protocolos de nivel superior) requieren modificaciones para poder usar correctamente IPv6.</span><span class="sxs-lookup"><span data-stu-id="365ca-105">Part of the process to modify your code to support IPv6 should include determining whether the use of the underlying protocols (from the perspective of the stack, these protocols are considered higher-layer protocols) require modification in order to properly make use of IPv6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="365ca-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="365ca-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365ca-107">Guía de IPv6 para aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="365ca-107">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="365ca-108">Cambiar las estructuras de datos para IPv6 Winsock Appications</span><span class="sxs-lookup"><span data-stu-id="365ca-108">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="365ca-109">Sockets de doble pila para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="365ca-109">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="365ca-110">Llamadas de función para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="365ca-110">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="365ca-111">Uso de direcciones IPv4 codificadas</span><span class="sxs-lookup"><span data-stu-id="365ca-111">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="365ca-112">Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="365ca-112">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> </dl>

 

 



