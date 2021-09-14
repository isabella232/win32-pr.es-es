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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256988"
---
# <a name="local-user-profiles"></a>Perfiles de usuario local

Windows seguridad requiere un perfil de usuario para cada cuenta de usuario de un equipo. El sistema crea automáticamente un perfil *de usuario local* para cada usuario cuando el usuario inicia sesión en el equipo por primera vez. El sistema mantiene automáticamente la configuración del entorno de trabajo de cada usuario en un perfil de usuario en el equipo local.

Windows Vista y versiones posteriores: los perfiles de usuario se administran a través **del** elemento del panel de control Cuentas de usuario.

Windows 2000 y Windows XP: para copiar o eliminar un  perfil de usuario, seleccione Sistema en el Panel de control, la pestaña Avanzadas  y, a continuación, el botón **Configuración** en el área Perfil de usuario. 

El perfil del usuario no se carga automáticamente cuando el usuario inicia sesión con la [**función LogonUser.**](/windows/win32/api/winbase/nf-winbase-logonusera) Para cargar un perfil de usuario mediante programación, use la [**función LoadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) Para descargar un perfil de usuario cargado **por LoadUserProfile,** llame a la [**función UnloadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)

 

 
