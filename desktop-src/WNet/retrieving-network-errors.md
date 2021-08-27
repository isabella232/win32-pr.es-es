---
title: Recuperación de errores de red
description: Las funciones de WNet devuelven códigos de error por compatibilidad con Windows para grupos de trabajo. Cada función WNet también establece el valor de código de error devuelto por GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f02a05ab93d50b9c448ae280e5de7ddbed1260cf1df8b8b3e56aa33aaeff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072025"
---
# <a name="retrieving-network-errors"></a>Recuperación de errores de red

Las funciones de WNet devuelven códigos de error por compatibilidad con Windows para grupos de trabajo. Cada función de WNet también establece el valor de código de error devuelto [**por GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Cuando una de las funciones de WNet devuelve ERROR EXTENDED ERROR, una aplicación puede llamar a la función \_ \_ [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) para recuperar información adicional sobre el error. Esta información suele ser específica del proveedor de red.

En el ejemplo siguiente se muestra una función de control de errores definida por la aplicación (NetErrorHandler). La función toma tres argumentos: un identificador de ventana, el código de error devuelto por una de las funciones de WNet y el nombre de la función que produjo el error. Si el código de error es ERROR EXTENDED ERROR, NetErrorHandler llama a \_ \_ **WNetGetLastError para** obtener información de error extendida e imprime la información. El ejemplo llama a la [**función MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) para procesar mensajes.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 