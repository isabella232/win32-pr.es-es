---
title: Funciones comunes (Windows Internet)
description: Los distintos protocolos de Internet (como ftp y http) usan varias de las mismas funciones de WinINet para controlar la información en Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7b6a68c2633175eca793f48b2180b7212905762ca0f58290436aa17ae9a728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132898"
---
# <a name="common-functions-windows-internet"></a>Funciones comunes (Windows Internet)

Los distintos protocolos de Internet (como ftp y http) usan varias de las mismas funciones de WinINet para controlar la información en Internet. Estas funciones comunes controlan sus tareas de forma coherente, independientemente del protocolo concreto al que se aplican. Las aplicaciones pueden usar estas funciones para crear funciones de uso general que controlan tareas en los distintos protocolos (por ejemplo, leer archivos para ftp y http).

Las funciones comunes controlan las siguientes tareas:

-   Descarga de recursos de Internet [**(InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetSetFilePointer,**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)e [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Configuración de operaciones asincrónicas ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Ver y cambiar opciones ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Cerrar todos los tipos [**de identificadores HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Colocación y eliminación de bloqueos en recursos [**(InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) e [**InternetUnlockRequestFile).**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)

## <a name="using-common-functions"></a>Uso de funciones comunes

En la tabla siguiente se enumeran las funciones comunes incluidas en las funciones de WinINet. Las funciones comunes se pueden usar en diferentes tipos de [**identificadores HINTERNET**](appendix-a-hinternet-handles.md) o se pueden usar durante diferentes tipos de sesiones.



| Función                                                         | Descripción                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Continúa la enumeración o búsqueda de archivos. Requiere un identificador creado por la [**función FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Permite al usuario colocar un bloqueo en el archivo que se está utilizando. Esta función requiere un identificador devuelto por la [**función FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)o [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Recupera la cantidad de datos disponibles. Requiere un identificador creado por la [**función FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Recupera la configuración de una opción de Internet.                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Lee los datos de la dirección URL. Requiere un identificador creado por [**la función InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Establece la posición de la siguiente lectura en un archivo. Requiere un identificador creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en una dirección URL HTTP) o un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) mediante el verbo HTTP GET.                 |
| [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Establece una opción de Internet.                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Establece una función de devolución de llamada que recibe información de estado. Asigna una función de devolución de llamada al identificador [**HINTERNET**](appendix-a-hinternet-handles.md) designado y a todos los identificadores derivados de él.                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Desbloquea un archivo bloqueado mediante la [**función InternetLockRequestFile.**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)                                                                                                                                           |



 

La lectura de archivos, la búsqueda del siguiente archivo, la manipulación de opciones y la configuración de operaciones asincrónicas son comunes a las funciones que admiten varios protocolos y tipos de identificador [**HINTERNET.**](appendix-a-hinternet-handles.md)

### <a name="reading-files"></a>Leer archivos

La [**función InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) se usa para descargar recursos de un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) devuelto por la función [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) acepta una variable de puntero void que contiene la dirección de un búfer y un puntero a una variable que contiene la longitud del búfer. La función devuelve los datos del búfer y la cantidad de datos descargados en el búfer.

Las funciones de WinINet proporcionan dos técnicas para descargar un recurso completo:

-   La [**función InternetQueryDataAvailable.**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)
-   Valores devueltos de [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) toma el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (después de llamar a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) en el identificador) y devuelve el número de bytes disponibles. La aplicación debe asignar un búfer igual al número de bytes disponibles, más 1 para el carácter **nulo** de terminación, y usar ese búfer [**con InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Este método no siempre funciona porque [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) está comprobando el tamaño del archivo que aparece en el encabezado y no el archivo real. La información del archivo de encabezado podría estar obsoleta o podría faltar el archivo de encabezado, ya que actualmente no es necesaria en todos los estándares.

En el ejemplo siguiente se lee el contenido del recurso al que tiene acceso el identificador hResource y se muestra en el cuadro de edición indicado por intCtrlID.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



[**InternetReadFile devuelve**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) cero bytes leídos y se completa correctamente cuando se han leído todos los datos disponibles. Esto permite que una aplicación use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) en un bucle para descargar los datos y salir cuando devuelve cero bytes leídos y se completa correctamente.

En el ejemplo siguiente se lee el recurso de Internet y se muestra el recurso en el cuadro de edición indicado por intCtrlID. [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) devolvieron el identificador [**HINTERNET,**](appendix-a-hinternet-handles.md) hInternet , o HttpOpenRequest (después de ser enviado por [**HttpSendRequest).**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a>Buscar el siguiente archivo

La [**función InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) se usa para buscar el siguiente archivo en una búsqueda de archivos, mediante los parámetros de búsqueda y el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

Para completar una búsqueda de archivos, siga llamada a [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) mediante el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) devuelto por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) hasta que se produce un error en la función con el mensaje de error [extendido ERROR NO MORE \_ \_ \_ FILES](wininet-errors.md). Para obtener la información de error extendida, llame a [**la función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

En el ejemplo siguiente se muestra el contenido de un directorio FTP en el cuadro de lista indicado por lstDirectory. El [**identificador HINTERNET,**](appendix-a-hinternet-handles.md) hConnect, es un identificador devuelto por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) después de establecer una sesión FTP.


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a>Manipulación de opciones

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) se usan para manipular las opciones de WinINet.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) acepta una variable que indica la opción que se establece, un búfer para contener el valor de opción y un puntero que contiene la dirección de la variable que contiene la longitud del búfer.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) acepta una variable que indica la opción que se debe recuperar, un búfer para contener el valor de opción y un puntero que contiene la dirección de la variable que contiene la longitud del búfer.

### <a name="setting-up-asynchronous-operations"></a>Configuración de operaciones asincrónicas

De forma predeterminada, las funciones de WinINet funcionan sincrónicamente. Una aplicación puede solicitar una operación asincrónica estableciendo la marca [ \_ INTERNET FLAG \_ ASYNC](api-flags.md) en la llamada a la [**función InternetOpen.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) Todas las llamadas futuras realizadas en los identificadores derivados del identificador devuelto [**de InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) se realizan de forma asincrónica.

La lógica de la operación asincrónica frente a la sincrónica es permitir que una aplicación de un solo subproceso maximice su uso de la CPU sin tener que esperar a que se complete la E/S de red. Por lo tanto, en función de la solicitud, la operación podría completarse de forma sincrónica o asincrónica. La aplicación debe comprobar el código de retorno. Si una función devuelve **FALSE** o **NULL,** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR IO PENDING, la solicitud se ha realizado de forma asincrónica y la aplicación se llama de nuevo con LA SOLICITUD DE ESTADO DE INTERNET COMPLETE cuando se ha completado la \_ \_ \_ \_ \_ función.

Para comenzar la operación asincrónica, la aplicación debe establecer la marca [ \_ INTERNET FLAG \_ ASYNC](api-flags.md) en su llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). A continuación, la aplicación debe registrar una función de devolución de llamada válida, [**mediante InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).

Después de registrar una función de devolución de llamada para un identificador, todas las operaciones en ese identificador pueden generar indicaciones de estado, siempre que el valor de contexto que se proporcionó cuando se creó el identificador no fuera cero. Si se proporciona un valor de contexto cero, una operación se completa sincrónicamente, aunque [internet \_ FLAG \_ ASYNC](api-flags.md) se especificó en [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

Las indicaciones de estado dan a la aplicación comentarios sobre el progreso de las operaciones de red, como resolver un nombre de host, conectarse a un servidor y recibir datos. Se pueden realizar tres indicaciones de estado de propósito especial para un identificador:

-   INTERNET \_ STATUS HANDLE CLOSING es la última indicación de estado que se realiza para un \_ \_ identificador.
-   INTERNET \_ STATUS HANDLE CREATED indica cuándo se crea \_ \_ inicialmente el identificador.
-   INTERNET \_ STATUS REQUEST COMPLETE indica que se ha completado una operación \_ \_ asincrónica.

La aplicación debe comprobar la estructura DE RESULTADOS DE [**INTERNET \_ ASYNC \_**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) para determinar si la operación se ha completado correctamente o no después de recibir una indicación INTERNET STATUS REQUEST \_ \_ \_ COMPLETE.

En el ejemplo siguiente se muestra un ejemplo de una función de devolución de llamada y una llamada a [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para registrar la función como función de devolución de llamada.


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a>Cierre de identificadores HINTERNET

Todos [**los identificadores HINTERNET**](appendix-a-hinternet-handles.md) se pueden cerrar mediante [**la función InternetCloseHandle.**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) Las aplicaciones cliente deben cerrar todos los **identificadores HINTERNET** derivados del identificador **HINTERNET** que están intentando cerrar antes de llamar a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) en el identificador.

En el ejemplo siguiente se muestra la jerarquía de identificadores.


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a>Bloqueo y desbloqueo de recursos

La [**función InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permite a una aplicación asegurarse de que el recurso almacenado en caché asociado al identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que se le pasa no desaparece de la memoria caché. Si otra descarga intenta confirmar un recurso que tiene la misma dirección URL que el archivo bloqueado, la memoria caché evita quitar el archivo mediante una eliminación segura. Una vez que la aplicación llama [**a la función InternetUnlockRequestFile,**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) la memoria caché tiene permiso para eliminar el archivo.

Si se ha establecido la marca [INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE](api-flags.md) o [INTERNET FLAG \_ \_ DONT \_ CACHE,](api-flags.md) [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crea un archivo temporal con la extensión TMP, a menos que el identificador esté conectado a un recurso https. Si la función tiene acceso a un recurso https y se ha establecido INTERNET \_ FLAG NO CACHE WRITE \_ \_ \_ (o INTERNET FLAG \_ \_ DONT \_ CACHE), [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) produce un error.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
