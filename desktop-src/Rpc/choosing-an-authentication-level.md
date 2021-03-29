---
title: Elección de un nivel de autenticación
description: Al elegir un nivel de autenticación, use la siguiente instrucción.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486738"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="7762f-103">Elección de un nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="7762f-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="7762f-104">Al elegir un nivel de autenticación, use la siguiente instrucción.</span><span class="sxs-lookup"><span data-stu-id="7762f-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="7762f-105">Si no importa si los datos que se envían se pueden interceptar y modificar, y los datos recibidos se pueden interceptar o modificar, use \_ \_ el nivel none de autenticación de RPC C \_ \_ , que es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7762f-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="7762f-106">Si los datos no se deben modificar y los datos privados no se envían ni reciben, use la integridad de nivel de autenticación de RPC \_ C \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7762f-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="7762f-107">En todos los demás casos, use la privacidad de nivel de autenticación de RPC \_ C \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7762f-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="7762f-108">No use el \_ \_ nivel predeterminado de autenticación de RPC c, conexión de nivel de autenticación de \_ \_ RPC \_ c \_ \_ , llamada de nivel de autenticación de RPC \_ \_ c \_ \_ \_ o PKT de nivel de autenticación de RPC \_ c \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7762f-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="7762f-109">Un atacante sofisticado puede romper estos niveles de autenticación y representarlos de forma ineficaz.</span><span class="sxs-lookup"><span data-stu-id="7762f-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="7762f-110">Cada uno de estos niveles hace que sea ligeramente más difícil para un atacante interceptar y modificar los datos, y para suplantar, pero la seguridad no se logra realmente.</span><span class="sxs-lookup"><span data-stu-id="7762f-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="7762f-111">Dado que rara vez se conoce el nivel de sofisticación de un atacante, no se recomiendan estas opciones.</span><span class="sxs-lookup"><span data-stu-id="7762f-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




