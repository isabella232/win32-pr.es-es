---
title: Iniciando usuario
description: Iniciando usuario
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904841"
---
# <a name="launching-user"></a><span data-ttu-id="40d8f-103">Iniciando usuario</span><span class="sxs-lookup"><span data-stu-id="40d8f-103">Launching User</span></span>

<span data-ttu-id="40d8f-104">Esta es la configuración predeterminada para la identidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40d8f-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="40d8f-105">Cuando se elige el usuario iniciador para la identidad de la aplicación, cada cuenta de cliente obtiene una nueva instancia del servidor y cada servidor obtiene su propia [estación de ventana](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="40d8f-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="40d8f-106">Debido a las instancias de servidor independientes, el usuario que inicia es el valor de identidad de protección de seguridad de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="40d8f-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="40d8f-107">Sin embargo, hay límites finitos en el consumo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40d8f-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="40d8f-108">Además, el cliente no verá las GUI que muestre el servidor.</span><span class="sxs-lookup"><span data-stu-id="40d8f-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="40d8f-109">Si la aplicación tiene la identidad del usuario que inicia, se ejecuta con un token de suplantación.</span><span class="sxs-lookup"><span data-stu-id="40d8f-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="40d8f-110">Para obtener más información sobre la suplantación y los tokens de acceso, vea [niveles de suplantación](impersonation-levels.md) y [ocultación](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="40d8f-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40d8f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40d8f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40d8f-112">Identidad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="40d8f-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="40d8f-113">Usuario interactivo</span><span class="sxs-lookup"><span data-stu-id="40d8f-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="40d8f-114">Identidad de servicio</span><span class="sxs-lookup"><span data-stu-id="40d8f-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="40d8f-115">Usuario especificado</span><span class="sxs-lookup"><span data-stu-id="40d8f-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 