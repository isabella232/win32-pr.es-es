---
description: El sistema crea automáticamente un perfil de usuario local para cada usuario cuando el usuario inicia sesión en el equipo por primera vez. El sistema mantiene automáticamente la configuración del entorno de trabajo de cada usuario en un perfil de usuario en el equipo local.
title: Perfiles de usuario local
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985667"
---
# <a name="local-user-profiles"></a><span data-ttu-id="70f3f-104">Perfiles de usuario local</span><span class="sxs-lookup"><span data-stu-id="70f3f-104">Local User Profiles</span></span>

<span data-ttu-id="70f3f-105">La seguridad de Windows requiere un perfil de usuario para cada cuenta de usuario de un equipo.</span><span class="sxs-lookup"><span data-stu-id="70f3f-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="70f3f-106">El sistema crea automáticamente un *Perfil de usuario local* para cada usuario cuando el usuario inicia sesión en el equipo por primera vez.</span><span class="sxs-lookup"><span data-stu-id="70f3f-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="70f3f-107">El sistema mantiene automáticamente la configuración del entorno de trabajo de cada usuario en un perfil de usuario en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="70f3f-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="70f3f-108">Windows Vista y versiones posteriores: los perfiles de usuario se administran a través del elemento de panel de control **cuentas de usuario** .</span><span class="sxs-lookup"><span data-stu-id="70f3f-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="70f3f-109">Windows 2000 y Windows XP: para copiar o eliminar un perfil de usuario, seleccione **sistema** en el panel de control, luego en la ficha **Opciones avanzadas** y, a continuación, en el botón **configuración** en el área **Perfil de usuario** .</span><span class="sxs-lookup"><span data-stu-id="70f3f-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="70f3f-110">El perfil del usuario no se carga automáticamente cuando el usuario inicia sesión con la función [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="70f3f-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="70f3f-111">Para cargar un perfil de usuario mediante programación, use la función [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="70f3f-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="70f3f-112">Para descargar un perfil de usuario cargado por **LoadUserProfile**, llame a la función [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="70f3f-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
