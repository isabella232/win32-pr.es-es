---
title: Ejemplo de redirección del registro en WOW64
description: En el ejemplo de código siguiente se muestran las vistas independientes del registro proporcionadas por el redirector del registro en Windows de 64 bits.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- 'ejemplos 64: programación de Windows de bits'
- Guía de programación de Windows de 64 bits ejemplos de programación de Windows de 64 bits
- Guía de programación de Windows de 64 bits ejemplos de programación de Windows de 64 bits, redirección del registro en WOW64
- ejemplo de redirección del registro 64 programación de Windows de bits
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, ejemplos consulte ejemplos de la guía de programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff37b077137e9802e6716319623fe8e372941500
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104421556"
---
# <a name="example-of-registry-redirection-on-wow64"></a><span data-ttu-id="90ff1-108">Ejemplo de redirección del registro en WOW64</span><span class="sxs-lookup"><span data-stu-id="90ff1-108">Example of Registry Redirection on WOW64</span></span>

<span data-ttu-id="90ff1-109">En el ejemplo de código siguiente se muestran las vistas independientes del registro proporcionadas por el redirector del registro en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="90ff1-109">The following example code demonstrates the separate views of the registry provided by the registry redirector on 64-bit Windows.</span></span> <span data-ttu-id="90ff1-110">También muestra cómo se establecen los valores de las claves dependiendo de si una clave está compartida o redirigida.</span><span class="sxs-lookup"><span data-stu-id="90ff1-110">It also demonstrates how the values of keys are set depending on whether a key is shared or redirected.</span></span> <span data-ttu-id="90ff1-111">Para obtener más información, consulte [claves del registro afectadas por WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="90ff1-111">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>

<span data-ttu-id="90ff1-112">Compile el código siguiente por separado para Windows de 32 y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="90ff1-112">Compile the following code separately for both 32-bit and 64-bit Windows.</span></span> <span data-ttu-id="90ff1-113">Ejecute cada archivo ejecutable resultante en Windows de 64 bits y compare el resultado.</span><span class="sxs-lookup"><span data-stu-id="90ff1-113">Run each resulting executable file on 64-bit Windows and compare the output.</span></span> <span data-ttu-id="90ff1-114">La salida de ejemplo para ambas versiones se muestra debajo del código fuente.</span><span class="sxs-lookup"><span data-stu-id="90ff1-114">Sample output for both versions is listed below the source code.</span></span>


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



<span data-ttu-id="90ff1-115">Cuando se ejecuta la versión de 64 bits del ejemplo, se genera el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="90ff1-115">When the 64-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="90ff1-116">Los valores de las vistas predeterminada y alternativa de **\\ Hola de HKCR** son los mismos porque esta clave está compartida.</span><span class="sxs-lookup"><span data-stu-id="90ff1-116">The values of both the default and alternate views of **HKCR\\Hello** are the same because this key is shared.</span></span> <span data-ttu-id="90ff1-117">Los valores de las otras claves difieren porque se redirigen.</span><span class="sxs-lookup"><span data-stu-id="90ff1-117">The values of the other keys differ because they are redirected.</span></span>

<span data-ttu-id="90ff1-118">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Cuando este ejemplo se ejecuta en estos sistemas operativos, las vistas predeterminadas y alternativas de la clave LocalServer32 tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="90ff1-118">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** When this example is run on these operating systems, the default and alternate views of the LocalServer32 key have the same value.</span></span> <span data-ttu-id="90ff1-119">Esto se debe a que la clave LocalServer32 se redirige y *refleja*, lo que hace que su valor se sincronice entre las vistas de 64 bits y 32 bits del registro en cuanto se cierre el identificador de la clave.</span><span class="sxs-lookup"><span data-stu-id="90ff1-119">This is because the LocalServer32 key is redirected and *reflected*, which causes its value to be synchronized between the 64-bit and 32-bit views of the registry as soon as the handle to the key is closed.</span></span> <span data-ttu-id="90ff1-120">La reflexión del registro se quitó a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="90ff1-120">Registry reflection was removed starting with Windows 7.</span></span> <span data-ttu-id="90ff1-121">Para obtener más información, vea [reflexión del registro](registry-reflection.md).</span><span class="sxs-lookup"><span data-stu-id="90ff1-121">For more information, see [Registry Reflection](registry-reflection.md).</span></span>

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

<span data-ttu-id="90ff1-122">Cuando se ejecuta la versión de 32 bits del ejemplo, se genera el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="90ff1-122">When the 32-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="90ff1-123">En el caso de una aplicación de 32 bits, la vista de 64 bits del registro es la vista alternativa, por lo que se invierten los valores, excepto HKCR \\ Hola, que es una clave compartida.</span><span class="sxs-lookup"><span data-stu-id="90ff1-123">For a 32-bit application, the 64-bit view of the registry is the alternate view so the values are reversed, except for HKCR\\Hello, which is a shared key.</span></span>

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

<span data-ttu-id="90ff1-124">Para examinar el efecto de ejecutar este ejemplo con regedit, revise los valores de las siguientes claves.</span><span class="sxs-lookup"><span data-stu-id="90ff1-124">To examine the effect of running this example with regedit, inspect the values of the following keys.</span></span> <span data-ttu-id="90ff1-125">Tenga en cuenta que las aplicaciones deben evitar el uso de Wow6432Node en rutas de acceso del registro codificadas de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="90ff1-125">Note that applications should avoid using Wow6432Node in hard-coded registry paths.</span></span>

<span data-ttu-id="90ff1-126">**HKLM \\ SOFTWARE \\ Hola mundo**</span><span class="sxs-lookup"><span data-stu-id="90ff1-126">**HKLM\\SOFTWARE\\Hello World**</span></span>  
<span data-ttu-id="90ff1-127">**HKLM \\ software \\ Wow6432Node \\ Hola mundo**</span><span class="sxs-lookup"><span data-stu-id="90ff1-127">**HKLM\\SOFTWARE\\Wow6432Node\\Hello World**</span></span>  
<span data-ttu-id="90ff1-128">**\\Identificador CLSID \\ de HKCR {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="90ff1-128">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="90ff1-129">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InProcServer32**</span><span class="sxs-lookup"><span data-stu-id="90ff1-129">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="90ff1-130">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="90ff1-130">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="90ff1-131">**HKCR \\ Hola HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="90ff1-131">**HKCR\\Hello HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="90ff1-132">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InProcServer32**</span><span class="sxs-lookup"><span data-stu-id="90ff1-132">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="90ff1-133">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="90ff1-133">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="90ff1-134">**Wow6432Node de HKCR \\ \\**</span><span class="sxs-lookup"><span data-stu-id="90ff1-134">**HKCR\\Wow6432Node\\Hello**</span></span>  


## <a name="related-topics"></a><span data-ttu-id="90ff1-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90ff1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ff1-136">Redirector del registro</span><span class="sxs-lookup"><span data-stu-id="90ff1-136">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="90ff1-137">Reflexión del registro</span><span class="sxs-lookup"><span data-stu-id="90ff1-137">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 




