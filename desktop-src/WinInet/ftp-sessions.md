---
title: Sesiones FTP
description: WinINet permite a las aplicaciones navegar y manipular directorios y archivos en un servidor FTP. Dado que los proxies de CERN no admiten FTP, las aplicaciones que usan exclusivamente el proxy CERN deben usar la función InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078047"
---
# <a name="ftp-sessions"></a>Sesiones FTP

WinINet permite a las aplicaciones navegar y manipular directorios y archivos en un servidor FTP. Dado que los proxies de CERN no admiten FTP, las aplicaciones que usan exclusivamente el proxy CERN deben usar la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . Para obtener más información sobre cómo usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), consulte [acceso directo a las direcciones URL](handling-uniform-resource-locators.md).

Para iniciar una sesión de FTP, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para crear el identificador de sesión.

WinINet le permite realizar las siguientes acciones en un servidor FTP:

-   Desplazarse por los directorios.
-   Enumerar, crear, quitar y cambiar el nombre de los directorios.
-   Cambiar el nombre, cargar, descargar y eliminar archivos.

La navegación la proporcionan las funciones [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) y [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) . Estas funciones usan el identificador de sesión creado por una llamada anterior a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para determinar el directorio en el que se encuentra la aplicación actualmente, o para cambiar a otro subdirectorio.

La enumeración de directorios se realiza mediante las funciones [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) y [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) . [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para buscar el primer archivo que coincide con los criterios de búsqueda especificados y devuelve un identificador para continuar con la enumeración de directorios. [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usa el identificador devuelto por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) para devolver el siguiente archivo que coincide con los criterios de búsqueda originales. La aplicación debe seguir llamando a [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) hasta que no queden más archivos en el directorio.

Utilice la función [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) para crear nuevos directorios. Esta función usa el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y crea el directorio especificado por la cadena que se pasa a la función. La cadena puede contener un nombre de directorio relativo al directorio actual o una ruta de acceso de directorio completa.

Para cambiar el nombre de los archivos o directorios, la aplicación puede llamar a [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea). Esta función reemplaza el nombre original por el nuevo nombre que se pasa a la función. El nombre del archivo o directorio puede ser relativo al directorio actual o a un nombre completo.

Para cargar o colocar archivos en un servidor FTP, la aplicación puede usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (junto con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)). Se puede usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) si el archivo ya existe localmente, mientras que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) se pueden usar si los datos se deben escribir en un archivo en el servidor FTP.

Para descargar u obtener archivos, la aplicación puede usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)). [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) se usa para recuperar un archivo de un servidor FTP y almacenarlo de forma local, mientras que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) se pueden usar para controlar dónde va la información descargada (por ejemplo, la aplicación podría mostrar la información en un cuadro de edición).

Elimine archivos en un servidor FTP mediante la función [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . Esta función quita un nombre de archivo que es relativo al directorio actual o a un nombre de archivo completo del servidor FTP. [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requiere un identificador de sesión devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

## <a name="ftp-function-handles"></a>Controladores de funciones FTP

Para que funcione correctamente, las funciones de FTP requieren determinados tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) . Estos identificadores deben crearse en un orden específico, empezando por el identificador raíz creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). A continuación, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) puede crear un identificador de sesión de FTP.

En el diagrama siguiente se muestran las funciones que dependen del identificador de sesión FTP devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Los cuadros sombreados representan funciones que devuelven los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , mientras que los cuadros simples representan funciones que utilizan el identificador HINTERNET creado por la función de la que dependen.

![funciones FTP que dependen del identificador de sesión FTP devuelto por internetconnect](images/ax-wnt06.png)

En el diagrama siguiente se muestran las dos funciones que devuelven los identificadores [HINTERNET](appendix-a-hinternet-handles.md) y las funciones que dependen de ellos. Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones de FTP que devuelven identificadores de HINTERNET](images/ax-wnt03.png)

Para obtener más información, vea [identificadores de HINTERNET](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Usar las funciones WinINet para sesiones FTP

Las siguientes funciones se usan durante las sesiones FTP. Los proxies de CERN no reconocen estas funciones. Las aplicaciones que deben funcionar a través de servidores proxy CERN deben usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y tener acceso directamente a los recursos. Para obtener más información sobre el acceso directo a los recursos, consulte [acceso directo a las direcciones URL](handling-uniform-resource-locators.md).



| Función                                                 | Descripción                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Crea un nuevo directorio en el servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Elimina un archivo del servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                         |
| [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Inicia la enumeración de archivos o la búsqueda de archivos en el directorio actual. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Devuelve el directorio actual del cliente en el servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                   |
| [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Recupera un archivo del servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Inicia el acceso a un archivo en el servidor para lectura o escritura. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Escribe un archivo en el servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Elimina un directorio del servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Cambia el nombre de un archivo en el servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Cambia el directorio actual del cliente en el servidor. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Escribe datos en un archivo abierto en el servidor. Esta función requiere un identificador creado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).                                      |



 

### <a name="starting-an-ftp-session"></a>Iniciar una sesión de FTP

La aplicación establece una sesión FTP mediante una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) en un identificador creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) necesita el nombre del servidor, el número de puerto, el nombre de usuario, la contraseña y el tipo de servicio (que debe establecerse en servicio de Internet \_ \_ FTP). En el caso de la semántica de FTP pasivo, la aplicación también debe establecer la marca [ \_ \_ pasiva de marca de Internet](api-flags.md) .

El \_ puerto FTP predeterminado de Internet \_ \_ y \_ \_ \_ los valores de número de puerto de Internet no válidos se pueden usar para el número de puerto. El \_ puerto FTP predeterminado de Internet \_ \_ utiliza el puerto FTP predeterminado, pero todavía debe establecerse el tipo de servicio. El \_ \_ número de puerto de Internet no válido \_ usa el valor predeterminado para el tipo de servicio indicado.

Los valores de nombre de usuario y contraseña pueden establecerse en **null**. Si ambos valores están establecidos en **null**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa "Anonymous" para el nombre de usuario y la dirección de correo electrónico del usuario para la contraseña. Si solo la contraseña se establece en **null**, el nombre de usuario que se pasa a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) se usa para el nombre de usuario y se usa una cadena vacía para la contraseña. Si ninguno de los valores es **null**, se usan el nombre de usuario y la contraseña proporcionados a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .

### <a name="enumerating-directories"></a>Enumerar directorios

La enumeración de un directorio en un servidor FTP requiere la creación de un controlador de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Este identificador es una rama del identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) busca el primer archivo o directorio en el servidor y lo devuelve en una estructura [**de \_ \_ datos de búsqueda de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) hasta que devuelva el [**error \_ no \_ más \_ archivos**](wininet-errors.md). Este método busca todos los archivos y directorios subsiguientes en el servidor. Para obtener más información sobre [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consulte [Buscar el siguiente archivo](common-functions.md).

Para determinar si el archivo recuperado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) es un directorio, compruebe el miembro **dwFileAttributes** de la estructura de [**\_ \_ datos de búsqueda de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) para ver si es igual al directorio de atributos de archivo \_ \_ .

Si la aplicación realiza cambios en el servidor FTP o si el servidor FTP cambia con frecuencia, se deben establecer las marcas de [Internet Flag \_ \_ no \_ Cache \_ Write](api-flags.md) y [Internet \_ Flag \_ Reload](api-flags.md) en [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Estas marcas garantizan que la información de directorio que se recupera del servidor FTP es actual.

Una vez que la aplicación completa la enumeración de directorios, la aplicación debe realizar una llamada a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) en el identificador creado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Hasta que se cierre el identificador, la aplicación no podrá volver a llamar a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) en el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Si se realiza una llamada a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) en el mismo identificador de sesión antes de que se cierre la llamada anterior a la misma función, se produce un error en la función y se devuelve el [error \_ \_ de transferencia FTP \_ en \_ curso](wininet-errors.md).

En el ejemplo siguiente se enumera el contenido de un directorio FTP en un control de cuadro de lista. El parámetro *hConnection* es un identificador devuelto por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) después de que se establece una sesión FTP. Puede encontrar el código fuente de ejemplo para la función InternetErrorOut a la que se hace referencia en este ejemplo en el tema [errores de control](appendix-c-handling-errors.md).


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



### <a name="navigating-directories"></a>Navegar por los directorios

Las funciones [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) y [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) controlan la navegación del directorio.

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) devuelve el directorio actual de la aplicación en el servidor FTP. Se incluye la ruta de acceso del directorio desde el directorio raíz del servidor FTP.

[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) cambia el directorio de trabajo en el servidor. La información del directorio que se pasa a [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) puede ser un nombre de ruta de acceso parcial o completo en relación con el directorio actual. Por ejemplo, si la aplicación se encuentra actualmente en el directorio "Public/info" y la ruta de acceso es "FTP/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) cambia el directorio actual a "Public/info/FTP/example".

En el ejemplo siguiente se usa el identificador de sesión FTP hConnection, devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). El nuevo nombre de directorio se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nDirNameId* . Antes de realizar el cambio de directorio, la función recupera el directorio actual y lo almacena en el mismo cuadro de edición. Aquí se muestra el código de código de código de la función DisplayFtpDir llamada al final.


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



### <a name="manipulating-directories-on-an-ftp-server"></a>Manipular directorios en un servidor FTP

WinINet proporciona la capacidad de crear y quitar directorios en un servidor FTP en el que la aplicación tenga los privilegios necesarios. Si la aplicación debe iniciar sesión en un servidor con un nombre de usuario y una contraseña específicos, los valores se pueden usar en [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) al crear el identificador de sesión FTP.

La función [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) toma un identificador de sesión FTP válido y una cadena terminada en **null** que contiene una ruta de acceso completa o un nombre relativo al directorio actual y crea un directorio en el servidor FTP.

En el ejemplo siguiente se muestran dos llamadas independientes a [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). En ambos ejemplos, hFtpSession es el identificador de sesión creado por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y el directorio raíz es el directorio actual.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

La función [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) toma un identificador de sesión y una cadena terminada en **null** que contiene una ruta de acceso completa o un nombre relativo al directorio actual y quita ese directorio del servidor FTP.

En el ejemplo siguiente se muestran dos llamadas de ejemplo a [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). En ambas llamadas, hFtpSession es el identificador de sesión creado por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y el directorio raíz es el directorio actual. Hay un directorio denominado "Test" en el directorio raíz y un directorio denominado "example" en el directorio "Test".

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



En el ejemplo siguiente se crea un nuevo directorio en el servidor FTP. El nuevo nombre de directorio se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nDirNameId* . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP. A continuación se muestra el código fuente de la función DisplayFtpDir llamada al final.


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



En el ejemplo siguiente se elimina un directorio del servidor FTP. El nombre del directorio que se va a eliminar se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa al parámetro *nDirNameId* . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP. A continuación se muestra el código fuente de la función DisplayFtpDir llamada al final.


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

Existen tres métodos para recuperar archivos de un servidor FTP:

-   Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).

Para obtener más información sobre el uso de la función [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , vea [leer archivos](common-functions.md).

Si la dirección URL del archivo está disponible, la aplicación puede llamar a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para conectarse a esa dirección URL y, a continuación, usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para controlar la descarga del archivo. Esto permite que la aplicación tenga un mayor control sobre la descarga y es ideal para situaciones en las que no es necesario realizar ninguna otra operación en el servidor FTP. Para obtener más información sobre cómo acceder directamente a los recursos, consulte [acceso directo a las direcciones URL](handling-uniform-resource-locators.md).

Si la aplicación ha establecido un identificador de sesión FTP en el servidor con [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), la aplicación puede llamar a [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con el nombre de archivo existente y con un nuevo nombre para el archivo almacenado localmente. A continuación, la aplicación puede utilizar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para descargar el archivo. Esto permite que la aplicación controle mejor la descarga y mantiene la conexión con el servidor FTP, por lo que se pueden ejecutar más comandos.

Si la aplicación no necesita un control estricto sobre la descarga, la aplicación puede usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) con el identificador de sesión FTP, el nombre de archivo remoto y el nombre de archivo local para recuperar el archivo. [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) realiza toda la contabilidad y la sobrecarga asociada con la lectura de un archivo desde un servidor FTP y su almacenamiento local.

En el ejemplo siguiente se recupera un archivo de un servidor FTP y se guarda localmente. El nombre del archivo en el servidor FTP se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nFtpFileNameId* y el nombre local en el que se guarda el archivo se toma del cuadro de edición, cuyo IDC se pasa en el parámetro *nLocalFileNameId* . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.


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

Una aplicación que debe enviar datos a un servidor FTP, pero no tiene un archivo local que contenga todos los datos, debe utilizar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) para crear y abrir un archivo en el servidor FTP. A continuación, la aplicación puede utilizar [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para cargar la información en el archivo.

Si el archivo ya existe localmente, la aplicación puede utilizar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) para cargar el archivo en el servidor FTP. [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) realiza toda la sobrecarga que se produce al cargar un archivo local en un servidor FTP remoto.

En el ejemplo siguiente se copia un archivo local en el servidor FTP. El nombre local del archivo se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nLocalFileNameId* y el nombre con el que se guarda el archivo en el servidor FTP se toma del cuadro de edición, cuyo IDC se pasa en el parámetro *nFtpFileNameId* . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.


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

Para eliminar un archivo de un servidor FTP, utilice la función [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . La aplicación que realiza la llamada debe tener los privilegios necesarios para eliminar un archivo del servidor FTP.

En el ejemplo siguiente se elimina un archivo del servidor FTP. El nombre del archivo que se va a eliminar se toma del cuadro de edición del cuadro de diálogo primario, cuyo IDC se pasa int al parámetro *nFtpFileNameId* . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP. Puesto que esta función no actualiza los listados de archivos ni la presentación de directorios, el proceso de llamada debería hacerlo tras una eliminación correcta.


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

Se puede cambiar el nombre de los archivos y directorios de un servidor FTP mediante la función [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) . [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) acepta dos cadenas terminadas en **null** que contienen nombres parciales o completos en relación con el directorio actual. La función cambia el nombre del archivo designado por la primera cadena por el nombre designado por la segunda cadena.

En el ejemplo siguiente se cambia el nombre de un archivo o directorio en el servidor FTP. El nombre actual del archivo o directorio se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nOldFileNameId* y el nuevo nombre se toma del cuadro de edición, cuyo IDC se pasa en el parámetro *nNewFileNameId* . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP. Puesto que esta función no actualiza los listados de archivos ni la presentación de directorios, el proceso de llamada debería hacerlo tras cambiar el nombre correctamente.


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
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 