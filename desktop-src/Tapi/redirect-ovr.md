---
description: La redirección de la sesión permite que una aplicación desvíe una sesión ofrecida a otra dirección sin responder a la llamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819435"
---
# <a name="redirect"></a><span data-ttu-id="9ee4e-103">Redirect</span><span class="sxs-lookup"><span data-stu-id="9ee4e-103">Redirect</span></span>

<span data-ttu-id="9ee4e-104">La redirección de la sesión permite que una aplicación desvíe una sesión ofrecida a otra dirección sin responder a la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="9ee4e-105">La aplicación puede realizar la redirección en función de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="9ee4e-106">Por ejemplo, una aplicación podría permitir a un usuario especificar redireccionamientos diferentes en función de la información del identificador del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="9ee4e-107">Una vez que se ha redirigido correctamente una llamada, el estado normalmente realiza la transición a los recursos inactivos y asociados.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="9ee4e-108">La redirección es diferente de [reenviar](forward-ovr.md) en que, una vez que se ha configurado el reenvío, la operación la realiza TAPI, el proveedor de servicios o el conmutador sin necesidad de más implicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="9ee4e-109">La redirección es diferente de la [transferencia](transfer-ovr.md) en que la redirección no requiere responder primero a la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="9ee4e-110">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="9ee4e-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="9ee4e-111">**TAPI 2. x:** Vea [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span><span class="sxs-lookup"><span data-stu-id="9ee4e-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
