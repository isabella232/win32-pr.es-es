---
description: Cuando una llamada al método genera un error, muchas funciones devuelven un código de error.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Recuperación de mensajes de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96ffb6627dac4f8612a80c68b1a227516ec645440c56dd7c58672cd8222c23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900525"
---
# <a name="retrieving-error-messages"></a>Recuperación de mensajes de error

Cuando una llamada al método genera un error, muchas funciones devuelven un código de error. Para la mayoría de las interfaces de Servicios de certificados y los elementos de API que devuelven un código de error, el texto del mensaje de error se puede recuperar llamando a [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con un identificador de módulo **NULL.** Si **FormatMessage no** se realiza correctamente, lo más probable es que el código de error sea el resultado de un error relacionado con la base de datos o un elemento de la API de copia de seguridad. llamar **a FormatMessage** con un identificador de módulo correspondiente a la biblioteca Ntdsbmsg.dll debe recuperar el texto del mensaje de error. En el ejemplo siguiente se muestra cómo recuperar el texto del mensaje de error en una aplicación de Servicios de certificados.


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
