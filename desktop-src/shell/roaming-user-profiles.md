---
description: Si un equipo ejecuta Windows 2000 Server o posterior en una red, los usuarios pueden almacenar sus perfiles en el servidor. Estos perfiles se denominan perfiles de usuario móviles.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267828"
---
# <a name="roaming-user-profiles"></a>Perfiles de usuario móviles

Si un equipo ejecuta Windows 2000 Server o posterior en una red, los usuarios pueden almacenar sus perfiles en el servidor. Estos perfiles se *denominan perfiles de usuario móviles.*

Los perfiles de usuario móviles tienen las siguientes ventajas:

-   Disponibilidad automática de recursos. El perfil único de un usuario está disponible automáticamente cuando inicia sesión en cualquier equipo de la red. Los usuarios no necesitan crear un perfil en cada equipo que usan en una red.
-   Reemplazo y copia de seguridad de equipos simplificados. Cuando se debe reemplazar el equipo de un usuario, se puede reemplazar fácilmente porque toda la información de perfil del usuario se mantiene por separado en la red, independientemente de un equipo individual. Cuando el usuario inicia sesión en el nuevo equipo por primera vez, la copia del servidor del perfil del usuario se copia en el nuevo equipo.

El perfil del usuario no se carga automáticamente cuando el usuario inicia sesión mediante la [**función LogonUser.**](/windows/win32/api/winbase/nf-winbase-logonusera) Para cargar un perfil de usuario móvil mediante programación, use la [**función LoadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) Para descargar un perfil de usuario móvil cargado **por LoadUserProfile,** llame a [**la función UnloadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)

 

 
