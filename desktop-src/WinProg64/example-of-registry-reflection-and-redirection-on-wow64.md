---
title: Ejemplo de redirección del Registro en WOW64
description: En el código de ejemplo siguiente se muestran las vistas independientes del registro proporcionadas por el redirector del registro en archivos de 64 Windows.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- ejemplos de programación de Windows de 64 bits
- Guía de programación de Windows de 64 bits ejemplos de programación de 64 Windows bits
- Guía de programación de Windows de 64 bits ejemplos de programación de 64 Windows, redirección del Registro en WOW64
- Ejemplo de redirección del registro de 64 bits Windows programación
- Guía de programación de 64 Windows de programación de 64 bits Windows programación , ejemplos Vea ejemplos de la guía de programación de Windows de 64 bits.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83428edb31e53bdd1c70825c7fa5a4d799a36536fa9c17f9ce1c4587ab096048
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680235"
---
# <a name="example-of-registry-redirection-on-wow64"></a>Ejemplo de redirección del Registro en WOW64

En el código de ejemplo siguiente se muestran las vistas independientes del registro proporcionadas por el redirector del registro en archivos de 64 Windows. También muestra cómo se establecen los valores de las claves en función de si una clave se comparte o se redirige. Para obtener más información, vea [Claves del Registro afectadas por WOW64.](shared-registry-keys.md)

Compile el código siguiente por separado para las versiones de 32 y 64 Windows. Ejecute cada archivo ejecutable resultante en archivos ejecutables de 64 Windows y compare la salida. La salida de ejemplo para ambas versiones se muestra debajo del código fuente.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



Cuando se ejecuta la versión de 64 bits del ejemplo, genera la siguiente salida. Los valores de las vistas predeterminadas y alternativas de **HKCR \\ Hello** son los mismos porque esta clave se comparte. Los valores de las otras claves difieren porque se redirigen.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Cuando este ejemplo se ejecuta en estos sistemas operativos, las vistas predeterminadas y alternativas de la clave LocalServer32 tienen el mismo valor. Esto se debe a que la clave LocalServer32 se redirige y *refleja,* lo que hace que su valor se sincronice entre las vistas de 64 bits y 32 bits del Registro en cuanto se cierre el identificador de la clave. La reflexión del Registro se quitó a partir Windows 7. Para obtener más información, vea [Reflexión del Registro.](registry-reflection.md)

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

Cuando se ejecuta la versión de 32 bits del ejemplo, genera la siguiente salida. Para una aplicación de 32 bits, la vista de 64 bits del Registro es la vista alternativa, por lo que los valores se invierten, excepto HKCR Hello, que es una clave \\ compartida.

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

Para examinar el efecto de ejecutar este ejemplo con regedit, inspeccione los valores de las claves siguientes. Tenga en cuenta que las aplicaciones deben evitar el uso de Wow6432Node en rutas de acceso del Registro codificadas de forma hard-coded.

**HKLM \\ SOFTWARE \\ Hola mundo**  
**HKLM \\ SOFTWARE \\ Wow6432Node \\ Hola mundo**  
**HKCR \\ CLSID \\ {000000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ CLSID \\ {000000000-0000-0000-0000-ABCD0000000} \\ InprocServer32**  
**HKCR \\ CLSID \\ {000000000-0000-0000-0000-ABCD0000000} \\ LocalServer32**  
**HKCR \\ Hello HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD0000000} \\ LocalServer32**  
**HKCR \\ Wow6432Node \\ Hello**  


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del Registro](registry-redirector.md)
</dt> <dt>

[Reflexión del Registro](registry-reflection.md)
</dt> </dl>

 

 




