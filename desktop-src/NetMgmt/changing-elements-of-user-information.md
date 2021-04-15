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
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="e3977-103">Cambiar elementos de información de usuario</span><span class="sxs-lookup"><span data-stu-id="e3977-103">Changing Elements of User Information</span></span>

<span data-ttu-id="e3977-104">Las funciones de administración de red proporcionan una variedad de niveles de información para ayudar a cambiar la información del usuario.</span><span class="sxs-lookup"><span data-stu-id="e3977-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="e3977-105">Algunos niveles requieren privilegios administrativos para ejecutarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3977-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="e3977-106">Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="e3977-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="e3977-107">En el código de ejemplo de este tema se muestra cómo cambiar varios elementos de información de usuario mediante una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-108">El código utiliza varias estructuras de información de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="e3977-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="e3977-109">Al cambiar la información del usuario, es mejor usar el nivel específico para esa parte de la información.</span><span class="sxs-lookup"><span data-stu-id="e3977-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="e3977-110">Esto evita el restablecimiento accidental de información no relacionada cuando se utilizan los valores de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e3977-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="e3977-111">En los siguientes ejemplos de código se muestra la configuración de algunos de los niveles más usados:</span><span class="sxs-lookup"><span data-stu-id="e3977-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="e3977-112">Establecimiento de la contraseña de usuario, nivel 1003</span><span class="sxs-lookup"><span data-stu-id="e3977-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="e3977-113">Establecimiento del privilegio de usuario, nivel 1005</span><span class="sxs-lookup"><span data-stu-id="e3977-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="e3977-114">Configuración del directorio principal de usuario, nivel 1006</span><span class="sxs-lookup"><span data-stu-id="e3977-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="e3977-115">Configuración del campo de comentario de usuario, nivel 1007</span><span class="sxs-lookup"><span data-stu-id="e3977-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="e3977-116">Establecer las marcas de usuario, nivel 1008</span><span class="sxs-lookup"><span data-stu-id="e3977-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="e3977-117">Establecer la ruta de acceso del script de usuario, nivel 1009</span><span class="sxs-lookup"><span data-stu-id="e3977-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="e3977-118">Establecimiento de las marcas de autoridad de usuario, nivel 1010</span><span class="sxs-lookup"><span data-stu-id="e3977-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="e3977-119">Establecer el nombre completo del usuario, nivel 1011</span><span class="sxs-lookup"><span data-stu-id="e3977-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="e3977-120">Todos los fragmentos de código suponen que el usuario ha definido la Directiva de compilación Unicode e incluido los archivos de encabezado apropiados del SDK, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e3977-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


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



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="e3977-121">Establecimiento de la contraseña de usuario, nivel 1003</span><span class="sxs-lookup"><span data-stu-id="e3977-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="e3977-122">El siguiente fragmento de código muestra cómo establecer la contraseña de un usuario en un valor conocido con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-123">El [**tema \_ información \_ de usuario 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contiene información adicional.</span><span class="sxs-lookup"><span data-stu-id="e3977-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


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



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="e3977-124">Establecimiento del privilegio de usuario, nivel 1005</span><span class="sxs-lookup"><span data-stu-id="e3977-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="e3977-125">En el fragmento de código siguiente se muestra cómo especificar el nivel de privilegio asignado a un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-126">El [**tema \_ información \_ de usuario 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contiene información adicional.</span><span class="sxs-lookup"><span data-stu-id="e3977-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="e3977-127">Para obtener más información sobre los privilegios de cuenta, vea [privilegios](/windows/desktop/SecAuthZ/privileges) y [constantes de autorización](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="e3977-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


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



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="e3977-128">Configuración del directorio principal de usuario, nivel 1006</span><span class="sxs-lookup"><span data-stu-id="e3977-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="e3977-129">En el fragmento de código siguiente se muestra cómo especificar la ruta de acceso del directorio principal de un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-130">El directorio puede ser una ruta de acceso codificada de forma rígida o una ruta de acceso Unicode válida.</span><span class="sxs-lookup"><span data-stu-id="e3977-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="e3977-131">El [**tema \_ información \_ de usuario 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contiene información adicional.</span><span class="sxs-lookup"><span data-stu-id="e3977-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


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



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="e3977-132">Configuración del campo de comentario de usuario, nivel 1007</span><span class="sxs-lookup"><span data-stu-id="e3977-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="e3977-133">En el fragmento de código siguiente se muestra cómo asociar un comentario a un usuario mediante una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-134">El [**tema \_ información \_ de usuario 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contiene información adicional.</span><span class="sxs-lookup"><span data-stu-id="e3977-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


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



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="e3977-135">Establecer las marcas de usuario, nivel 1008</span><span class="sxs-lookup"><span data-stu-id="e3977-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="e3977-136">En el fragmento de código siguiente se muestra cómo establecer marcas de usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-137">El [**tema \_ información \_ de usuario 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contiene una lista de valores válidos para las marcas y una descripción de cada marca.</span><span class="sxs-lookup"><span data-stu-id="e3977-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="e3977-138">Tenga en cuenta que la \_ marca de la secuencia de comandos de la instalación de Windows NT, windows 2000, Windows XP y LAN Manager debe estar establecida.</span><span class="sxs-lookup"><span data-stu-id="e3977-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="e3977-139">Si intenta establecer otras marcas sin establecer \_ el script de marca de instalación en estas redes, se producirá un error en la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


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



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="e3977-140">Establecer la ruta de acceso del script de usuario, nivel 1009</span><span class="sxs-lookup"><span data-stu-id="e3977-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="e3977-141">En el fragmento de código siguiente se muestra cómo establecer la ruta de acceso del archivo de script de inicio de sesión de un usuario determinado con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-142">El archivo de script puede ser un. Archivo CMD,. Archivo EXE o. Archivo BAT.</span><span class="sxs-lookup"><span data-stu-id="e3977-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="e3977-143">La cadena también puede ser null.</span><span class="sxs-lookup"><span data-stu-id="e3977-143">The string can also be null.</span></span> <span data-ttu-id="e3977-144">El [**tema \_ información \_ de usuario 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contiene información adicional.</span><span class="sxs-lookup"><span data-stu-id="e3977-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


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



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="e3977-145">Establecimiento de las marcas de autoridad de usuario, nivel 1010</span><span class="sxs-lookup"><span data-stu-id="e3977-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="e3977-146">El siguiente fragmento de código muestra cómo establecer las marcas de privilegios de operador para un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-147">El [**tema \_ información \_ de usuario 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contiene una lista de valores válidos para las marcas y una descripción de cada marca.</span><span class="sxs-lookup"><span data-stu-id="e3977-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


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



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="e3977-148">Establecer el nombre completo del usuario, nivel 1011</span><span class="sxs-lookup"><span data-stu-id="e3977-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="e3977-149">El siguiente fragmento de código muestra cómo establecer el nombre completo de un usuario con una llamada a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3977-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="e3977-150">El [**tema \_ información \_ de usuario 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contiene información adicional.</span><span class="sxs-lookup"><span data-stu-id="e3977-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


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



 

 