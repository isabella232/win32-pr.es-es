---
description: Un perfil de usuario obligatorio es un tipo especial de Perfil de usuario móvil preconfigurado que los administradores pueden usar para especificar la configuración de los usuarios.
title: Perfiles de usuario obligatorios
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539471"
---
# <a name="mandatory-user-profiles"></a><span data-ttu-id="1e524-103">Perfiles de usuario obligatorios</span><span class="sxs-lookup"><span data-stu-id="1e524-103">Mandatory User Profiles</span></span>

<span data-ttu-id="1e524-104">Un perfil de usuario obligatorio es un tipo especial de Perfil de [usuario móvil](roaming-user-profiles.md) preconfigurado que los administradores pueden usar para especificar la configuración de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1e524-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="1e524-105">Con los perfiles de usuario obligatorios, un usuario puede modificar su escritorio, pero los cambios no se guardan cuando el usuario cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="1e524-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="1e524-106">La próxima vez que el usuario inicie sesión, se descargará el perfil de usuario obligatorio creado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="1e524-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="1e524-107">Hay dos tipos de perfiles obligatorios: perfiles *obligatorios normales* y perfiles *superobligatorios* .</span><span class="sxs-lookup"><span data-stu-id="1e524-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="1e524-108">Los perfiles de usuario se convierten en perfiles obligatorios cuando el administrador cambia el nombre del archivo NTuser. DAT (el subárbol del registro) en el servidor a NTuser. Man.</span><span class="sxs-lookup"><span data-stu-id="1e524-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="1e524-109">La extensión. Man hace que el perfil de usuario sea un perfil de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1e524-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="1e524-110">Los perfiles de usuario se convierten en *súper obligatorios* cuando el nombre de la carpeta de la ruta de acceso del perfil finaliza en. Man; por ejemplo, \\ \\ Server \\ share \\ mandatoryprofile. man \\ .</span><span class="sxs-lookup"><span data-stu-id="1e524-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="1e524-111">Los perfiles de usuario superobligatorios son similares a los perfiles obligatorios normales, con la excepción de que los usuarios que tienen perfiles superobligatorios no pueden iniciar sesión cuando el servidor que almacena el perfil obligatorio no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1e524-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="1e524-112">Los usuarios con perfiles obligatorios normales pueden iniciar sesión con la copia en caché local del perfil obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e524-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="1e524-113">Solo los administradores del sistema pueden realizar cambios en los perfiles de usuario obligatorios.</span><span class="sxs-lookup"><span data-stu-id="1e524-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



