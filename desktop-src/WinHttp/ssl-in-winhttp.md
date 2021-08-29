---
description: Microsoft Windows HTTP Services (WinHTTP) admite transacciones Capa de sockets seguros (SSL), incluidos los certificados de cliente. En este tema se explican los conceptos implicados en una transacción SSL y cómo se controlan mediante WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a041d55de85250edb1932aa3df4d114af8ef89fce6e56c3763cb235168b65be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133038"
---
# <a name="ssl-in-winhttp"></a>SSL en WinHTTP

Microsoft Windows HTTP Services (WinHTTP) admite transacciones Capa de sockets seguros (SSL), incluidos los certificados de cliente. En este tema se explican los conceptos implicados en una transacción SSL y cómo se controlan mediante WinHTTP.

## <a name="secure-sockets-layer"></a>Capa de sockets seguros

SSL es un estándar establecido para garantizar transacciones HTTP seguras. SSL proporciona un mecanismo para realizar un cifrado de hasta 128 bits en todas las transacciones entre el cliente y el servidor. Permite al cliente comprobar que el servidor pertenece a una entidad de confianza mediante el uso de certificados de servidor. También permite al servidor confirmar la identidad del cliente con certificados de cliente.

Cada uno de estos problemas de cifrado, identidad de servidor e identidad de cliente se negocian en el protocolo de enlace SSL que tiene lugar cuando un cliente solicita por primera vez un recurso de un servidor https (Protocolo de transferencia de hipertexto seguro). Básicamente, el cliente y el servidor presentan una lista de configuraciones obligatorias y preferidas. Si se puede acordar y cumplir un conjunto común de requisitos, se establece una conexión SSL.

WinHTTP proporciona una interfaz de alto nivel para usar SSL. Aunque los detalles del protocolo de enlace SSL y la transacción se controlan internamente, WinHTTP permite recuperar niveles de cifrado, especificar el protocolo de seguridad e interactuar con certificados de servidor y cliente. En las secciones siguientes se proporcionan detalles sobre cómo crear aplicaciones basadas en WinHTTP que eligen una versión del protocolo SSL, examinan los certificados de servidor y seleccionan los certificados de cliente que se envían a los servidores HTTPS.

## <a name="server-certificates"></a>Certificados de servidor

Los certificados de servidor se envían desde el servidor al cliente para que el cliente pueda obtener una clave pública para el servidor y asegurarse de que el servidor ha sido comprobado por una entidad de certificación. Los certificados pueden contener tipos diferentes de datos. Por ejemplo, un certificado X.509 incluye el formato del certificado, el número de serie del certificado, el algoritmo utilizado para firmar el certificado, el nombre de la entidad de certificación (CA) que emitió el certificado, el nombre y la clave pública de la entidad que solicita el certificado y la firma de la entidad de certificación.

Al usar la interfaz de programación de aplicaciones (API) WinHTTP, puede recuperar un certificado de servidor llamando a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y especificando la marca [**\_ \_ \_ \_ STRUCT DE CERTIFICADO**](option-flags.md) DE SEGURIDAD DE WINHTTP OPTION. El certificado de servidor se devuelve en una [**estructura DE INFORMACIÓN DE CERTIFICADO \_ \_ WINHTTP.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) Si prefiere recuperar el contexto del certificado, especifique la marca [**WINHTTP \_ OPTION SERVER CERT \_ \_ \_ CONTEXT**](option-flags.md) en su lugar.

Si un certificado de servidor contiene errores, se pueden obtener detalles sobre el error en la función de devolución de llamada de estado. La [**notificación WINHTTP \_ CALLBACK STATUS SECURE \_ \_ \_ FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica un error con un certificado de servidor. El *parámetro lpvStatusInformation* contiene una o varias marcas de error detalladas. Consulte [**DEVOLUCIÓN DE \_ LLAMADA DE \_ ESTADO WINHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para obtener más información.

## <a name="client-certificates"></a>Certificados de cliente

Durante el protocolo de enlace SSL, el servidor puede requerir autenticación. El cliente se autentica mediante el suministro de un certificado de cliente válido al servidor. WinHTTP permite seleccionar y enviar un certificado desde un almacén de [*certificados local.*](glossary.md) En las secciones siguientes se describe el proceso que proporciona certificados de cliente cuando se usa la API WinHTTP o el [**objeto WinHttpRequest.**](winhttprequest.md)

### <a name="winhttp-api"></a>WinHTTP API

Tanto [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) pueden no indicar que una solicitud no se ha hecho correctamente porque el servidor HTTPS requiere autenticación. En estos casos, llame [**a GetLastError para**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolver ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED. Tras recibir este error, use las funciones [de CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) adecuadas para encontrar un certificado adecuado. Indique que este certificado se debe enviar con la siguiente solicitud llamando a [**WinHttpSetOption con**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) la marca DE CONTEXTO DE CERT [**\_ \_ \_ \_ DE CLIENTE**](option-flags.md) DE LA OPCIÓN WINHTTP.

En el ejemplo de código [](glossary.md) siguiente se muestra cómo abrir un almacén de certificados y buscar un certificado basado en el nombre del sujeto después de que se haya devuelto el error ERROR \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED.


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



Antes de volver a enviar una solicitud que contiene un certificado de cliente, puede determinar si el nivel de cifrado admitido es aceptable para la aplicación. Llame [**a WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y especifique la [**marca WINHTTP OPTION SECURITY \_ \_ \_ FLAGS**](option-flags.md) para determinar el nivel de cifrado que se usa.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Recuperación de la lista de emisores para la autenticación de cliente SSL

Cuando la aplicación cliente WinHttp envía una solicitud a un servidor HTTP seguro que requiere autenticación de cliente SSL, WinHttp devuelve un **ERROR \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED** si la aplicación no ha proporcionado un certificado de cliente. En el caso de los equipos que se ejecutan en Windows Server 2008 y Windows Vista, WinHttp permite a la aplicación recuperar la lista de emisores de certificados proporcionada por el servidor en el desafío de autenticación. La lista de emisores especifica una lista de entidades de certificación (CA) autorizadas por el servidor para emitir certificados de cliente. La aplicación filtra la lista de emisores para obtener el certificado necesario.

La aplicación cliente WinHttp recupera la lista de emisores cuando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve **ERROR \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED**. Cuando se devuelve este error, la aplicación llama [**a WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción **\_ WINHTTP OPTION \_ CLIENT CERT \_ \_ ISSUER \_ LIST.** El *parámetro lpBuffer* debe ser lo suficientemente grande como para contener un puntero a la estructura [SecPkgContext \_ IssuerListInfoEx.](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) En el ejemplo de código siguiente se muestra cómo recuperar la lista de emisores.


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



La información de la estructura [ \_ SecPkgContext IssuerListInfoEx,](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) *cIssuers* y *aIssuers* se puede usar para buscar el certificado, como se muestra en el ejemplo de código siguiente. Para obtener más información, [**vea CertFindChainInStore.**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore)


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

A partir Windows Server 2008 y Windows Vista, la API WinHttp admite certificados de cliente opcionales. Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un **error ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED.** Si el servidor solicita el certificado, pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado. El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor. La aplicación especifica la macro **WINHTTP \_ NO CLIENT \_ CERT \_ \_ CONTEXT** en el parámetro *lpBuffer* de [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) como se muestra en el ejemplo de código siguiente.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Si se **establece WINHTTP \_ NO CLIENT \_ CERT \_ \_ CONTEXT** y el servidor todavía requiere un certificado de cliente, puede enviar un código de estado HTTP 403. Para obtener más información, vea la **opción \_ WINHTTP OPTION \_ CLIENT CERT \_ \_ ISSUER \_ LIST.**

### <a name="winhttprequest-object"></a>Objeto WinHttpRequest

Use el [**método SetClientCertificate**](iwinhttprequest-setclientcertificate.md) del [**objeto WinHttpRequest**](winhttprequest.md) para seleccionar los certificados de cliente que se enviarán al servidor con una solicitud. Seleccione un certificado especificando una cadena de selección de certificado con el [**método SetClientCertificate.**](iwinhttprequest-setclientcertificate.md) La cadena de selección de certificado consta de la ubicación [*del*](glossary.md)certificado, el almacén de certificados y el nombre del firmantes delimitados por barras diagonales inversas. En la tabla siguiente se enumeran los componentes de esta cadena de selección.



| Componente                                                  | Descripción                                                                                                                                                                                        | Valores posibles                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ubicación                                                   | Determina la clave del Registro en la que se almacenan los certificados.                                                                                                                               | Los valores posibles son "LOCAL \_ MACHINE" para indicar que el almacén [*de certificados*](glossary.md) está en **HKEY LOCAL \_ \_ MACHINE**<br/> y "CURRENT \_ USER" para indicar que el almacén *de certificados* está en el **HKEY CURRENT USER no \_ \_ suplantado.**<br/> Este componente distingue mayúsculas de minúsculas. |
| [*Almacén de certificados*](glossary.md) | Indica el nombre del almacén [*de certificados*](glossary.md) que contiene el certificado correspondiente.                                                                       | Los [*almacenes de certificados*](glossary.md) típicos son "MY", "Root" y "TrustedPeople". Este componente distingue mayúsculas de minúsculas.                                                                                                                                                                                          |
| Nombre de sujeto                                               | Identifica un certificado dentro del almacén de [*certificados especificado.*](glossary.md) Se selecciona el primer certificado que contiene la cadena especificada para este componente. | El nombre del sujeto puede ser cualquier cadena. Una cadena en blanco indica que se debe usar el primer certificado del [*almacén*](glossary.md) de certificados. Este componente no tiene en cuenta mayúsculas de minúsculas.                                                                                                                         |



 

El [*nombre y la*](glossary.md) ubicación del almacén de certificados son componentes opcionales. Sin embargo, si especifica un almacén *de certificados*, también debe especificar la ubicación de ese almacén *de certificados.* La ubicación predeterminada es CURRENT \_ USER y el almacén de certificados *predeterminado* es "MY".

En el ejemplo de código siguiente se muestra cómo especificar que se debe elegir un [](glossary.md) certificado con el asunto "Mi certificado de Middle-Tier" del almacén de certificados "Personal" en el Registro en **HKEY LOCAL \_ \_ MACHINE**.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> En algunos idiomas, la barra diagonal inversa es un carácter de escape. No olvide modificar la cadena de selección de certificado para tener en cuenta esto. Por ejemplo, en Microsoft JScript, use dos barras diagonales inversas adyacentes en lugar de una.

 

Si no especifica un certificado y un servidor HTTPS requiere un certificado de cliente, WinHTTP selecciona el primer certificado en el almacén [*de certificados predeterminado.*](glossary.md) Si no existe ningún certificado, se produce un error. Si no se acepta el certificado, el servidor devuelve un código de estado 403 para indicar que no se puede cumplir la solicitud. A continuación, puede elegir un certificado más adecuado [**con SetClientCertificate**](iwinhttprequest-setclientcertificate.md) y volver a enviar la solicitud.

 

