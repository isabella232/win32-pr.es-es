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
# <a name="roaming-user-profiles"></a>Perfiles de usuario móviles

Si un equipo ejecuta Windows 2000 Server o una versión posterior en una red, los usuarios pueden almacenar sus perfiles en el servidor. Estos perfiles se denominan *perfiles de usuario móviles*.

Los perfiles de usuario móviles tienen las siguientes ventajas:

-   Disponibilidad de recursos automática. El perfil único de un usuario está disponible automáticamente cuando inicia sesión en cualquier equipo de la red. No es necesario que los usuarios creen un perfil en cada equipo que utilicen en una red.
-   Copia de seguridad y reemplazo de equipos simplificados. Cuando se debe reemplazar el equipo de un usuario, se puede reemplazar fácilmente porque toda la información de perfil del usuario se mantiene por separado en la red, independientemente de un equipo individual. Cuando el usuario inicia sesión en el nuevo equipo por primera vez, la copia del perfil del usuario se copia en el nuevo equipo.

El perfil del usuario no se carga automáticamente cuando el usuario inicia sesión con la función [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Para cargar un perfil de usuario móvil mediante programación, use la función [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Para descargar un perfil de usuario móvil cargado por **LoadUserProfile**, llame a la función [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
