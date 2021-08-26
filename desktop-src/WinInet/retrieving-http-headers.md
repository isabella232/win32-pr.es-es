---
title: Recuperación de encabezados HTTP
description: En este tutorial se describe cómo recuperar información de encabezado de solicitudes HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955515"
---
# <a name="retrieving-http-headers"></a>Recuperación de encabezados HTTP

En este tutorial se describe cómo recuperar información de encabezado de solicitudes HTTP.

## <a name="implementation-steps"></a>Pasos de implementación

Hay dos maneras de recuperar la información del encabezado:

-   Use una de las [**constantes de la**](query-info-flags.md) marca de información de consulta asociadas al encabezado HTTP que necesita la aplicación.
-   Use la marca \_ de atributo HTTP QUERY CUSTOM y pase el nombre del encabezado \_ HTTP.

El uso de la constante asociada al encabezado HTTP que la aplicación necesita es más rápido internamente, pero puede haber encabezados HTTP que no tengan una constante asociada a ellos. En esos casos, el método que usa la marca de atributo HTTP \_ QUERY \_ CUSTOM está disponible.

Ambos métodos usan la [**función HttpQueryInfo.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) toma el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) en el que se realizó la solicitud HTTP, un atributo, un búfer, un valor DWORD que contiene el tamaño del búfer y un valor de índice. También se puede agregar un modificador al atributo pasado a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para indicar en qué formato se deben devolver los datos.

### <a name="retrieving-headers-using-a-constant"></a>Recuperar encabezados mediante una constante

Para usar la [**función HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar un encabezado HTTP mediante una constante, siga estos pasos:

1.  Llame [**a HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con una constante de la lista [**Atributos,**](query-info-flags.md) un búfer **NULL** y la variable que contiene el tamaño de búfer establecido en cero. Además, si la aplicación necesita los datos en un formato determinado, puede agregar una constante de la [**lista Modificadores.**](query-info-flags.md)
2.  Si existe el encabezado HTTP solicitado, se debe producir un error en la llamada a [**HttpQueryInfo,**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) debe devolver ERROR INSUFFICIENT BUFFER y la variable pasada para el parámetro \_ \_ *lpdwBufferLength* debe establecerse en el número de bytes necesarios.
3.  Asigne un búfer con el número de bytes necesarios.
4.  Vuelva a intentar la llamada [**a HttpQueryInfo.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)

En el ejemplo siguiente se muestra una llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mediante la constante CRLF HTTP QUERY RAW HEADERS, que es un valor especial que solicita todos los \_ \_ \_ \_ encabezados HTTP devueltos.


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a>Recuperar encabezados mediante HTTP \_ QUERY \_ CUSTOM

Para usar la [**función HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar un encabezado HTTP mediante HTTP \_ QUERY \_ CUSTOM, siga estos pasos:

1.  Asigne un búfer lo suficientemente grande como para contener el nombre de cadena del encabezado HTTP.
2.  Escriba el nombre de cadena del encabezado HTTP en el búfer.
3.  Llame [**a HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con HTTP QUERY CUSTOM, el búfer que contiene el nombre de cadena del encabezado HTTP y la variable que \_ contiene el tamaño del \_ búfer. Además, si la aplicación necesita los datos en un formato determinado, puede agregar una constante de la [**lista Modificadores.**](query-info-flags.md)
4.  Si se produce un error en la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER, vuelva a crear un búfer con el \_ número de bytes \_ necesarios.
5.  Vuelva a escribir el nombre de cadena del encabezado HTTP en el búfer.
6.  Vuelva a intentar la llamada [**a HttpQueryInfo.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)

En el ejemplo siguiente se muestra una llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mediante la constante HTTP \_ QUERY CUSTOM para solicitar el encabezado HTTP \_ Content-Type.


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 