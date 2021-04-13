---
title: Juegos con cuentas de usuario de Least-Privileged
description: En este artículo se describe cómo los desarrolladores de juegos pueden crear juegos de Microsoft Windows que funcionan bien con cuentas de usuario con privilegios mínimos (también conocidas como cuentas de usuario limitado).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c44d94345462fc02ec649c5674ed88c38c12ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487998"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Juegos con cuentas de usuario de Least-Privileged

En este artículo se describe cómo los desarrolladores de juegos pueden crear juegos de Microsoft Windows que funcionan bien con cuentas de usuario con privilegios mínimos (también conocidas como cuentas de usuario limitado).

-   [Introducción](#introduction)
-   [Acceso a archivos para cuentas de usuario de Least-Privileged](#file-access-for-least-privileged-user-accounts)
    -   [Escenario 1: archivos que los usuarios no necesitan ver ni modificar](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Escenario 2: archivos que los usuarios deben ver o modificar](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Acceso al registro para cuentas de usuario de Least-Privileged](#registry-access-for-least-privileged-user-accounts)
-   [Aplicar revisiones con cuentas de usuario de Least-Privileged](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introducción

Windows administra sus usuarios con cuentas. En la actualidad, más del 80 por ciento de los usuarios del equipo en casa comparten su equipo con otros miembros de la familia. Cuando varios usuarios comparten un equipo Windows, se crean varias cuentas de usuario y cada usuario inicia sesión con una cuenta individual para tener acceso al equipo. Con el mayor conocimiento de la seguridad, más personas trabajan con sus equipos con cuentas de usuario con privilegios mínimos, también conocidas como cuentas de usuario limitado, que no tienen control total sobre el sistema. Normalmente, las cuentas de administrador tienen acceso sin restricciones a todas las partes del equipo. Esto puede afectar al funcionamiento de los juegos basados en Windows.

Hay otras ventajas para los desarrolladores de juegos que escriben sus juegos para trabajar con cuentas de usuario con privilegios mínimos. En Windows Vista y versiones posteriores, se aplican las cuentas de usuario con privilegios mínimos, lo que significa que cada cuenta del sistema, con la excepción del administrador local, es una cuenta de usuario con privilegios mínimos. Esto afectará a la forma en que los juegos que no siguen la directriz (aplicaciones heredadas) se ejecutan en Windows Vista y versiones posteriores. Por ejemplo, cuando una aplicación intenta escribir en una carpeta o un valor del registro para el que no tiene permiso, la escritura del archivo se redirige a un almacén de archivos virtual para el usuario. Este almacén de archivos virtual residirá en una carpeta en la que el usuario tenga acceso de escritura. Es posible que este comportamiento no parezca tan catastrófico como la causa del error en el intento de escritura. sin embargo, las aplicaciones que crean archivos virtualizados pueden confundir a los usuarios, ya que los archivos no se escribirán en la ubicación que esperan los usuarios. Por ejemplo, los juegos que escriben archivos de puntuación alta en la misma carpeta que la carpeta ejecutable escribirán estos archivos en una carpeta virtualizada en su lugar. Por lo tanto, un usuario no puede ver la puntuación máxima que ha conseguido otro usuario porque cada usuario tiene un almacén de archivos virtualizado independiente.

Los juegos que siguen las instrucciones de este artículo se ejecutarán con cuentas de usuario con privilegios mínimos y, por consiguiente, mantendrán la compatibilidad con Windows Vista y versiones posteriores.

## <a name="file-access-for-least-privileged-user-accounts"></a>Acceso a archivos para cuentas de usuario de Least-Privileged

Windows admite dos sistemas de archivos: FAT32 y NTFS. FAT32 es un sistema de archivos heredado que solo se admite por compatibilidad con versiones anteriores; NTFS admite permisos de archivo más eficaces y sólidos. El uso de NTFS se está expandiendo a medida que los distribuidores envían nuevos equipos con Windows preinstalado en una unidad de disco duro con particiones NTFS. En un sistema Windows XP basado en NTFS, los usuarios con cuentas de usuario con privilegios mínimos solo tienen acceso limitado a varias carpetas. Sin embargo, tendrán acceso completo en un sistema de Windows XP basado en FAT32.

En la tabla siguiente se muestra la ubicación predeterminada de estas carpetas y sus permisos.



| Ruta                                               | Contenido de la carpeta              | Lectura | Escritura | Crear/Eliminar |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | El sistema operativo Windows | X    |       |               |
| <Drive>: \\ Archivos de programa                      | Archivos de aplicación ejecutable | X    |       |               |
| <Drive>: \\ Documents and Settings \\ nombre de usuario\* | Archivos de cada usuario            | X    | X     | X             |
| <Drive>: \\ Documentos y configuraciones \\ todos los usuarios  | Todos los archivos de usuario               | X    | X     | X             |



 

\* Username es el nombre de inicio de sesión del usuario.

En una cuenta de usuario con privilegios mínimos, puede leer, escribir, crear y eliminar archivos en cualquier carpeta: Documents and Settings \\ nombre de usuario o Documents and Settings \\ All Users.

Esto significa que no debe colocar Save Games en \\ los archivos de programa, en lugar de hacerlo en una subcarpeta de \\ Mis documentos. Además, no debe colocar datos de aplicación temporales en \\ archivos de programa o en \\ Mis documentos, sino que debe colocarse en la carpeta de datos de la aplicación (CSIDL \_ local \_ AppData).

Más concretamente, hay dos escenarios que debe controlar cada juego:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Escenario 1: archivos que los usuarios no necesitan ver ni modificar

Un ejemplo típico sería el archivo de configuración del juego, los archivos temporales y los archivos de la memoria caché del juego. Normalmente, estos archivos se conservan en la carpeta datos de la aplicación. Para obtener esta ruta de acceso a la carpeta, llame a la función [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ AppData o CSIDL \_ local \_ AppData, tal y como se muestra en el ejemplo de código siguiente.

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

La diferencia entre las carpetas de datos de aplicaciones locales y móviles es que en Windows 2000 y Windows XP, el contenido móvil se copia en y desde el servidor durante el proceso de inicio y cierre de sesión, mientras que el contenido local no lo es. Para la mayoría de los juegos, los datos de aplicaciones locales son suficientes.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Escenario 2: archivos que los usuarios deben ver o modificar

Un ejemplo típico sería el de los archivos de juego guardados de un usuario. Almacene los archivos en la carpeta de documentos del usuario para que sean fácilmente visibles para el usuario. Una aplicación obtiene la ruta de acceso de la carpeta de documentos del usuario mediante una llamada a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ personal, como se muestra en el ejemplo de código siguiente:

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

En ocasiones, es posible que un juego necesite almacenar archivos que todos los usuarios están diseñados para ver y usar. Un ejemplo es el registro de puntuación alto, donde todos los usuarios escriben en el mismo archivo de registro para que las puntuaciones altas se mantengan en todo el sistema en lugar de una puntuación alta independiente para cada usuario. En otros ejemplos se descargan mapas, misiones y modificaciones de juegos. Si se comparten, solo un usuario tiene que descargarlas en lugar de todos los usuarios. En este escenario, use la carpeta de documentos en la carpeta de perfil compartido, como se muestra en el código siguiente.

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

## <a name="registry-access-for-least-privileged-user-accounts"></a>Acceso al registro para cuentas de usuario de Least-Privileged

Es habitual que las aplicaciones usen el registro de Windows para almacenar información. Al igual que el acceso a archivos, el administrador y las cuentas de usuario con privilegios mínimos no tienen el mismo permiso en el registro. En el caso de las cuentas de usuario con privilegios mínimos, todo el nodo de la \_ máquina local HKEY \_ es de solo lectura. Por ejemplo, un juego puede leer la información de configuración predeterminada, pero no puede escribir información nueva en este nodo. Por lo tanto, los juegos que se ejecutan en modo de usuario con privilegios mínimos que necesitan escribir en el registro deberán usar el \_ nodo de usuario actual HKEY \_ para almacenar información por usuario, como se muestra en el código siguiente.

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

Merece la pena mencionar que, durante la instalación, la información del registro debe escribirse en el \_ equipo local HKEY \_ , no en el \_ \_ usuario actual. Esto se debe a que la persona que ejecuta la instalación es normalmente un administrador y puede que no sea la única persona que utiliza el programa. En esta situación, la escritura en HKEY \_ Current \_ User hace que la información no esté disponible para otros usuarios. Esto no suele ser un problema, ya que la información escrita en el registro durante la instalación es la configuración predeterminada y la configuración que se aplica a todos los usuarios del programa.

Al desinstalar el juego, es necesario realizar un esfuerzo adicional para quitar todos los valores que el juego ha escrito en el registro. Dado que el desinstalador es ejecutado por una persona, normalmente el administrador, simplemente eliminando la información relevante en HKEY \_ local \_ Machine y HKEY \_ Current \_ User no quitará los valores de otros usuarios. Una manera de quitar la información por usuario en el registro es enumerar la \_ raíz del subárbol del registro HKEY users. Cada subclave de HKEY \_ users corresponde al \_ \_ subárbol del usuario HKEY actual para un usuario determinado del sistema. Al enumerar \_ los usuarios de HKEY y quitar la información específica del juego en cada subclave, el desinstalador puede garantizar que no quede información.

## <a name="patching-with-least-privileged-user-accounts"></a>Aplicar revisiones con cuentas de usuario de Least-Privileged

La revisión de un juego implica actualizar los archivos del juego. Por lo tanto, normalmente es necesario tener acceso de escritura a la carpeta de programas del juego. La aplicación de revisiones a un juego es un proceso sencillo cuando lo hace un administrador porque tienen acceso sin restricciones a la carpeta de programas del juego. Por el contrario, tradicionalmente ha sido difícil, si no imposible, para un usuario con menos privilegios para aplicar revisiones a los juegos debido a la restricción de acceso. Ahora, se ha mejorado [Windows Installer](/windows/desktop/Msi/windows-installer-portal) para hacer posible la revisión de la cuenta de usuario con privilegios mínimos. Para aprovechar esta característica, se recomienda que los juegos utilicen Windows Installer para la instalación y la revisión.

A partir de Windows Installer 3,0, los usuarios con menos privilegios pueden aplicar las revisiones de aplicación cuando se cumplen determinadas condiciones. Estas condiciones son:

-   La aplicación se instaló con Windows Installer 3,0.
-   La aplicación se instaló originalmente por equipo.
-   La aplicación se instala desde un medio extraíble, como un CD-ROM o un disco de vídeo digital (DVD).
-   Las revisiones están firmadas digitalmente por un certificado identificado por el paquete del instalador original (archivo. msi).
-   Las revisiones se pueden validar con la firma digital.
-   El paquete del instalador original no ha deshabilitado la revisión de la cuenta de usuario con privilegios mínimos.
-   El administrador del sistema no ha deshabilitado la revisión de cuentas de usuario con privilegios mínimos a través de la Directiva del sistema.

Normalmente, un usuario con privilegios mínimos no puede modificar los archivos de programa de un juego. Sin embargo, cuando se cumplen las condiciones anteriores y la revisión de LUA está habilitada, Windows Installer puede actualizar los archivos del juego para que el usuario obtenga la versión más reciente.

> [!Note]  
> La información contenida en este artículo se relaciona con el producto de software de versión preliminar, que puede modificarse sustancialmente antes de la primera versión comercial. En consecuencia, es posible que la información no describa o refleje con precisión el producto de software cuando se lance por primera vez. Este artículo se proporciona solo con fines informativos y Microsoft no otorga ninguna garantía, ni expresa ni implícita, con respecto a este artículo o la información que contiene.

 

 

 