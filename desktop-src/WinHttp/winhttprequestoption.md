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
# <a name="winhttprequestoption-enumeration"></a>Enumeración WinHttpRequestOption

La enumeración **WinHttpRequestOption** incluye opciones que se pueden establecer o recuperar para la sesión actual de servicios http de Microsoft Windows (WinHTTP).

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

Establece o recupera un **valor de tipo Variant** que contiene la cadena del [*agente de usuario*](glossary.md) .

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_Dirección URL de WinHttpRequestOption**
</dt> <dd>

Recupera un **valor de tipo Variant** que contiene la dirección URL del recurso. Este valor es de solo lectura; no se puede establecer la dirección URL mediante esta propiedad. No se puede leer la dirección URL hasta que se llame al método [**Open**](iwinhttprequest-open.md) . Esta opción es útil para comprobar la dirección URL una vez finalizado el método [**send**](iwinhttprequest-send.md) para comprobar que se ha producido alguna redirección.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**
</dt> <dd>

Establece o recupera una **variante** que identifica la [*Página de códigos*](glossary.md) de la cadena de dirección URL. El valor predeterminado es la página de códigos UTF-8. La página de códigos se usa para convertir la cadena de dirección URL de Unicode, pasada en el método [**Open**](iwinhttprequest-open.md) , en una representación de cadena de un solo byte.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica si los caracteres de porcentaje de la cadena de dirección URL se convierten en una secuencia de escape. El valor predeterminado de esta opción es **Variant \_ true** , que especifica todos los caracteres de American National Standards Institute no seguros (ANSI), excepto que el símbolo de porcentaje se convierte en una secuencia de escape.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica qué errores de certificado de servidor se deben omitir. Puede ser una combinación de uno o varios de los siguientes marcadores.



| Error                                                  | Value  |
|--------------------------------------------------------|--------|
| Entidad de certificación (CA) desconocida o raíz que no es de confianza | 0x0100 |
| Uso incorrecto                                            | 0x0200 |
| Nombre común (CN) no válido                               | 0x1000 |
| Fecha no válida o certificado expirado                    | 0x2000 |



 

El valor predeterminado de esta opción en la versión 5,1 de WinHTTP es cero, lo que da lugar a que no se omitan errores. En versiones anteriores de WinHTTP, la configuración predeterminada era 0x3300, lo que daba lugar a que todos los errores de certificado de servidor se omitiran de forma predeterminada.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

Establece una **variante** que especifica el certificado de cliente que se envía a un servidor para la autenticación. Esta opción indica la ubicación, el [*almacén de certificados*](glossary.md)y el asunto de un certificado de cliente delimitado por barras diagonales inversas. Para obtener más información acerca de cómo seleccionar un certificado de cliente, consulte [SSL en WinHTTP](ssl-in-winhttp.md).

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica si las solicitudes se redirigen automáticamente cuando el servidor especifica una nueva ubicación para el recurso. El valor predeterminado de esta opción es **Variant \_ true** para indicar que las solicitudes se redirigen automáticamente.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica si los caracteres no seguros de la ruta de acceso y los componentes de consulta de una dirección URL se convierten en secuencias de escape. El valor predeterminado de esta opción es **Variant \_ true**, que especifica que se convierten los caracteres de la ruta de acceso y la consulta.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica si los caracteres no seguros del componente de consulta de la dirección URL se convierten en secuencias de escape. El valor predeterminado de esta opción es **Variant \_ true**, que especifica que se convierten los caracteres de la consulta.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica qué protocolos seguros se pueden usar. Esta opción selecciona los protocolos aceptables para el cliente. Se negocia el protocolo durante el protocolo de enlace de Capa de sockets seguros (SSL). Puede ser una combinación de uno o varios de los siguientes marcadores.



| Protocolo                           | Value  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Seguridad de la capa de transporte (TLS) 1,0 | 0x0080 |



 

El valor predeterminado de esta opción es 0x0028, que indica que se puede usar SSL 2,0 o SSL 3,0. Si esta opción se establece en cero, el cliente y el servidor no pueden determinar un protocolo de seguridad aceptable y el [**envío**](iwinhttprequest-send.md) siguiente produce un error.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ enabletracing (**
</dt> <dd>

Establece o recupera un **valor de tipo Variant** que indica si el seguimiento está habilitado actualmente. Para obtener más información acerca de la utilidad de seguimiento en los servicios HTTP de Microsoft Windows (WinHTTP), consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

Controla si el objeto [**WinHttpRequest**](winhttprequest.md) revierte temporalmente la suplantación del cliente durante la ejecución de las operaciones de autenticación de certificado SSL. La configuración predeterminada del objeto **WinHttpRequest** es **true**. Establezca esta opción en **false** para mantener la suplantación mientras realiza operaciones de autenticación de certificado.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

Controla si WinHTTP permite o no redirecciones. De forma predeterminada, se siguen automáticamente todas las redirecciones, excepto las que se transfieren desde una dirección URL segura (https) a una dirección URL no segura (http). Establezca esta opción en **true** para habilitar las redirecciones de https a http.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

Habilita o deshabilita la compatibilidad con la autenticación de Passport. De forma predeterminada, la compatibilidad automática con la autenticación de Passport está deshabilitada. Establezca esta opción en **true** para habilitar la compatibilidad con la autenticación de Passport.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

Establece o recupera el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10. Este límite evita que sitios no autorizados realicen la detención del cliente WinHTTP después de un gran número de redirecciones.

**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

Establece o recupera un conjunto enlazado en el tamaño máximo de la parte del encabezado de la respuesta del servidor. Este enlace protege el cliente de un servidor malintencionado que intenta detener el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado. El valor predeterminado es 64 KB.

**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

Establece o recupera un límite en la cantidad de datos que se van a purgar de las respuestas para reutilizar una conexión. El valor predeterminado es 1 MB.

**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Establece o recupera un valor booleano que indica si se debe usar HTTP/1.1 o HTTP/1.0. El valor predeterminado es **true**, por lo que se utiliza http/1.1 de forma predeterminada.

**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

Habilita la comprobación de revocación de certificados de servidor durante la negociación SSL. Cuando el servidor presenta un certificado, se realiza una comprobación para determinar si el emisor ha revocado el certificado. Si el certificado se revoca realmente o se produce un error en la comprobación de revocación porque no se puede descargar la lista de revocación de certificados (CRL), se produce un error en la solicitud. estos errores de revocación no se pueden suprimir.

**Windows XP con SP1 y windows 2000 con SP3:** No se admite este valor de enumeración.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Establezca una opción especificando una de las constantes anteriores como parámetro de la propiedad [**Option**](iwinhttprequest-option.md) .

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




