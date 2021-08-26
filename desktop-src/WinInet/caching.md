---
title: Almacenamiento en caché (Windows Internet)
description: Las funciones de WinINet tienen compatibilidad con el almacenamiento en caché integrado simple, pero flexible.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea485e1c6fc8b2b474d217d940c715b65b45de8f7d211ad37bff9bdd9a4243b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955615"
---
# <a name="caching-windows-internet"></a>Almacenamiento en caché (Windows Internet)

Las funciones de WinINet tienen compatibilidad con el almacenamiento en caché integrado simple, pero flexible. Los datos recuperados de la red se almacenan en caché en el disco duro y se recuperan para las solicitudes posteriores. La aplicación puede controlar el almacenamiento en caché en cada solicitud. Para las solicitudes HTTP del servidor, la mayoría de los encabezados recibidos también se almacenan en caché. Cuando se satisface una solicitud HTTP desde la memoria caché, los encabezados almacenados en caché también se devuelven al autor de la llamada. Esto hace que la descarga de datos sea perfecta, independientemente de si los datos vienen de la memoria caché o de la red.

Las aplicaciones deben asignar correctamente un búfer para obtener los resultados deseados al usar las funciones de almacenamiento en caché de direcciones URL persistentes. Para obtener más información, [vea Using Buffers](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Comportamiento de la caché durante el procesamiento de respuestas

La caché de WinINet es compatible con las directivas de control de caché HTTP descritas en RFC 2616. Las directivas de control de caché y las marcas del conjunto de aplicaciones determinan lo que se puede almacenar en caché. Sin embargo, WinINet determina lo que realmente se almacena en caché en función del criterio siguiente:

-   WinINet solo almacena en caché las respuestas HTTP y FTP.
-   Solo una caché puede almacenar las respuestas bien comportadas y usarse en una respuesta a una solicitud posterior. Las respuestas bien comportadas se definen como respuestas que devuelven correctamente.
-   De forma predeterminada, WinINet almacenará en caché las respuestas correctas a menos que una directiva de control de caché del servidor o una marca definida por la aplicación denota específicamente que la respuesta no se puede almacenar en caché.
-   En general, las respuestas al verbo GET se almacenan en caché si se cumplen los requisitos indicados anteriormente. Las respuestas a los verbos PUT y POST no se almacenan en caché en ninguna circunstancia.
-   Los elementos se almacenarán en caché incluso cuando la memoria caché esté llena. Si un elemento agregado coloca la memoria caché por encima del límite de tamaño, se programa el scaveier de caché. De forma predeterminada, no se garantiza que los elementos permanezcan más de 10 minutos en la memoria caché. Para obtener más información, consulte la [sección Cache Scavenger a](#cache-scavenger) continuación.
-   Https se almacena en caché de forma predeterminada. Esto se administra mediante una configuración global que no se puede invalidar mediante directivas de caché definidas por la aplicación. Para invalidar la configuración global, seleccione el applet Opciones de Internet en el panel de control y vaya a la pestaña Avanzadas. Active la casilla "No guardar páginas cifradas en el disco" en la sección "Seguridad".

## <a name="cache-scavenger"></a>Scaveave de caché

El scaveier de caché limpia periódicamente los elementos de la memoria caché. Si se agrega un elemento a la memoria caché y la memoria caché está llena, el elemento se agrega a la memoria caché y se programa el scaveier de caché. Si la búsqueda de caché completa una ronda de scavenging y la memoria caché no ha alcanzado el límite de caché, el scavering se programa para otra ronda cuando se agrega otro elemento a la memoria caché. En general, el scaveier se programa cuando un elemento agregado coloca la memoria caché por encima de su límite de tamaño. De forma predeterminada, el tiempo mínimo de vida en la memoria caché se establece en 10 minutos a menos que se especifique lo contrario en una directiva cache-control. Cuando se inicia la búsqueda de caché, no hay ninguna garantía de que los elementos más antiguos sean los primeros en eliminarse de la memoria caché.

La memoria caché se comparte entre todas las aplicaciones WinINet del equipo para el mismo usuario. A partir de Windows Vista y Windows Server 2008, el tamaño de caché se establece en 1/32 como el tamaño del disco, con un tamaño mínimo de 8 MB y un tamaño máximo de 50 MB.

## <a name="using-flags-to-control-caching"></a>Uso de marcas para controlar el almacenamiento en caché

Las marcas de almacenamiento en caché permiten a una aplicación controlar cuándo y cómo usa la memoria caché. Estas marcas se pueden usar solas o en combinación con el parámetro *dwFlags* en funciones que acceden a información o recursos en Internet. De forma predeterminada, las funciones almacenan todos los datos descargados de Internet.

Las marcas siguientes se pueden usar para controlar el almacenamiento en caché.



| Value                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SINCRONIZACIÓN \_ DE CACHÉ DE LA MARCA DE \_ \_ INTERNET**](api-flags.md)                                                                            | Esta marca no tiene efecto.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**CACHÉ \_ DE LA MARCA DE INTERNET SI SE PRODUCIRÁ UN ERROR EN LA \_ \_ \_ \_ RED**](api-flags.md)                                                              | Devuelve el recurso de la memoria caché si se produce un error en la solicitud de red para el recurso debido a un error de ERROR [ \_ INTERNET CONNECTION \_ \_ RESET](wininet-errors.md) o [ERROR INTERNET CANNOT \_ \_ \_ CONNECT.](wininet-errors.md) HttpOpenRequest usa esta [**marca.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                                                                              |
| [**INTERNET \_ FLAG \_ DONT \_ CACHE**](api-flags.md)                                                                              | No almacena en caché los datos, ya sea localmente o en ninguna puerta de enlace. Idéntico al valor preferido, [**INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Indica que se trata de un envío de formularios.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**INTERNET \_ ENVÍO DE \_ \_ FORMULARIOS DE**](api-flags.md)[**MARCA DE INTERNET DE MARCA \_ DE \_ CACHÉ \_**](api-flags.md) | No realiza solicitudes de red. Todas las entidades se devuelven desde la memoria caché. Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como ERROR \_ FILE \_ NOT \_ FOUND. Solo la [**función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.                                                                                                                                                                                                       |
| [**INTERNET \_ FLAG \_ FWD \_ BACK**](api-flags.md)                                                                                  | Indica que la función debe usar la copia del recurso que se encuentra actualmente en la caché de Internet. No se comprueba la fecha de expiración ni otra información sobre el recurso. Si el elemento solicitado no se encuentra en la caché de Internet, el sistema intenta localizar el recurso en la red. Este valor se introdujo en Microsoft Internet Explorer 5  y  está asociado a las operaciones de botón Reenviar y Atrás de Internet Explorer. |
| [**HIPERVÍNCULO \_ DE MARCA DE \_ INTERNET**](api-flags.md)                                                                                 | Obliga a la aplicación a volver a cargar un recurso si no se ha devuelto ninguna hora de expiración y no se ha devuelto ninguna hora de última modificación cuando el recurso se ha almacenado en la memoria caché.                                                                                                                                                                                                                                                                                                                  |
| [**MARCA DE INTERNET \_ \_ MAKE \_ PERSISTENT**](api-flags.md)                                                                    | Ya no se admite.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**LA MARCA DE INTERNET \_ DEBE ALMACENAR EN CACHÉ LA \_ \_ \_ SOLICITUD**](api-flags.md)                                                             | Hace que se cree un archivo temporal si no se puede almacenar en caché. Es idéntico al valor preferido, [**INTERNET \_ FLAG NEED \_ \_ FILE**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**INTERNET \_ FLAG \_ NEED \_ FILE**](api-flags.md)                                                                                | Hace que se cree un archivo temporal si no se puede almacenar en caché.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**MARCA DE INTERNET \_ \_ SIN ESCRITURA EN \_ \_ CACHÉ**](api-flags.md)                                                                     | Rechaza cualquier intento de la función de almacenar los datos descargados de Internet en la memoria caché. Esta marca es necesaria si la aplicación no quiere que los recursos descargados se almacenen localmente.                                                                                                                                                                                                                                                               |
| [**INTERNET \_ FLAG \_ NO \_ UI**](api-flags.md)                                                                                        | Deshabilita el cuadro de diálogo cookie. [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pueden usar esta marca (solo solicitudes HTTP).                                                                                                                                                                                                                                                                                          |
| [**INTERNET \_ FLAG \_ OFFLINE**](api-flags.md)                                                                                     | Impide que la aplicación envíe solicitudes a la red. Todas las solicitudes se resuelven mediante los recursos almacenados en la memoria caché. Si el recurso no está en la memoria caché, se devuelve un error adecuado, como ERROR \_ FILE \_ NOT \_ FOUND.                                                                                                                                                                                                                            |
| [**MARCA DE INTERNET \_ \_ PRAGMA \_ NOCACHE**](api-flags.md)                                                                      | Obliga a que el servidor de origen resuelva la solicitud, incluso si existe una copia almacenada en caché en el proxy. La [**función InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en solicitudes HTTP y HTTPS) y la [**función HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca.                                                                                                                                                                                               |
| [**RECARGA \_ DE LA MARCA DE \_ INTERNET**](api-flags.md)                                                                                       | Fuerza a la función a recuperar el recurso solicitado directamente desde Internet. La información que se descarga se almacena en la memoria caché.                                                                                                                                                                                                                                                                                                                     |
| [**\_RESINCRONIZACIÓN DE \_ LA MARCA DE INTERNET**](api-flags.md)                                                                         | Hace que una aplicación realice una descarga condicional del recurso desde Internet. Si la versión almacenada en la memoria caché es actual, la información se descarga de la memoria caché. De lo contrario, la información se vuelve a cargar desde el servidor.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Funciones de almacenamiento en caché persistentes

Los clientes que necesitan servicios de almacenamiento en caché persistentes usan las funciones de almacenamiento en caché persistentes para permitir que sus aplicaciones guarden datos en el sistema de archivos local para su uso posterior, como en situaciones en las que un vínculo de ancho de banda bajo limita el acceso a los datos o el acceso no está disponible en absoluto.

Las funciones de caché proporcionan almacenamiento en caché persistente y exploración sin conexión. A menos [**que la marca INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE**](api-flags.md) no especifique explícitamente ningún almacenamiento en caché, las funciones almacenarán en caché todos los datos descargados de la red. Las respuestas a los datos POST no se almacenan en caché.

## <a name="using-the-persistent-url-cache-functions"></a>Uso de las funciones de caché de direcciones URL persistentes

Las siguientes funciones de caché de direcciones URL persistentes permiten a una aplicación acceder a la información almacenada en la memoria caché y manipularla.



| Función                                                           | Descripción                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Almacena en caché los datos del archivo especificado en el almacenamiento de caché y los asocia a la dirección URL especificada.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Almacena en caché los datos del archivo especificado en el almacenamiento de caché y los asocia a la dirección URL especificada.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Asigna el almacenamiento en caché solicitado y crea un nombre de archivo local para guardar la entrada de caché correspondiente al nombre de origen.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Genera una identificación del grupo de caché.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Quita el archivo asociado al nombre de origen de la memoria caché, si el archivo existe.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Libera un **GROUPID y** cualquier estado asociado en el archivo de índice de caché.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Cierra el identificador de enumeración especificado.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Comienza la enumeración de la memoria caché.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Comienza una enumeración filtrada de la memoria caché.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Recupera la siguiente entrada de la memoria caché.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Recupera la siguiente entrada en una enumeración de caché filtrada.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Recupera información sobre una entrada de caché.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Busca la dirección URL después de traducir los redireccionamientos almacenados en caché que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)aplicaría en modo sin conexión.           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Lee los datos almacenados en caché de una secuencia que se ha abierto [**mediante RetrieveUrlCacheEntryStream.**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Recupera una entrada de caché de la memoria caché en forma de archivo.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Proporciona la manera más eficaz e independiente de la implementación de acceder a los datos de caché.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Agrega o quita entradas de un grupo de caché.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Establece los miembros especificados de la estructura [**INTERNET \_ CACHE ENTRY \_ \_ INFO.**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Desbloquea la entrada de caché que se bloqueó cuando se recuperó el archivo para su uso desde la memoria caché [**mediante RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea). |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Cierra la secuencia que se ha recuperado mediante [**RetrieveUrlCacheEntryStream.**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)                                           |



 

### <a name="enumerating-the-cache"></a>Enumeración de la caché

Las [**funciones FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) y [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumeran la información almacenada en la memoria caché. [**FindFirstUrlCacheEntry inicia**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) la enumeración tomando un patrón de búsqueda, un búfer y un tamaño de búfer para crear un identificador y devolver la primera entrada de caché. [**FindNextUrlCacheEntry toma**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) el identificador creado por [**FindFirstUrlCacheEntry,**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)un búfer y un tamaño de búfer para devolver la siguiente entrada de caché.

Ambas funciones almacenan una estructura [**INTERNET \_ CACHE ENTRY \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) en el búfer. El tamaño de esta estructura varía para cada entrada. Si el tamaño de búfer pasado a cualquiera de las funciones es insuficiente, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ INSUFFICIENT \_ BUFFER. La variable de tamaño de búfer contiene el tamaño de búfer necesario para recuperar esa entrada de caché. Se debe asignar un búfer del tamaño indicado por la variable de tamaño de búfer y se debe llamar de nuevo a la función con el nuevo búfer.

La estructura [**INTERNET \_ CACHE ENTRY \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) contiene el tamaño de la estructura, la dirección URL de la información almacenada en caché, el nombre de archivo local, el tipo de entrada de caché, el recuento de uso, la tasa de aciertos, el tamaño, la hora de la última modificación, la expiración, el último acceso, la hora de la última sincronización, la información de encabezado, el tamaño de la información de encabezado y la extensión de nombre de archivo.

La [**función FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) toma un patrón de búsqueda, un búfer que almacena la estructura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) y el tamaño del búfer. Actualmente, solo se implementa el patrón de búsqueda predeterminado, que devuelve todas las entradas de caché.

Una vez enumerada la memoria caché, la aplicación debe llamar a [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) para cerrar el identificador de enumeración de caché.

En el ejemplo siguiente se muestra la dirección URL de cada entrada de caché en un cuadro de lista, **IDC \_ CacheList**. Usa MAX CACHE ENTRY INFO SIZE para asignar inicialmente un búfer, ya que las primeras versiones de la \_ \_ API de \_ WinINet no enumeran la memoria caché correctamente de \_ lo contrario. Las versiones posteriores enumeran la memoria caché correctamente y no hay ningún límite de tamaño de caché. Todas las aplicaciones que se ejecutan en equipos con la versión de la API WinINet de Internet Explorer 4.0 deben asignar un búfer del tamaño necesario. Para obtener más información, [vea Using Buffers](appendix-b-using-buffers.md).


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>Recuperar información de entrada de caché

La [**función GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) permite recuperar la estructura [**DE INFORMACIÓN INTERNET CACHE ENTRY \_ \_ \_ para**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) la dirección URL especificada. Esta estructura contiene el tamaño de la estructura, la dirección URL de la información almacenada en caché, el nombre de archivo local, el tipo de entrada de caché, el recuento de uso, la tasa de aciertos, el tamaño, la hora de la última modificación, la expiración, el último acceso, la hora de la última sincronización, la información de encabezado, el tamaño de la información de encabezado y la extensión de nombre de archivo.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) acepta una dirección URL, un búfer para una estructura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) y el tamaño del búfer. Si se encuentra la dirección URL, la información se copia en el búfer. De lo contrario, se produce un error en la [**función y GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ FILE NOT \_ \_ FOUND. Si el tamaño del búfer no es suficiente para almacenar la información de entrada de caché, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ INSUFFICIENT \_ BUFFER. El tamaño necesario para recuperar la información se almacena en la variable de tamaño de búfer.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) no realiza ningún análisis de direcciones URL, por lo que no se encontrará una dirección URL que contenga un delimitador ( ) en la memoria caché, incluso si el recurso está almacenado en \# caché. Por ejemplo, si se pasa la dirección URL " " , la función devuelve https://example.com/example.htm\#sample ERROR FILE NOT FOUND aunque " " esté en la memoria \_ \_ \_ https://example.com/example.htm caché.

En el ejemplo siguiente se recupera la información de entrada de caché de la dirección URL especificada. A continuación, la función muestra la información del encabezado en el **cuadro de edición \_ CacheDump de IDC.**


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>Creación de una entrada de caché

Una aplicación usa las [**funciones CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) [**y CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) para crear una entrada de caché.

[**CreateUrlCacheEntry acepta la**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) dirección URL, el tamaño de archivo esperado y la extensión de nombre de archivo. A continuación, la función crea un nombre de archivo local para guardar la entrada de caché que corresponde a la dirección URL y la extensión de nombre de archivo.

Con el nombre de archivo local, escriba los datos en el archivo local. Una vez escritos los datos en el archivo local, la aplicación debe llamar a [**CommitUrlCacheEntry.**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) acepta la dirección URL, el nombre de archivo local, la expiración, la hora de la última modificación, el tipo de entrada de caché, la información de encabezado, el tamaño de la información de encabezado y la extensión de nombre de archivo. A continuación, la función almacena en caché los datos del archivo especificado en el almacenamiento en caché y los asocia a la dirección URL especificada.

En el ejemplo siguiente se usa el nombre de archivo local, creado por una llamada anterior a [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), almacenado en el cuadro de **texto, IDC \_ LocalFile**, para almacenar el texto del cuadro de texto, **IDC \_ CacheDump**, en la entrada de caché. Una vez que los datos se han escrito en el archivo mediante **fopen**, **fprintf** y **fclose**, la entrada se confirma mediante [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>Eliminación de una entrada de caché

La [**función DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) toma una dirección URL y quita el archivo de caché asociado a ella. Si el archivo de caché no existe, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ FILE NOT \_ \_ FOUND. Si el archivo de caché está bloqueado actualmente o en uso, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ ACCESS \_ DENIED. El archivo se elimina cuando se desbloquea.

### <a name="retrieving-cache-entry-files"></a>Recuperar archivos de entrada de caché

Para las aplicaciones que requieren el nombre de archivo de un recurso, use las funciones [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) y [**UnlockUrlCacheEntryFile.**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) Las aplicaciones que no requieren el nombre de archivo deben usar las funciones [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)y [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) para recuperar la información de la memoria caché.

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) no realiza ningún análisis de direcciones URL, por lo que no se encontrará una dirección URL que contenga un delimitador ( ) en la memoria caché, incluso si el recurso está almacenado en \# caché. Por ejemplo, si se pasa la dirección URL " " , la función devuelve https://example.com/example.htm\#sample ERROR FILE NOT FOUND aunque " " esté en la memoria \_ \_ \_ https://example.com/example.htm caché.

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) acepta una dirección URL, un búfer que almacena la estructura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) y el tamaño del búfer. La función se recupera y bloquea para el autor de la llamada.

Una vez que se ha usado la información del archivo, la aplicación debe llamar a [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) para desbloquear el archivo.

### <a name="cache-groups"></a>Grupos de caché

Para crear un grupo de caché, se debe llamar a la función [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) para generar un **GROUPID** para el grupo de caché. Las entradas se pueden agregar al grupo de caché si se proporciona la dirección URL de la entrada de caché y la marca INTERNET CACHE GROUP ADD a la \_ \_ función \_ [**SetUrlCacheEntryGroup.**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) Para quitar una entrada de caché de un grupo, pase la dirección URL de la entrada de caché y la marca INTERNET CACHE GROUP REMOVE a \_ \_ \_ [**SetUrlCacheEntryGroup.**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)

Las [**funciones FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) y [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) se pueden usar para enumerar las entradas de un grupo de caché especificado. Una vez completada la enumeración, la función debe llamar a [**FindCloseUrlCache.**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)

## <a name="handling-structures-with-variable-size-information"></a>Control de estructuras con información de tamaño variable

La memoria caché puede contener información de tamaño variable para cada dirección URL almacenada. Esto se refleja en la estructura [**INTERNET \_ CACHE ENTRY \_ \_ INFO.**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Cuando las funciones de caché devuelven esta estructura, crean un búfer que siempre es el tamaño de [**INTERNET \_ CACHE ENTRY \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) más cualquier información de tamaño variable. Si un miembro de puntero no es **NULL,** apunta al área de memoria inmediatamente después de la estructura . Al copiar el búfer devuelto por una función en otro búfer, los miembros del puntero deben ser fijos para que apunten al lugar adecuado en el nuevo búfer, como se muestra en el ejemplo siguiente.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Algunas funciones de caché producirán un error con el mensaje de error ERROR INSUFFICIENT BUFFER si especifica un búfer demasiado pequeño para contener la información de entrada de caché recuperada \_ \_ por la función. En este caso, la función también devuelve el tamaño necesario del búfer. A continuación, puede asignar un búfer del tamaño adecuado y volver a llamar a la función.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 
