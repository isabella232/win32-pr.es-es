---
title: Funciones de usuario de estación de trabajo y estación de trabajo
description: Las funciones de la estación de trabajo de administración de redes realizan tareas administrativas en una estación de trabajo local o remota.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665865"
---
# <a name="workstation-and-workstation-user-functions"></a>Funciones de usuario de estación de trabajo y estación de trabajo

Las funciones de la estación de trabajo de administración de redes realizan tareas administrativas en una estación de trabajo local o remota. Solo un usuario o aplicación con pertenencia a un grupo de administradores, en un servidor local o remoto, puede realizar tareas administrativas en una estación de trabajo para controlar el funcionamiento, el acceso de usuario y el uso compartido de recursos. Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

A continuación se enumeran las funciones de estación de trabajo.



| Función                                   | Descripción                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | Devuelve información sobre los elementos de configuración de una estación de trabajo. |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | Configura una estación de trabajo.                                               |



 

Las funciones de estación de trabajo permiten el acceso a dos tipos discretos de información de la estación de trabajo:

-   Información del sistema
-   Información específica de la plataforma

Dentro de cada tipo, los datos se clasifican por acceso de seguridad. Los datos a los que se puede tener acceso como invitados son un subconjunto de los datos a los que puede acceder el usuario, que a su vez es un subconjunto de los datos accesibles desde el administrador.

La información de la estación de trabajo está disponible en los siguientes niveles:

-   [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**WKSTA \_ INFO \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**WKSTA \_ INFO \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

Las funciones de usuario de la estación de trabajo de administración de red permiten el acceso a información específica del usuario. La información específica del usuario se separa de la información de la estación de trabajo porque puede haber más de un usuario en una estación de trabajo.

A continuación se enumeran las funciones de usuario de la estación de trabajo.



| Función                                           | Descripción                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Muestra información acerca de todos los usuarios que han iniciado sesión actualmente en la estación de trabajo.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Devuelve información acerca de un usuario que ha iniciado sesión actualmente.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Establece la información específica del usuario para los elementos de configuración de una estación de trabajo. |



 

La información de usuario de la estación de trabajo está disponible en los siguientes niveles:

-   [**Información de usuario de WKSTA \_ \_ \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**Información de usuario de WKSTA \_ \_ \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**Información de usuario de WKSTA \_ \_ \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 