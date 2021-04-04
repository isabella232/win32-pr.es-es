---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) exponen un conjunto de funciones de C/C++ que permiten a la aplicación tener acceso a recursos HTTP en la Web. En este tema se proporciona información general sobre cómo se usan estas funciones para interactuar con un servidor HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Información general sobre las sesiones de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154316"
---
# <a name="winhttp-sessions-overview"></a>Información general sobre las sesiones de WinHTTP

Los servicios HTTP de Microsoft Windows (WinHTTP) exponen un conjunto de funciones de C/C++ que permiten a la aplicación tener acceso a recursos HTTP en la Web. En este tema se proporciona información general sobre cómo se usan estas funciones para interactuar con un servidor HTTP.

-   [Uso de la API de WinHTTP para tener acceso a la web](#using-the-winhttp-api-to-access-the-web)
-   [Inicializando WinHTTP](#initializing-winhttp)
-   [Abrir una solicitud](#opening-a-request)
-   [Agregar encabezados de solicitud](#adding-request-headers)
-   [Envío de una solicitud](#sending-a-request)
-   [Publicar datos en el servidor](#posting-data-to-the-server)
-   [Obtención de información acerca de una solicitud](#getting-information-about-a-request)
-   [Descargar recursos de la web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Uso de la API de WinHTTP para tener acceso a la web

En el diagrama siguiente se muestra el orden en el que normalmente se llama a las funciones WinHTTP al interactuar con un servidor HTTP. Los cuadros sombreados representan funciones que generan un identificador [HINTERNET](hinternet-handles-in-winhttp.md) , mientras que los cuadros simples representan funciones que utilizan esos controladores.

![funciones que crean identificadores](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Inicializando WinHTTP

Antes de interactuar con un servidor, se debe inicializar WinHTTP llamando a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) crea un contexto de sesión para mantener los detalles sobre la sesión http y devuelve un identificador de sesión. Con este identificador, la función [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) puede especificar un servidor http o de protocolo seguro de transferencia de hipertexto (https) de destino.

> [!Note]  
> Una llamada a [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) no produce una conexión real con el servidor http hasta que se realiza una solicitud para un recurso específico.

 

## <a name="opening-a-request"></a>Abrir una solicitud

La función [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) abre una solicitud HTTP para un recurso determinado y devuelve un identificador [HINTERNET](hinternet-handles-in-winhttp.md) que pueden usar las otras funciones http. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) no envía la solicitud al servidor cuando se le llama. La función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) establece realmente una conexión a través de la red y envía la solicitud.

En el ejemplo siguiente se muestra una llamada de ejemplo a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) que usa las opciones predeterminadas.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Agregar encabezados de solicitud

La función [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) permite a una aplicación anexar encabezados de solicitud de formato libre adicionales al identificador de la solicitud HTTP. Está diseñado para aplicaciones sofisticadas que requieren un control preciso de las solicitudes enviadas al servidor HTTP.

La función [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) requiere un identificador de solicitud HTTP creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), una cadena que contiene los encabezados, la longitud de los encabezados y los modificadores.

Los modificadores siguientes se pueden usar con [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).



| Modificador                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**incorporación de la \_ marca WinHTTP ADDREQ \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Agrega el encabezado si no existe. Se usa con la [**\_ \_ marca \_ Replace de ADDREQ de WinHTTP**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).                                                                                                                                                                                                               |
| [**la \_ marca de WinHTTP ADDREQ \_ \_ agregar \_ si es \_ nueva**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Agrega el encabezado solo si aún no existe; de lo contrario, se devuelve un error.                                                                                                                                                                                                                                                           |
| [**incorporación de marcas de WINHTTP \_ ADDREQ \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Combina los encabezados del mismo nombre.                                                                                                                                                                                                                                                                                                              |
| [**\_ \_ incorporación de la marca de WinHTTP ADDREQ \_ \_ con \_ coma**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Combina los encabezados del mismo nombre mediante una coma. Por ejemplo, al agregar "Accept: Text/ \* " seguido de "Accept: audio/ \* " con esta marca, se forma el encabezado único "Accept: Text/ \* , audio/ \* ", lo que hace que se combine el primer encabezado. Depende de la aplicación que realiza la llamada garantizar un esquema coherente con respecto a los encabezados combinados/independientes. |
| [**la \_ marca de WinHTTP ADDREQ se \_ \_ combina \_ con un \_ punto y coma**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Combina los encabezados del mismo nombre con un punto y coma.                                                                                                                                                                                                                                                                                            |
| [**ADDREQ de la marca de WINHTTP \_ \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Reemplaza o quita un encabezado. Si el valor del encabezado está vacío y se encuentra el encabezado, se quita. Si el valor del encabezado no está vacío, se reemplaza el valor del encabezado.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Envío de una solicitud

La función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) establece una conexión con el servidor y envía la solicitud al sitio especificado. Esta función requiere un identificador de [HINTERNET](hinternet-handles-in-winhttp.md) creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) también puede enviar encabezados adicionales u información opcional. La información opcional se utiliza generalmente para las operaciones que escriben información en el servidor, como PUT y POST.

Después de que la función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) envíe la solicitud, la aplicación puede usar las funciones [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) y [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) en el controlador [HINTERNET](hinternet-handles-in-winhttp.md) para descargar los recursos del servidor.

## <a name="posting-data-to-the-server"></a>Publicar datos en el servidor

Para publicar datos en un servidor, el [*verbo http*](glossary.md) de la llamada a [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) debe ser post o Put. Cuando se llama a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , el parámetro *dwTotalLength* debe establecerse en el tamaño de los datos en bytes. A continuación, use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) para enviar los datos al servidor.

Como alternativa, establezca el parámetro *lpOptional* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) en la dirección de un búfer que contenga los datos que se van a publicar en el servidor. Al usar esta técnica, debe establecer los parámetros *dwOptionalLength* y *dwTotalLength* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) para que sea el tamaño de los datos que se van a exponer. La llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) de esta manera elimina la necesidad de llamar a [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).

## <a name="getting-information-about-a-request"></a>Obtención de información acerca de una solicitud

La función [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) permite que una aplicación recupere información acerca de una solicitud HTTP. La función requiere un identificador [HINTERNET](hinternet-handles-in-winhttp.md) creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), un valor de nivel de información y una longitud de búfer. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) también acepta un búfer que almacena la información y un índice de encabezado basado en cero que enumera varios encabezados con el mismo nombre.

Use cualquiera de los valores de nivel de información que se encuentran en la página [**marcas de información de consulta**](query-info-flags.md) con un modificador para controlar el formato en el que se almacena la información en el parámetro *lpvBuffer* de [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

## <a name="downloading-resources-from-the-web"></a>Descargar recursos de la web

Después de abrir una solicitud con la función [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , enviarla al servidor con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)y preparar el identificador de solicitud para recibir una respuesta con [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), la aplicación puede usar las funciones [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) y [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) para descargar el recurso desde el servidor http.

En el código de ejemplo siguiente se muestra cómo descargar un recurso con semántica de transacciones seguras. El código de ejemplo inicializa la interfaz de programación de aplicaciones (API) de WinHTTP, selecciona un servidor HTTPS de destino y, a continuación, abre y envía una solicitud para este recurso seguro. [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) se usa con el identificador de solicitud para determinar la cantidad de datos disponibles para su descarga y, a continuación, se usa [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) para leer los datos. Este proceso se repite hasta que se ha recuperado y mostrado todo el documento.


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



