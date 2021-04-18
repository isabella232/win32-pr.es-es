---
title: Recuperación de encabezados HTTP
description: En este tutorial se describe cómo recuperar información de encabezado de las solicitudes HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656381"
---
# <a name="retrieving-http-headers"></a>Recuperación de encabezados HTTP

En este tutorial se describe cómo recuperar información de encabezado de las solicitudes HTTP.

## <a name="implementation-steps"></a>Pasos de implementación

Hay dos maneras de recuperar la información del encabezado:

-   Use una de las constantes de [**marca de información de consulta**](query-info-flags.md) asociadas al encabezado HTTP que necesita su aplicación.
-   Use la \_ \_ marca de atributo personalizado de consulta http y pase el nombre del encabezado HTTP.

El uso de la constante asociada con el encabezado HTTP que necesita su aplicación es más rápido internamente, pero puede haber encabezados HTTP que no tengan una constante asociada. En esos casos, el método que utiliza la \_ marca de atributo personalizado de consulta HTTP \_ está disponible.

Ambos métodos usan la función [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) toma el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) en el que se realizó la solicitud HTTP, un atributo, un búfer, un valor DWORD que contiene el tamaño de búfer y un valor de índice. También se puede Agregar un modificador al atributo que se pasa a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para indicar en qué formato se deben devolver los datos.

### <a name="retrieving-headers-using-a-constant"></a>Recuperar encabezados mediante una constante

Para usar la función [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar un encabezado HTTP mediante una constante, siga estos pasos:

1.  Llame a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con una constante de la lista de [**atributos**](query-info-flags.md) , un búfer **null** y la variable que contiene el tamaño de búfer establecido en cero. Además, si la aplicación necesita los datos en un formato determinado, puede Agregar una constante desde la lista de [**Modificadores**](query-info-flags.md) .
2.  Si el encabezado HTTP solicitado existe, se debe producir un error en la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) debe devolver el error \_ búfer insuficiente \_ y la variable que se ha pasado para el parámetro *lpdwBufferLength* debe establecerse en el número de bytes necesario.
3.  Asigne un búfer con el número de bytes necesario.
4.  Vuelva a intentar la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

En el ejemplo siguiente se muestra una llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mediante la \_ constante CRLF de encabezados de consulta HTTP \_ \_ \_ , que es un valor especial que solicita todos los encabezados HTTP devueltos.


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



### <a name="retrieving-headers-using-http_query_custom"></a>Recuperación de encabezados mediante la \_ consulta HTTP \_ personalizada

Para usar la función [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar un encabezado HTTP mediante la \_ consulta HTTP \_ personalizada, siga estos pasos:

1.  Asigne un búfer lo suficientemente grande como para contener el nombre de la cadena del encabezado HTTP.
2.  Escriba el nombre de la cadena del encabezado HTTP en el búfer.
3.  Llame a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con la \_ consulta HTTP \_ Custom, el búfer que contiene el nombre de cadena del encabezado HTTP y la variable que contiene el tamaño del búfer. Además, si la aplicación necesita los datos en un formato determinado, puede Agregar una constante desde la lista de [**Modificadores**](query-info-flags.md) .
4.  Si se produce un error en la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) y [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ búfer insuficiente \_ , reasigne un búfer con el número de bytes necesario.
5.  Vuelva a escribir el nombre de cadena del encabezado HTTP en el búfer.
6.  Vuelva a intentar la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

En el ejemplo siguiente se muestra una llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mediante la \_ constante personalizada de consulta HTTP \_ para solicitar el encabezado HTTP Content-Type.


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
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 