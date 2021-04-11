---
title: Control de errores (Windows Internet)
description: La función GetLastError recupera el último código de error para todas las funciones de WinINet.
ms.assetid: ee619803-b2a3-4a99-a3e6-120e147843f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc175c80fd8bd10b6a3807376e1a207d805aee65
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104274504"
---
# <a name="handling-errors-windows-internet"></a>Control de errores (Windows Internet)

La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) recupera el último código de error para todas las funciones de Wininet. Si se devuelve un error de error [**\_ \_ extendido \_ de Internet**](wininet-errors.md) , hay una cadena o un búfer que contiene un mensaje de error detallado. Llame a la función [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) para recuperar el texto de error extendido.

Para obtener el texto de error de un error, llame a la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) , pasándole un identificador **HMODULE** a Wininet.dll, que se puede obtener mediante la función [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .

El siguiente es un ejemplo de una función de control de errores.


```C++
#include <windows.h>
#include "strsafe.h"
#include "wininet.h"
#include <stdlib.h>
#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  INET_ERR_OUT_MSG_BOX_BUFFER_SIZE      512
#define  INET_ERR_OUT_FORMAT_BUFFER_SIZE       256

#ifdef  _UNICODE
#define _itot _itow_s
#else
#define _itot _itoa_s
#endif

// Forward declaration of helper function
void WINAPI addLastErrorToMsg( LPTSTR szMsgBuffer, DWORD dwSize );

// Function for displaying Internet Error information in a message box
BOOL WINAPI InternetErrorOut(
                              HWND hWnd,
                              DWORD dwError,
                              LPCTSTR szFailingFunctionName )
{
  HANDLE hProcHeap;
  TCHAR  szMsgBoxBuffer[INET_ERR_OUT_MSG_BOX_BUFFER_SIZE],
         szFormatBuffer[INET_ERR_OUT_FORMAT_BUFFER_SIZE],
         szConnectiveText[]  = { TEXT( "\nAdditional Information: " )},
        *szExtErrMsg         = NULL,
        *szCombinedErrMsg    = NULL;
  DWORD  dwInetError,
         dwBaseLength,
         dwExtLength = 0;

  if( ( hProcHeap = GetProcessHeap( ) ) == NULL )
  {
    StringCchCopy( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "Call to GetProcessHeap( ) failed..." ) ); 
    goto InetErrorOutError_1;
  }

  dwBaseLength = FormatMessage(
    FORMAT_MESSAGE_FROM_HMODULE,             // dwFlags
    GetModuleHandle( TEXT("wininet.dll") ),  // lpSource
    dwError,                                 // dwMessageId
    0,                                       // dwLanguageId
    (LPTSTR)szFormatBuffer,                  // lpBuffer
    INET_ERR_OUT_FORMAT_BUFFER_SIZE,         // nSize
    NULL );                                  // * arguments

  if( !dwBaseLength )
  {
    StringCchCopy( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
                   TEXT( "Call to FormatMessage( ) failed..." ) ); 
    addLastErrorToMsg( szMsgBoxBuffer, 
                       INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
    goto InetErrorOutError_1;
  }

  if( FAILED( StringCchPrintf( szMsgBoxBuffer, 
                INET_ERR_OUT_MSG_BOX_BUFFER_SIZE,
                TEXT( "%s error; code: %d\nDescription: %s\n" ),
                szFailingFunctionName, dwError, szFormatBuffer ) ) )
  {
    StringCchCopy( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "Call to StringCchPrintf( ) failed...\n" ) ); 
    goto InetErrorOutError_1;
  }

  StringCchLength( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE,
                (size_t*) &dwBaseLength );
  // Adjust base-length value to count the number of bytes:
  dwBaseLength *= sizeof( TCHAR );

  if( dwError == ERROR_INTERNET_EXTENDED_ERROR )
  {
    InternetGetLastResponseInfo( &dwInetError, NULL, &dwExtLength );
    // Adjust the extended-length value to a byte count 
    // that includes the terminating null:
    ++dwExtLength *= sizeof( TCHAR );
    if( ( szExtErrMsg = (TCHAR*)HeapAlloc( hProcHeap, 0, dwExtLength)) 
         == NULL )
    {
      StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
        TEXT("\nFailure: Could not allocate buffer for addional details.")); 
      addLastErrorToMsg( szMsgBoxBuffer, 
                         INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
      goto InetErrorOutError_1;
    }

    if( !InternetGetLastResponseInfo( &dwInetError, 
                                      szExtErrMsg, 
                                      &dwExtLength ) )
    {
      StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
        TEXT( "\nCall to InternetGetLastResponseInfo( ) failed--" ) ); 
      addLastErrorToMsg( szMsgBoxBuffer, 
                         INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
      goto InetErrorOutError_2;
    }
    dwBaseLength += dwExtLength + sizeof( szConnectiveText );
  }

  if( ( szCombinedErrMsg = (TCHAR*)HeapAlloc( hProcHeap, 0, 
                                              dwBaseLength + sizeof(TCHAR) ) ) 
                         == NULL )
  {
    StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "\nFailure: Could not allocate final output buffer." ) ); 
    addLastErrorToMsg( szMsgBoxBuffer, 
                       INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
    goto InetErrorOutError_2;
  }

  if( FAILED( StringCchCopy( szCombinedErrMsg, 
                dwBaseLength, szMsgBoxBuffer ) ) ||
      ( dwExtLength && 
        ( FAILED( StringCchCat( szCombinedErrMsg, 
                    dwBaseLength, szConnectiveText ) ) ||
          FAILED( StringCchCat( szCombinedErrMsg, 
                    dwBaseLength, szExtErrMsg ) ) ) ) )
  {
    StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "\nFailure: Could not assemble final message." ) ); 
    goto InetErrorOutError_3;
  }

  MessageBox( hWnd, 
    szCombinedErrMsg, 
    TEXT( "Internet Error Message" ),
    MB_OK | MB_ICONERROR );
  HeapFree( hProcHeap, 0, szExtErrMsg );
  HeapFree( hProcHeap, 0, szCombinedErrMsg );

  return( TRUE );

InetErrorOutError_3:
  HeapFree( hProcHeap, 0, szCombinedErrMsg );
InetErrorOutError_2:
  HeapFree( hProcHeap, 0, szExtErrMsg );
InetErrorOutError_1:
  MessageBox( hWnd,
    (LPCTSTR) szMsgBoxBuffer,
    TEXT( "InternetErrorOut( ) Failed" ),
    MB_OK | MB_ICONERROR );
  return( FALSE );
}


void WINAPI addLastErrorToMsg( LPTSTR szMsgBuffer, DWORD dwSize )
{
  TCHAR szNumberBuffer[32];

  _itot( GetLastError( ), szNumberBuffer, 10 );
  StringCchCat( szMsgBuffer, dwSize, 
        TEXT( "\n   System Error number: " ) ); 
  StringCchCat( szMsgBuffer, dwSize, szNumberBuffer );
  StringCchCat( szMsgBuffer, dwSize, TEXT( ".\n" ) ); 
}
```



> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
