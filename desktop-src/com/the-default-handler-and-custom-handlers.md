---
title: Controlador predeterminado y controladores personalizados
description: Controlador predeterminado y controladores personalizados
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994051"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="c3f77-103">Controlador predeterminado y controladores personalizados</span><span class="sxs-lookup"><span data-stu-id="c3f77-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="c3f77-104">La mayoría de las aplicaciones usan el controlador predeterminado, una implementación proporcionada por OLE, como controlador.</span><span class="sxs-lookup"><span data-stu-id="c3f77-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="c3f77-105">Una aplicación implementa un controlador personalizado cuando las capacidades del controlador predeterminado son insuficientes.</span><span class="sxs-lookup"><span data-stu-id="c3f77-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="c3f77-106">Un controlador personalizado puede reemplazar por completo el controlador predeterminado o usar partes de la funcionalidad que proporciona cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="c3f77-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="c3f77-107">En el último caso, el controlador de la aplicación se implementa como un objeto agregado compuesto por un nuevo objeto de control y por el controlador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c3f77-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="c3f77-108">Los controladores predeterminados o de aplicación combinados también se conocen como *controladores en proceso*.</span><span class="sxs-lookup"><span data-stu-id="c3f77-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="c3f77-109">El *controlador de comunicación remota* se utiliza para los objetos que no tienen asignado un CLSID en el registro del sistema o que no tienen un controlador especificado.</span><span class="sxs-lookup"><span data-stu-id="c3f77-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="c3f77-110">Todo lo que se necesita de un controlador para estos tipos de objetos es que pasan información a través del límite del proceso.</span><span class="sxs-lookup"><span data-stu-id="c3f77-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3f77-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3f77-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3f77-112">Controladores de objetos</span><span class="sxs-lookup"><span data-stu-id="c3f77-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




