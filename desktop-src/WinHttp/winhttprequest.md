---
Description: En este tema se proporciona información sobre el uso del objeto COM WinHTTP WinHttpRequest con lenguajes de scripting.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Objeto WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708874"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="c5d2b-103">Objeto WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="c5d2b-103">WinHttpRequest object</span></span>

<span data-ttu-id="c5d2b-104">En este tema se proporciona información sobre el uso del objeto com WinHTTP **WinHttpRequest** con lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="c5d2b-105">Para obtener más información, incluida la API de C++ (WinHTTP), consulte [acerca de WinHTTP](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="c5d2b-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="c5d2b-106">Vea [elegir una interfaz WinHTTP](choosing-a-winhttp-interface.md) para obtener una comparación de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="c5d2b-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5d2b-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="c5d2b-108">Ejemplos de código tomados de la [propiedad IWinHttpRequest:: status](iwinhttprequest-status.md).</span><span class="sxs-lookup"><span data-stu-id="c5d2b-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="c5d2b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5d2b-109">Members</span></span>

<span data-ttu-id="c5d2b-110">El objeto **WinHttpRequest** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c5d2b-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="c5d2b-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="c5d2b-111">Events</span></span>](#events)
-   [<span data-ttu-id="c5d2b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5d2b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5d2b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5d2b-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="c5d2b-114">Events</span><span class="sxs-lookup"><span data-stu-id="c5d2b-114">Events</span></span>

<span data-ttu-id="c5d2b-115">El objeto **WinHttpRequest** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="c5d2b-116">Evento</span><span class="sxs-lookup"><span data-stu-id="c5d2b-116">Event</span></span>                                                                            | <span data-ttu-id="c5d2b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5d2b-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="c5d2b-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="c5d2b-119">Se produce cuando hay un error de tiempo de ejecución en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="c5d2b-120">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="c5d2b-121">Se produce cuando los datos están disponibles en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="c5d2b-122">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="c5d2b-123">Se produce cuando se completan los datos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="c5d2b-124">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="c5d2b-125">Se produce cuando se inicia la recepción de los datos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="c5d2b-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5d2b-126">Methods</span></span>

<span data-ttu-id="c5d2b-127">El objeto **WinHttpRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="c5d2b-128">Método</span><span class="sxs-lookup"><span data-stu-id="c5d2b-128">Method</span></span>                                                                 | <span data-ttu-id="c5d2b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5d2b-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5d2b-130">**Aborta**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="c5d2b-131">Anula un método de [**envío**](iwinhttprequest-send.md) de [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d2b-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="c5d2b-132">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="c5d2b-133">Recupera todos los encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="c5d2b-134">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="c5d2b-135">Recupera los encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="c5d2b-136">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="c5d2b-137">Abre una conexión HTTP a un recurso HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="c5d2b-138">**Enviar**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="c5d2b-139">Envía una solicitud HTTP a un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="c5d2b-140">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="c5d2b-141">Establece la [Directiva de inicio de sesión automático](authentication-in-winhttp.md)actual.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="c5d2b-142">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="c5d2b-143">Selecciona un certificado de cliente para enviar a un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="c5d2b-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="c5d2b-144">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="c5d2b-145">Establece las credenciales que se van a usar con un servidor HTTP como un origen o un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="c5d2b-146">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="c5d2b-147">Establece la información del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="c5d2b-148">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="c5d2b-149">Agrega, cambia o elimina un encabezado de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="c5d2b-150">**SetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="c5d2b-151">Especifica, en milisegundos, los componentes de tiempo de espera individuales de una operación de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="c5d2b-152">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="c5d2b-153">Especifica el tiempo de espera, en segundos, para que se complete un método de [**envío**](iwinhttprequest-send.md) asincrónico, con un valor de tiempo de espera opcional.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c5d2b-154">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5d2b-154">Properties</span></span>

<span data-ttu-id="c5d2b-155">El objeto **WinHttpRequest** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="c5d2b-156">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5d2b-156">Property</span></span>                                                            | <span data-ttu-id="c5d2b-157">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c5d2b-157">Access type</span></span>           | <span data-ttu-id="c5d2b-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5d2b-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="c5d2b-159">**Opción**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="c5d2b-160">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c5d2b-160">Read/write</span></span><br/> | <span data-ttu-id="c5d2b-161">Establece o recupera un valor de opción de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="c5d2b-162">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="c5d2b-163">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5d2b-163">Read-only</span></span><br/>  | <span data-ttu-id="c5d2b-164">Recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="c5d2b-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="c5d2b-166">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5d2b-166">Read-only</span></span><br/>  | <span data-ttu-id="c5d2b-167">Recupera el cuerpo de la entidad de respuesta como una [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="c5d2b-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="c5d2b-168">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="c5d2b-169">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5d2b-169">Read-only</span></span><br/>  | <span data-ttu-id="c5d2b-170">Recupera el cuerpo de la entidad de respuesta como texto.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="c5d2b-171">**Status**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="c5d2b-172">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5d2b-172">Read-only</span></span><br/>  | <span data-ttu-id="c5d2b-173">Recupera el código de Estado HTTP de la última respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="c5d2b-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="c5d2b-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="c5d2b-175">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5d2b-175">Read-only</span></span><br/>  | <span data-ttu-id="c5d2b-176">Recupera el texto de Estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="c5d2b-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5d2b-177">Remarks</span></span>

<span data-ttu-id="c5d2b-178">El objeto **WinHttpRequest** usa la interfaz [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) para proporcionar datos de error.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="c5d2b-179">Se puede obtener una descripción y un valor de error numérico con el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) en Microsoft Visual Basic Scripting Edition (VBScript) y el objeto [error](https://msdn.microsoft.com/library/dww52sbt.aspx) en Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="c5d2b-180">Los 16 bits inferiores de un número de error corresponden a los valores que se encuentran en [**los mensajes de error**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c5d2b-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="c5d2b-181">En Windows XP y Windows 2000, consulte [requisitos de tiempo de ejecución](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="c5d2b-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5d2b-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5d2b-182">Requirements</span></span>



| <span data-ttu-id="c5d2b-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d2b-183">Requirement</span></span> | <span data-ttu-id="c5d2b-184">Value</span><span class="sxs-lookup"><span data-stu-id="c5d2b-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d2b-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5d2b-185">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d2b-186">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="c5d2b-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c5d2b-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5d2b-187">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d2b-188">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="c5d2b-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c5d2b-189">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c5d2b-189">Redistributable</span></span><br/>          | <span data-ttu-id="c5d2b-190">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c5d2b-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c5d2b-191">IDL</span><span class="sxs-lookup"><span data-stu-id="c5d2b-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5d2b-192"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5d2b-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="c5d2b-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5d2b-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="c5d2b-194"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5d2b-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c5d2b-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5d2b-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5d2b-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5d2b-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5d2b-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5d2b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d2b-198">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c5d2b-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

