---
title: Buscar texto en busca de números de código de error
description: A veces es necesario mostrar el texto de error asociado a los códigos de error devueltos por las funciones relacionadas con la red. Es posible que tenga que realizar esta tarea con las funciones de administración de red proporcionadas por el sistema.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069400"
---
# <a name="looking-up-text-for-error-code-numbers"></a>Buscar texto en busca de números de código de error

A veces es necesario mostrar el texto de error asociado a los códigos de error devueltos por las funciones relacionadas con la red. Es posible que tenga que realizar esta tarea con las funciones de administración de red proporcionadas por el sistema.

El texto de error de estos mensajes se encuentra en el archivo de tabla de mensajes denominado Netmsg.dll, que se encuentra en %systemroot% \\ system32. Este archivo contiene mensajes de error en el intervalo NERR \_ BASE (2100) a MAX \_ NERR(NERR \_ BASE+899). Estos códigos de error se definen en el archivo de encabezado del SDK lmerr.h.

Las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) pueden cargar Netmsg.dll. La [**función FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) asigna un código de error al texto del mensaje, dado un identificador de módulo al Netmsg.dll archivo.

En el ejemplo siguiente se muestra cómo mostrar el texto de error asociado a las funciones de administración de red, además de mostrar el texto de error asociado a códigos de error relacionados con el sistema. Si el número de error proporcionado está en un intervalo específico, se carga el módulo de mensaje netmsg.dll y se usa para buscar el número de error especificado con la [**función FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage)


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



Después de compilar este programa, puede insertar el número de código de error como argumento y el programa mostrará el texto. Por ejemplo:

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 