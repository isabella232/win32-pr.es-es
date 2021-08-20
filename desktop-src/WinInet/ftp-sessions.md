---
title: Sesiones ftp
description: WinINet permite a las aplicaciones navegar y manipular directorios y archivos en un servidor FTP. Dado que los servidores proxy de CERN no admiten FTP, las aplicaciones que usan un proxy CERN deben usar exclusivamente la función InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70942fea5865fa96c9ee81ab996238e3f382471a701ac44969d1ff8797c8780d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113983"
---
# <a name="ftp-sessions"></a>Sesiones ftp

WinINet permite a las aplicaciones navegar y manipular directorios y archivos en un servidor FTP. Dado que los servidores proxy de CERN no admiten FTP, las aplicaciones que usan un proxy CERN deben usar exclusivamente [**la función InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Para obtener más información sobre cómo usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), vea [Accessing URLs Directly](handling-uniform-resource-locators.md).

Para iniciar una sesión FTP, use [**InternetConnect para**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) crear el identificador de sesión.

WinINet permite realizar las siguientes acciones en un servidor FTP:

-   Navegue entre directorios.
-   Enumerar, crear, quitar y cambiar el nombre de los directorios.
-   Cambie el nombre, cargue, descargue y elimine archivos.

La navegación la proporcionan las [**funciones FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**y FtpSetCurrentDirectory.**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) Estas funciones usan el identificador de sesión creado por una llamada anterior a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para determinar en qué directorio se encuentra actualmente la aplicación o para cambiar a otro subdirectorio.

La enumeración de directorios se realiza mediante [**las funciones FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**e InternetFindNextFile.**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para buscar el primer archivo que coincida con los criterios de búsqueda especificados y devuelve un identificador para continuar con la enumeración de directorios. [**InternetFindNextFile usa**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) el identificador devuelto por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) para devolver el siguiente archivo que coincida con los criterios de búsqueda originales. La aplicación debe seguir llamada a [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) hasta que no haya más archivos en el directorio.

Use la [**función FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) para crear directorios. Esta función usa el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y crea el directorio especificado por la cadena que se pasa a la función. La cadena puede contener un nombre de directorio relativo al directorio actual o una ruta de acceso de directorio completa.

Para cambiar el nombre de archivos o directorios, la aplicación puede llamar a [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea). Esta función reemplaza el nombre original por el nuevo nombre pasado a la función. El nombre del archivo o directorio puede ser relativo al directorio actual o a un nombre completo.

Para cargar o colocar archivos en un servidor FTP, la aplicación puede usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (junto con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)). [**FtpPutFile se**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) puede usar si el archivo ya existe localmente, mientras que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) se pueden usar si es necesario escribir datos en un archivo en el servidor FTP.

Para descargar u obtener archivos, la aplicación puede usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (con [**InternetReadFile).**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) se usa para recuperar un archivo de un servidor FTP y almacenarlo localmente, mientras que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) se pueden usar para controlar dónde va la información descargada (por ejemplo, la aplicación podría mostrar la información en un cuadro de edición).

Elimine los archivos de un servidor FTP mediante la [**función FtpDeleteFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) Esta función quita un nombre de archivo relativo al directorio actual o a un nombre de archivo completo del servidor FTP. [**FtpDeleteFile requiere**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) un identificador de sesión devuelto por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

## <a name="ftp-function-handles"></a>Identificadores de función FTP

Para funcionar correctamente, las funciones FTP requieren ciertos tipos de [**identificadores HINTERNET.**](appendix-a-hinternet-handles.md) Estos identificadores deben crearse en un orden específico, empezando por el identificador raíz creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect puede**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) crear un identificador de sesión FTP.

En el diagrama siguiente se muestran las funciones que dependen del identificador de sesión FTP devuelto [**por InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Los cuadros sombreados representan funciones que devuelven identificadores [**HINTERNET,**](appendix-a-hinternet-handles.md) mientras que los cuadros sin formato representan funciones que usan el identificador HINTERNET creado por la función de la que dependen.

![Funciones ftp dependientes del identificador de sesión ftp devuelto por internetconnect](images/ax-wnt06.png)

En el diagrama siguiente se muestran las dos funciones que devuelven [identificadores HINTERNET](appendix-a-hinternet-handles.md) y las funciones que dependen de ellas. Los cuadros sombreados representan funciones que devuelven identificadores **HINTERNET,** mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función de la que dependen.

![Funciones ftp que devuelven identificadores hinternet](images/ax-wnt03.png)

Para obtener más información, vea [HINTERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Uso de las funciones de WinINet para sesiones FTP

Las siguientes funciones se usan durante las sesiones FTP. Estos servidores proxy de CERN no reconocen estas funciones. Las aplicaciones que deben funcionar a través de servidores proxy CERN deben usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y acceder directamente a los recursos. Para obtener más información sobre el acceso directo a los recursos, consulte [Acceso a direcciones URL directamente.](handling-uniform-resource-locators.md)



| Función                                                 | Descripción                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Crea un nuevo directorio en el servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Elimina un archivo del servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                         |
| [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Inicia la enumeración de archivos o la búsqueda de archivos en el directorio actual. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Devuelve el directorio actual del cliente en el servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Recupera un archivo del servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Inicia el acceso a un archivo en el servidor para lectura o escritura. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Escribe un archivo en el servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Elimina un directorio del servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Cambia el nombre de un archivo en el servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Cambia el directorio actual del cliente en el servidor. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Escribe datos en un archivo abierto en el servidor. Esta función requiere un identificador creado por [**FtpOpenFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                                      |



 

### <a name="starting-an-ftp-session"></a>Inicio de una sesión ftp

La aplicación establece una sesión FTP llamando a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) en un identificador creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) necesita el nombre del servidor, el número de puerto, el nombre de usuario, la contraseña y el tipo de servicio (que deben establecerse en \_ FTP del SERVICIO DE \_ INTERNET). Para la semántica de FTP pasiva, la aplicación también debe establecer la [marca INTERNET \_ FLAG \_ PASSIVE.](api-flags.md)

Los valores PUERTO FTP PREDETERMINADO de INTERNET e INTERNET NÚMERO DE PUERTO NO VÁLIDO \_ se pueden usar para el número de \_ \_ \_ \_ \_ puerto. INTERNET \_ DEFAULT FTP PORT usa el puerto FTP \_ \_ predeterminado, pero el tipo de servicio todavía debe establecerse. INTERNET \_ INVALID PORT NUMBER usa el valor predeterminado para el tipo de servicio \_ \_ indicado.

Los valores del nombre de usuario y la contraseña se pueden establecer en **NULL.** Si ambos valores se establecen en **NULL,** [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa "anonymous" para el nombre de usuario y la dirección de correo electrónico del usuario para la contraseña. Si solo la contraseña se establece en **NULL,** el nombre de usuario pasado a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) se usa para el nombre de usuario y se usa una cadena vacía para la contraseña. Si ninguno de los valores **es NULL,** se usan el nombre de usuario y la contraseña [**dados a InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

### <a name="enumerating-directories"></a>Enumerar directorios

La enumeración de un directorio en un servidor FTP requiere la creación de un identificador mediante [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Este identificador es una rama del identificador de sesión creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) busca el primer archivo o directorio en el servidor y lo devuelve en una estructura [**\_ FIND DATA \_ de WIN32.**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Use [**InternetFindNextFile hasta**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) que devuelva [**ERROR NO MORE \_ \_ \_ FILES**](wininet-errors.md). Este método busca todos los archivos y directorios posteriores en el servidor. Para obtener más información sobre [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), vea [Finding the Next File](common-functions.md).

Para determinar si el archivo recuperado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) es un directorio, compruebe el **miembro dwFileAttributes** de la estructura FIND DATA de [**WIN32 \_ \_**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) para ver si es igual a FILE \_ ATTRIBUTE \_ DIRECTORY.

Si la aplicación realiza cambios en el servidor FTP o si el servidor FTP cambia con frecuencia, las marcas [INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE](api-flags.md) y [INTERNET FLAG \_ \_ RELOAD](api-flags.md) deben establecerse en [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Estas marcas garantizan que la información del directorio que se recupera del servidor FTP es actual.

Una vez que la aplicación completa la enumeración de directorios, la aplicación debe realizar una llamada a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) en el identificador creado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Hasta que se cierre ese identificador, la aplicación no puede volver a llamar a [**FtpFindFirstFile en**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) el identificador de sesión creado [**por InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Si se realiza una llamada a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) en el mismo identificador de sesión antes de que se cierre la llamada anterior a la misma función, se produce un error en la función y devuelve [ERROR FTP TRANSFER IN \_ \_ \_ \_ PROGRESS](wininet-errors.md).

En el ejemplo siguiente se enumera el contenido de un directorio FTP en un control de cuadro de lista. El *parámetro hConnection* es un identificador devuelto por la [**función InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) después de establecer una sesión FTP. El código fuente de ejemplo de la función InternetErrorOut a la que se hace referencia en este ejemplo se puede encontrar en el [tema Control de errores.](appendix-c-handling-errors.md)


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a>Navegar por directorios

Las [**funciones FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) y [**FtpSetCurrentDirectory controlan**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) la navegación por directorios.

[**FtpGetCurrentDirectory devuelve**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) el directorio actual de la aplicación en el servidor FTP. Se incluye la ruta de acceso del directorio raíz en el servidor FTP.

[**FtpSetCurrentDirectory cambia**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) el directorio de trabajo en el servidor. La información de directorio que se pasa a [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) puede ser un nombre de ruta de acceso parcial o completo en relación con el directorio actual. Por ejemplo, si la aplicación se encuentra actualmente en el directorio "public/info" y la ruta de acceso es "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) cambia el directorio actual a "public/info/ftp/example".

En el ejemplo siguiente se usa el identificador de sesión de FTP hConnection, devuelto por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) El nuevo nombre de directorio se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa en el *parámetro nDirNameId.* Antes de realizar el cambio de directorio, la función recupera el directorio actual y lo almacena en el mismo cuadro de edición. El código de configuración de la función DisplayFtpDir a la que se llama al final se muestra anteriormente.


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a>Manipulación de directorios en un servidor FTP

WinINet proporciona la capacidad de crear y quitar directorios en un servidor FTP en el que la aplicación tiene los privilegios necesarios. Si la aplicación debe iniciar sesión en un servidor con un nombre de usuario y una contraseña específicos, los valores se pueden usar [**en InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) al crear el identificador de sesión FTP.

La [**función FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) toma un identificador de sesión FTP válido y una cadena terminada en NULL que contiene una ruta de acceso completa o un nombre relativo al directorio actual y crea un directorio en el servidor FTP.

En el ejemplo siguiente se muestran dos llamadas independientes [**a FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). En ambos ejemplos, hFtpSession es el identificador de sesión creado por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y el directorio raíz es el directorio actual.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

La [**función FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) toma un identificador de sesión y una cadena terminada en **NULL** que contiene una ruta de acceso completa o un nombre relativo al directorio actual y quita ese directorio del servidor FTP.

En el ejemplo siguiente se muestran dos llamadas de ejemplo [**a FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). En ambas llamadas, hFtpSession es el identificador de sesión creado por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y el directorio raíz es el directorio actual. Hay un directorio denominado "test" en el directorio raíz y un directorio denominado "example" en el directorio "test".

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



En el ejemplo siguiente se crea un nuevo directorio en el servidor FTP. El nuevo nombre de directorio se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa en el *parámetro nDirNameId.* InternetConnect creó el [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) identificador *hConnection* después de establecer una sesión FTP. El código fuente de la función DisplayFtpDir a la que se llama al final se muestra anteriormente.


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



En el ejemplo siguiente se elimina un directorio del servidor FTP. El nombre del directorio que se va a eliminar se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa al *parámetro nDirNameId.* InternetConnect creó el [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) identificador *hConnection* después de establecer una sesión FTP. El código fuente de la función DisplayFtpDir a la que se llama al final se muestra anteriormente.


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a>Obtener archivos en un servidor FTP

Hay tres métodos para recuperar archivos de un servidor FTP:

-   Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)
-   Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)
-   Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).

Para obtener más información sobre el uso [**de la función InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) vea [Leer archivos](common-functions.md).

Si la dirección URL del archivo está disponible, la aplicación puede llamar a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para conectarse a esa dirección URL y, a continuación, usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para controlar la descarga del archivo. Esto permite a la aplicación un control más estricto sobre la descarga y es ideal para situaciones en las que no es necesario realizar ninguna otra operación en el servidor FTP. Para obtener más información sobre cómo acceder directamente a los recursos, vea [Acceso a direcciones URL directamente.](handling-uniform-resource-locators.md)

Si la aplicación ha establecido un identificador de sesión FTP para el servidor con [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), la aplicación puede llamar a [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con el nombre de archivo existente y con un nuevo nombre para el archivo almacenado localmente. A continuación, la aplicación [**puede usar InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para descargar el archivo. Esto permite a la aplicación un control más estricto sobre la descarga y mantiene la conexión con el servidor FTP, por lo que se pueden ejecutar más comandos.

Si la aplicación no necesita un control estricto sobre la descarga, la aplicación puede usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) con el identificador de sesión FTP, el nombre de archivo remoto y el nombre de archivo local para recuperar el archivo. [**FtpGetFile realiza**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) toda la contabilidad y la sobrecarga asociadas a la lectura de un archivo desde un servidor FTP y su almacenamiento local.

En el ejemplo siguiente se recupera un archivo de un servidor FTP y se guarda localmente. El nombre del archivo en el servidor FTP se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa en el parámetro *nFtpFileNameId* y el nombre local con el que se guarda el archivo se toma del cuadro de edición cuyo IDC se pasa en el parámetro *nLocalFileNameId.* InternetConnect creó el [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) identificador *hConnection* después de establecer una sesión FTP.


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a>Colocar archivos en un servidor FTP

Hay dos métodos para colocar un archivo en un servidor FTP:

-   Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).

Una aplicación que debe enviar datos a un servidor FTP, pero que no tiene un archivo local que contenga todos los datos, debe usar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) para crear y abrir un archivo en el servidor ftp. A continuación, la [**aplicación puede usar InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para cargar la información en el archivo.

Si el archivo ya existe localmente, la aplicación puede usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) para cargar el archivo en el servidor FTP. [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) realiza toda la sobrecarga que se realiza al cargar un archivo local en un servidor FTP remoto.

En el ejemplo siguiente se copia un archivo local en el servidor FTP. El nombre local del archivo se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa en el parámetro *nLocalFileNameId* y el nombre con el que se guarda el archivo en el servidor FTP se toma del cuadro de edición cuyo IDC se pasa en el *parámetro nFtpFileNameId.* InternetConnect creó el [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) identificador *hConnection* después de establecer una sesión FTP.


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a>Eliminar archivos de un servidor FTP

Para eliminar un archivo de un servidor FTP, use la [**función FtpDeleteFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) La aplicación que realiza la llamada debe tener los privilegios necesarios para eliminar un archivo del servidor FTP.

En el ejemplo siguiente se elimina un archivo del servidor FTP. El nombre del archivo que se va a eliminar se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa int al *parámetro nFtpFileNameId.* InternetConnect creó el [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) identificador *hConnection* después de establecer una sesión FTP. Puesto que esta función no actualiza las listas de archivos ni la presentación de directorios, el proceso de llamada debe hacerlo tras la eliminación correcta.


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>Cambiar el nombre de archivos y directorios en un servidor FTP

Se puede cambiar el nombre de los archivos y directorios de un servidor FTP mediante la [**función FtpRenameFile.**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) acepta dos cadenas terminadas en **null** que contienen nombres parciales o completos relativos al directorio actual. La función cambia el nombre del archivo designado por la primera cadena por el nombre designado por la segunda cadena.

En el ejemplo siguiente se cambia el nombre de un archivo o directorio en el servidor FTP. El nombre actual del archivo o directorio se toma del cuadro de edición del cuadro de diálogo primario cuyo IDC se pasa en el *parámetro nOldFileNameId* y el nuevo nombre se toma del cuadro de edición cuyo IDC se pasa en el parámetro *nNewFileNameId.* InternetConnect creó el [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) identificador *hConnection* después de establecer una sesión FTP. Puesto que esta función no actualiza las listas de archivos ni la presentación de directorios, el proceso de llamada debe hacerlo tras un cambio de nombre correcto.


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 