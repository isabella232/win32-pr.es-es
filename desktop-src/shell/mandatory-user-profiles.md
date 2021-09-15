---
description: Un perfil de usuario obligatorio es un tipo especial de perfil de usuario móvil preconfigurado que los administradores pueden usar para especificar la configuración de los usuarios.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466786"
---
# <a name="mandatory-user-profiles"></a>Perfiles de usuario obligatorios

Un perfil de usuario obligatorio es un [](roaming-user-profiles.md) tipo especial de perfil de usuario móvil preconfigurado que los administradores pueden usar para especificar la configuración de los usuarios. Con los perfiles de usuario obligatorios, un usuario puede modificar su escritorio, pero los cambios no se guardan cuando el usuario cierra la sesión. La próxima vez que el usuario inicie sesión, se descargará el perfil de usuario obligatorio creado por el administrador. Hay dos tipos de perfiles obligatorios: perfiles obligatorios *normales* y *perfiles* superceptos.

Los perfiles de usuario se convierten en perfiles obligatorios cuando el administrador cambia el nombre del archivo NTuser.dat (el subárbol del Registro) del servidor a NTuser.man. La extensión .man hace que el perfil de usuario sea un perfil de solo lectura.

Los perfiles de usuario *se vuelven superceptorosos* cuando el nombre de la carpeta de la ruta de acceso del perfil termina en .man; por ejemplo, \\ \\ el recurso compartido de \\ servidor \\ mandatoryprofile.man \\ .

Los perfiles de usuario superceptibles son similares a los perfiles obligatorios normales, con la excepción de que los usuarios que tienen perfiles superceptibles no pueden iniciar sesión cuando el servidor que almacena el perfil obligatorio no está disponible. Los usuarios con perfiles obligatorios normales pueden iniciar sesión con la copia almacenada en caché localmente del perfil obligatorio.

Solo los administradores del sistema pueden realizar cambios en los perfiles de usuario obligatorios.

 

 



