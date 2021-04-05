---
title: Servicios de autorización
description: Un servicio de autorización es el método que usa el SSP para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076032"
---
# <a name="authorization-services"></a><span data-ttu-id="75088-105">Servicios de autorización</span><span class="sxs-lookup"><span data-stu-id="75088-105">Authorization Services</span></span>

<span data-ttu-id="75088-106">Un servicio de autorización es el método que usa el SSP para autorizar el acceso a un procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="75088-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="75088-107">Los SSP pueden proporcionar más de un servicio de autorización.</span><span class="sxs-lookup"><span data-stu-id="75088-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="75088-108">Sin embargo, normalmente seleccionan uno como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="75088-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="75088-109">La aplicación puede utilizar el método de autorización predeterminado para el SSP actual o puede especificar uno.</span><span class="sxs-lookup"><span data-stu-id="75088-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="75088-110">En la actualidad, Microsoft RPC admite dos métodos de autorización.</span><span class="sxs-lookup"><span data-stu-id="75088-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="75088-111">Uno es para que el servidor proporcione autorización basada en el nombre del programa cliente.</span><span class="sxs-lookup"><span data-stu-id="75088-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="75088-112">El otro es para que el servidor Compare las credenciales de autenticación del cliente con la lista de control de acceso (ACL) del servidor.</span><span class="sxs-lookup"><span data-stu-id="75088-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="75088-113">Para obtener una lista de servicios de autorización, consulte [constantes de servicio de autorización](authorization-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75088-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="75088-114">Se recomienda que los desarrolladores usen RPC \_ C \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="75088-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




