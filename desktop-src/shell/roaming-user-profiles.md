---
description: Si un equipo ejecuta Windows 2000 Server o una versión posterior en una red, los usuarios pueden almacenar sus perfiles en el servidor. Estos perfiles se denominan perfiles de usuario móviles.
title: Perfiles de usuario móviles
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985630"
---
# <a name="roaming-user-profiles"></a><span data-ttu-id="fd4e0-104">Perfiles de usuario móviles</span><span class="sxs-lookup"><span data-stu-id="fd4e0-104">Roaming User Profiles</span></span>

<span data-ttu-id="fd4e0-105">Si un equipo ejecuta Windows 2000 Server o una versión posterior en una red, los usuarios pueden almacenar sus perfiles en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="fd4e0-106">Estos perfiles se denominan *perfiles de usuario móviles*.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="fd4e0-107">Los perfiles de usuario móviles tienen las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="fd4e0-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="fd4e0-108">Disponibilidad de recursos automática.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-108">Automatic resource availability.</span></span> <span data-ttu-id="fd4e0-109">El perfil único de un usuario está disponible automáticamente cuando inicia sesión en cualquier equipo de la red.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="fd4e0-110">No es necesario que los usuarios creen un perfil en cada equipo que utilicen en una red.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="fd4e0-111">Copia de seguridad y reemplazo de equipos simplificados.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="fd4e0-112">Cuando se debe reemplazar el equipo de un usuario, se puede reemplazar fácilmente porque toda la información de perfil del usuario se mantiene por separado en la red, independientemente de un equipo individual.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="fd4e0-113">Cuando el usuario inicia sesión en el nuevo equipo por primera vez, la copia del perfil del usuario se copia en el nuevo equipo.</span><span class="sxs-lookup"><span data-stu-id="fd4e0-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="fd4e0-114">El perfil del usuario no se carga automáticamente cuando el usuario inicia sesión con la función [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="fd4e0-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="fd4e0-115">Para cargar un perfil de usuario móvil mediante programación, use la función [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="fd4e0-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="fd4e0-116">Para descargar un perfil de usuario móvil cargado por **LoadUserProfile**, llame a la función [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="fd4e0-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
