---
title: Elección del tipo de identificadores de enlace que se va a usar
description: Elección del tipo de identificadores de enlace que se va a usar
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075436"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="a7639-103">Elección del tipo de identificadores de enlace que se va a usar</span><span class="sxs-lookup"><span data-stu-id="a7639-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="a7639-104">**Procedimiento recomendado:** Si sabe qué servidor usará la aplicación, use identificadores explícitos.</span><span class="sxs-lookup"><span data-stu-id="a7639-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="a7639-105">Si no es así, use los identificadores explícitos en cada ocasión, o bien use identificadores genéricos con rutinas de **\_ enlace** y **\_ desenlace** .</span><span class="sxs-lookup"><span data-stu-id="a7639-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="a7639-106">No use identificadores ni identificadores automáticos.</span><span class="sxs-lookup"><span data-stu-id="a7639-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="a7639-107">Los identificadores implícitos no son seguros para subprocesos y, aunque la seguridad para subprocesos puede parecer innecesaria, podría ser necesario más adelante.</span><span class="sxs-lookup"><span data-stu-id="a7639-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="a7639-108">Los identificadores automáticos tienen una gran sobrecarga y requieren una gran cantidad de configuración para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="a7639-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="a7639-109">Los servicios de Active Directory han reemplazado sus capacidades de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a7639-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="a7639-110">Los identificadores explícitos son muy eficaces y muchas funciones atractivas solo están disponibles para los identificadores explícitos.</span><span class="sxs-lookup"><span data-stu-id="a7639-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="a7639-111">Por ejemplo, si varias llamadas RPC van al mismo servidor, puede construir el identificador de enlace una vez y realizar todas las llamadas con él.</span><span class="sxs-lookup"><span data-stu-id="a7639-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="a7639-112">Este enfoque es mucho más eficaz que cualquier otro método.</span><span class="sxs-lookup"><span data-stu-id="a7639-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="a7639-113">Si no se conoce el servidor al que se va a llamar, construya un identificador de enlace explícito para cada llamada o use identificadores de enlace genéricos.</span><span class="sxs-lookup"><span data-stu-id="a7639-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="a7639-114">En Microsoft™ Windows XP, el tiempo de ejecución de RPC es bastante eficaz en las llamadas de reutilización y almacenamiento en caché, por lo que si la llamada *n*+ 1ª termina en el mismo servidor que la llamada *n*, RPC vuelve a usar los recursos asignados para la llamada *n*, evitando la necesidad de almacenar en caché los identificadores de enlace para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a7639-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




