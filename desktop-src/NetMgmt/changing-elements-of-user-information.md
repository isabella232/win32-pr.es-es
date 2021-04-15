---
title: Cambiar elementos de información de usuario
description: Las funciones de administración de red proporcionan una variedad de niveles de información para ayudar a cambiar la información del usuario.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676391"
---
# <a name="changing-elements-of-user-information"></a>Cambiar elementos de información de usuario

Las funciones de administración de red proporcionan una variedad de niveles de información para ayudar a cambiar la información del usuario. Algunos niveles requieren privilegios administrativos para ejecutarse correctamente. Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

En el código de ejemplo de este tema se muestra cómo cambiar varios elementos de información de usuario mediante una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El código utiliza varias estructuras de información de administración de redes.

Al cambiar la información del usuario, es mejor usar el nivel específico para esa parte de la información. Esto evita el restablecimiento accidental de información no relacionada cuando se utilizan los valores de nivel inferior.

En los siguientes ejemplos de código se muestra la configuración de algunos de los niveles más usados:

-   [Establecimiento de la contraseña de usuario, nivel 1003](#setting-the-user-password-level-1003)
-   [Establecimiento del privilegio de usuario, nivel 1005](#setting-the-user-privilege-level-1005)
-   [Configuración del directorio principal de usuario, nivel 1006](#setting-the-user-home-directory-level-1006)
-   [Configuración del campo de comentario de usuario, nivel 1007](#setting-the-user-comment-field-level-1007)
-   [Establecer las marcas de usuario, nivel 1008](#setting-the-user-flags-level-1008)
-   [Establecer la ruta de acceso del script de usuario, nivel 1009](#setting-the-user-script-path-level-1009)
-   [Establecimiento de las marcas de autoridad de usuario, nivel 1010](#setting-the-user-authority-flags-level-1010)
-   [Establecer el nombre completo del usuario, nivel 1011](#setting-the-user-full-name-level-1011)

Todos los fragmentos de código suponen que el usuario ha definido la Directiva de compilación Unicode e incluido los archivos de encabezado apropiados del SDK, como se indica a continuación:


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a>Establecimiento de la contraseña de usuario, nivel 1003

El siguiente fragmento de código muestra cómo establecer la contraseña de un usuario en un valor conocido con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El [**tema \_ información \_ de usuario 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contiene información adicional.


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a>Establecimiento del privilegio de usuario, nivel 1005

En el fragmento de código siguiente se muestra cómo especificar el nivel de privilegio asignado a un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El [**tema \_ información \_ de usuario 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contiene información adicional. Para obtener más información sobre los privilegios de cuenta, vea [privilegios](/windows/desktop/SecAuthZ/privileges) y [constantes de autorización](/windows/desktop/SecAuthZ/authorization-constants).


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a>Configuración del directorio principal de usuario, nivel 1006

En el fragmento de código siguiente se muestra cómo especificar la ruta de acceso del directorio principal de un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El directorio puede ser una ruta de acceso codificada de forma rígida o una ruta de acceso Unicode válida. El [**tema \_ información \_ de usuario 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contiene información adicional.


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a>Configuración del campo de comentario de usuario, nivel 1007

En el fragmento de código siguiente se muestra cómo asociar un comentario a un usuario mediante una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El [**tema \_ información \_ de usuario 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contiene información adicional.


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a>Establecer las marcas de usuario, nivel 1008

En el fragmento de código siguiente se muestra cómo establecer marcas de usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El [**tema \_ información \_ de usuario 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contiene una lista de valores válidos para las marcas y una descripción de cada marca.

Tenga en cuenta que la \_ marca de la secuencia de comandos de la instalación de Windows NT, windows 2000, Windows XP y LAN Manager debe estar establecida. Si intenta establecer otras marcas sin establecer \_ el script de marca de instalación en estas redes, se producirá un error en la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a>Establecer la ruta de acceso del script de usuario, nivel 1009

En el fragmento de código siguiente se muestra cómo establecer la ruta de acceso del archivo de script de inicio de sesión de un usuario determinado con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El archivo de script puede ser un. Archivo CMD,. Archivo EXE o. Archivo BAT. La cadena también puede ser null. El [**tema \_ información \_ de usuario 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contiene información adicional.


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a>Establecimiento de las marcas de autoridad de usuario, nivel 1010

El siguiente fragmento de código muestra cómo establecer las marcas de privilegios de operador para un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El [**tema \_ información \_ de usuario 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contiene una lista de valores válidos para las marcas y una descripción de cada marca.


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a>Establecer el nombre completo del usuario, nivel 1011

El siguiente fragmento de código muestra cómo establecer el nombre completo de un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . El [**tema \_ información \_ de usuario 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contiene información adicional.


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 