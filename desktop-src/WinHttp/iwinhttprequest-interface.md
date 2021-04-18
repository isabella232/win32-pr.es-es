---
description: La interfaz IWinHttpRequest proporciona todos los métodos no pares para los servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interfaz IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277134"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="34775-103">Interfaz IWinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="34775-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="34775-104">La interfaz **IWinHttpRequest** proporciona todos los métodos no pares para los [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="34775-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="34775-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="34775-105">Members</span></span>

<span data-ttu-id="34775-106">La interfaz **IWinHttpRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="34775-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="34775-107">**IWinHttpRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="34775-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="34775-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="34775-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="34775-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34775-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34775-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="34775-110">Methods</span></span>

<span data-ttu-id="34775-111">La interfaz **IWinHttpRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="34775-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="34775-112">Método</span><span class="sxs-lookup"><span data-stu-id="34775-112">Method</span></span>                                                                 | <span data-ttu-id="34775-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="34775-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34775-114">**Aborta**</span><span class="sxs-lookup"><span data-stu-id="34775-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="34775-115">Anula un método de [**envío**](iwinhttprequest-send.md) de [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="34775-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="34775-116">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="34775-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="34775-117">Recupera todos los encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="34775-118">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="34775-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="34775-119">Recupera los encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="34775-120">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="34775-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="34775-121">Abre una conexión HTTP a un recurso HTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="34775-122">**Enviar**</span><span class="sxs-lookup"><span data-stu-id="34775-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="34775-123">Envía una solicitud HTTP a un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="34775-124">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="34775-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="34775-125">Establece la [Directiva de inicio de sesión automático](authentication-in-winhttp.md)actual.</span><span class="sxs-lookup"><span data-stu-id="34775-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="34775-126">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="34775-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="34775-127">Selecciona un certificado de cliente para enviar a un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="34775-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="34775-128">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="34775-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="34775-129">Establece las credenciales que se van a usar con un servidor HTTP, ya sea un servidor proxy o un servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="34775-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="34775-130">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="34775-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="34775-131">Establece la información del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="34775-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="34775-132">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="34775-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="34775-133">Agrega, cambia o elimina un encabezado de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="34775-134">**SetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="34775-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="34775-135">Especifica los componentes de tiempo de espera individuales de una operación de envío y recepción, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="34775-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="34775-136">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="34775-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="34775-137">Espera a que se complete un método de [**envío**](iwinhttprequest-send.md) asincrónico, en segundos, con un valor de tiempo de espera opcional.</span><span class="sxs-lookup"><span data-stu-id="34775-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="34775-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34775-138">Properties</span></span>

<span data-ttu-id="34775-139">La interfaz **IWinHttpRequest** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="34775-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="34775-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34775-140">Property</span></span>                                                            | <span data-ttu-id="34775-141">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="34775-141">Access type</span></span>           | <span data-ttu-id="34775-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="34775-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="34775-143">**Opción**</span><span class="sxs-lookup"><span data-stu-id="34775-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="34775-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="34775-144">Read/write</span></span><br/> | <span data-ttu-id="34775-145">Un valor de la opción WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="34775-146">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="34775-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="34775-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34775-147">Read-only</span></span><br/>  | <span data-ttu-id="34775-148">El cuerpo de la entidad de respuesta como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="34775-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="34775-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="34775-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="34775-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34775-150">Read-only</span></span><br/>  | <span data-ttu-id="34775-151">El cuerpo de la entidad de respuesta como una [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="34775-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="34775-152">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="34775-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="34775-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34775-153">Read-only</span></span><br/>  | <span data-ttu-id="34775-154">El cuerpo de la entidad de respuesta.</span><span class="sxs-lookup"><span data-stu-id="34775-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="34775-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="34775-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="34775-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34775-156">Read-only</span></span><br/>  | <span data-ttu-id="34775-157">Código de Estado HTTP de la última respuesta.</span><span class="sxs-lookup"><span data-stu-id="34775-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="34775-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="34775-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="34775-159">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34775-159">Read-only</span></span><br/>  | <span data-ttu-id="34775-160">El texto de Estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="34775-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="34775-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34775-161">Remarks</span></span>

<span data-ttu-id="34775-162">La interfaz **IWinHttpRequest** definida en HttpRequest. idl está implementada por una clase con el **identificador \_ WinHttpRequest CLSID**.</span><span class="sxs-lookup"><span data-stu-id="34775-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="34775-163">Una aplicación obtiene esta interfaz llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID. de clase de **CLSID \_ WinHttpRequest** y un ID. de interfaz de **IID \_ IWinHttpRequest**.</span><span class="sxs-lookup"><span data-stu-id="34775-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="34775-164">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="34775-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34775-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34775-165">Requirements</span></span>



| <span data-ttu-id="34775-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="34775-166">Requirement</span></span> | <span data-ttu-id="34775-167">Value</span><span class="sxs-lookup"><span data-stu-id="34775-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="34775-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34775-168">Minimum supported client</span></span><br/> | <span data-ttu-id="34775-169">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="34775-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="34775-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34775-170">Minimum supported server</span></span><br/> | <span data-ttu-id="34775-171">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="34775-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="34775-172">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="34775-172">Redistributable</span></span><br/>          | <span data-ttu-id="34775-173">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="34775-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="34775-174">IDL</span><span class="sxs-lookup"><span data-stu-id="34775-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34775-175"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34775-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="34775-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34775-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="34775-177"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34775-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="34775-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34775-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34775-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34775-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="34775-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="34775-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34775-181">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="34775-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="34775-182">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="34775-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

