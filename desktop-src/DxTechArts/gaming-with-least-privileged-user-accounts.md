---
title: Juegos con cuentas Least-Privileged usuario
description: En este artículo se describe cómo los desarrolladores de juegos pueden crear juegos de Microsoft Windows que funcionan bien con cuentas de usuario con menos privilegios (también conocidas como cuentas de usuario limitado).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db15302eb856aaeb05c68fae4746110dd42cb4a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887383"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Juegos con cuentas Least-Privileged usuario

En este artículo se describe cómo los desarrolladores de juegos pueden crear juegos de Microsoft Windows que funcionan bien con cuentas de usuario con menos privilegios (también conocidas como cuentas de usuario limitado).

-   [Introducción](#introduction)
-   [Acceso a archivos para Least-Privileged de usuario](#file-access-for-least-privileged-user-accounts)
    -   [Escenario 1: Archivos que los usuarios no necesitan ver ni modificar](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Escenario 2: Archivos que los usuarios deben ver o modificar](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Acceso al Registro para Least-Privileged de usuario](#registry-access-for-least-privileged-user-accounts)
-   [Aplicación de revisiones con Least-Privileged de usuario](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introducción

Windows administra sus usuarios con cuentas. En la actualidad, más del 80 % de los usuarios del equipo en casa comparten su equipo con otros miembros de la familia. Cuando varios usuarios comparten un Windows, se crean varias cuentas de usuario y cada usuario inicia sesión con una cuenta individual para acceder al equipo. Con el creciente conocimiento de la seguridad, más personas operan sus equipos con cuentas de usuario con menos privilegios, también conocidas como cuentas de usuario limitado, que no tienen control total sobre el sistema. Las cuentas de administrador suelen tener acceso sin restricciones a todas las partes del equipo. Esto puede afectar a cómo funcionan Windows juegos basados en la nube.

Hay ventajas adicionales para los desarrolladores de juegos que escriben sus juegos para trabajar con cuentas de usuario con menos privilegios. En Windows Vista y versiones posteriores, se aplican las cuentas de usuario con menos privilegios, lo que significa que todas las cuentas del sistema, a excepción del administrador local, son una cuenta de usuario con menos privilegios. Esto afectará a cómo se ejecutan los juegos que no siguen las instrucciones (aplicaciones heredadas) en Windows Vista y versiones posteriores. Por ejemplo, cuando una aplicación intenta escribir en una carpeta o un valor del Registro para el que no tiene permiso, la escritura de archivos se redirige a un almacén de archivos virtual para el usuario. Este almacén de archivos virtual residirá en una carpeta en la que el usuario tenga acceso de escritura. Este comportamiento puede no parecer tan catastrófico como un error total en el intento de escritura. sin embargo, las aplicaciones que crean archivos virtualizados pueden confundir a los usuarios porque los archivos no se escribirán en la ubicación esperada por los usuarios. Por ejemplo, los juegos que escriben archivos de puntuación alta en la misma carpeta que la carpeta ejecutable escribirán estos archivos en una carpeta virtualizada en su lugar. Por lo tanto, un usuario no puede ver la puntuación alta lograda por otro usuario porque cada usuario tiene un almacén de archivos virtualizado independiente.

Los juegos que siguen las directrices de este artículo se ejecutarán con cuentas de usuario con menos privilegios y, por tanto, mantendrán la compatibilidad con Windows Vista y versiones posteriores.

## <a name="file-access-for-least-privileged-user-accounts"></a>Acceso a archivos para Least-Privileged de usuario

Windows admite dos sistemas de archivos: FAT32 y NTFS. FAT32 es un sistema de archivos heredado que solo se admite por compatibilidad con versiones anteriores; NTFS admite permisos de archivo más eficaces y sólidos. El uso de NTFS se está expandiendo a medida que los distribuidores están enviando nuevos equipos con Windows preinstalado en una unidad de disco duro con particiones NTFS. En un sistema Windows XP basado en NTFS, los usuarios con cuentas de usuario con menos privilegios solo tienen acceso limitado a varias carpetas. Sin embargo, tendrían acceso completo en un sistema basado en FAT32 Windows XP.

En la tabla siguiente se muestra la ubicación predeterminada de estas carpetas y sus permisos.



| Ruta de acceso                                               | Contenido de la carpeta              | Lectura | Escritura | Crear/Eliminar |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| &lt;Unidad: &gt; \\ Windows                            | El Windows operativo | X    |       |               |
| &lt;Unidad: &gt; \\ Archivos de programa                      | Archivos de aplicación ejecutables | X    |       |               |
| &lt;Unidad: &gt; Documentos y nombre Configuración \\ \\ usuario\* | Archivos de cada usuario            | X    | X     | X             |
| &lt;Unidad: &gt; Documentos y Configuración Todos los \\ \\ usuarios  | Todos los archivos de usuario               | X    | X     | X             |



 

\* Username es el nombre de inicio de sesión del usuario.

En una cuenta de usuario con privilegios mínimos, puede leer, escribir, crear y eliminar archivos en cualquiera de las carpetas: Documentos y Configuración Nombre de usuario o Documentos \\ y Configuración Todos los \\ usuarios.

Esto significa que no debe colocar juegos guardados en archivos de programa, sino que deben ir en una subpágdala \\ \\ en Mis documentos. Además, no debe colocar datos temporales de la aplicación en archivos de programa Mis documentos, sino que se deben colocar en la carpeta Datos de aplicación \\ \\ (CSIDL \_ LOCAL \_ APPDATA).

Más concretamente, hay dos escenarios que cada juego debe controlar:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Escenario 1: Archivos que los usuarios no necesitan ver ni modificar

Un ejemplo típico sería el archivo de configuración del juego, los archivos temporales y los archivos de caché del juego. Normalmente, estos archivos se mantienen en la carpeta Datos de la aplicación. Para obtener esta ruta de acceso de carpeta, llame a la función [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL APPDATA o \_ CSIDL LOCAL APPDATA como se muestra en el \_ ejemplo de código \_ siguiente.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

La diferencia entre las carpetas de datos de aplicación locales y móviles es que en Windows 2000 y Windows XP, el contenido móvil se copia hacia y desde el servidor durante el proceso de inicio y cierre de sesión, mientras que el contenido local no lo es. Para la mayoría de los juegos, los datos de aplicación locales son suficientes.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Escenario 2: Archivos que los usuarios deben ver o modificar

Un ejemplo típico serían los archivos de juego guardados de un usuario. Almacene los archivos en la carpeta de documentos del usuario para que sean fácilmente visibles para el usuario. Una aplicación obtiene la ruta de acceso de la carpeta del documento del usuario mediante una llamada a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL PERSONAL, como se muestra en el \_ ejemplo de código siguiente:

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

En ocasiones, un juego puede necesitar almacenar archivos que todos los usuarios están diseñados para ver y usar. Un ejemplo es el registro de puntuación alta, donde todos los usuarios escriben en el mismo archivo de registro para que las puntuaciones altas se mantengan en todo el sistema en lugar de una puntuación alta independiente para cada usuario. Otros ejemplos son mapas descargados, misiones y modificaciones de juegos. Si se comparten, solo un usuario tiene que descargarlos en lugar de cada usuario. En este escenario, use la carpeta del documento en la carpeta de perfil compartido, como se muestra en el código siguiente.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a>Acceso al Registro para Least-Privileged de usuario

Es habitual que las aplicaciones usen el registro Windows para almacenar información. De forma similar al acceso a archivos, las cuentas de administrador y de usuario con menos privilegios no tienen el mismo permiso para el registro. En el caso de las cuentas de usuario con privilegios mínimos, todo el nodo HKEY \_ LOCAL MACHINE es de solo \_ lectura. Por ejemplo, un juego puede leer la información de configuración predeterminada, pero es posible que no escriba ninguna información nueva en este nodo. Por lo tanto, los juegos que se ejecutan en modo de usuario con privilegios mínimos que necesitan escribir en el Registro tendrán que usar el nodo HKEY CURRENT USER para almacenar información por usuario, como se muestra en el \_ \_ código siguiente.

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

Merece la pena tener en cuenta que durante la instalación, la información del Registro debe escribirse en HKEY \_ LOCAL \_ MACHINE, no en HKEY \_ CURRENT \_ USER. Esto se debe a que la persona que ejecuta la instalación suele ser un administrador y puede que no sea la única persona que use el programa. En esta situación, escribir en HKEY \_ CURRENT USER hace que la información no esté disponible para otros \_ usuarios. Esto no suele ser un problema porque la información escrita en el Registro durante la instalación es la configuración y la configuración predeterminada que se aplican a todos los usuarios del programa.

Al desinstalar el juego, es necesario realizar un esfuerzo adicional para quitar todos los valores que el juego ha escrito en el registro. Dado que el desinstalador lo ejecuta una persona, normalmente el administrador, basta con eliminar la información pertinente en HKEY LOCAL MACHINE y HKEY CURRENT USER no quitará los valores de \_ \_ otros \_ \_ usuarios. Una manera de quitar la información por usuario del Registro es enumerar la raíz del subárbol del Registro HKEY \_ USERS. Cada subclave de HKEY USERS corresponde al subárbol \_ HKEY \_ CURRENT USER para un usuario determinado del \_ sistema. Al enumerar HKEY USERS y quitar la información específica del juego en cada subclave, el desinstalador puede asegurarse de que no se deja \_ información.

## <a name="patching-with-least-privileged-user-accounts"></a>Aplicación de revisiones con Least-Privileged de usuario

La aplicación de revisiones a un juego implica actualizar los archivos del juego. Por lo tanto, normalmente requiere acceso de escritura a la carpeta del programa del juego. Aplicar revisiones a un juego es un proceso sencillo cuando lo hace un administrador porque tienen acceso sin restricciones a la carpeta del programa del juego. Por el contrario, tradicionalmente ha sido difícil, si no imposible, que un usuario con menos privilegios aplicara revisiones a los juegos debido a la restricción de acceso. Ahora, [Windows instalador se](/windows/desktop/Msi/windows-installer-portal) ha mejorado para hacer posible la aplicación de revisiones de cuentas de usuario con privilegios mínimos. Para aprovechar esta característica, se recomienda que los juegos utilicen Windows Installer para la instalación y aplicación de revisiones.

A partir Windows Installer 3.0, los usuarios con menos privilegios pueden aplicar revisiones de aplicación cuando se cumplen ciertas condiciones. Estas condiciones son:

-   La aplicación se instaló mediante Windows Installer 3.0.
-   La aplicación se instaló originalmente por máquina.
-   La aplicación se instala desde medios extraíbles, como cd-ROM o disco de vídeo digital (DVD).
-   Las revisiones están firmadas digitalmente por un certificado identificado por el paquete del instalador original (.msi archivo).
-   Las revisiones se pueden validar con la firma digital.
-   El paquete del instalador original no ha deshabilitado la aplicación de revisiones de cuentas de usuario con privilegios mínimos.
-   El administrador del sistema no ha deshabilitado la aplicación de revisiones de cuentas de usuario con privilegios mínimos a través de la directiva del sistema.

Normalmente, un usuario con menos privilegios no puede modificar los archivos de programa de un juego. Sin embargo, cuando se cumplen las condiciones anteriores y se habilita la aplicación de revisiones de LUA, Windows Installer puede actualizar los archivos del juego para que el usuario tenga la versión más reciente.

> [!Note]  
> La información contenida en este artículo está relacionada con el producto de software de versión previa, que puede modificarse considerablemente antes de su primera versión comercial. En consecuencia, es posible que la información no describa o refleje con precisión el producto de software cuando se lanza por primera vez comercialmente. Este artículo se proporciona solo con fines informativos y Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a este artículo o a la información contenida en él.

 

 

 
