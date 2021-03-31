---
title: Almacenamiento en caché (Internet de Windows)
description: Las funciones WinINet tienen compatibilidad con almacenamiento en caché simple, pero flexible y integrada.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149793"
---
# <a name="caching-windows-internet"></a>Almacenamiento en caché (Internet de Windows)

Las funciones WinINet tienen compatibilidad con almacenamiento en caché simple, pero flexible y integrada. Los datos recuperados de la red se almacenan en la memoria caché del disco duro y se recuperan para las solicitudes posteriores. La aplicación puede controlar el almacenamiento en caché en cada solicitud. En el caso de las solicitudes HTTP del servidor, la mayoría de los encabezados recibidos también se almacenan en caché. Cuando se satisface una solicitud HTTP de la memoria caché, los encabezados almacenados en caché también se devuelven al autor de la llamada. Esto hace que los datos se descarguen sin problemas, independientemente de si los datos proceden de la memoria caché o de la red.

Las aplicaciones deben asignar correctamente un búfer para obtener los resultados deseados al utilizar las funciones de almacenamiento en caché de URL persistentes. Para obtener más información, consulte [uso de búferes](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Comportamiento de caché durante el procesamiento de la respuesta

La caché de WinINet es compatible con las directivas de control de caché HTTP descritas en RFC 2616. Las directivas de control de caché y las marcas de conjunto de aplicaciones determinan lo que se puede almacenar en caché. sin embargo, WinINet determina lo que realmente se almacena en la memoria caché en función del criterio siguiente:

-   WinINet solo almacena en caché las respuestas HTTP y FTP.
-   Solo las respuestas con buen comportamiento pueden almacenarse en una memoria caché y utilizarse en una respuesta a una solicitud posterior. Las respuestas con buen comportamiento se definen como respuestas que se devuelven correctamente.
-   De forma predeterminada, WinINet almacenará en caché las respuestas correctas a menos que una directiva cache-control del servidor o una marca definida por la aplicación denoten específicamente que la respuesta no se puede almacenar en caché.
-   En general, las respuestas al verbo GET se almacenan en caché si se cumplen los requisitos mencionados anteriormente. Las respuestas a los verbos PUT y POST no se almacenan en caché bajo ninguna circunstancia.
-   Los elementos se almacenarán en caché incluso cuando la memoria caché esté llena. Si un elemento agregado coloca la memoria caché en el límite de tamaño, se programa el borrador de caché. De forma predeterminada, no se garantiza que los elementos sigan siendo más de 10 minutos en la memoria caché. Para obtener más información, vea la sección sobre el [borrador de caché](#cache-scavenger) más adelante.
-   Https está almacenado en caché de forma predeterminada. Se administra mediante una configuración global que no se puede invalidar mediante directivas de caché definidas por la aplicación. Para invalidar la configuración global, seleccione el applet opciones de Internet en el panel de control y vaya a la pestaña avanzadas. Active la casilla "no guardar páginas cifradas en el disco" en la sección "seguridad".

## <a name="cache-scavenger"></a>Limpieza de caché

El borrador de caché limpia periódicamente los elementos de la memoria caché. Si se agrega un elemento a la memoria caché y la memoria caché está llena, el elemento se agrega a la memoria caché y se programa el borrador de caché. Si el borrador de caché completa una ronda de eliminación de registros obsoletos y la memoria caché no alcanzó el límite de caché, el borrador se programa para otro redondeo cuando se agrega otro elemento a la memoria caché. En general, el borrador se programa cuando un elemento agregado coloca la memoria caché a lo largo de su límite de tamaño. De forma predeterminada, el período de vida mínimo en la memoria caché se establece en 10 minutos, a menos que se especifique lo contrario en una directiva cache-control. Cuando se inicia el borrador de caché, no hay ninguna garantía de que los elementos más antiguos sean los primeros que se eliminarán de la memoria caché.

La memoria caché se comparte entre todas las aplicaciones WinINet del equipo para el mismo usuario. A partir de Windows Vista y Windows Server 2008, el tamaño de la caché se establece en 1/32 º el tamaño del disco, con un tamaño mínimo de 8 MB y un tamaño máximo de 50 MB.

## <a name="using-flags-to-control-caching"></a>Usar marcas para controlar el almacenamiento en caché

Las marcas de almacenamiento en caché permiten que una aplicación controle cuándo y cómo usa la memoria caché. Estas marcas se pueden utilizar por sí solas o en combinación con el parámetro *dwFlags* en las funciones que tienen acceso a la información o a los recursos de Internet. De forma predeterminada, las funciones almacenan todos los datos descargados de Internet.

Las marcas siguientes se pueden usar para controlar el almacenamiento en caché.



| Value                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**caché de marcas de INTERNET \_ \_ \_ asincrónica**](api-flags.md)                                                                            | Esta marca no tiene efecto.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**caché de marcas de INTERNET \_ \_ si se \_ \_ \_ produce un error de red**](api-flags.md)                                                              | Devuelve el recurso de la memoria caché si se produce un error en la solicitud de red para el recurso debido a un [error de restablecimiento de \_ \_ conexión \_ a Internet](wininet-errors.md) o error [ \_ Internet \_ no puede \_ conectar](wininet-errors.md) . [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)usa esta marca.                                                                                                              |
| [**marca de INTERNET no \_ \_ \_ almacenar en caché**](api-flags.md)                                                                              | No almacena en caché los datos, ya sea de forma local o en cualquier puerta de enlace. Del mismo modo que el valor preferido, [**Internet \_ Flag \_ no \_ \_ escribir en caché**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Indica que se trata de un envío de formularios.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Internet \_ de marca \_ de la \_ memoria caché**](api-flags.md)[**envío de \_ \_ formularios \_ de marcas de Internet**](api-flags.md) | No realiza solicitudes de red. Todas las entidades se devuelven desde la memoria caché. Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado. Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.                                                                                                                                                                                                       |
| [**indicador de INTERNET de \_ \_ FWD \_ back**](api-flags.md)                                                                                  | Indica que la función debe usar la copia del recurso que se encuentra actualmente en la caché de Internet. La fecha de expiración y otra información sobre el recurso no se comprueban. Si el elemento solicitado no se encuentra en la caché de Internet, el sistema intentará localizar el recurso en la red. Este valor se presentó en Microsoft Internet Explorer 5 y está asociado a las operaciones de botón **adelante** y **atrás** de Internet Explorer. |
| [**hipervínculo de marca de INTERNET \_ \_**](api-flags.md)                                                                                 | Fuerza a la aplicación a recargar un recurso si no hay tiempo de expiración y no se devolvió ninguna hora de última modificación cuando el recurso se almacenó en la memoria caché.                                                                                                                                                                                                                                                                                                                  |
| [**marca de INTERNET para \_ \_ hacer \_ persistente**](api-flags.md)                                                                    | Ya no se admite.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**la \_ marca de Internet \_ debe \_ almacenar en caché la \_ solicitud**](api-flags.md)                                                             | Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché. Es idéntico al valor preferido, el [**\_ \_ \_ archivo**](api-flags.md)de la marca de Internet.                                                                                                                                                                                                                                                                            |
| [**\_archivo de \_ necesidad de marca de Internet \_**](api-flags.md)                                                                                | Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**marca de INTERNET \_ \_ sin \_ escritura de caché \_**](api-flags.md)                                                                     | Rechaza cualquier intento por parte de la función para almacenar los datos descargados de Internet en la memoria caché. Esta marca es necesaria si la aplicación no desea que los recursos descargados se almacenen localmente.                                                                                                                                                                                                                                                               |
| [**marca de INTERNET \_ \_ sin \_ interfaz de usuario**](api-flags.md)                                                                                        | Deshabilita el cuadro de diálogo cookie. Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo solicitudes HTTP).                                                                                                                                                                                                                                                                                          |
| [**marca de INTERNET \_ \_ sin conexión**](api-flags.md)                                                                                     | Impide que la aplicación envíe solicitudes a la red. Todas las solicitudes se resuelven mediante los recursos almacenados en la memoria caché. Si el recurso no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado.                                                                                                                                                                                                                            |
| [**marca de INTERNET \_ \_ pragma \_ nocache**](api-flags.md)                                                                      | Fuerza la resolución de la solicitud por el servidor de origen, incluso si existe una copia almacenada en caché en el proxy. La función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en solicitudes HTTP y https) y la función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca.                                                                                                                                                                                               |
| [**RECARGA de la marca de INTERNET \_ \_**](api-flags.md)                                                                                       | Fuerza a la función a recuperar el recurso solicitado directamente desde Internet. La información que se descarga se almacena en la memoria caché.                                                                                                                                                                                                                                                                                                                     |
| [**marca de INTERNET volver a \_ \_ sincronizar**](api-flags.md)                                                                         | Hace que una aplicación realice una descarga condicional del recurso desde Internet. Si la versión almacenada en la memoria caché es actual, la información se descarga de la memoria caché. De lo contrario, la información se recarga desde el servidor.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Funciones persistentes de almacenamiento en caché

Los clientes que necesitan servicios persistentes de almacenamiento en caché usan las funciones de almacenamiento en caché persistentes para permitir que sus aplicaciones guarden datos en el sistema de archivos local para su uso posterior, como en situaciones en las que un vínculo de ancho de banda bajo limita el acceso a los datos o el acceso no está disponible en absoluto.

Las funciones de caché proporcionan almacenamiento en caché persistente y exploración sin conexión. A menos que la marca de Internet no especifique ningún marcador de [**\_ \_ \_ \_ escritura de caché**](api-flags.md) , las funciones almacenan en caché todos los datos descargados de la red. Las respuestas a los datos POST no se almacenan en caché.

## <a name="using-the-persistent-url-cache-functions"></a>Usar las funciones de caché de direcciones URL persistentes

Las siguientes funciones de caché de dirección URL persistente permiten a una aplicación tener acceso a la información almacenada en la memoria caché y manipularla.



| Función                                                           | Descripción                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Almacena en memoria caché los datos del archivo especificado en el almacenamiento de caché y los asocia a la dirección URL especificada.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Almacena en memoria caché los datos del archivo especificado en el almacenamiento de caché y los asocia a la dirección URL especificada.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Asigna el almacenamiento de caché solicitado y crea un nombre de archivo local para guardar la entrada de caché que corresponde al nombre de origen.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Genera una identificación de grupo de caché.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Quita el archivo asociado al nombre de origen de la memoria caché, si el archivo existe.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Libera un **GROUPID** y cualquier estado asociado en el archivo de índice de la memoria caché.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Cierra el identificador de enumeración especificado.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Comienza la enumeración de la memoria caché.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Comienza una enumeración filtrada de la memoria caché.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Recupera la entrada siguiente en la memoria caché.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Recupera la entrada siguiente en una enumeración de caché filtrada.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Recupera información sobre una entrada de la memoria caché.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Busca la dirección URL después de traducir cualquier redirección almacenada en caché que se aplicaría en el modo sin conexión de [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Lee los datos almacenados en caché de una secuencia que se ha abierto mediante [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Recupera una entrada de caché de la memoria caché en forma de archivo.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Proporciona la manera más eficaz e independiente de la implementación de obtener acceso a los datos de la memoria caché.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Agrega o quita entradas de un grupo de caché.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Establece los miembros especificados de la estructura de [**información de entrada de caché de Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Desbloquea la entrada de caché que se bloqueó cuando el archivo se recuperó para su uso desde la memoria caché por parte de [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea). |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Cierra la secuencia que se ha recuperado mediante [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                                           |



 

### <a name="enumerating-the-cache"></a>Enumerar la memoria caché

Las funciones [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) y [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumeran la información almacenada en la memoria caché. [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) inicia la enumeración tomando un patrón de búsqueda, un búfer y un tamaño de búfer para crear un identificador y devolver la primera entrada de la memoria caché. [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) toma el identificador creado por [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), un búfer y un tamaño de búfer para devolver la siguiente entrada de caché.

Ambas funciones almacenan una estructura de información de entrada de caché de Internet en el búfer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) El tamaño de esta estructura varía para cada entrada. Si el tamaño de búfer que se pasa a cualquiera de las funciones es insuficiente, la función genera un error y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ búfer insuficiente \_ . La variable de tamaño de búfer contiene el tamaño de búfer necesario para recuperar esa entrada de caché. Se debe asignar un búfer del tamaño indicado por la variable de tamaño de búfer y volver a llamar a la función con el nuevo búfer.

La estructura de información de entrada de caché de Internet contiene el tamaño de la estructura, la dirección URL de la información almacenada en caché, el nombre de archivo local, el tipo de entrada de caché, el recuento de uso, la tasa de aciertos, el tamaño, la hora de última modificación, la expiración, el último acceso, la hora de última sincronización, la información de encabezado [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)

La función [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) toma un patrón de búsqueda, un búfer que almacena la estructura de información de entrada de caché de [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) y el tamaño del búfer. Actualmente, solo se implementa el patrón de búsqueda predeterminado, que devuelve todas las entradas de la memoria caché.

Una vez enumerada la memoria caché, la aplicación debe llamar a [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) para cerrar el identificador de la enumeración de la memoria caché.

En el ejemplo siguiente se muestra la dirección URL de cada entrada de caché en un cuadro de lista, **IDC \_ CacheList**. Utiliza el \_ tamaño máximo \_ \_ \_ de la información de entrada de caché para asignar inicialmente un búfer, ya que las versiones anteriores de la API WinInet no enumeran la caché correctamente en caso contrario. Las versiones posteriores enumeran la caché correctamente y no hay ningún límite de tamaño de caché. Todas las aplicaciones que se ejecutan en equipos con la versión de la API WinINet de Internet Explorer 4,0 deben asignar un búfer del tamaño requerido. Para obtener más información, consulte [uso de búferes](appendix-b-using-buffers.md).


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



### <a name="retrieving-cache-entry-information"></a>Recuperando información de entrada de caché

La función [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) permite recuperar la estructura [**de \_ \_ \_ información de entrada de caché de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) para la dirección URL especificada. Esta estructura contiene el tamaño de la estructura, la dirección URL de la información almacenada en caché, el nombre de archivo local, el tipo de entrada de caché, el recuento de uso, la tasa de aciertos, el tamaño, la hora de última modificación, la expiración, el último acceso, la hora de última sincronización, la información de encabezado, el tamaño de la información

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) acepta una dirección URL, un búfer para una estructura de información de entrada de caché de Internet y el tamaño del búfer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Si se encuentra la dirección URL, la información se copia en el búfer. De lo contrario, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el archivo de error \_ \_ no \_ encontrado. Si el tamaño del búfer es insuficiente para almacenar la información de la entrada de caché, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ búfer insuficiente \_ . El tamaño necesario para recuperar la información se almacena en la variable de tamaño de búfer.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) no realiza ningún análisis de direcciones URL, por lo que una dirección URL que contenga un delimitador ( \# ) no se encontrará en la memoria caché, incluso si el recurso está almacenado en caché. Por ejemplo, si se pasa la dirección URL " https://example.com/example.htm\#sample ", la función devuelve el \_ archivo \_ de error no \_ encontrado aunque " https://example.com/example.htm " esté en la memoria caché.

En el ejemplo siguiente se recupera la información de la entrada de caché para la dirección URL especificada. A continuación, la función muestra la información del encabezado en el cuadro de edición **IDC \_ CacheDump** .


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



### <a name="creating-a-cache-entry"></a>Crear una entrada de caché

Una aplicación usa las funciones [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) y [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) para crear una entrada de caché.

[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) acepta la dirección URL, el tamaño de archivo esperado y la extensión de nombre de archivo. A continuación, la función crea un nombre de archivo local para guardar la entrada de caché que corresponde a la dirección URL y la extensión de nombre de archivo.

Con el nombre de archivo local, escriba los datos en el archivo local. Una vez que los datos se han escrito en el archivo local, la aplicación debe llamar a [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) acepta la dirección URL, el nombre de archivo local, la expiración, la hora de última modificación, el tipo de entrada de caché, la información de encabezado, el tamaño de información de encabezado y la extensión de nombre de archivo. A continuación, la función almacena en caché los datos en el archivo especificado en el almacenamiento en caché y los asocia a la dirección URL especificada.

En el ejemplo siguiente se usa el nombre de archivo local, creado por una llamada anterior a [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), almacenado en el cuadro de texto **IDC \_ archivolocal**, para almacenar el texto del cuadro de texto, **IDC \_ CacheDump**, en la entrada de caché. Una vez que los datos se han escrito en el archivo mediante **fopen**, **fprintf** y **fclose**, la entrada se confirma mediante [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


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



### <a name="deleting-a-cache-entry"></a>Eliminar una entrada de caché

La función [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) toma una dirección URL y quita el archivo de caché asociado a ella. Si el archivo caché no existe, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el archivo de error \_ \_ no \_ encontrado. Si el archivo caché está actualmente bloqueado o en uso, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error \_ acceso \_ denegado. El archivo se elimina cuando se desbloquea.

### <a name="retrieving-cache-entry-files"></a>Recuperando archivos de entrada de caché

En el caso de las aplicaciones que requieren el nombre de archivo de un recurso, use las funciones [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) y [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) . Las aplicaciones que no requieren el nombre de archivo deben usar las funciones [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)y [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) para recuperar la información de la memoria caché.

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) no realiza ningún análisis de direcciones URL, por lo que una dirección URL que contenga un delimitador ( \# ) no se encontrará en la memoria caché, incluso si el recurso está almacenado en caché. Por ejemplo, si se pasa la dirección URL " https://example.com/example.htm\#sample ", la función devuelve el \_ archivo \_ de error no \_ encontrado aunque " https://example.com/example.htm " esté en la memoria caché.

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) acepta una dirección URL, un búfer que almacena la estructura de información de entrada de caché de Internet y el tamaño del búfer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) La función se recupera y se bloquea para el autor de la llamada.

Una vez que se ha usado la información del archivo, la aplicación debe llamar a [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) para desbloquear el archivo.

### <a name="cache-groups"></a>Grupos de caché

Para crear un grupo de caché, se debe llamar a la función [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) para generar un **GROUPID** para el grupo de caché. Las entradas se pueden agregar al grupo de caché proporcionando la dirección URL de la entrada de caché y la marca de adición del grupo de caché de INTERNET \_ \_ \_ a la función [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) . Para quitar una entrada de la memoria caché de un grupo, pase la dirección URL de la entrada de caché y la marca de eliminación del grupo de caché de INTERNET \_ \_ \_ a [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

Las funciones [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) y [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) se pueden usar para enumerar las entradas de un grupo de caché especificado. Una vez completada la enumeración, la función debe llamar a [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).

## <a name="handling-structures-with-variable-size-information"></a>Controlar estructuras con información de tamaño variable

La memoria caché puede contener información de tamaño variable para cada dirección URL almacenada. Esto se refleja en la estructura de [**información de entrada de caché de Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) . Cuando las funciones de caché devuelven esta estructura, crean un búfer que siempre es el tamaño de la información de entrada de caché de Internet más cualquier información de tamaño variable. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Si un miembro de puntero no es **null**, apunta al área de memoria inmediatamente después de la estructura. Mientras se copia el búfer devuelto por una función en otro búfer, los miembros de puntero deben corregirse para que apunten al lugar adecuado en el nuevo búfer, como se muestra en el ejemplo siguiente.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Algunas funciones de caché generan un error con el \_ mensaje de error de búfer insuficiente \_ si especifica un búfer que es demasiado pequeño para contener la información de entrada de caché recuperada por la función. En este caso, la función también devuelve el tamaño requerido del búfer. Después, puede asignar un búfer del tamaño adecuado y volver a llamar a la función.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
