---
title: Control de localizadores uniformes de recursos
description: Un localizador uniforme de recursos (URL) es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419433c8a06b6243bf048896664a67da31a3c58d1d79eb6fea65f9fc99dbe63a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121875"
---
# <a name="handling-uniform-resource-locators"></a>Control de localizadores uniformes de recursos

Un localizador uniforme de recursos (URL) es una representación compacta de la ubicación y el método de acceso de un recurso ubicado en Internet. Cada dirección URL consta de un esquema (HTTP, HTTPS o FTP) y una cadena específica del esquema. Esta cadena también puede incluir una combinación de una ruta de acceso de directorio, una cadena de búsqueda o el nombre del recurso. Las funciones de WinINet proporcionan la capacidad de crear, combinar, dividir y canonizar direcciones URL. Para obtener más información sobre las direcciones URL, [vea RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) en Localizadores uniformes de recursos (URL).

Las funciones de dirección URL funcionan de forma orientada a tareas. No se comprueba el contenido y el formato de la dirección URL que se da a la función. La aplicación que realiza la llamada debe realizar un seguimiento del uso de estas funciones para asegurarse de que los datos están en el formato previsto. Por ejemplo, la función [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) convertiría el carácter "%" en la secuencia de escape "%25" cuando no se usa ninguna marca. Si [**InternetCanicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) se usa en la dirección URL canónica, la secuencia de escape "%25" se convertiría en la secuencia de escape "%2525", que no funcionaría correctamente.

-   [¿Qué es una dirección URL canónica?](#what-is-a-canonicalized-url)
-   [Uso de las funciones de WinINet para controlar direcciones URL](#using-the-wininet-functions-to-handle-urls)
-   [Canonización de direcciones URL](#what-is-a-canonicalized-url)
-   [Combinación de direcciones URL base y relativas](#combining-base-and-relative-urls)
-   [Descifrar direcciones URL](#cracking-urls)
-   [Creación de direcciones URL](#creating-urls)
-   [Acceso directo a direcciones URL](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>¿Qué es una dirección URL canónica?

El formato de todas las direcciones URL debe seguir la sintaxis y semántica aceptadas para acceder a los recursos a través de Internet. La canonización es el proceso de dar formato a una dirección URL para seguir esta sintaxis y semántica aceptadas.

Los caracteres que se deben codificar incluyen los caracteres que no tienen ningún carácter gráfico correspondiente en el juego de caracteres codificados US-ASCII (hexadecimal 80-FF, que no se usan en el juego de caracteres codificados US-ASCII, y hexadecimales 00-1F y 7F, que son caracteres de control), espacios en blanco, "%" (que se usa para codificar otros caracteres) y caracteres no seguros (<, >, ", \# , {, }, \| , , \\ ^, ~, \[ , y \] ').

## <a name="using-the-wininet-functions-to-handle-urls"></a>Uso de las funciones de WinINet para controlar direcciones URL

En la tabla siguiente se resumen las funciones de dirección URL.



| Función                                                   | Descripción                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**InternetNtenicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Canoniza la dirección URL.                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Combina direcciones URL base y relativas.                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analiza una cadena de dirección URL en componentes.               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Crea una cadena de dirección URL a partir de componentes.              |
| [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Comienza a recuperar un recurso FTP, HTTP o HTTPS. |



 

## <a name="canonicalizing-urls"></a>Canonización de direcciones URL

La canonización de una dirección URL es el proceso que convierte una dirección URL, que puede contener caracteres no seguros, como espacios en blanco, caracteres reservados, entre otros, en un formato aceptado.

La [**función InternetCanicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) se puede usar para canonizar las direcciones URL. Esta función está muy orientada a tareas, por lo que la aplicación debe realizar un seguimiento de su uso con cuidado. [**InternetCanicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) no comprueba que la dirección URL que se le ha pasado ya está canónica y que la dirección URL que devuelve es válida.

Las cinco marcas siguientes controlan cómo [**InternetCanalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) controla una dirección URL determinada. Las marcas se pueden usar en combinación. Si no se usa ninguna marca, la función codifica la dirección URL de forma predeterminada.



| Value                     | Significado                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO EXPLORADOR DE ICU \_ \_        | No debe codificar ni descodificar caracteres después de " " o "?", y no quite el espacio en blanco \# final después de "?". Si no se especifica este valor, se codifica toda la dirección URL y se quita el espacio en blanco final. |
| DESCODIFICACIÓN \_ DE ICU               | Convierta todas las secuencias %XX en caracteres, incluidas las secuencias de escape, antes de analizar la dirección URL.                                                                                                          |
| SOLO \_ CODIFICACIÓN DE \_ ESPACIOS DE ICU \_ | Codificar solo espacios.                                                                                                                                                                                     |
| ICU \_ NO \_ ENCODE           | No convierta caracteres no seguros en secuencias de escape.                                                                                                                                                   |
| ICU \_ NO \_ META             | No quite las meta secuencias (como "." y "..") de la dirección URL.                                                                                                                                       |



 

La marca DECODE de ICU solo debe usarse en direcciones URL canónicas, ya que supone que todas las secuencias %XX son códigos de escape y las convierte en los caracteres indicados por el \_ código. Si la dirección URL tiene un símbolo "%" que no forma parte de un código de escape, ICU DECODE todavía lo \_ trata como uno. Esta característica puede hacer [**que InternetCanicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) cree una dirección URL no válida.

Para usar [**InternetCanonicalizeUrl para**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) devolver una dirección URL completamente descodificada, se deben especificar las marcas \_ ICU DECODE e ICU NO \_ \_ ENCODE. Esta configuración supone que la dirección URL que se pasa [**a InternetCanicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) se ha canónico previamente.

## <a name="combining-base-and-relative-urls"></a>Combinación de direcciones URL base y relativas

Una dirección URL relativa es una representación compacta de la ubicación de un recurso en relación con una dirección URL base absoluta. El analizador debe conocer la dirección URL base y normalmente incluye el esquema, la ubicación de red y las partes de la ruta de acceso de la dirección URL. Una aplicación puede llamar a [**InternetCombineUrl para**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) combinar la dirección URL relativa con su dirección URL base. [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) también canoniza la dirección URL resultante.

## <a name="cracking-urls"></a>Descifrar direcciones URL

La [**función InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) separa una dirección URL en sus partes de componente y devuelve los componentes indicados por la estructura [**\_ COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) de dirección URL que se pasa a la función.

Los componentes que son la estructura COMPONENTES DE [**DIRECCIÓN URL \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) son el número de esquema, el nombre de host, el número de puerto, el nombre de usuario, la contraseña, la ruta de acceso url y la información adicional (por ejemplo, los parámetros de búsqueda). Cada componente, excepto los números de esquema y puerto, tiene un miembro de cadena que contiene la información y un miembro que contiene la longitud del miembro de cadena. Los números de esquema y puerto solo tienen un miembro que almacena el valor correspondiente; Ambos se devuelven en todas las llamadas correctas [**a InternetCrackUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)

Para obtener el valor de un componente determinado en la estructura COMPONENTES DE DIRECCIÓN [**URL, \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) el miembro que almacena la longitud de cadena de ese componente debe establecerse en un valor distinto de cero. El miembro de cadena puede ser la dirección de un búfer o **NULL.**

Si el miembro de puntero contiene la dirección de un búfer, el miembro de longitud de cadena debe contener el tamaño de ese búfer. [**InternetCrackUrl devuelve**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) la información del componente como una cadena en el búfer y almacena la longitud de la cadena en el miembro de longitud de cadena.

Si el miembro de puntero **es NULL**, el miembro de longitud de cadena se puede establecer en cualquier valor distinto de cero. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) almacena la dirección del primer carácter de la cadena de dirección URL que contiene la información del componente y establece la longitud de la cadena en el número de caracteres de la parte restante de la cadena de dirección URL que pertenece al componente.

Todos los miembros de puntero establecidos **en NULL** con un punto de miembro de longitud distinta de cero al punto inicial adecuado en la cadena de dirección URL. La longitud almacenada en el miembro de longitud debe usarse para determinar el final de la información del componente individual.

Para terminar de inicializar correctamente la estructura COMPONENTES DE DIRECCIÓN [**URL, \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) el **miembro dwStructSize** debe establecerse en el tamaño de la estructura COMPONENTES DE DIRECCIÓN [**URL, \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) en bytes.

En el ejemplo siguiente se devuelven los componentes de la dirección URL del cuadro de edición, IDC PreOpen1, y se devuelven los componentes al cuadro de \_ lista, IDC \_ PreOpenList. Para mostrar solo la información de un componente individual, esta función copia el carácter inmediatamente después de la información del componente en la cadena y la reemplaza temporalmente por un **valor NULL.**


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Creación de direcciones URL

La [**función InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) usa la información de la estructura [**COMPONENTES \_ DE DIRECCIÓN URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) para crear un localizador uniforme de recursos.

Los componentes que forma la estructura COMPONENTES DE [**DIRECCIÓN URL \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) son el esquema, el nombre de host, el número de puerto, el nombre de usuario, la contraseña, la ruta de acceso url y la información adicional (por ejemplo, los parámetros de búsqueda). Cada componente, excepto el número de puerto, tiene un miembro de cadena que contiene la información y un miembro que contiene la longitud del miembro de cadena.

Para cada componente necesario, el miembro de puntero debe contener la dirección del búfer que contiene la información. El miembro de longitud debe establecerse en cero si el miembro de puntero contiene la dirección de una cadena terminada en cero; el miembro length debe establecerse en la longitud de cadena si el miembro de puntero contiene la dirección de una cadena que no termina en cero. El miembro de puntero de los componentes que no son necesarios debe ser **NULL.**

## <a name="accessing-urls-directly"></a>Acceso directo a direcciones URL

Se puede acceder directamente a los recursos FTP y HTTP de Internet mediante las funciones [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetFindNextFile.**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) abre una conexión al recurso en la dirección URL que se pasa a la función. Cuando se establece esta conexión, hay dos pasos posibles. En primer lugar, si el recurso es un archivo, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) puede descargarlo; en segundo lugar, si el recurso es un directorio, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) puede enumerar los archivos dentro del directorio (excepto cuando se usan servidores proxy CERN). Para obtener más información sobre [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), vea [Leer archivos](common-functions.md). Para obtener más información sobre [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), vea [Finding the Next File](common-functions.md).

En el caso de las aplicaciones que necesitan funcionar a través de un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) se puede usar para acceder a archivos y directorios FTP. Las solicitudes FTP se empaquetan para que aparezcan como una solicitud HTTP, que el proxy CERN aceptaría.

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por la [**función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) y la dirección URL del recurso. La dirección URL debe incluir el esquema (http:, ftp:, file: para un archivo local o https: para el protocolo de \[ \] \[ hipertexto seguro) y la ubicación de \] red (como `www.microsoft.com` ). La dirección URL también puede incluir una ruta de acceso (por ejemplo, /isapi/gomscom.asp? TARGET=/windows/feature/) y el nombre del recurso (por ejemplo, default.htm). Para las solicitudes HTTP o HTTPS, se pueden incluir encabezados adicionales.

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo direcciones URL HTTP o HTTPS) pueden usar el identificador creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para descargar el recurso.

En el diagrama siguiente se muestran los identificadores que se usarán con cada función.

![identificadores que se usan con funciones](images/ax-wnt02.png)

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)usa el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz creado [**por InternetOpen.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (no se muestra aquí) e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo direcciones URL HTTP o HTTPS) pueden usar el identificador **HINTERNET** creado por [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

Para obtener más información, vea [**HINTERNET Handles**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 