---
title: Obteniendo información de error de RPC extendida
description: RPC proporciona la capacidad de obtener información de error extendida. En esta sección se describe cómo se puede obtener esta información de error y se ofrecen recomendaciones sobre cómo usar la información.
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- RPC (llamada a procedimiento remoto), procedimientos recomendados, información de error extendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775954"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="32b08-105">Obteniendo información de error de RPC extendida</span><span class="sxs-lookup"><span data-stu-id="32b08-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="32b08-106">RPC proporciona la capacidad de obtener información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="32b08-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="32b08-107">En esta sección se describe cómo se puede obtener esta información de error y se ofrecen recomendaciones sobre cómo usar la información.</span><span class="sxs-lookup"><span data-stu-id="32b08-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="32b08-108">Esta sección se divide en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="32b08-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="32b08-109">La necesidad de información de error extendida</span><span class="sxs-lookup"><span data-stu-id="32b08-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="32b08-110">Seguridad e información de error ampliada</span><span class="sxs-lookup"><span data-stu-id="32b08-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="32b08-111">Habilitar información de error extendida</span><span class="sxs-lookup"><span data-stu-id="32b08-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="32b08-112">Descripción de la información de error extendida</span><span class="sxs-lookup"><span data-stu-id="32b08-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="32b08-113">Confiabilidad de la información de error extendida</span><span class="sxs-lookup"><span data-stu-id="32b08-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="32b08-114">Independencia de otros componentes</span><span class="sxs-lookup"><span data-stu-id="32b08-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="32b08-115">Información de error extendida para el usuario</span><span class="sxs-lookup"><span data-stu-id="32b08-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="32b08-116">Información de error extendida para el servidor o la aplicación</span><span class="sxs-lookup"><span data-stu-id="32b08-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="32b08-117">Ubicaciones de detección de información de error extendida</span><span class="sxs-lookup"><span data-stu-id="32b08-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="32b08-118">Esta sección está estrechamente relacionada con la depuración de la aplicación RPC.</span><span class="sxs-lookup"><span data-stu-id="32b08-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="32b08-119">Para obtener más información sobre la depuración RPC, vea \[ paquete del depurador \] .</span><span class="sxs-lookup"><span data-stu-id="32b08-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




