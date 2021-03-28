---
description: El sistema crea un perfil de usuario la primera vez que un usuario inicia sesión en un equipo. En los inicios de sesión posteriores, el sistema carga el perfil del usuario y, a continuación, otros componentes del sistema configuran el entorno del usuario de acuerdo con la información del perfil.
title: Acerca de los perfiles de usuario
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bafd5df7d59787104c2904b4e83c734deaf28708
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984370"
---
# <a name="about-user-profiles"></a>Acerca de los perfiles de usuario

El sistema crea un perfil de usuario la primera vez que un usuario inicia sesión en un equipo. En los inicios de sesión posteriores, el sistema carga el perfil del usuario y, a continuación, otros componentes del sistema configuran el entorno del usuario de acuerdo con la información del perfil.

## <a name="types-of-user-profiles"></a>Tipos de perfiles de usuario

-   [Perfiles de usuario local](local-user-profiles.md). Un perfil de usuario local se crea la primera vez que un usuario inicia sesión en un equipo. El perfil se almacena en el disco duro local del equipo. Los cambios realizados en el perfil de usuario local son específicos para el usuario y para el equipo en el que se realizan los cambios.
-   [Perfiles de usuario móviles](roaming-user-profiles.md). Un perfil de usuario móvil es una copia del perfil local que se copia y se almacena en un recurso compartido de servidor. Este perfil se descarga en cualquier equipo en el que un usuario inicie sesión en una red. Los cambios realizados en un perfil de usuario móvil se sincronizan con la copia del servidor del perfil cuando el usuario cierra la sesión. La ventaja de los perfiles de usuario móviles es que los usuarios no necesitan crear un perfil en cada equipo que usan en una red.
-   [Perfiles de usuario obligatorios](mandatory-user-profiles.md). Un perfil de usuario obligatorio es un tipo de perfil que los administradores pueden usar para especificar la configuración de los usuarios. Solo los administradores del sistema pueden realizar cambios en los perfiles de usuario obligatorios. Los cambios realizados por los usuarios en la configuración del escritorio se pierden cuando el usuario cierra la sesión.
-   [Perfiles de usuario temporales](temporary-user-profiles.md). Cada vez que una condición de error evita que se cargue el perfil del usuario, se emite un perfil temporal. Los perfiles temporales se eliminan al final de cada sesión y los cambios realizados por el usuario en la configuración de escritorio y los archivos se pierden cuando el usuario cierra la sesión. Los perfiles temporales solo están disponibles en equipos que ejecutan Windows 2000 y versiones posteriores.

Un perfil de usuario consta de los siguientes elementos:

-   Subárbol del registro. El subárbol del registro es el archivo NTuser. dat. El sistema carga el subárbol en el inicio de sesión del usuario y se asigna a la clave del registro del **\_ \_ usuario actual HKEY** . El subárbol del registro del usuario mantiene las preferencias y la configuración basadas en el registro del usuario.
-   Un conjunto de carpetas de perfil almacenadas en el sistema de archivos. Los archivos de Perfil de usuario se almacenan en el directorio de **perfiles** , en cada usuario. La carpeta de Perfil de usuario es un contenedor de aplicaciones y otros componentes del sistema para rellenar con subcarpetas y datos por usuario, como documentos y archivos de configuración. El explorador de Windows usa las carpetas de perfiles de usuario exhaustivamente para tales elementos como el escritorio del usuario, el menú **Inicio** y la carpeta **documentos** .

Los perfiles de usuario proporcionan las siguientes ventajas:

-   Cuando el usuario inicia sesión en un equipo, el sistema utiliza la misma configuración que estaba en uso cuando el usuario cerró la sesión por última vez.
-   Al compartir un equipo con otros usuarios, cada usuario recibe su escritorio personalizado después de iniciar sesión.
-   La configuración del perfil de usuario es exclusiva de cada usuario. Otros usuarios no pueden tener acceso a la configuración. Los cambios realizados en el perfil de un usuario no afectan a otros usuarios ni a los perfiles de otros usuarios.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>Iconos de Perfil de usuario en Windows 7 y versiones posteriores

En Windows 7 o versiones posteriores, cada perfil de usuario tiene una imagen asociada que se presenta como un icono de usuario. Estos iconos se muestran a los usuarios en el elemento del panel de control **cuentas de usuario** y en su subpágina **administrar cuentas** . Los archivos de imagen del invitado predeterminado y las cuentas de usuario predeterminadas también aparecen aquí si tiene derechos de acceso de administrador.

> [!Note]  
> Se tiene acceso a la subpágina **administrar cuentas** a través del vínculo **administrar otra cuenta** en el panel de control **cuentas de usuario** .

 

-   % ProgramData% \\ imágenes de la cuenta de usuario de Microsoft \\ \\Guest.bmp
-   % ProgramData% \\ imágenes de la cuenta de usuario de Microsoft \\ \\User.bmp

La imagen del icono del usuario se almacena en la \\ carpeta temporal local% SystemDrive% users \\ <username> \\ AppData \\ \\ como <username> . bmp. Los caracteres de barra diagonal ( \\ ) se convierten en caracteres de signo más (+). Por ejemplo, el \\ usuario del dominio se convierte en dominio + usuario.

El archivo de imagen aparece en la carpeta **temporal** del usuario:

-   Una vez que el usuario completa la instalación inicial del sistema (OOBE).
-   Cuando el usuario inicia por primera vez el elemento de panel de control de **cuentas de usuario** .
-   Cuando el usuario llega a la subpágina **administrar cuentas** del elemento de panel de control **cuentas de usuario** . Además, se muestran iconos para todos los demás usuarios del equipo.

Esas instancias son las únicas veces en las que se crean o actualizan las imágenes. Por lo tanto, hay varias advertencias que se deben tener en cuenta al utilizar la ubicación de la carpeta **temporal** mediante programación:

1.  No se garantiza que el icono del usuario esté presente. Si el usuario elimina el archivo. bmp, por ejemplo, de forma manual o a través de una utilidad que elimine los archivos temporales, ese icono de usuario no se vuelve a crear automáticamente hasta que el usuario inicia el elemento del panel de control **cuentas de usuario** o la subpágina **administrar cuentas** .

2.  Es posible que los iconos de usuario de otros usuarios del equipo no estén presentes en la carpeta **temporal** del usuario que ha iniciado sesión actualmente. Por ejemplo, si el usuario A crea el usuario B a través del elemento del panel de control **cuentas de usuario** , el icono del usuario b se crea en la carpeta **temporal** del usuario a cuando Windows envía el usuario a a la subpágina **administrar cuentas** . Dado que la estructura de directorios no se crea para el usuario B hasta que inicie sesión, la carpeta **temp** del usuario A es la única ubicación en la que se almacena el icono del usuario b. Cuando el usuario B inicia sesión, la única imagen almacenada en la carpeta **temp** del usuario b es suya.

    1.  Para obtener todos los iconos de usuario de los usuarios de un sistema, es posible que las aplicaciones necesiten buscar en el directorio **temporal** de cada usuario.
    2.  Dado que la lista de control de acceso (ACL) de estos directorios **temporales** permite el acceso al sistema, administrador y al usuario actual, las aplicaciones deben elevar el acceso a otros usuarios.

3.  No se garantiza que los iconos de otros usuarios estén actualizados en sus carpetas **temporales** . Si el usuario B actualiza su icono de usuario, el usuario A no verá el cambio hasta que el usuario a tenga acceso a la subpágina **administrar cuentas** . Por lo tanto, si las aplicaciones usan la carpeta **temp** del usuario a para obtener el icono del usuario B, esas aplicaciones pueden obtener un archivo de imagen obsoleto.

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

[Cambio rápido de usuario](fast-user-switching.md)
</dt> </dl>

 

 



