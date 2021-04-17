---
description: El ejemplo siguiente es el código fuente necesario para crear un archivo DLL simple, Myputs.dll.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Creación de una biblioteca de Dynamic-Link simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572c25c87a3130739a55fcccfc9d8f9c6514d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687147"
---
# <a name="creating-a-simple-dynamic-link-library"></a>Creación de una biblioteca de Dynamic-Link simple

El ejemplo siguiente es el código fuente necesario para crear un archivo DLL simple, Myputs.dll. Define una función simple de impresión de cadenas llamada allocas. La DLL allocas no define una función de punto de entrada, porque está vinculada a la biblioteca en tiempo de ejecución de C y no tiene funciones de inicialización o limpieza propias para realizar.

Para compilar el archivo DLL, siga las instrucciones de la documentación que se incluye con las herramientas de desarrollo.

Para obtener un ejemplo en el que se usan allocas, vea [usar la vinculación dinámica de Load-Time](using-load-time-dynamic-linking.md) o [usar Run-Time vinculación dinámica](using-run-time-dynamic-linking.md).


```C++
// The myPuts function writes a null-terminated string to
// the standard output device.
 
// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.
 
 
#include <windows.h>
 
#define EOF (-1)
 
#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif
 
__declspec(dllexport) int __cdecl myPuts(LPWSTR lpszMsg)
{
    DWORD cchWritten;
    HANDLE hConout;
    BOOL fRet;
 
    // Get a handle to the console output device.

    hConout = CreateFileW(L"CONOUT$",
                         GENERIC_WRITE,
                         FILE_SHARE_WRITE,
                         NULL,
                         OPEN_EXISTING,
                         FILE_ATTRIBUTE_NORMAL,
                         NULL);

    if (INVALID_HANDLE_VALUE == hConout)
        return EOF;
 
    // Write a null-terminated string to the console output device.
 
    while (*lpszMsg != L'\0')
    {
        fRet = WriteConsole(hConout, lpszMsg, 1, &cchWritten, NULL);
        if( (FALSE == fRet) || (1 != cchWritten) )
            return EOF;
        lpszMsg++;
    }
    return 1;
}
 
#ifdef __cplusplus
}
#endif
```



 

 



