---
description: Incluye opciones que se pueden establecer o recuperar para la sesión actual de servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Enumeración WinHttpRequestOption
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541675"
---
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="7b208-103">Enumeración WinHttpRequestOption</span><span class="sxs-lookup"><span data-stu-id="7b208-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="7b208-104">La enumeración **WinHttpRequestOption** incluye opciones que se pueden establecer o recuperar para la sesión actual de servicios http de Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="7b208-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b208-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b208-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a><span data-ttu-id="7b208-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7b208-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7b208-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**</span><span class="sxs-lookup"><span data-stu-id="7b208-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-108">Establece o recupera un **valor de tipo Variant** que contiene la cadena del [*agente de usuario*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="7b208-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_Dirección URL de WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="7b208-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-110">Recupera un **valor de tipo Variant** que contiene la dirección URL del recurso.</span><span class="sxs-lookup"><span data-stu-id="7b208-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="7b208-111">Este valor es de solo lectura; no se puede establecer la dirección URL mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7b208-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="7b208-112">No se puede leer la dirección URL hasta que se llame al método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7b208-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="7b208-113">Esta opción es útil para comprobar la dirección URL una vez finalizado el método [**send**](iwinhttprequest-send.md) para comprobar que se ha producido alguna redirección.</span><span class="sxs-lookup"><span data-stu-id="7b208-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**</span><span class="sxs-lookup"><span data-stu-id="7b208-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-115">Establece o recupera una **variante** que identifica la [*Página de códigos*](glossary.md) de la cadena de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="7b208-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="7b208-116">El valor predeterminado es la página de códigos UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7b208-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="7b208-117">La página de códigos se usa para convertir la cadena de dirección URL de Unicode, pasada en el método [**Open**](iwinhttprequest-open.md) , en una representación de cadena de un solo byte.</span><span class="sxs-lookup"><span data-stu-id="7b208-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**</span><span class="sxs-lookup"><span data-stu-id="7b208-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-119">Establece o recupera un **valor de tipo Variant** que indica si los caracteres de porcentaje de la cadena de dirección URL se convierten en una secuencia de escape.</span><span class="sxs-lookup"><span data-stu-id="7b208-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="7b208-120">El valor predeterminado de esta opción es **Variant \_ true** , que especifica todos los caracteres de American National Standards Institute no seguros (ANSI), excepto que el símbolo de porcentaje se convierte en una secuencia de escape.</span><span class="sxs-lookup"><span data-stu-id="7b208-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**</span><span class="sxs-lookup"><span data-stu-id="7b208-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-122">Establece o recupera un **valor de tipo Variant** que indica qué errores de certificado de servidor se deben omitir.</span><span class="sxs-lookup"><span data-stu-id="7b208-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="7b208-123">Puede ser una combinación de uno o varios de los siguientes marcadores.</span><span class="sxs-lookup"><span data-stu-id="7b208-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="7b208-124">Error</span><span class="sxs-lookup"><span data-stu-id="7b208-124">Error</span></span>                                                  | <span data-ttu-id="7b208-125">Value</span><span class="sxs-lookup"><span data-stu-id="7b208-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="7b208-126">Entidad de certificación (CA) desconocida o raíz que no es de confianza</span><span class="sxs-lookup"><span data-stu-id="7b208-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="7b208-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="7b208-127">0x0100</span></span> |
| <span data-ttu-id="7b208-128">Uso incorrecto</span><span class="sxs-lookup"><span data-stu-id="7b208-128">Wrong usage</span></span>                                            | <span data-ttu-id="7b208-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="7b208-129">0x0200</span></span> |
| <span data-ttu-id="7b208-130">Nombre común (CN) no válido</span><span class="sxs-lookup"><span data-stu-id="7b208-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="7b208-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="7b208-131">0x1000</span></span> |
| <span data-ttu-id="7b208-132">Fecha no válida o certificado expirado</span><span class="sxs-lookup"><span data-stu-id="7b208-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="7b208-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="7b208-133">0x2000</span></span> |



 

<span data-ttu-id="7b208-134">El valor predeterminado de esta opción en la versión 5,1 de WinHTTP es cero, lo que da lugar a que no se omitan errores.</span><span class="sxs-lookup"><span data-stu-id="7b208-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="7b208-135">En versiones anteriores de WinHTTP, la configuración predeterminada era 0x3300, lo que daba lugar a que todos los errores de certificado de servidor se omitiran de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b208-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="7b208-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-137">Establece una **variante** que especifica el certificado de cliente que se envía a un servidor para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="7b208-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="7b208-138">Esta opción indica la ubicación, el [*almacén de certificados*](glossary.md)y el asunto de un certificado de cliente delimitado por barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="7b208-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="7b208-139">Para obtener más información acerca de cómo seleccionar un certificado de cliente, consulte [SSL en WinHTTP](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="7b208-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b208-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**</span><span class="sxs-lookup"><span data-stu-id="7b208-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-141">Establece o recupera un **valor de tipo Variant** que indica si las solicitudes se redirigen automáticamente cuando el servidor especifica una nueva ubicación para el recurso.</span><span class="sxs-lookup"><span data-stu-id="7b208-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="7b208-142">El valor predeterminado de esta opción es **Variant \_ true** para indicar que las solicitudes se redirigen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7b208-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**</span><span class="sxs-lookup"><span data-stu-id="7b208-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-144">Establece o recupera un **valor de tipo Variant** que indica si los caracteres no seguros de la ruta de acceso y los componentes de consulta de una dirección URL se convierten en secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="7b208-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="7b208-145">El valor predeterminado de esta opción es **Variant \_ true**, que especifica que se convierten los caracteres de la ruta de acceso y la consulta.</span><span class="sxs-lookup"><span data-stu-id="7b208-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**</span><span class="sxs-lookup"><span data-stu-id="7b208-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-147">Establece o recupera un **valor de tipo Variant** que indica si los caracteres no seguros del componente de consulta de la dirección URL se convierten en secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="7b208-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="7b208-148">El valor predeterminado de esta opción es **Variant \_ true**, que especifica que se convierten los caracteres de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7b208-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**</span><span class="sxs-lookup"><span data-stu-id="7b208-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-150">Establece o recupera un **valor de tipo Variant** que indica qué protocolos seguros se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="7b208-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="7b208-151">Esta opción selecciona los protocolos aceptables para el cliente.</span><span class="sxs-lookup"><span data-stu-id="7b208-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="7b208-152">Se negocia el protocolo durante el protocolo de enlace de Capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="7b208-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="7b208-153">Puede ser una combinación de uno o varios de los siguientes marcadores.</span><span class="sxs-lookup"><span data-stu-id="7b208-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="7b208-154">Protocolo</span><span class="sxs-lookup"><span data-stu-id="7b208-154">Protocol</span></span>                           | <span data-ttu-id="7b208-155">Value</span><span class="sxs-lookup"><span data-stu-id="7b208-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="7b208-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="7b208-156">SSL 2.0</span></span>                            | <span data-ttu-id="7b208-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="7b208-157">0x0008</span></span> |
| <span data-ttu-id="7b208-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="7b208-158">SSL 3.0</span></span>                            | <span data-ttu-id="7b208-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="7b208-159">0x0020</span></span> |
| <span data-ttu-id="7b208-160">Seguridad de la capa de transporte (TLS) 1,0</span><span class="sxs-lookup"><span data-stu-id="7b208-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="7b208-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="7b208-161">0x0080</span></span> |



 

<span data-ttu-id="7b208-162">El valor predeterminado de esta opción es 0x0028, que indica que se puede usar SSL 2,0 o SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="7b208-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="7b208-163">Si esta opción se establece en cero, el cliente y el servidor no pueden determinar un protocolo de seguridad aceptable y el [**envío**](iwinhttprequest-send.md) siguiente produce un error.</span><span class="sxs-lookup"><span data-stu-id="7b208-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ enabletracing (**</span><span class="sxs-lookup"><span data-stu-id="7b208-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-165">Establece o recupera un **valor de tipo Variant** que indica si el seguimiento está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="7b208-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="7b208-166">Para obtener más información acerca de la utilidad de seguimiento en los servicios HTTP de Microsoft Windows (WinHTTP), consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="7b208-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b208-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**</span><span class="sxs-lookup"><span data-stu-id="7b208-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-168">Controla si el objeto [**WinHttpRequest**](winhttprequest.md) revierte temporalmente la suplantación del cliente durante la ejecución de las operaciones de autenticación de certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="7b208-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="7b208-169">La configuración predeterminada del objeto **WinHttpRequest** es **true**.</span><span class="sxs-lookup"><span data-stu-id="7b208-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="7b208-170">Establezca esta opción en **false** para mantener la suplantación mientras realiza operaciones de autenticación de certificado.</span><span class="sxs-lookup"><span data-stu-id="7b208-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**</span><span class="sxs-lookup"><span data-stu-id="7b208-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-172">Controla si WinHTTP permite o no redirecciones.</span><span class="sxs-lookup"><span data-stu-id="7b208-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="7b208-173">De forma predeterminada, se siguen automáticamente todas las redirecciones, excepto las que se transfieren desde una dirección URL segura (https) a una dirección URL no segura (http).</span><span class="sxs-lookup"><span data-stu-id="7b208-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="7b208-174">Establezca esta opción en **true** para habilitar las redirecciones de https a http.</span><span class="sxs-lookup"><span data-stu-id="7b208-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**</span><span class="sxs-lookup"><span data-stu-id="7b208-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-176">Habilita o deshabilita la compatibilidad con la autenticación de Passport.</span><span class="sxs-lookup"><span data-stu-id="7b208-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="7b208-177">De forma predeterminada, la compatibilidad automática con la autenticación de Passport está deshabilitada. Establezca esta opción en **true** para habilitar la compatibilidad con la autenticación de Passport.</span><span class="sxs-lookup"><span data-stu-id="7b208-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**</span><span class="sxs-lookup"><span data-stu-id="7b208-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-179">Establece o recupera el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="7b208-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="7b208-180">Este límite evita que sitios no autorizados realicen la detención del cliente WinHTTP después de un gran número de redirecciones.</span><span class="sxs-lookup"><span data-stu-id="7b208-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="7b208-181">**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7b208-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="7b208-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-183">Establece o recupera un conjunto enlazado en el tamaño máximo de la parte del encabezado de la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="7b208-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="7b208-184">Este enlace protege el cliente de un servidor malintencionado que intenta detener el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="7b208-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="7b208-185">El valor predeterminado es 64 KB.</span><span class="sxs-lookup"><span data-stu-id="7b208-185">The default value is 64 KB.</span></span>

<span data-ttu-id="7b208-186">**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7b208-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**</span><span class="sxs-lookup"><span data-stu-id="7b208-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-188">Establece o recupera un límite en la cantidad de datos que se van a purgar de las respuestas para reutilizar una conexión.</span><span class="sxs-lookup"><span data-stu-id="7b208-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="7b208-189">El valor predeterminado es 1 MB.</span><span class="sxs-lookup"><span data-stu-id="7b208-189">The default is 1 MB.</span></span>

<span data-ttu-id="7b208-190">**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7b208-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7b208-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-192">Establece o recupera un valor booleano que indica si se debe usar HTTP/1.1 o HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="7b208-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="7b208-193">El valor predeterminado es **true**, por lo que se utiliza http/1.1 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b208-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="7b208-194">**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7b208-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7b208-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="7b208-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="7b208-196">Habilita la comprobación de revocación de certificados de servidor durante la negociación SSL.</span><span class="sxs-lookup"><span data-stu-id="7b208-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="7b208-197">Cuando el servidor presenta un certificado, se realiza una comprobación para determinar si el emisor ha revocado el certificado.</span><span class="sxs-lookup"><span data-stu-id="7b208-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="7b208-198">Si el certificado se revoca realmente o se produce un error en la comprobación de revocación porque no se puede descargar la lista de revocación de certificados (CRL), se produce un error en la solicitud. estos errores de revocación no se pueden suprimir.</span><span class="sxs-lookup"><span data-stu-id="7b208-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="7b208-199">**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7b208-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b208-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b208-200">Remarks</span></span>

<span data-ttu-id="7b208-201">Establezca una opción especificando una de las constantes anteriores como parámetro de la propiedad [**Option**](iwinhttprequest-option.md) .</span><span class="sxs-lookup"><span data-stu-id="7b208-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="7b208-202">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="7b208-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b208-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b208-203">Requirements</span></span>



| <span data-ttu-id="7b208-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b208-204">Requirement</span></span> | <span data-ttu-id="7b208-205">Value</span><span class="sxs-lookup"><span data-stu-id="7b208-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b208-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b208-206">Minimum supported client</span></span><br/> | <span data-ttu-id="7b208-207">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="7b208-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7b208-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b208-208">Minimum supported server</span></span><br/> | <span data-ttu-id="7b208-209">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="7b208-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7b208-210">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7b208-210">Redistributable</span></span><br/>          | <span data-ttu-id="7b208-211">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7b208-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7b208-212">IDL</span><span class="sxs-lookup"><span data-stu-id="7b208-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b208-213"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b208-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b208-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b208-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b208-215">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7b208-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




