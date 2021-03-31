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
# <a name="ssl-in-winhttp"></a><span data-ttu-id="a6a98-104">SSL en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a6a98-104">SSL in WinHTTP</span></span>

<span data-ttu-id="a6a98-105">Los servicios HTTP de Microsoft Windows (WinHTTP) admiten transacciones de Capa de sockets seguros (SSL), incluidos los certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="a6a98-106">En este tema se explican los conceptos implicados en una transacción SSL y cómo se administran mediante WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a6a98-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="a6a98-107">Capa de sockets seguros</span><span class="sxs-lookup"><span data-stu-id="a6a98-107">Secure Sockets Layer</span></span>

<span data-ttu-id="a6a98-108">SSL es un estándar establecido para garantizar la seguridad de las transacciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6a98-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="a6a98-109">SSL proporciona un mecanismo para realizar el cifrado de hasta 128 bits en todas las transacciones entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="a6a98-110">Permite al cliente comprobar que el servidor pertenece a una entidad de confianza mediante el uso de certificados de servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="a6a98-111">También permite al servidor confirmar la identidad del cliente con los certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="a6a98-112">Cada uno de estos problemas, el cifrado, la identidad del servidor y la identidad del cliente se negocian en el protocolo de enlace SSL que se produce cuando un cliente solicita primero un recurso de un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="a6a98-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="a6a98-113">Esencialmente, el cliente y el servidor presentan cada uno una lista de los valores obligatorios y preferidos.</span><span class="sxs-lookup"><span data-stu-id="a6a98-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="a6a98-114">Si se puede acordar y cumplir un conjunto común de requisitos, se establece una conexión SSL.</span><span class="sxs-lookup"><span data-stu-id="a6a98-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="a6a98-115">WinHTTP proporciona una interfaz de alto nivel para usar SSL.</span><span class="sxs-lookup"><span data-stu-id="a6a98-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="a6a98-116">Aunque los detalles del Protocolo de enlace SSL y la transacción se controlan internamente, WinHTTP le permite recuperar los niveles de cifrado, especificar el protocolo de seguridad e interactuar con los certificados de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="a6a98-117">En las secciones siguientes se proporcionan detalles sobre la creación de aplicaciones basadas en WinHTTP que eligen una versión del protocolo SSL, examinan los certificados de servidor y seleccionan los certificados de cliente que se envían a los servidores HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a6a98-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="a6a98-118">Certificados de servidor</span><span class="sxs-lookup"><span data-stu-id="a6a98-118">Server Certificates</span></span>

<span data-ttu-id="a6a98-119">Los certificados de servidor se envían desde el servidor al cliente para que el cliente pueda obtener una clave pública para el servidor y asegurarse de que una entidad de certificación ha comprobado el servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="a6a98-120">Los certificados pueden contener tipos diferentes de datos.</span><span class="sxs-lookup"><span data-stu-id="a6a98-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="a6a98-121">Por ejemplo, un certificado X. 509 incluye el formato del certificado, el número de serie del certificado, el algoritmo utilizado para firmar el certificado, el nombre de la entidad de certificación (CA) que emitió el certificado, el nombre y la clave pública de la entidad que solicita el certificado y la firma de la CA.</span><span class="sxs-lookup"><span data-stu-id="a6a98-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="a6a98-122">Cuando se usa la interfaz de programación de aplicaciones (API) de WinHTTP, se puede recuperar un certificado de servidor mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y especificar la [**\_ opción WinHTTP \_ certificado de seguridad \_ \_**](option-flags.md) de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a6a98-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="a6a98-123">El certificado de servidor se devuelve en una estructura de [**\_ \_ información de certificado WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="a6a98-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="a6a98-124">Si prefiere recuperar el contexto del certificado, especifique en su lugar la [**opción WinHTTP del \_ \_ \_ \_ contexto del servidor**](option-flags.md) de la opción.</span><span class="sxs-lookup"><span data-stu-id="a6a98-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="a6a98-125">Si un certificado de servidor contiene errores, se pueden obtener detalles sobre el error en la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="a6a98-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="a6a98-126">La notificación de [**\_ \_ \_ \_ error seguro de estado de devolución de llamada de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indica un error con un certificado de servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="a6a98-127">El parámetro *lpvStatusInformation* contiene una o más marcas de error detalladas.</span><span class="sxs-lookup"><span data-stu-id="a6a98-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="a6a98-128">Consulte [**\_ devolución de \_ llamada de estado de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a6a98-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="a6a98-129">Certificados de cliente</span><span class="sxs-lookup"><span data-stu-id="a6a98-129">Client Certificates</span></span>

<span data-ttu-id="a6a98-130">Durante el protocolo de enlace SSL, es posible que el servidor requiera autenticación.</span><span class="sxs-lookup"><span data-stu-id="a6a98-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="a6a98-131">El cliente se autentica proporcionando un certificado de cliente válido al servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="a6a98-132">WinHTTP permite seleccionar y enviar un certificado desde un [*almacén de certificados*](glossary.md)local.</span><span class="sxs-lookup"><span data-stu-id="a6a98-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="a6a98-133">En las secciones siguientes se describe el proceso que proporciona certificados de cliente cuando se usa la API de WinHTTP o el objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a98-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="a6a98-134">API de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a6a98-134">WinHTTP API</span></span>

<span data-ttu-id="a6a98-135">Tanto [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) pueden no indicar que una solicitud no se realizó correctamente porque el servidor HTTPS requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="a6a98-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="a6a98-136">En estos casos, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para devolver el error \_ WinHTTP \_ Client \_ auth \_ CERT \_ necesario.</span><span class="sxs-lookup"><span data-stu-id="a6a98-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="a6a98-137">Tras recibir este error, use las funciones de [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) adecuadas para encontrar un certificado adecuado.</span><span class="sxs-lookup"><span data-stu-id="a6a98-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="a6a98-138">Indique que este certificado se debe enviar con la solicitud siguiente; para ello, llame a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la [**opción de WinHTTP de \_ \_ \_ \_ contexto de certificado de cliente**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a98-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="a6a98-139">En el ejemplo de código siguiente se muestra cómo abrir un [*almacén de certificados*](glossary.md) y ubicar un certificado basado en el nombre del sujeto después de que se \_ \_ \_ \_ \_ haya devuelto el error de certificado de autenticación del cliente winhttp.</span><span class="sxs-lookup"><span data-stu-id="a6a98-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


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



<span data-ttu-id="a6a98-140">Antes de volver a enviar una solicitud que contiene un certificado de cliente, puede determinar si el nivel de cifrado admitido es aceptable para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6a98-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="a6a98-141">Llame a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y especifique la marca de seguridad de la [**\_ opción \_ \_ WinHTTP**](option-flags.md) para determinar el nivel de cifrado que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a6a98-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="a6a98-142">Recuperación de lista de emisores para la autenticación de cliente SSL</span><span class="sxs-lookup"><span data-stu-id="a6a98-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="a6a98-143">Cuando la aplicación cliente de WinHttp envía una solicitud a un servidor HTTP seguro que requiere autenticación de cliente SSL, WinHttp devuelve un **error de \_ certificado de autenticación de \_ cliente WinHTTP \_ \_ \_ necesario** si la aplicación no ha proporcionado un certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="a6a98-144">En el caso de los equipos que ejecutan Windows Server 2008 y Windows Vista, WinHttp permite que la aplicación recupere la lista de emisores de certificados proporcionada por el servidor en el desafío de autenticación.</span><span class="sxs-lookup"><span data-stu-id="a6a98-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="a6a98-145">La lista de emisores especifica una lista de entidades de certificación (CA) autorizadas por el servidor para emitir certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="a6a98-146">La aplicación filtra la lista de emisores para obtener el certificado necesario.</span><span class="sxs-lookup"><span data-stu-id="a6a98-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="a6a98-147">La aplicación cliente WinHttp recupera la lista de emisores cuando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve el **error \_ WinHTTP \_ Client \_ auth \_ CERT \_ necesario**.</span><span class="sxs-lookup"><span data-stu-id="a6a98-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="a6a98-148">Cuando se devuelve este error, la aplicación llama a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente de la opción WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="a6a98-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="a6a98-149">El parámetro *lpBuffer* debe ser lo suficientemente grande como para contener un puntero a la estructura [ \_ IssuerListInfoEx de SecPkgContext](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) .</span><span class="sxs-lookup"><span data-stu-id="a6a98-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="a6a98-150">En el ejemplo de código siguiente se muestra cómo recuperar la lista de emisores.</span><span class="sxs-lookup"><span data-stu-id="a6a98-150">The following code example shows how to retrieve the issuer list.</span></span>


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



<span data-ttu-id="a6a98-151">La información de la estructura [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* y *aIssuers*, se puede usar para buscar el certificado, tal como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="a6a98-152">Para obtener más información, vea [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span><span class="sxs-lookup"><span data-stu-id="a6a98-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


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



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="a6a98-153">Certificados SSL de cliente opcionales</span><span class="sxs-lookup"><span data-stu-id="a6a98-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="a6a98-154">A partir de Windows Server 2008 y Windows Vista, la API de WinHttp admite certificados de cliente opcionales.</span><span class="sxs-lookup"><span data-stu-id="a6a98-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="a6a98-155">Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un error de certificado de **\_ \_ autenticación de cliente \_ \_ \_ WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="a6a98-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="a6a98-156">Si el servidor solicita el certificado, pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado.</span><span class="sxs-lookup"><span data-stu-id="a6a98-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="a6a98-157">El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor.</span><span class="sxs-lookup"><span data-stu-id="a6a98-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="a6a98-158">La aplicación especifica la macro de **\_ contexto WinHTTP no \_ Client \_ CERT \_** en el parámetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="a6a98-159">Si se establece el **\_ contexto de certificado de \_ cliente \_ \_ WinHTTP no** y el servidor requiere un certificado de cliente, puede enviar un código de estado http 403.</span><span class="sxs-lookup"><span data-stu-id="a6a98-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="a6a98-160">Para obtener más información, consulte la opción **WinHTTP \_ \_ \_ \_ \_ lista de emisores de certificados de cliente** .</span><span class="sxs-lookup"><span data-stu-id="a6a98-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="a6a98-161">Objeto WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="a6a98-161">WinHttpRequest Object</span></span>

<span data-ttu-id="a6a98-162">Use el método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) del objeto [**WinHttpRequest**](winhttprequest.md) para seleccionar los certificados de cliente que se enviarán al servidor con una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6a98-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="a6a98-163">Seleccione un certificado especificando una cadena de selección de certificado con el método [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a98-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="a6a98-164">La cadena de selección de certificado consta de la ubicación del certificado, el [*almacén de certificados*](glossary.md)y el nombre de sujeto delimitados por barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="a6a98-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="a6a98-165">En la tabla siguiente se enumeran los componentes de esta cadena de selección.</span><span class="sxs-lookup"><span data-stu-id="a6a98-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="a6a98-166">Componente</span><span class="sxs-lookup"><span data-stu-id="a6a98-166">Component</span></span>                                                  | <span data-ttu-id="a6a98-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6a98-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="a6a98-168">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a6a98-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a98-169">Location</span><span class="sxs-lookup"><span data-stu-id="a6a98-169">Location</span></span>                                                   | <span data-ttu-id="a6a98-170">Determina la clave del registro en la que se almacenan los certificados.</span><span class="sxs-lookup"><span data-stu-id="a6a98-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="a6a98-171">Los valores posibles son " \_ equipo local" para indicar que el [*almacén de certificados*](glossary.md) está en **HKEY \_ local \_ Machine** .</span><span class="sxs-lookup"><span data-stu-id="a6a98-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="a6a98-172">y " \_ usuario actual" para indicar que el *almacén de certificados* está bajo el **\_ usuario actual HKEY \_** no suplantado.</span><span class="sxs-lookup"><span data-stu-id="a6a98-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="a6a98-173">Este componente distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6a98-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="a6a98-174">*Almacén de certificados*</span><span class="sxs-lookup"><span data-stu-id="a6a98-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="a6a98-175">Indica el nombre del [*almacén de certificados*](glossary.md) que contiene el certificado pertinente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="a6a98-176">Los [*almacenes de certificados*](glossary.md) típicos son "My", "root" y "TrustedPeople".</span><span class="sxs-lookup"><span data-stu-id="a6a98-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="a6a98-177">Este componente distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6a98-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a6a98-178">Nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="a6a98-178">Subject name</span></span>                                               | <span data-ttu-id="a6a98-179">Identifica un certificado en el [*almacén de certificados*](glossary.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="a6a98-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="a6a98-180">Se selecciona el primer certificado que contiene la cadena especificada para este componente.</span><span class="sxs-lookup"><span data-stu-id="a6a98-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="a6a98-181">El nombre del firmante puede ser cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="a6a98-181">The subject name can be any string.</span></span> <span data-ttu-id="a6a98-182">Una cadena en blanco indica que se debe utilizar el primer certificado del [*almacén de certificados*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a98-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="a6a98-183">Este componente no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6a98-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="a6a98-184">El nombre y la ubicación del [*almacén de certificados*](glossary.md) son componentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="a6a98-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="a6a98-185">Sin embargo, si especifica un *almacén de certificados*, también debe especificar la ubicación del *almacén de certificados*.</span><span class="sxs-lookup"><span data-stu-id="a6a98-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="a6a98-186">La ubicación predeterminada es \_ usuario actual y el *almacén de certificados* predeterminado es "My".</span><span class="sxs-lookup"><span data-stu-id="a6a98-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="a6a98-187">En el ejemplo de código siguiente se muestra cómo especificar que se debe elegir un certificado con el asunto "My Middle-Tier Certificate" en el [*almacén de certificados*](glossary.md) "personal" del registro en **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="a6a98-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="a6a98-188">En algunos idiomas, la barra diagonal inversa es un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="a6a98-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="a6a98-189">Recuerde modificar la cadena de selección de certificado para ello.</span><span class="sxs-lookup"><span data-stu-id="a6a98-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="a6a98-190">Por ejemplo, en Microsoft JScript, use dos barras diagonales inversas adyacentes en lugar de una.</span><span class="sxs-lookup"><span data-stu-id="a6a98-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="a6a98-191">Si no especifica un certificado y un servidor HTTPS requiere un certificado de cliente, WinHTTP selecciona el primer certificado del [*almacén de certificados*](glossary.md)predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6a98-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="a6a98-192">Si no existe ningún certificado, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a6a98-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="a6a98-193">Si no se acepta el certificado, el servidor devuelve un código de estado 403 para indicar que no se puede cumplir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6a98-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="a6a98-194">Después, puede elegir un certificado más adecuado con [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) y volver a enviar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6a98-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 

