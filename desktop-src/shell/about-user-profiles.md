---
description: El sistema crea un perfil de usuario la primera vez que un usuario inicia sesión en un equipo. En los inicios de sesión posteriores, el sistema carga el perfil del usuario y, a continuación, otros componentes del sistema configuran el entorno del usuario según la información del perfil.
title: Acerca de los perfiles de usuario
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cc6715a63c86913d5a525805e6178b3230505d0b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879541"
---
# <a name="about-user-profiles"></a>Acerca de los perfiles de usuario

El sistema crea un perfil de usuario la primera vez que un usuario inicia sesión en un equipo. En los inicios de sesión posteriores, el sistema carga el perfil del usuario y, a continuación, otros componentes del sistema configuran el entorno del usuario según la información del perfil.

## <a name="types-of-user-profiles"></a>Tipos de perfiles de usuario

-   [Perfiles de usuario local.](local-user-profiles.md) Se crea un perfil de usuario local la primera vez que un usuario inicia sesión en un equipo. El perfil se almacena en el disco duro local del equipo. Los cambios realizados en el perfil de usuario local son específicos del usuario y del equipo en el que se realizan los cambios.
-   [Perfiles de usuario móviles](roaming-user-profiles.md). Un perfil de usuario móvil es una copia del perfil local que se copia en un recurso compartido de servidor y se almacena en este. Este perfil se descarga en cualquier equipo en el que un usuario inicie sesión en una red. Los cambios realizados en un perfil de usuario móvil se sincronizan con la copia del servidor del perfil cuando el usuario cierra la sesión. La ventaja de los perfiles de usuario móviles es que los usuarios no necesitan crear un perfil en cada equipo que usan en una red.
-   [Perfiles de usuario obligatorios.](mandatory-user-profiles.md) Un perfil de usuario obligatorio es un tipo de perfil que los administradores pueden usar para especificar la configuración de los usuarios. Solo los administradores del sistema pueden realizar cambios en los perfiles de usuario obligatorios. Los cambios realizados por los usuarios en la configuración de escritorio se pierden cuando el usuario cierra la sesión.
-   [Perfiles de usuario temporales](temporary-user-profiles.md). Se emite un perfil temporal cada vez que una condición de error impide que se cargue el perfil del usuario. Los perfiles temporales se eliminan al final de cada sesión y los cambios realizados por el usuario en la configuración de escritorio y los archivos se pierden cuando el usuario cierra la sesión. Los perfiles temporales solo están disponibles en equipos que ejecutan Windows 2000 y versiones posteriores.

Un perfil de usuario consta de los siguientes elementos:

-   Un subárbol del Registro. El subárbol del Registro es el archivo NTuser.dat. El sistema carga el subárbol en el inicio de sesión del usuario y se asigna a la clave del Registro **HKEY \_ CURRENT \_ USER.** El subárbol del Registro del usuario mantiene las preferencias y la configuración basadas en el registro del usuario.
-   Conjunto de carpetas de perfil almacenadas en el sistema de archivos. Los archivos de perfil de usuario se almacenan en **el directorio Perfiles,** en una carpeta por usuario. La carpeta de perfil de usuario es un contenedor para que las aplicaciones y otros componentes del sistema se rellenen con subcarpetas y datos por usuario, como documentos y archivos de configuración. Windows El Explorador usa las carpetas de perfil de usuario ampliamente para elementos como el escritorio del usuario, **el** menú Inicio y la **carpeta** Documentos.

Los perfiles de usuario proporcionan las siguientes ventajas:

-   Cuando el usuario inicia sesión en un equipo, el sistema usa la misma configuración que estaba en uso cuando el usuario inició sesión por última vez.
-   Al compartir un equipo con otros usuarios, cada usuario recibe su escritorio personalizado después de iniciar sesión.
-   Configuración en el perfil de usuario son únicos para cada usuario. Otros usuarios no pueden acceder a la configuración. Los cambios realizados en el perfil de un usuario no afectan a los perfiles de otros usuarios u otros usuarios.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>Iconos de perfil de usuario en Windows 7 y versiones posteriores

En Windows 7 o posterior, cada perfil de usuario tiene una imagen asociada presentada como un icono de usuario. Estos iconos aparecen a los usuarios en el elemento **De Panel de control** y su **subpágina Administrar** cuentas. Los archivos de imagen de las cuentas de invitado y de usuario predeterminadas también aparecen aquí si tiene derechos de acceso de administrador.

> [!Note]  
> Se **tiene acceso a la**  subpágina Administrar cuentas a través del vínculo Administrar otra cuenta en **el** Panel de control usuario.

 

-   %ProgramData% \\ Microsoft User Account Pictures \\ \\Guest.bmp
-   %ProgramData% \\ Microsoft User Account Pictures \\ \\User.bmp

La imagen de icono del usuario se almacena en la carpeta %SystemDrive% Users username AppData Local Temp como nombre de \\ \\ &lt; &gt; \\ usuario \\ \\ &lt; &gt;.bmp. Los caracteres de barra diagonal ( \\ ) se convierten en más caracteres de signo (+). Por ejemplo, el \\ usuario DE DOMINIO se convierte en DOMINIO+usuario.

El archivo de imagen aparece en la carpeta **Temp del** usuario:

-   Una vez que el usuario complete la configuración inicial del sistema (OOBE).
-   La primera vez que el usuario inicia el elemento **cuentas** Panel de control usuario.
-   Cuando el usuario va a la subpágina **Administrar** cuentas del elemento **Cuentas** Panel de control usuario. Además, se muestran iconos para todos los demás usuarios del equipo.

Esas instancias son las únicas veces que se crean o actualizan las imágenes. Por lo tanto, hay varias advertencias que se deben tener en cuenta al usar la **ubicación de** la carpeta Temp mediante programación:

1.  No se garantiza que el icono del usuario esté presente. Si el usuario elimina el archivo .bmp, por ejemplo manualmente o a través de una utilidad que elimina archivos temporales, ese icono de usuario no se vuelve a crear automáticamente hasta que el usuario inicia el elemento Cuentas de usuario **Panel de control** o la  subpágina Administrar cuentas.

2.  Es posible que los iconos de usuario de otros usuarios del equipo no se encuentran en la carpeta Temp del usuario que ha iniciado **sesión** actualmente. Por ejemplo, si el usuario **A** crea el usuario B a través del elemento Cuentas  de usuario Panel de control, el icono del usuario B se crea en la carpeta Temp del usuario A cuando Windows envía el usuario A a la subpágina Administrar cuentas.  Dado que la estructura de directorios no se crea para  el usuario B hasta que inicia sesión, la carpeta Temp del usuario A es la única ubicación donde se almacena el icono del usuario B. Cuando el usuario B inicia sesión, la única imagen almacenada en la carpeta **Temp** del usuario B es la suya propia.

    1.  Para obtener todos los iconos de usuario para los usuarios de un sistema, es posible que las aplicaciones deba buscar en el directorio Temp de **cada** usuario.
    2.  Dado que la lista de  control de acceso (ACL) de estos directorios temporales permite el acceso a SYSTEM, Administrator y al usuario actual, las aplicaciones deben elevarse al acceso de otros usuarios.

3.  No se garantiza que los iconos de otros usuarios estén actualizados en sus **carpetas** Temp. Si el usuario B actualiza su icono de usuario, el usuario A no verá el cambio hasta que el usuario A acceda a la subpágina **Administrar** cuentas. Por lo tanto, si las aplicaciones usan la carpeta **Temp** del usuario A para obtener el icono del usuario B, esas aplicaciones pueden obtener un archivo de imagen no actualizado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfiles de usuario local](local-user-profiles.md)
</dt> <dt>

[Perfiles de usuario móviles](roaming-user-profiles.md)
</dt> <dt>

[Perfiles de usuario obligatorios](mandatory-user-profiles.md)
</dt> <dt>

[Perfiles de usuario temporales](temporary-user-profiles.md)
</dt> <dt>

[Directorio de perfiles](profiles-directory.md)
</dt> <dt>

[Variables de entorno de usuario](user-environment-variables.md)
</dt> <dt>

[Cambio rápido de usuarios](fast-user-switching.md)
</dt> </dl>

 

 



