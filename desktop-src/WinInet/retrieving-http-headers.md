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
# <a name="retrieving-http-headers"></a><span data-ttu-id="270d1-103">Recuperación de encabezados HTTP</span><span class="sxs-lookup"><span data-stu-id="270d1-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="270d1-104">En este tutorial se describe cómo recuperar información de encabezado de las solicitudes HTTP.</span><span class="sxs-lookup"><span data-stu-id="270d1-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="270d1-105">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="270d1-105">Implementation Steps</span></span>

<span data-ttu-id="270d1-106">Hay dos maneras de recuperar la información del encabezado:</span><span class="sxs-lookup"><span data-stu-id="270d1-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="270d1-107">Use una de las constantes de [**marca de información de consulta**](query-info-flags.md) asociadas al encabezado HTTP que necesita su aplicación.</span><span class="sxs-lookup"><span data-stu-id="270d1-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="270d1-108">Use la \_ \_ marca de atributo personalizado de consulta http y pase el nombre del encabezado HTTP.</span><span class="sxs-lookup"><span data-stu-id="270d1-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="270d1-109">El uso de la constante asociada con el encabezado HTTP que necesita su aplicación es más rápido internamente, pero puede haber encabezados HTTP que no tengan una constante asociada.</span><span class="sxs-lookup"><span data-stu-id="270d1-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="270d1-110">En esos casos, el método que utiliza la \_ marca de atributo personalizado de consulta HTTP \_ está disponible.</span><span class="sxs-lookup"><span data-stu-id="270d1-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="270d1-111">Ambos métodos usan la función [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="270d1-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="270d1-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) toma el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) en el que se realizó la solicitud HTTP, un atributo, un búfer, un valor DWORD que contiene el tamaño de búfer y un valor de índice.</span><span class="sxs-lookup"><span data-stu-id="270d1-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="270d1-113">También se puede Agregar un modificador al atributo que se pasa a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para indicar en qué formato se deben devolver los datos.</span><span class="sxs-lookup"><span data-stu-id="270d1-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="270d1-114">Recuperar encabezados mediante una constante</span><span class="sxs-lookup"><span data-stu-id="270d1-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="270d1-115">Para usar la función [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar un encabezado HTTP mediante una constante, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="270d1-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="270d1-116">Llame a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con una constante de la lista de [**atributos**](query-info-flags.md) , un búfer **null** y la variable que contiene el tamaño de búfer establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="270d1-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="270d1-117">Además, si la aplicación necesita los datos en un formato determinado, puede Agregar una constante desde la lista de [**Modificadores**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="270d1-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="270d1-118">Si el encabezado HTTP solicitado existe, se debe producir un error en la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) debe devolver el error \_ búfer insuficiente \_ y la variable que se ha pasado para el parámetro *lpdwBufferLength* debe establecerse en el número de bytes necesario.</span><span class="sxs-lookup"><span data-stu-id="270d1-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="270d1-119">Asigne un búfer con el número de bytes necesario.</span><span class="sxs-lookup"><span data-stu-id="270d1-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="270d1-120">Vuelva a intentar la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="270d1-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="270d1-121">En el ejemplo siguiente se muestra una llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mediante la \_ constante CRLF de encabezados de consulta HTTP \_ \_ \_ , que es un valor especial que solicita todos los encabezados HTTP devueltos.</span><span class="sxs-lookup"><span data-stu-id="270d1-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


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



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="270d1-122">Recuperación de encabezados mediante la \_ consulta HTTP \_ personalizada</span><span class="sxs-lookup"><span data-stu-id="270d1-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="270d1-123">Para usar la función [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar un encabezado HTTP mediante la \_ consulta HTTP \_ personalizada, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="270d1-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="270d1-124">Asigne un búfer lo suficientemente grande como para contener el nombre de la cadena del encabezado HTTP.</span><span class="sxs-lookup"><span data-stu-id="270d1-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="270d1-125">Escriba el nombre de la cadena del encabezado HTTP en el búfer.</span><span class="sxs-lookup"><span data-stu-id="270d1-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="270d1-126">Llame a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con la \_ consulta HTTP \_ Custom, el búfer que contiene el nombre de cadena del encabezado HTTP y la variable que contiene el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="270d1-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="270d1-127">Además, si la aplicación necesita los datos en un formato determinado, puede Agregar una constante desde la lista de [**Modificadores**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="270d1-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="270d1-128">Si se produce un error en la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) y [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ búfer insuficiente \_ , reasigne un búfer con el número de bytes necesario.</span><span class="sxs-lookup"><span data-stu-id="270d1-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="270d1-129">Vuelva a escribir el nombre de cadena del encabezado HTTP en el búfer.</span><span class="sxs-lookup"><span data-stu-id="270d1-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="270d1-130">Vuelva a intentar la llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="270d1-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="270d1-131">En el ejemplo siguiente se muestra una llamada a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mediante la \_ constante personalizada de consulta HTTP \_ para solicitar el encabezado HTTP Content-Type.</span><span class="sxs-lookup"><span data-stu-id="270d1-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


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
> <span data-ttu-id="270d1-132">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="270d1-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="270d1-133">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="270d1-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="270d1-134">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="270d1-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 