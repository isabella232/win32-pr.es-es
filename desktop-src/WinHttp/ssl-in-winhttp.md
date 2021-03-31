---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) admiten transacciones de Capa de sockets seguros (SSL), incluidos los certificados de cliente. En este tema se explican los conceptos implicados en una transacción SSL y cómo se administran mediante WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277327"
---
# <a name="ssl-in-winhttp"></a>SSL en WinHTTP

Los servicios HTTP de Microsoft Windows (WinHTTP) admiten transacciones de Capa de sockets seguros (SSL), incluidos los certificados de cliente. En este tema se explican los conceptos implicados en una transacción SSL y cómo se administran mediante WinHTTP.

## <a name="secure-sockets-layer"></a>Capa de sockets seguros

SSL es un estándar establecido para garantizar la seguridad de las transacciones HTTP. SSL proporciona un mecanismo para realizar el cifrado de hasta 128 bits en todas las transacciones entre el cliente y el servidor. Permite al cliente comprobar que el servidor pertenece a una entidad de confianza mediante el uso de certificados de servidor. También permite al servidor confirmar la identidad del cliente con los certificados de cliente.

Cada uno de estos problemas, el cifrado, la identidad del servidor y la identidad del cliente se negocian en el protocolo de enlace SSL que se produce cuando un cliente solicita primero un recurso de un servidor de protocolo seguro de transferencia de hipertexto (HTTPS). Esencialmente, el cliente y el servidor presentan cada uno una lista de los valores obligatorios y preferidos. Si se puede acordar y cumplir un conjunto común de requisitos, se establece una conexión SSL.

WinHTTP proporciona una interfaz de alto nivel para usar SSL. Aunque los detalles del Protocolo de enlace SSL y la transacción se controlan internamente, WinHTTP le permite recuperar los niveles de cifrado, especificar el protocolo de seguridad e interactuar con los certificados de cliente y servidor. En las secciones siguientes se proporcionan detalles sobre la creación de aplicaciones basadas en WinHTTP que eligen una versión del protocolo SSL, examinan los certificados de servidor y seleccionan los certificados de cliente que se envían a los servidores HTTPS.

## <a name="server-certificates"></a>Certificados de servidor

Los certificados de servidor se envían desde el servidor al cliente para que el cliente pueda obtener una clave pública para el servidor y asegurarse de que una entidad de certificación ha comprobado el servidor. Los certificados pueden contener tipos diferentes de datos. Por ejemplo, un certificado X. 509 incluye el formato del certificado, el número de serie del certificado, el algoritmo utilizado para firmar el certificado, el nombre de la entidad de certificación (CA) que emitió el certificado, el nombre y la clave pública de la entidad que solicita el certificado y la firma de la CA.

Cuando se usa la interfaz de programación de aplicaciones (API) de WinHTTP, se puede recuperar un certificado de servidor mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y especificar la [**\_ opción WinHTTP \_ certificado de seguridad \_ \_**](option-flags.md) de la etiqueta. El certificado de servidor se devuelve en una estructura de [**\_ \_ información de certificado WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . Si prefiere recuperar el contexto del certificado, especifique en su lugar la [**opción WinHTTP del \_ \_ \_ \_ contexto del servidor**](option-flags.md) de la opción.

Si un certificado de servidor contiene errores, se pueden obtener detalles sobre el error en la función de devolución de llamada de estado. La notificación de [**\_ \_ \_ \_ error seguro de estado de devolución de llamada de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica un error con un certificado de servidor. El parámetro *lpvStatusInformation* contiene una o más marcas de error detalladas. Consulte [**\_ devolución de \_ llamada de estado de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para obtener más información.

## <a name="client-certificates"></a>Certificados de cliente

Durante el protocolo de enlace SSL, es posible que el servidor requiera autenticación. El cliente se autentica proporcionando un certificado de cliente válido al servidor. WinHTTP permite seleccionar y enviar un certificado desde un [*almacén de certificados*](glossary.md)local. En las secciones siguientes se describe el proceso que proporciona certificados de cliente cuando se usa la API de WinHTTP o el objeto [**WinHttpRequest**](winhttprequest.md) .

### <a name="winhttp-api"></a>API de WinHTTP

Tanto [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) pueden no indicar que una solicitud no se realizó correctamente porque el servidor HTTPS requiere autenticación. En estos casos, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para devolver el error \_ WinHTTP \_ Client \_ auth \_ CERT \_ necesario. Tras recibir este error, use las funciones de [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) adecuadas para encontrar un certificado adecuado. Indique que este certificado se debe enviar con la solicitud siguiente; para ello, llame a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la [**opción de WinHTTP de \_ \_ \_ \_ contexto de certificado de cliente**](option-flags.md) .

En el ejemplo de código siguiente se muestra cómo abrir un [*almacén de certificados*](glossary.md) y ubicar un certificado basado en el nombre del sujeto después de que se \_ \_ \_ \_ \_ haya devuelto el error de certificado de autenticación del cliente winhttp.


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



Antes de volver a enviar una solicitud que contiene un certificado de cliente, puede determinar si el nivel de cifrado admitido es aceptable para su aplicación. Llame a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y especifique la marca de seguridad de la [**\_ opción \_ \_ WinHTTP**](option-flags.md) para determinar el nivel de cifrado que se utiliza.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Recuperación de lista de emisores para la autenticación de cliente SSL

Cuando la aplicación cliente de WinHttp envía una solicitud a un servidor HTTP seguro que requiere autenticación de cliente SSL, WinHttp devuelve un **error de \_ certificado de autenticación de \_ cliente WinHTTP \_ \_ \_ necesario** si la aplicación no ha proporcionado un certificado de cliente. En el caso de los equipos que ejecutan Windows Server 2008 y Windows Vista, WinHttp permite que la aplicación recupere la lista de emisores de certificados proporcionada por el servidor en el desafío de autenticación. La lista de emisores especifica una lista de entidades de certificación (CA) autorizadas por el servidor para emitir certificados de cliente. La aplicación filtra la lista de emisores para obtener el certificado necesario.

La aplicación cliente WinHttp recupera la lista de emisores cuando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve el **error \_ WinHTTP \_ Client \_ auth \_ CERT \_ necesario**. Cuando se devuelve este error, la aplicación llama a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente de la opción WinHTTP** . El parámetro *lpBuffer* debe ser lo suficientemente grande como para contener un puntero a la estructura [ \_ IssuerListInfoEx de SecPkgContext](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) . En el ejemplo de código siguiente se muestra cómo recuperar la lista de emisores.


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



La información de la estructura [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* y *aIssuers*, se puede usar para buscar el certificado, tal como se muestra en el ejemplo de código siguiente. Para obtener más información, vea [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a>Certificados SSL de cliente opcionales

A partir de Windows Server 2008 y Windows Vista, la API de WinHttp admite certificados de cliente opcionales. Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un error de certificado de **\_ \_ autenticación de cliente \_ \_ \_ WinHTTP** . Si el servidor solicita el certificado, pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado. El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor. La aplicación especifica la macro de **\_ contexto WinHTTP no \_ Client \_ CERT \_** en el parámetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , tal y como se muestra en el ejemplo de código siguiente.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Si se establece el **\_ contexto de certificado de \_ cliente \_ \_ WinHTTP no** y el servidor requiere un certificado de cliente, puede enviar un código de estado http 403. Para obtener más información, consulte la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente** .

### <a name="winhttprequest-object"></a>Objeto WinHttpRequest

Use el método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) del objeto [**WinHttpRequest**](winhttprequest.md) para seleccionar los certificados de cliente que se enviarán al servidor con una solicitud. Seleccione un certificado especificando una cadena de selección de certificado con el método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) . La cadena de selección de certificado consta de la ubicación del certificado, el [*almacén de certificados*](glossary.md)y el nombre de sujeto delimitados por barras diagonales inversas. En la tabla siguiente se enumeran los componentes de esta cadena de selección.



| Componente                                                  | Descripción                                                                                                                                                                                        | Valores posibles                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Location                                                   | Determina la clave del registro en la que se almacenan los certificados.                                                                                                                               | Los valores posibles son " \_ equipo local" para indicar que el [*almacén de certificados*](glossary.md) está en **HKEY \_ local \_ Machine** .<br/> y " \_ usuario actual" para indicar que el *almacén de certificados* está bajo el **\_ usuario actual HKEY \_** no suplantado.<br/> Este componente distingue entre mayúsculas y minúsculas. |
| [*Almacén de certificados*](glossary.md) | Indica el nombre del [*almacén de certificados*](glossary.md) que contiene el certificado pertinente.                                                                       | Los [*almacenes de certificados*](glossary.md) típicos son "My", "root" y "TrustedPeople". Este componente distingue entre mayúsculas y minúsculas.                                                                                                                                                                                          |
| Nombre de sujeto                                               | Identifica un certificado en el [*almacén de certificados*](glossary.md)especificado. Se selecciona el primer certificado que contiene la cadena especificada para este componente. | El nombre del firmante puede ser cualquier cadena. Una cadena en blanco indica que se debe utilizar el primer certificado del [*almacén de certificados*](glossary.md) . Este componente no distingue mayúsculas de minúsculas.                                                                                                                         |



 

El nombre y la ubicación del [*almacén de certificados*](glossary.md) son componentes opcionales. Sin embargo, si especifica un *almacén de certificados*, también debe especificar la ubicación del *almacén de certificados*. La ubicación predeterminada es \_ usuario actual y el *almacén de certificados* predeterminado es "My".

En el ejemplo de código siguiente se muestra cómo especificar que se debe elegir un certificado con el asunto "My Middle-Tier Certificate" en el [*almacén de certificados*](glossary.md) "personal" del registro en **HKEY \_ local \_ Machine**.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> En algunos idiomas, la barra diagonal inversa es un carácter de escape. Recuerde modificar la cadena de selección de certificado para ello. Por ejemplo, en Microsoft JScript, use dos barras diagonales inversas adyacentes en lugar de una.

 

Si no especifica un certificado y un servidor HTTPS requiere un certificado de cliente, WinHTTP selecciona el primer certificado del [*almacén de certificados*](glossary.md)predeterminado. Si no existe ningún certificado, se produce un error. Si no se acepta el certificado, el servidor devuelve un código de estado 403 para indicar que no se puede cumplir la solicitud. Después, puede elegir un certificado más adecuado con [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) y volver a enviar la solicitud.

 

