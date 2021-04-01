---
description: Cuando una llamada al método genera un error, muchas funciones devuelven un código de error.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Recuperación de mensajes de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefeab75e4419bc1e36785236962069a6913e84d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909630"
---
# <a name="retrieving-error-messages"></a>Recuperación de mensajes de error

Cuando una llamada al método genera un error, muchas funciones devuelven un código de error. Para la mayoría de las interfaces de servicios de Certificate Server y los elementos de API que devuelven un código de error, el texto del mensaje de error se puede recuperar llamando a [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con un identificador de módulo **nulo** . Si **FormatMessage** no se realiza correctamente, es posible que el código de error sea el resultado de un error relacionado con la base de datos o un elemento de API de copia de seguridad. la llamada a **FormatMessage** con un identificador de módulo correspondiente a la biblioteca de Ntdsbmsg.dll debe recuperar el texto del mensaje de error. En el ejemplo siguiente se muestra cómo recuperar el texto de un mensaje de error en una aplicación de servicios de Certificate Server.


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



 

 
