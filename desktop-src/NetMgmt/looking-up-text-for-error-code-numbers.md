---
title: Buscar texto para números de códigos de error
description: A veces es necesario mostrar el texto de error asociado a los códigos de error devueltos por las funciones relacionadas con redes. Es posible que tenga que realizar esta tarea con las funciones de administración de red proporcionadas por el sistema.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685732"
---
# <a name="looking-up-text-for-error-code-numbers"></a><span data-ttu-id="f4902-104">Buscar texto para números de códigos de error</span><span class="sxs-lookup"><span data-stu-id="f4902-104">Looking Up Text for Error Code Numbers</span></span>

<span data-ttu-id="f4902-105">A veces es necesario mostrar el texto de error asociado a los códigos de error devueltos por las funciones relacionadas con redes.</span><span class="sxs-lookup"><span data-stu-id="f4902-105">It is sometimes necessary to display error text associated with error codes returned from networking-related functions.</span></span> <span data-ttu-id="f4902-106">Es posible que tenga que realizar esta tarea con las funciones de administración de red proporcionadas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="f4902-106">You may need to perform this task with the network management functions provided by the system.</span></span>

<span data-ttu-id="f4902-107">El texto de error de estos mensajes se encuentra en el archivo de tabla de mensajes denominado Netmsg.dll, que se encuentra en% systemroot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="f4902-107">The error text for these messages is found in the message table file named Netmsg.dll, which is found in %systemroot%\\system32.</span></span> <span data-ttu-id="f4902-108">Este archivo contiene mensajes de error en el intervalo NERR \_ base (2100) hasta el máximo \_ NERR (NERR \_ base + 899).</span><span class="sxs-lookup"><span data-stu-id="f4902-108">This file contains error messages in the range NERR\_BASE (2100) through MAX\_NERR(NERR\_BASE+899).</span></span> <span data-ttu-id="f4902-109">Estos códigos de error se definen en el archivo de encabezado del SDK lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="f4902-109">These error codes are defined in the SDK header file lmerr.h.</span></span>

<span data-ttu-id="f4902-110">Las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) pueden cargar Netmsg.dll.</span><span class="sxs-lookup"><span data-stu-id="f4902-110">The [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) functions can load Netmsg.dll.</span></span> <span data-ttu-id="f4902-111">La función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) asigna un código de error al texto del mensaje, dado un identificador de módulo para el archivo de Netmsg.dll.</span><span class="sxs-lookup"><span data-stu-id="f4902-111">The [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function maps an error code to message text, given a module handle to the Netmsg.dll file.</span></span>

<span data-ttu-id="f4902-112">En el ejemplo siguiente se muestra cómo mostrar el texto de error asociado a las funciones de administración de red, además de mostrar el texto de error asociado a los códigos de error relacionados con el sistema.</span><span class="sxs-lookup"><span data-stu-id="f4902-112">The following sample illustrates how to display error text associated with network management functions, in addition to displaying error text associated with system-related error codes.</span></span> <span data-ttu-id="f4902-113">Si el número de error proporcionado está en un intervalo específico, el módulo de mensajes de netmsg.dll se carga y se utiliza para buscar el número de error especificado con la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="f4902-113">If the supplied error number is in a specific range, the netmsg.dll message module is loaded and used to look up the specified error number with the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



<span data-ttu-id="f4902-114">Después de compilar este programa, puede insertar el número de código de error como argumento y el programa mostrará el texto.</span><span class="sxs-lookup"><span data-stu-id="f4902-114">After you compile this program, you can insert the error code number as an argument and the program will display the text.</span></span> <span data-ttu-id="f4902-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f4902-115">For example:</span></span>

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 