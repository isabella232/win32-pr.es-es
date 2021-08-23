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
ms.openlocfilehash: 4b064eefae4916576cb8ccc6b3dfe058ea4e2e34f960315b74d384194f61ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967840"
---
# <a name="user-profiles-reference"></a>Referencia de perfiles de usuario

Los siguientes elementos de API se usan con perfiles de usuario.

## <a name="functions"></a>Functions



| Función                                                                   | Descripción                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Recupera las variables de entorno para el usuario especificado.                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Crea un nuevo perfil de usuario. (solo Windows Vista y versiones posteriores).                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Elimina el perfil de usuario y toda la configuración relacionada con el usuario del equipo especificado.                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Libera las variables de entorno creadas [**por la función CreateEnvironmentBlock.**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Expande la cadena de origen mediante el bloque de entorno establecido para el usuario especificado.                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Recupera la ruta de acceso a la raíz del perfil Todos los usuarios.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Recupera la ruta de acceso a la raíz del perfil de usuario predeterminado.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Recupera la ruta de acceso al directorio raíz donde se almacenan todos los perfiles de usuario.                                  |
| [**GetProfileType**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Recupera el tipo de perfil cargado para el usuario actual.                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Recupera la ruta de acceso al directorio raíz del perfil del usuario especificado.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Carga el perfil del usuario especificado.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Descarga el perfil de un usuario cargado por la [**función LoadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)          |



 

No [**se admite la función CreateUserProfileEx.**](createuserprofileex.md)

## <a name="structures"></a>Estructuras



| Estructura                          | Descripción                                |
|------------------------------------|--------------------------------------------|
| [**PROFILEINFO**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Contiene información sobre un perfil de usuario. |



 

 

 



