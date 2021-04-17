---
description: Requisitos de Server-Side para la suplantación
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Requisitos de Server-Side para la suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714829"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="19c82-103">Requisitos de Server-Side para la suplantación</span><span class="sxs-lookup"><span data-stu-id="19c82-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="19c82-104">El servidor realiza la suplantación mediante programación.</span><span class="sxs-lookup"><span data-stu-id="19c82-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="19c82-105">Asume explícitamente las credenciales de seguridad del cliente mediante [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="19c82-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="19c82-106">Cuando el cliente ha concedido al servidor autoridad suficiente, tiene el efecto de sustituir las credenciales de seguridad del cliente por el token del subproceso del servidor, en lugar del token del proceso.</span><span class="sxs-lookup"><span data-stu-id="19c82-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="19c82-107">Una vez hecho esto, el servidor puede, por ejemplo, usar el token de cliente para tener acceso a los recursos protegidos con un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="19c82-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="19c82-108">O bien, puede realizar llamadas bajo la identidad del cliente, si está habilitada la ocultación.</span><span class="sxs-lookup"><span data-stu-id="19c82-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="19c82-109">El servidor puede establecer explícitamente la ocultación mediante programación o puede depender de una configuración administrativa.</span><span class="sxs-lookup"><span data-stu-id="19c82-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="19c82-110">De forma predeterminada, las aplicaciones COM+ están configuradas para usar el Cloaking dinámico.</span><span class="sxs-lookup"><span data-stu-id="19c82-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="19c82-111">Para obtener más información, consulte [Cloaking](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="19c82-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="19c82-112">Si el servidor está implementando la delegación en nombre del cliente, mediante la identidad del cliente a través de la red, la identidad del proceso del servidor debe marcarse como "de confianza para delegación" en el servicio Active Directory; de lo contrario, se producirá un error de delegación.</span><span class="sxs-lookup"><span data-stu-id="19c82-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="19c82-113">Cuando ha terminado de usar la identidad del cliente, el servidor puede revertir a su propio token de proceso mediante [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="19c82-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="19c82-114">Para más información sobre cómo implementar la suplantación y la delegación, consulte [delegación y suplantación](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="19c82-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19c82-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19c82-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19c82-116">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="19c82-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="19c82-117">Requisitos del cliente para la suplantación</span><span class="sxs-lookup"><span data-stu-id="19c82-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="19c82-118">Esconder</span><span class="sxs-lookup"><span data-stu-id="19c82-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 
