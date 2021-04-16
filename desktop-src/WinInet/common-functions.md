---
title: Funciones comunes (Internet de Windows)
description: Los diferentes protocolos de Internet (como FTP y http) usan varias de las mismas funciones de WinINet para controlar la información en Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714511"
---
# <a name="common-functions-windows-internet"></a>Funciones comunes (Internet de Windows)

Los diferentes protocolos de Internet (como FTP y http) usan varias de las mismas funciones de WinINet para controlar la información en Internet. Estas funciones comunes controlan sus tareas de forma coherente, independientemente del protocolo concreto al que se aplican. Las aplicaciones pueden usar estas funciones para crear funciones de uso general que controlan las tareas en los diferentes protocolos (como la lectura de archivos para FTP y http).

Las funciones comunes de controlan las tareas siguientes:

-   Descargar recursos de Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)y [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Configurar operaciones asincrónicas ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Ver y cambiar opciones ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Cerrar todos los tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Colocar y quitar bloqueos en los recursos ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) y [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Usar funciones comunes

En la tabla siguiente se enumeran las funciones comunes incluidas en las funciones de WinINet. Las funciones comunes se pueden usar en diferentes tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) o se pueden usar durante diferentes tipos de sesiones.



| Función                                                         | Descripción                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Continúa la enumeración o búsqueda de archivos. Requiere un identificador creado por la función [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Permite al usuario colocar un bloqueo en el archivo que se está usando. Esta función requiere un identificador devuelto por la función [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Recupera la cantidad de datos disponibles. Requiere un identificador creado por la función [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Recupera el valor de una opción de Internet.                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Lee los datos de la dirección URL. Requiere un identificador creado por la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Establece la posición para la siguiente lectura en un archivo. Requiere un identificador creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en una dirección URL http) o un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) mediante el verbo HTTP GET.                 |
| [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Establece una opción de Internet.                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Establece una función de devolución de llamada que recibe información de estado. Asigna una función de devolución de llamada al identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) designado y a todos los identificadores derivados de ella.                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Desbloquea un archivo que se ha bloqueado mediante la función [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .                                                                                                                                           |



 

Leer archivos, buscar el siguiente archivo, manipular opciones y configurar operaciones asincrónicas es común a las funciones que admiten varios protocolos y tipos de identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) .

### <a name="reading-files"></a>Leer archivos

La función [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) se usa para descargar recursos de un [**identificador HINTERNET**](appendix-a-hinternet-handles.md) devuelto por la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) acepta una variable de puntero void que contiene la dirección de un búfer y un puntero a una variable que contiene la longitud del búfer. La función devuelve los datos en el búfer y la cantidad de datos descargados en el búfer.

Las funciones WinINet proporcionan dos técnicas para descargar un recurso completo:

-   La función [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .
-   Los valores devueltos de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) toma el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (después de llamar a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) en el identificador) y devuelve el número de bytes disponibles. La aplicación debe asignar un búfer igual al número de bytes disponibles, más 1 para el carácter **nulo** de terminación y usar ese búfer con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Este método no siempre funciona porque [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) comprueba el tamaño de archivo que aparece en el encabezado y no el archivo real. La información del archivo de encabezado podría estar obsoleta o falta el archivo de encabezado, ya que actualmente no es necesario en todos los estándares.

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



[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) devuelve cero bytes leídos y se completa correctamente cuando se han leído todos los datos disponibles. Esto permite que una aplicación use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) en un bucle para descargar los datos y salir cuando devuelva cero bytes leídos y se complete correctamente.

En el ejemplo siguiente se lee el recurso desde Internet y se muestra el recurso en el cuadro de edición indicado por intCtrlID. El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, fue devuelto por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (después de ser enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).


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

La función [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) se usa para buscar el siguiente archivo en una búsqueda de archivos mediante los parámetros de búsqueda y el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

Para completar una búsqueda de archivos, siga llamando a [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) con el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) devuelto por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) hasta que se produzca un error en la función con el mensaje de error extendido [ \_ no hay \_ más \_ archivos](wininet-errors.md). Para obtener la información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

En el ejemplo siguiente se muestra el contenido de un directorio FTP en el cuadro de lista indicado por lstDirectory. El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, es un identificador devuelto por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) después de establecer una sesión de FTP.


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



### <a name="manipulating-options"></a>Manipular opciones

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) se usan para manipular las opciones de Wininet.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) acepta una variable que indica la opción que se va a establecer, un búfer para contener el valor de la opción y un puntero que contiene la dirección de la variable que contiene la longitud del búfer.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) acepta una variable que indica la opción de recuperación, un búfer para contener la configuración de opción y un puntero que contiene la dirección de la variable que contiene la longitud del búfer.

### <a name="setting-up-asynchronous-operations"></a>Configurar operaciones asincrónicas

De forma predeterminada, las funciones WinINet funcionan sincrónicamente. Una aplicación puede solicitar una operación asincrónica estableciendo la marca [ \_ \_ Async de marca de Internet](api-flags.md) en la llamada a la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . Todas las llamadas futuras realizadas en los identificadores derivados del identificador devuelto desde [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) se realizan de forma asincrónica.

La lógica para la operación asincrónica frente a la sincrónica es permitir que una aplicación de un único subproceso Maximice su uso de la CPU sin tener que esperar a que se complete la e/s de red. Por lo tanto, dependiendo de la solicitud, la operación puede completarse de forma sincrónica o asincrónica. La aplicación debe comprobar el código de retorno. Si una función devuelve **false** o **null**, y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ e/s \_ pendiente, la solicitud se ha realizado de forma asincrónica y se vuelve a llamar a la aplicación con la solicitud de estado de Internet \_ \_ \_ completa cuando se completa la función.

Para comenzar la operación asincrónica, la aplicación debe establecer la [marca \_ \_ Async de marca de Internet](api-flags.md) en su llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). A continuación, la aplicación debe registrar una función de devolución de llamada válida mediante [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).

Después de registrar una función de devolución de llamada para un identificador, todas las operaciones en ese identificador pueden generar indicaciones de estado, siempre que el valor de contexto que se proporcionó cuando se creó el identificador no sea cero. Proporcionar un valor de contexto cero obliga a que una operación se complete de forma sincrónica, aunque se especificó la [marca de Internet \_ \_ Async](api-flags.md) en [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

Las indicaciones de estado proporcionan a la aplicación comentarios sobre el progreso de las operaciones de red, como la resolución de un nombre de host, la conexión a un servidor y la recepción de datos. Se pueden realizar tres indicaciones de estado de uso especial para un identificador:

-   \_ \_ \_ El cierre del identificador de estado de Internet es la última indicación de estado que se realiza para un identificador.
-   \_ \_ Identificador de estado \_ de Internet creado indica cuándo se crea inicialmente el identificador.
-   La \_ solicitud de estado de Internet \_ \_ completa indica que se ha completado una operación asincrónica.

La aplicación debe comprobar la estructura de [**\_ \_ resultados asincrónicos de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) para determinar si la operación se realizó correctamente o no después de recibir una indicación de estado de Internet \_ \_ \_ rellenada.

En el ejemplo siguiente se muestra un ejemplo de una función de devolución de llamada y una llamada a [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para registrar la función como la función de devolución de llamada.


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



### <a name="closing-hinternet-handles"></a>Cerrar los identificadores de HINTERNET

Todos los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) se pueden cerrar mediante la función [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) . Las aplicaciones cliente deben cerrar todos los identificadores de **HINTERNET** derivados del identificador **HINTERNET** que están intentando cerrar antes de llamar a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) en el identificador.

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



### <a name="locking-and-unlocking-resources"></a>Bloquear y desbloquear recursos

La función [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permite a una aplicación asegurarse de que el recurso almacenado en caché asociado al identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que se ha pasado no desaparece de la caché. Si otra descarga intenta confirmar un recurso que tiene la misma dirección URL que el archivo bloqueado, la memoria caché evita la eliminación del archivo mediante una eliminación segura. Una vez que la aplicación llama a la función [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , se concede permiso a la memoria caché para eliminar el archivo.

Si se ha establecido la marca [Internet Flag not cache \_ \_ \_ \_ Write](api-flags.md) o [Internet \_ Flag not \_ \_ Cache](api-flags.md) , [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crea un archivo temporal con la extensión tmp, a menos que el identificador esté conectado a un recurso https. Si la función tiene acceso a un recurso https y a la marca de INTERNET no se ha \_ \_ \_ establecido ninguna escritura en caché \_ (o se ha establecido la marca de Internet como no \_ \_ \_ almacenada en caché), [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) produce un error.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
