---
description: Cada proceso tiene un bloque de entorno asociado a él.
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: Cambiar variables de entorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677874"
---
# <a name="changing-environment-variables"></a><span data-ttu-id="a4e35-103">Cambiar variables de entorno</span><span class="sxs-lookup"><span data-stu-id="a4e35-103">Changing Environment Variables</span></span>

<span data-ttu-id="a4e35-104">Cada proceso tiene un bloque de entorno asociado a él.</span><span class="sxs-lookup"><span data-stu-id="a4e35-104">Each process has an environment block associated with it.</span></span> <span data-ttu-id="a4e35-105">El bloque de entorno está formado por un bloque de cadenas terminadas en null (es decir, hay dos bytes nulos al final del bloque), donde cada cadena tiene el formato:</span><span class="sxs-lookup"><span data-stu-id="a4e35-105">The environment block consists of a null-terminated block of null-terminated strings (meaning there are two null bytes at the end of the block), where each string is in the form:</span></span>

<span data-ttu-id="a4e35-106">*nombre* = de *valor* de</span><span class="sxs-lookup"><span data-stu-id="a4e35-106">*name*=*value*</span></span>

<span data-ttu-id="a4e35-107">Todas las cadenas del bloque de entorno deben ordenarse alfabéticamente por nombre.</span><span class="sxs-lookup"><span data-stu-id="a4e35-107">All strings in the environment block must be sorted alphabetically by name.</span></span> <span data-ttu-id="a4e35-108">La ordenación no distingue entre mayúsculas y minúsculas, orden Unicode, sin tener en cuenta la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="a4e35-108">The sort is case-insensitive, Unicode order, without regard to locale.</span></span> <span data-ttu-id="a4e35-109">Dado que el signo igual es un separador, no se debe usar en el nombre de una variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="a4e35-109">Because the equal sign is a separator, it must not be used in the name of an environment variable.</span></span>

## <a name="example-1"></a><span data-ttu-id="a4e35-110">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4e35-110">Example 1</span></span>

<span data-ttu-id="a4e35-111">De forma predeterminada, un proceso secundario hereda una copia del bloque de entorno del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="a4e35-111">By default, a child process inherits a copy of the environment block of the parent process.</span></span> <span data-ttu-id="a4e35-112">En el ejemplo siguiente se muestra cómo crear un nuevo bloque de entorno para pasarlo a un proceso secundario mediante [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="a4e35-112">The following example demonstrates how to create a new environment block to pass to a child process using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

<span data-ttu-id="a4e35-113">En este ejemplo se usa el código del ejemplo tres como proceso secundario Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="a4e35-113">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a><span data-ttu-id="a4e35-114">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a4e35-114">Example 2</span></span>

<span data-ttu-id="a4e35-115">Modificar las variables de entorno de un proceso secundario durante la creación del proceso es la única manera en que un proceso puede cambiar directamente las variables de entorno de otro proceso.</span><span class="sxs-lookup"><span data-stu-id="a4e35-115">Altering the environment variables of a child process during process creation is the only way one process can directly change the environment variables of another process.</span></span> <span data-ttu-id="a4e35-116">Un proceso no puede cambiar nunca directamente las variables de entorno de otro proceso que no es un elemento secundario de dicho proceso.</span><span class="sxs-lookup"><span data-stu-id="a4e35-116">A process can never directly change the environment variables of another process that is not a child of that process.</span></span>

<span data-ttu-id="a4e35-117">Si desea que el proceso secundario herede la mayor parte del entorno del primario con solo unos pocos cambios, recupere los valores actuales mediante [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), guarde estos valores, cree un bloque actualizado para que el proceso secundario herede, cree el proceso secundario y, a continuación, restaure los valores guardados con [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4e35-117">If you want the child process to inherit most of the parent's environment with only a few changes, retrieve the current values using [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), save these values, create an updated block for the child process to inherit, create the child process, and then restore the saved values using [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), as shown in the following example.</span></span>

<span data-ttu-id="a4e35-118">En este ejemplo se usa el código del ejemplo tres como proceso secundario Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="a4e35-118">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a><span data-ttu-id="a4e35-119">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="a4e35-119">Example 3</span></span>

<span data-ttu-id="a4e35-120">En el ejemplo siguiente se recupera el bloque de entorno del proceso mediante [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) y se imprime el contenido en la consola.</span><span class="sxs-lookup"><span data-stu-id="a4e35-120">The following example retrieves the process's environment block using [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) and prints the contents to the console.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
