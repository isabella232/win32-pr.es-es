---
description: Los siguientes elementos de API se usan con perfiles de usuario.
title: Referencia de perfiles de usuario
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986015"
---
# <a name="user-profiles-reference"></a><span data-ttu-id="760ab-103">Referencia de perfiles de usuario</span><span class="sxs-lookup"><span data-stu-id="760ab-103">User Profiles Reference</span></span>

<span data-ttu-id="760ab-104">Los siguientes elementos de API se usan con perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="760ab-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="760ab-105">Functions</span><span class="sxs-lookup"><span data-stu-id="760ab-105">Functions</span></span>



| <span data-ttu-id="760ab-106">Función</span><span class="sxs-lookup"><span data-stu-id="760ab-106">Function</span></span>                                                                   | <span data-ttu-id="760ab-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="760ab-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="760ab-108">**CreateEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="760ab-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="760ab-109">Recupera las variables de entorno para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="760ab-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="760ab-110">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="760ab-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="760ab-111">Crea un nuevo perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="760ab-111">Creates a new user profile.</span></span> <span data-ttu-id="760ab-112">(Solo Windows Vista y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="760ab-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="760ab-113">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="760ab-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="760ab-114">Elimina el perfil de usuario y toda la configuración relacionada con el usuario del equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="760ab-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="760ab-115">**DestroyEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="760ab-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="760ab-116">Libera las variables de entorno creadas por la función [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) .</span><span class="sxs-lookup"><span data-stu-id="760ab-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="760ab-117">**ExpandEnvironmentStringsForUser**</span><span class="sxs-lookup"><span data-stu-id="760ab-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="760ab-118">Expande la cadena de origen utilizando el bloque de entorno establecido para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="760ab-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="760ab-119">**GetAllUsersProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="760ab-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="760ab-120">Recupera la ruta de acceso a la raíz del perfil de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="760ab-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="760ab-121">**GetDefaultUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="760ab-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="760ab-122">Recupera la ruta de acceso a la raíz del perfil de usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="760ab-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="760ab-123">**GetProfilesDirectory**</span><span class="sxs-lookup"><span data-stu-id="760ab-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="760ab-124">Recupera la ruta de acceso al directorio raíz donde se almacenan todos los perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="760ab-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="760ab-125">**GetProfileType**</span><span class="sxs-lookup"><span data-stu-id="760ab-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="760ab-126">Recupera el tipo de perfil cargado para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="760ab-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="760ab-127">**GetUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="760ab-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="760ab-128">Recupera la ruta de acceso al directorio raíz del perfil del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="760ab-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="760ab-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="760ab-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="760ab-130">Carga el perfil del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="760ab-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="760ab-131">**UnloadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="760ab-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="760ab-132">Descarga el perfil de un usuario cargado por la función [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="760ab-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="760ab-133">No se admite la función [**CreateUserProfileEx**](createuserprofileex.md) .</span><span class="sxs-lookup"><span data-stu-id="760ab-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="760ab-134">Estructuras</span><span class="sxs-lookup"><span data-stu-id="760ab-134">Structures</span></span>



| <span data-ttu-id="760ab-135">Estructura</span><span class="sxs-lookup"><span data-stu-id="760ab-135">Structure</span></span>                          | <span data-ttu-id="760ab-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="760ab-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="760ab-137">**PROFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="760ab-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="760ab-138">Contiene información acerca de un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="760ab-138">Contains information about a user profile.</span></span> |



 

 

 



