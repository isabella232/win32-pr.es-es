---
title: Schannel
description: El paquete de seguridad de canal seguro (Schannel), cuyo identificador de servicio de autenticación es RPC \_ C \_ authn \_ GSS \_ Schannel, admite los siguientes protocolos basados en clave pública SSL (capa de sockets seguros) versiones 2,0 y 3,0, seguridad de la capa de transporte (TLS) 1,0 y tecnología de comunicaciones privadas (PCT) 1,0. TLS 1,0 es una versión estándar, ligeramente modificada, de SSL 3,0 emitida por Internet Engineering Task Force (IETF) en enero de 1999, en el documento RFC 2246. Dado que TLS está normalizado, se recomienda a los desarrolladores que utilicen TLS en lugar de SSL. PCT se incluye solo por motivos de compatibilidad con versiones anteriores y no debe usarse para el desarrollo nuevo. Cuando se utiliza el paquete de seguridad Schannel, DCOM negocia automáticamente el mejor protocolo, en función de las capacidades del cliente y del servidor.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359452"
---
# <a name="schannel"></a>Schannel

El paquete de seguridad de canal seguro (Schannel), cuyo identificador de servicio de autenticación es RPC \_ C \_ authn \_ GSS \_ Schannel, admite los siguientes protocolos basados en claves públicas: SSL (capa de sockets seguros) versiones 2,0 y 3,0, seguridad de la capa de transporte (TLS) 1,0 y tecnología de comunicaciones privadas (PCT) 1,0. TLS 1,0 es una versión estándar, ligeramente modificada, de SSL 3,0 emitida por Internet Engineering Task Force (IETF) en enero de 1999, en el documento [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt). Dado que TLS está normalizado, se recomienda a los desarrolladores que utilicen TLS en lugar de SSL. PCT se incluye solo por motivos de compatibilidad con versiones anteriores y no debe usarse para el desarrollo nuevo. Cuando se utiliza el paquete de seguridad Schannel, DCOM negocia automáticamente el mejor protocolo, en función de las capacidades del cliente y del servidor.

En los siguientes temas se describe brevemente el protocolo TLS y cómo funciona con DCOM.

-   [Cuándo usar TLS](#when-to-use-tls)
-   [Breve descripción de cómo funciona TLS](#brief-overview-of-how-tls-works)
-   [Certificados X. 509](#x509-certificates)
    -   [Certificados de cliente](#client-certificates)
-   [Usar TLS en COM](#using-tls-in-com)
    -   [Cómo establece un servidor el marco de seguridad](#how-a-server-sets-the-security-blanket)
    -   [Cómo establece un cliente el marco de seguridad](#how-a-client-sets-the-security-blanket)
    -   [Cómo cambia un cliente el marco de seguridad](#how-a-client-changes-the-security-blanket)
    -   [Ejemplo: el cliente cambia el marco de seguridad](#example-client-changes-the-security-blanket)
-   [Temas relacionados](#related-topics)

> [!Note]  
> Toda la información sobre el protocolo TLS en estas secciones también se aplica a los protocolos SSL y PCT.

 

## <a name="when-to-use-tls"></a>Cuándo usar TLS

TLS es la única opción de seguridad disponible cuando los servidores necesitan demostrar su identidad a los clientes anónimos. Esto es especialmente importante para los sitios web que desean participar en el comercio electrónico porque ayuda a proteger la transmisión de información confidencial, como números de tarjeta de crédito. TLS garantiza que los clientes de comercio electrónico pueden estar seguros de quiénes están haciendo negocios, ya que se les proporciona una prueba de la identidad del servidor. También proporciona al servidor de comercio electrónico la eficiencia de no tener que preocuparse por la autenticación de la identidad de cada uno de sus clientes.

TLS requiere que todos los servidores demuestren su identidad a los clientes. Además, TLS ofrece la opción de hacer que los clientes demuestren su identidad a los servidores. Esta autenticación mutua puede ser útil a la vez que se restringe el acceso de ciertas páginas web en una intranet corporativa de gran tamaño.

TLS es compatible con los niveles de autenticación más seguros y ofrece una arquitectura abierta que permite que el nivel de cifrado aumente con el tiempo para mantenerse al día con la innovación tecnológica. TLS es la mejor opción para entornos en los que se desea el nivel más alto de seguridad para los datos en tránsito.

## <a name="brief-overview-of-how-tls-works"></a>Breve descripción de cómo funciona TLS

TLS se basa en una infraestructura de clave pública (PKI), que usa pares de claves pública y privada para habilitar el cifrado de datos y para establecer la integridad de los datos, y usa certificados X. 509 para la autenticación.

Muchos protocolos de seguridad, como el protocolo Kerberos V5, dependen de una única clave para cifrar y descifrar los datos. Por tanto, estos protocolos dependen del intercambio seguro de claves de cifrado. en el protocolo Kerberos, esto se hace a través de los vales obtenidos del Centro de distribución de claves (KDC). Esto requiere que todos los usuarios que usen el protocolo Kerberos se registren con el KDC, lo que sería una limitación inviable para un servidor Web de comercio electrónico destinado a atraer a millones de clientes de todo el mundo. Por consiguiente, TLS se basa en una PKI, que usa dos claves para Data encryptionâ € "cuando una clave del par cifra los datos, solo la otra clave del par puede descifrarlos. La ventaja principal de este diseño es que el cifrado se puede realizar sin necesidad de un intercambio seguro de claves de cifrado.

Una PKI usa una técnica en la que una de las claves se mantiene privada y solo está disponible para la entidad de seguridad en la que se registra, mientras que la otra clave se hace pública para que cualquiera tenga acceso. Si alguien desea enviar un mensaje privado al propietario de un par de claves, el mensaje se puede cifrar con la clave pública y solo se puede usar la clave privada para descifrar el mensaje.

Los pares de claves también se usan para comprobar la integridad de los datos que se envían. Para ello, el propietario del par de claves puede adjuntar una firma digital a los datos antes de enviarla. La creación de una firma digital implica el cálculo de un hash de los datos y el cifrado del hash con la clave privada. Cualquier persona que use la clave pública para descifrar la firma digital está seguro de que la firma digital debe haber sido procedente únicamente de la persona que posee la clave privada. Además, el destinatario puede calcular un hash de los datos utilizando el mismo algoritmo que el remitente y, si el hash calculado coincide con el que se envió en la firma digital, el destinatario puede estar seguro de que los datos no se modificaron una vez firmados digitalmente.

Una desventaja del uso de una PKI para el cifrado de datos de gran volumen es su rendimiento relativamente lento. Debido a las matemáticas intensivas implicadas, el cifrado y descifrado de los datos mediante un cifrado asimétrico que depende de un par de claves puede ser hasta 1.000 veces más lento que el cifrado y el descifrado mediante un cifrado simétrico que solo depende de una clave única. Por lo tanto, TLS utiliza una PKI solo para generar firmas digitales y para negociar la clave única específica de la sesión que el cliente y el servidor usarán para el cifrado y descifrado de datos de forma masiva. TLS admite una amplia variedad de cifrados simétricos de una sola clave y se pueden agregar cifrados adicionales en el futuro.

Para obtener más información acerca del Protocolo de enlace TLS, consulte [Protocolo de enlace TLS](/windows/desktop/SecAuthN/tls-handshake-protocol).

Para obtener más información sobre la criptografía detrás del protocolo TLS, consulte [Criptografía Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>Certificados X.509

Un problema crítico que debe administrar una PKI es la capacidad de confiar en la autenticidad de la clave pública que se está usando. Si usa una clave pública emitida para una empresa con la que desea hacer negocios, querrá asegurarse de que la clave pertenece realmente a la empresa en lugar de a un ladrón que desee detectar el número de su tarjeta de crédito.

Para garantizar la identidad de una entidad de seguridad que contiene un par de claves, una entidad de certificación (CA) emite un certificado X. 509 a la entidad de seguridad. Este certificado contiene información que identifica la entidad de seguridad, contiene la clave pública de la entidad de seguridad y está firmada digitalmente por la CA. Esta firma digital indica que la entidad de certificación considera que la clave pública incluida en el certificado realmente pertenece a la entidad de seguridad identificada por el certificado.

¿Y cómo confía en la entidad de certificación? Dado que la propia CA contiene un certificado X. 509 firmado por una CA de nivel superior. Esta cadena de firmas de certificado continúa hasta que llega a una CA raíz, que es una CA que firma sus propios certificados. Si confía en la integridad de la CA raíz de un certificado, debería poder confiar en la autenticidad del propio certificado. Por lo tanto, la selección de las CA raíz en las que está dispuesto a confiar es un derecho importante para un administrador del sistema.

### <a name="client-certificates"></a>Certificados de cliente

Cuando surgieron los protocolos de nivel de transporte de seguridad por primera vez, su objetivo principal era garantizar que un cliente se conectaba a un servidor auténtico y ayuda a proteger la privacidad de los datos durante el tránsito. Sin embargo, SSL 3,0 y TLS 1,0 también incluyen compatibilidad con la transmisión de un certificado de cliente durante el protocolo de enlace del protocolo. Esta característica opcional habilita la autenticación mutua del cliente y el servidor.

La decisión de si usar un certificado de cliente debe realizarse en el contexto de la aplicación. Los certificados de cliente no son necesarios si el requisito principal es la autenticación del servidor. Sin embargo, si la autenticación de cliente es esencial, se puede usar un certificado de cliente en lugar de confiar en la autenticación personalizada dentro de la aplicación. El uso de certificados de cliente es preferible a través de la autenticación personalizada, ya que proporciona a los usuarios un escenario de inicio de sesión único.

## <a name="using-tls-in-com"></a>Usar TLS en COM

TLS solo es compatible con el nivel de suplantación ( \_ \_ \_ \_ suplantación de nivel Imp de RPC C) de suplantación. Si COM negocia TLS como servicio de autenticación en un proxy, COM establecerá el nivel de suplantación en Impersonate independientemente del valor predeterminado del proceso. Para que la suplantación funcione correctamente en TLS, el cliente debe proporcionar un certificado X. 509 al servidor y el servidor debe tener ese certificado asignado a una cuenta de usuario determinada en el servidor. Para obtener más información, consulte la [Guía paso a paso para asignar certificados a cuentas de usuario](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates).

TLS no admite la [ocultación](cloaking.md). Si se especifica una marca de ocultación y TLS en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) , se \_ devolverá E INVALIDARG.

TLS no funciona con el nivel de autenticación establecido en ninguno. El protocolo de enlace entre el cliente y el servidor examina el nivel de autenticación establecido por cada y elige la configuración de seguridad más alta para la conexión.

Los parámetros de seguridad de TLS se pueden establecer llamando a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket). En las secciones siguientes se describen los matices implicados en la realización de esas llamadas.

### <a name="how-a-server-sets-the-security-blanket"></a>Cómo establece un servidor el marco de seguridad

Si un servidor desea utilizar TLS, debe especificar Schannel (RPC \_ C \_ authn \_ GSS \_ Schannel) como servicio de autenticación en el parámetro *asAuthSvc* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Para evitar que los clientes se conecten al servidor mediante un servicio de autenticación menos seguro, el servidor solo debe especificar Schannel como servicio de autenticación cuando llama a **CoInitializeSecurity**. El servidor no puede cambiar el marco de seguridad después de que se haya llamado **CoInitializeSecurity**.

Para usar TLS, deben especificarse los siguientes parámetros cuando un servidor llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *pVoid* debe ser un puntero a un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntero a un [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor). No debe ser **null** ni un puntero a un AppID.
-   *cAuthSvc* no puede ser 0 o-1. Los servidores COM nunca eligen Schannel cuando *cAuthSvc* es-1.
-   *asAuthSvc* debe especificar Schannel como posible servicio de autenticación. Esto se hace estableciendo los siguientes parámetros [**del \_ \_ servicio de autenticación único**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) para el miembro Schannel de la [**\_ \_ lista de autenticación única**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwAuthnSvc* debe ser RPC \_ C \_ authn \_ GSS \_ Schannel.
    -   *dwAuthzSvc* debe ser RPC \_ C \_ AUTHZ \_ ninguno. Actualmente, se omite.
    -   *pPrincipalName* debe ser un puntero a un [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), convertido en un puntero a OLECHAR, que representa el certificado X. 509 del servidor.
-   *dwAuthnLevel* indica el nivel de autenticación mínimo que se aceptará de los clientes para una conexión correcta. No puede ser el \_ \_ nivel ninguno de autenticación RPC C \_ \_ .
-   *dwCapabilities* no debe tener establecida la \_ marca EOAC AppID. La \_ marca de control de acceso EOAC \_ debe establecerse si *pVoid* apunta a un objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ; no debe establecerse si *pVoid* apunta a un \_ descriptor de seguridad. Para ver otras marcas que se pueden establecer, vea [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Para obtener más información sobre el uso de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), consulte [configuración de la seguridad de Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Cómo establece un cliente el marco de seguridad

Si un cliente desea usar TLS, debe especificar Schannel (RPC \_ C \_ authn \_ GSS \_ Schannel) en su lista de servicios de autenticación en el parámetro *pAuthList* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si Schannel no se especifica como un posible servicio de autenticación cuando se llama a **CoInitializeSecurity** , se producirá un error en una llamada posterior a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (o [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) si intenta especificar Schannel como el servicio de autenticación.

Se deben especificar los siguientes parámetros cuando un cliente llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *dwAuthnLevel* especifica el nivel de autenticación predeterminado que el cliente desea usar. No puede ser el \_ \_ nivel ninguno de autenticación RPC C \_ \_ .
-   *dwImpLevel* debe ser la \_ \_ \_ suplantación de nivel de Imp de RPC C \_ .
-   *pAuthList* debe tener los siguientes parámetros de [**\_ \_ información de autenticación únicos**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) como miembro de la lista:
    -   *dwAuthnSvc* debe ser RPC \_ C \_ authn \_ GSS \_ Schannel.
    -   *dwAuthzSvc* debe ser RPC \_ C \_ AUTHZ \_ None.
    -   *pAuthInfo* es un puntero a un [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), convertido en un puntero a void, que representa el certificado X. 509 del cliente. Si el cliente no tiene un certificado o no desea presentar su certificado en el servidor, *pAuthInfo* debe ser **null** y se intentará establecer una conexión anónima con el servidor.
-   *dwCapabilities* es un conjunto de marcas que indican funcionalidades de cliente adicionales. Consulte [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para obtener información sobre qué marcas se deben establecer.

Para obtener más información sobre el uso de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), consulte [configuración de la seguridad de Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Cómo cambia un cliente el marco de seguridad

Si un cliente desea utilizar TLS pero cambia la capa de seguridad después de llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), debe llamar a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) o [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) con parámetros similares a los que se usan en la llamada a **CoInitializeSecurity**, con las siguientes diferencias:

-   *pServerPrincName* indica el nombre principal del servidor, en formato msstd o fullsic. Para obtener información sobre estos formatos, consulte [nombres principales](/windows/desktop/Rpc/principal-names). Si el cliente tiene el certificado X. 509 del servidor, puede encontrar el nombre principal llamando a [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).
-   *pAuthInfo* es un puntero a un [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), convertido en un puntero al \_ identificador de identidad de autenticación de RPC \_ \_ , que representa el certificado X. 509 del cliente. Si el cliente no tiene un certificado o no desea presentar su certificado en el servidor, *pAuthInfo* debe ser **null** y se intentará establecer una conexión anónima con el servidor.
-   *dwCapabilities* consta de marcas que indican funcionalidades de cliente adicionales. Solo se pueden usar cuatro marcas para cambiar la configuración de la capa de seguridad: EOAC \_ default, EOAC \_ Mutual \_ auth, EOAC \_ cualquier \_ entidad (esta marca está en desuso) y EOAC \_ Make \_ FULLSIC. Para obtener más información, vea [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Para obtener más información sobre el uso de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), consulte [configuración de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).

### <a name="example-client-changes-the-security-blanket"></a>Ejemplo: el cliente cambia el marco de seguridad

En el ejemplo siguiente se muestra cómo un cliente puede cambiar la capa de seguridad para dar cabida a una solicitud del servidor para que el cliente proporcione su certificado X. 509. El código de control de errores se omite por motivos de brevedad.


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 