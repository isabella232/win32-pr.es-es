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
# <a name="local-user-profiles"></a>Perfiles de usuario local

La seguridad de Windows requiere un perfil de usuario para cada cuenta de usuario de un equipo. El sistema crea automáticamente un *Perfil de usuario local* para cada usuario cuando el usuario inicia sesión en el equipo por primera vez. El sistema mantiene automáticamente la configuración del entorno de trabajo de cada usuario en un perfil de usuario en el equipo local.

Windows Vista y versiones posteriores: los perfiles de usuario se administran a través del elemento de panel de control **cuentas de usuario** .

Windows 2000 y Windows XP: para copiar o eliminar un perfil de usuario, seleccione **sistema** en el panel de control, luego en la ficha **Opciones avanzadas** y, a continuación, en el botón **configuración** en el área **Perfil de usuario** .

El perfil del usuario no se carga automáticamente cuando el usuario inicia sesión con la función [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Para cargar un perfil de usuario mediante programación, use la función [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Para descargar un perfil de usuario cargado por **LoadUserProfile**, llame a la función [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
