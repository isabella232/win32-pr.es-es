---
title: Métodos de seguridad
description: Microsoft RPC admite dos métodos diferentes para agregar seguridad a la aplicación distribuida.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076175"
---
# <a name="security-methods"></a><span data-ttu-id="47001-103">Métodos de seguridad</span><span class="sxs-lookup"><span data-stu-id="47001-103">Security Methods</span></span>

<span data-ttu-id="47001-104">Microsoft RPC admite dos métodos diferentes para agregar seguridad a la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="47001-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="47001-105">El primer método consiste en usar la interfaz del proveedor de compatibilidad para seguridad (SSPI), a la que se puede tener acceso mediante las funciones RPC.</span><span class="sxs-lookup"><span data-stu-id="47001-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="47001-106">En general, es mejor utilizar este método.</span><span class="sxs-lookup"><span data-stu-id="47001-106">In general, it is best to use this method.</span></span> <span data-ttu-id="47001-107">SSPI proporciona las características de autenticación más flexibles y independientes de la red.</span><span class="sxs-lookup"><span data-stu-id="47001-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="47001-108">El segundo método consiste en utilizar las características de seguridad integradas en los protocolos de transporte del sistema.</span><span class="sxs-lookup"><span data-stu-id="47001-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="47001-109">El método de seguridad de nivel de transporte no es el método preferido.</span><span class="sxs-lookup"><span data-stu-id="47001-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="47001-110">Se recomienda usar SSPI porque funciona en todos los transportes, entre plataformas, y proporciona altos niveles de seguridad, incluida la privacidad.</span><span class="sxs-lookup"><span data-stu-id="47001-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="47001-111">En esta sección se proporciona información general sobre la seguridad de nivel de transporte y SSPI en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="47001-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="47001-112">Interfaz del proveedor de compatibilidad con seguridad (SSPI)</span><span class="sxs-lookup"><span data-stu-id="47001-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="47001-113">Seguridad de transporte</span><span class="sxs-lookup"><span data-stu-id="47001-113">Transport Security</span></span>](transport-security.md)

 

 




