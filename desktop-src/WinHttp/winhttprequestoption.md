---
description: Incluye opciones que se pueden establecer o recuperar para la sesión actual de Microsoft Windows HTTP Services (WinHTTP).
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465612"
---
# <a name="winhttprequestoption-enumeration"></a>Enumeración WinHttpRequestOption

La **enumeración WinHttpRequestOption** incluye opciones que se pueden establecer o recuperar para la sesión actual de Microsoft Windows HTTP Services (WinHTTP).

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**
</dt> <dd>

Establece o recupera una **variant que** contiene la cadena del [*agente de*](glossary.md) usuario.

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**Dirección URL de WinHttpRequestOption \_**
</dt> <dd>

Recupera una **variant que** contiene la dirección URL del recurso. Este valor es de solo lectura; no puede establecer la dirección URL mediante esta propiedad. La dirección URL no se puede leer hasta que se [**llama**](iwinhttprequest-open.md) al método Open. Esta opción es útil para comprobar la dirección URL una vez finalizado [**el método Send**](iwinhttprequest-send.md) para comprobar que se ha producido cualquier redireccionamiento.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**UrlCodePage de WinHttpRequestOption \_**
</dt> <dd>

Establece o recupera una **variant que** identifica la página [*de códigos*](glossary.md) de la cadena de dirección URL. El valor predeterminado es la página de códigos UTF-8. La página de códigos se usa para convertir la cadena de dirección URL Unicode, pasada en el [**método Open,**](iwinhttprequest-open.md) en una representación de cadena de un solo byte.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

Establece o recupera una **variant que** indica si los caracteres de porcentaje de la cadena de dirección URL se convierten en una secuencia de escape. El valor predeterminado de esta opción es **VARIANT \_ TRUE,** que especifica todos los caracteres de American National Standards Institute no seguros (ANSI), excepto el símbolo de porcentaje, se convierten en una secuencia de escape.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

Establece o recupera una **variant que** indica qué errores de certificado de servidor se deben omitir. Puede ser una combinación de una o varias de las marcas siguientes.



| Error                                                  | Value  |
|--------------------------------------------------------|--------|
| Entidad de certificación (CA) desconocida o raíz que no es de confianza | 0x0100 |
| Uso incorrecto                                            | 0x0200 |
| Nombre común no válido (CN)                               | 0x1000 |
| Fecha o certificado expirados no válidos                    | 0x2000 |



 

El valor predeterminado de esta opción en la versión 5.1 de WinHTTP es cero, lo que no provoca que se ignoren los errores. En versiones anteriores de WinHTTP, la configuración predeterminada era 0x3300, lo que resultaba en que todos los errores de certificado de servidor se omitieron de forma predeterminada.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

Establece una **VARIANT** que especifica el certificado de cliente que se envía a un servidor para la autenticación. Esta opción indica la ubicación, el almacén [*de certificados*](glossary.md)y el asunto de un certificado de cliente delimitado por barras diagonales inversas. Para obtener más información sobre cómo seleccionar un certificado de cliente, vea [SSL en WinHTTP.](ssl-in-winhttp.md)

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

Establece o recupera una **variant que** indica si las solicitudes se redirigen automáticamente cuando el servidor especifica una nueva ubicación para el recurso. El valor predeterminado de esta opción es **VARIANT \_ TRUE** para indicar que las solicitudes se redirigen automáticamente.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**
</dt> <dd>

Establece o recupera una **variant que** indica si los caracteres no seguros de la ruta de acceso y los componentes de consulta de una dirección URL se convierten en secuencias de escape. El valor predeterminado de esta opción es **VARIANT \_ TRUE,** que especifica que se convierten los caracteres de la ruta de acceso y la consulta.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

Establece o recupera una **variant que** indica si los caracteres no seguros del componente de consulta de la dirección URL se convierten en secuencias de escape. El valor predeterminado de esta opción es **VARIANT \_ TRUE,** que especifica que se convierten los caracteres de la consulta.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

Establece o recupera una **variant** que indica qué protocolos seguros se pueden usar. Esta opción selecciona los protocolos aceptables para el cliente. El protocolo se negocia durante el protocolo Capa de sockets seguros protocolo de enlace (SSL). Puede ser una combinación de una o varias de las marcas siguientes.



| Protocolo                           | Value  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Seguridad de la capa de transporte (TLS) 1.0 | 0x0080 |



 

El valor predeterminado de esta opción es 0x0028, lo que indica que se puede usar SSL 2.0 o SSL 3.0. Si esta opción se establece en cero, el cliente y el servidor [](iwinhttprequest-send.md) no pueden determinar un protocolo de seguridad aceptable y el siguiente envío produce un error.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**EnableTracing de WinHttpRequestOption \_**
</dt> <dd>

Establece o recupera una **variant que** indica si el seguimiento está habilitado actualmente. Para obtener más información sobre la instalación de seguimiento en Microsoft Windows HTTP Services (WinHTTP), vea [Instalación de seguimiento winHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

Controla si el [**objeto WinHttpRequest**](winhttprequest.md) revierte temporalmente la suplantación de cliente mientras duren las operaciones de autenticación de certificados SSL. El valor predeterminado del **objeto WinHttpRequest** es **TRUE.** Establezca esta opción en **FALSE para** mantener la suplantación mientras se realizan operaciones de autenticación de certificados.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

Controla si WinHTTP permite o no redirecciones. De forma predeterminada, todas las redirecciones se siguen automáticamente, excepto las que se transfieren desde una dirección URL segura (https) a una dirección URL no segura (http). Establezca esta opción en **TRUE para** habilitar las redirecciones HTTPS a HTTP.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

Habilita o deshabilita la compatibilidad con la autenticación de Passport. De forma predeterminada, la compatibilidad automática con la autenticación de Passport está deshabilitada; establezca esta opción en **TRUE para** habilitar la compatibilidad con la autenticación de Passport.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

Establece o recupera el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10. Este límite impide que los sitios no autorizados impidan que el cliente WinHTTP se detenga después de un gran número de redirecciones.

**Windows XP con SP1 y Windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

Establece o recupera un conjunto enlazado en el tamaño máximo de la parte de encabezado de la respuesta del servidor. Este límite protege al cliente de un servidor malintencionado que intenta detener el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado. El valor predeterminado es 64 KB.

**Windows XP con SP1 y Windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

Establece o recupera un límite en la cantidad de datos que se purgarán de las respuestas para reutilizar una conexión. El valor predeterminado es 1 MB.

**Windows XP con SP1 y Windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Establece o recupera un valor booleano que indica si se debe usar HTTP/1.1 o HTTP/1.0. El valor predeterminado **es TRUE,** por lo que HTTP/1.1 se usa de forma predeterminada.

**Windows XP con SP1 y Windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

Habilita la comprobación de revocación de certificados de servidor durante la negociación SSL. Cuando el servidor presenta un certificado, se realiza una comprobación para determinar si el emisor ha revocado el certificado. Si el certificado se revoca realmente o se produce un error en la comprobación de revocación porque no se puede descargar la lista de revocación de certificados (CRL), se produce un error en la solicitud. estos errores de revocación no se pueden suprimir.

**Windows XP con SP1 y Windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Establezca una opción especificando una de las constantes anteriores como parámetro de la [**propiedad Option.**](iwinhttprequest-option.md)

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

 




