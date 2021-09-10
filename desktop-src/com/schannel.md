---
title: Schannel
description: El paquete de seguridad de Canal seguro (Schannel), cuyo identificador de servicio de autenticación es RPC C AUTHN GSS SCHANNEL, admite los siguientes protocolos basados en clave pública SSL (Capa de sockets seguros) versiones 2.0 y 3.0, Seguridad de la capa de transporte (TLS) 1.0 y Tecnología de comunicación privada \_ \_ \_ \_ (PCT) 1.0. TLS 1.0 es una versión estandarizada y ligeramente modificada de SSL 3.0 que emitió internet Engineering Task Force (IETF) en enero de 1999, en el documento RFC 2246. Dado que TLS se ha estandarizado, se recomienda a los desarrolladores que usen TLS en lugar de SSL. PCT solo se incluye por compatibilidad con versiones anteriores y no debe usarse para el nuevo desarrollo. Cuando se usa el paquete de seguridad de Schannel, DCOM negocia automáticamente el mejor protocolo, en función de las funcionalidades de cliente y servidor.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369736"
---
# <a name="schannel"></a>Schannel

El paquete de seguridad de Canal seguro (Schannel), cuyo identificador de servicio de autenticación es RPC C AUTHN GSS SCHANNEL, admite los siguientes protocolos basados en clave \_ \_ \_ pública: SSL (Capa de sockets seguros) versiones 2.0 y 3.0, Seguridad de la capa de transporte (TLS) 1.0 y Tecnología de comunicación privada \_ (PCT) 1.0. TLS 1.0 es una versión estandarizada y ligeramente modificada de SSL 3.0 que emitió internet Engineering Task Force (IETF) en enero de 1999, en el [documento RFC 2246](https://www.ietf.org/rfc/rfc2246.txt). Dado que TLS se ha estandarizado, se recomienda a los desarrolladores que usen TLS en lugar de SSL. PCT solo se incluye por compatibilidad con versiones anteriores y no debe usarse para el nuevo desarrollo. Cuando se usa el paquete de seguridad de Schannel, DCOM negocia automáticamente el mejor protocolo, en función de las funcionalidades de cliente y servidor.

En los temas siguientes se describe brevemente el protocolo TLS y cómo funciona con DCOM.

-   [Cuándo usar TLS](#when-to-use-tls)
-   [Breve información general sobre cómo funciona TLS](#brief-overview-of-how-tls-works)
-   [Certificados X.509](#x509-certificates)
    -   [Certificados de cliente](#client-certificates)
-   [Uso de TLS en COM](#using-tls-in-com)
    -   [Cómo un servidor establece el nivel de seguridad](#how-a-server-sets-the-security-blanket)
    -   [Cómo un cliente establece el problema de seguridad](#how-a-client-sets-the-security-blanket)
    -   [Cómo cambia un cliente el problema de seguridad](#how-a-client-changes-the-security-blanket)
    -   [Ejemplo: El cliente cambia el nivel de seguridad](#example-client-changes-the-security-blanket)
-   [Temas relacionados](#related-topics)

> [!Note]  
> Toda la información sobre el protocolo TLS de estas secciones también se aplica a los protocolos SSL y PCT.

 

## <a name="when-to-use-tls"></a>Cuándo usar TLS

TLS es la única opción de seguridad disponible cuando los servidores necesitan demostrar su identidad a clientes anónimos. Esto es especialmente importante para los sitios web que desean participar en el comercio electrónico porque ayuda a proteger la transmisión de información confidencial, como números de tarjeta de crédito. TLS garantiza que los clientes de comercio electrónico pueden estar seguros de con quién están haciendo negocios, ya que se les proporciona una prueba de la identidad del servidor. También proporciona al servidor de comercio electrónico la eficacia de no tener que preocuparse por autenticar la identidad de cada uno de sus clientes.

TLS requiere que todos los servidores demuestren su identidad a los clientes. Además, TLS ofrece la opción de que los clientes demuestren su identidad en los servidores. Esta autenticación mutua puede ser útil para restringir el acceso de determinadas páginas web en una intranet corporativa grande.

TLS admite los niveles de autenticación más sólidos y ofrece una arquitectura abierta que permite que la seguridad del cifrado aumente con el tiempo para mantenerse al día con la innovación tecnológica. TLS es la mejor opción para entornos en los que se desea el mayor nivel de seguridad para los datos en tránsito.

## <a name="brief-overview-of-how-tls-works"></a>Breve información general sobre cómo funciona TLS

TLS se basa en una infraestructura de clave pública (PKI), que usa pares de claves públicas y privadas para habilitar el cifrado de datos y establecer la integridad de los datos, y usa certificados X.509 para la autenticación.

Muchos protocolos de seguridad, como el protocolo Kerberos v5, dependen de una sola clave para cifrar y descifrar los datos. Por lo tanto, estos protocolos dependen del intercambio seguro de claves de cifrado. en el protocolo Kerberos, esto se realiza a través de vales obtenidos del Centro de distribución de claves (KDC). Esto requiere que todos los usuarios que usan el protocolo Kerberos se registren en el KDC, lo que sería una limitación poco práctica para un servidor web de comercio electrónico que está pensado para atraer a millones de clientes de todo el mundo. Por lo tanto, TLS se basa en una PKI, que usa dos claves para el cifrado de datos: "cuando una clave del par cifra los datos, solo la otra clave del par puede descifrarlo. La principal ventaja de este diseño es que el cifrado se puede realizar sin necesidad de un intercambio seguro de claves de cifrado.

Una PKI usa una técnica en la que una de las claves se mantiene privada y solo está disponible para la entidad de seguridad a la que está registrada, mientras que la otra clave se hace pública para que cualquier usuario pueda acceder a ella. Si alguien desea enviar un mensaje privado al propietario de un par de claves, el mensaje se puede cifrar con la clave pública y solo se puede usar la clave privada para descifrar el mensaje.

Los pares de claves también se usan para comprobar la integridad de los datos que se envían. Para ello, el propietario del par de claves puede adjuntar una firma digital a los datos antes de enviarlos. La creación de una firma digital implica calcular un hash de los datos y cifrar el hash con la clave privada. Cualquier persona que use la clave pública para descifrar la firma digital está seguro de que la firma digital solo debe haber procededo de la persona que posee la clave privada. Además, el destinatario puede calcular un hash de los datos con el mismo algoritmo que el remitente y, si el hash calculado coincide con el enviado en la firma digital, el destinatario puede estar seguro de que los datos no se modificaron después de que se firmaron digitalmente.

Una desventaja de usar una PKI para el cifrado de datos de gran volumen es su rendimiento relativamente lento. Debido a las matemáticas intensivas implicadas, el cifrado y descifrado de datos mediante un cifrado asimétrico que depende de un par de claves puede ser hasta 1000 veces más lento que el cifrado y descifrado mediante un cifrado simétrico que depende solo de una sola clave. Por lo tanto, TLS usa una PKI solo para generar firmas digitales y para negociar la clave única específica de la sesión que usarán el cliente y el servidor para el cifrado y descifrado masivos de datos. TLS admite una amplia variedad de cifrados simétricos de clave única y se pueden agregar cifrados adicionales en el futuro.

Para obtener más información sobre el protocolo de protocolo de enlace TLS, vea [Protocolo de protocolo de enlace TLS](/windows/desktop/SecAuthN/tls-handshake-protocol).

Para obtener más detalles sobre la criptografía detrás del protocolo TLS, vea [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>Certificados X.509

Un problema crítico que debe controlar una PKI es la capacidad de confiar en la autenticidad de la clave pública que se está utilizando. Cuando se usa una clave pública emitida para una empresa con la que quiere hacer negocios, quiere estar seguro de que la clave pertenece realmente a la empresa en lugar de a un delincuente que quiere detectar el número de tarjeta de crédito.

Para garantizar la identidad de una entidad de seguridad que tiene un par de claves, una entidad de certificación (CA) emite un certificado X.509. Este certificado contiene información que identifica la entidad de seguridad, contiene la clave pública de la entidad de seguridad y está firmado digitalmente por la entidad de certificación. Esta firma digital indica que la CA cree que la clave pública contenida en el certificado pertenece realmente a la entidad de seguridad identificada por el certificado.

¿Y cómo confía en la CA? Dado que la propia CA contiene un certificado X.509 firmado por una entidad de certificación de nivel superior. Esta cadena de firmas de certificado continúa hasta que llega a una CA raíz, que es una CA que firma sus propios certificados. Si confía en la integridad de la CA raíz de un certificado, debería poder confiar en la autenticidad del propio certificado. Por lo tanto, la selección de CA raíz en las que esté dispuesto a confiar es una tarea importante para un administrador del sistema.

### <a name="client-certificates"></a>Certificados de cliente

Cuando surgieron por primera vez los protocolos de capa de transporte de seguridad, su propósito principal era garantizar que un cliente se conectaba a un servidor auténtico y ayudar a proteger la privacidad de los datos en tránsito. Sin embargo, SSL 3.0 y TLS 1.0 también incluyen compatibilidad para la transmisión del certificado de un cliente durante el protocolo de enlace del protocolo. Esta característica opcional permite la autenticación mutua del cliente y el servidor.

La decisión de si se debe usar un certificado de cliente se debe tomar en el contexto de la aplicación. Los certificados de cliente no son necesarios si el requisito principal es autenticar el servidor. Sin embargo, si la autenticación de cliente es esencial, se puede usar el certificado de un cliente en lugar de confiar en la autenticación personalizada dentro de la aplicación. El uso de certificados de cliente es preferible a la autenticación personalizada porque proporciona a los usuarios un escenario de inicio de sesión único.

## <a name="using-tls-in-com"></a>Uso de TLS en COM

TLS solo admite el nivel de suplantación (RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE) de suplantación. Si COM negocia TLS como servicio de autenticación en un proxy, COM establecerá el nivel de suplantación para suplantar independientemente del proceso predeterminado. Para que la suplantación funcione correctamente en TLS, el cliente debe proporcionar un certificado X.509 al servidor y el servidor debe tener ese certificado asignado a una cuenta de usuario determinada en el servidor. Para obtener más información, vea la Guía paso a paso para asignar certificados a [cuentas de usuario.](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates)

TLS no admite la [ocultación de](cloaking.md). Si se especifica una marca de ocultación y TLS en una llamada [**a CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**IClientSecurity::SetBlanket,**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) se devolverá E \_ INVALIDARG.

TLS no funciona con el nivel de autenticación establecido en Ninguno. El protocolo de enlace entre el cliente y el servidor examina el nivel de autenticación establecido por cada uno de ellos y elige la configuración de seguridad más alta para la conexión.

Los parámetros de seguridad de TLS se pueden establecer llamando a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y [**CoSetProxyBlanket.**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) En las secciones siguientes se describen los matices implicados en la realización de esas llamadas.

### <a name="how-a-server-sets-the-security-blanket"></a>Cómo un servidor establece el nivel de seguridad

Si un servidor quiere usar TLS, debe especificar Schannel (RPC C AUTHN GSS SCHANNEL) como servicio de autenticación en el parámetro \_ \_ \_ \_ *asAuthSvc* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Para evitar que los clientes se conecten al servidor mediante un servicio de autenticación menos seguro, el servidor debe especificar solo Schannel como servicio de autenticación cuando llama a **CoInitializeSecurity**. El servidor no puede cambiar la seguridad después de llamar a **CoInitializeSecurity**.

Para usar TLS, se deben especificar los parámetros siguientes cuando un servidor llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *pVoid* debe ser un puntero a un [**objeto IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntero a un [**DESCRIPTOR DE \_ SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor). No debe ser **NULL ni** un puntero a un AppID.
-   *cAuthSvc* no puede ser 0 o -1. Los servidores COM nunca eligen Schannel cuando *cAuthSvc* es -1.
-   *asAuthSvc debe* especificar Schannel como un posible servicio de autenticación. Para ello, se estableciendo los siguientes parámetros [**de SERVICIO \_ DE AUTENTICACIÓN \_ DE SOLE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) para el miembro Schannel de LA LISTA DE [**\_ AUTENTICACIÓN \_ DE SOLE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwAuthnSvc* debe ser RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL.
    -   *dwAuthzSvc* debe ser RPC \_ C \_ AUTHZ \_ NONE. Actualmente, se omite.
    -   *pPrincipalName debe* ser un puntero a [**CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), que se convierte como un puntero a OLECHAR, que representa el certificado X.509 del servidor.
-   *dwAuthnLevel* indica el nivel mínimo de autenticación que se aceptará de los clientes para una conexión correcta. No puede ser RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.
-   *dwCapabilities no* debe tener establecida la marca \_ APPID de EOAC. La marca EOAC ACCESS CONTROL debe establecerse si pVoid apunta a un objeto \_ \_ [**IAccessControl;**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)  no debe establecerse si *pVoid* apunta a un DESCRIPTOR DE \_ SEGURIDAD. Para ver otras marcas que se pueden establecer, [**vea CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Para obtener más información sobre el [**uso de CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)vea Establecer la seguridad [de todo el proceso con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Cómo un cliente establece el problema de seguridad

Si un cliente quiere usar TLS, debe especificar Schannel (RPC \_ C AUTHN GSS SCHANNEL) en su lista de servicios de autenticación en el \_ \_ parámetro \_ *pAuthList* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si Schannel no se especifica como un posible servicio de autenticación cuando se llama a **CoInitializeSecurity,** se producirá un error en una llamada posterior a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (o [**IClientSecurity::SetBlanket)**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)si intenta especificar Schannel como servicio de autenticación.

Se deben especificar los parámetros siguientes cuando un cliente llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *dwAuthnLevel* especifica el nivel de autenticación predeterminado que el cliente quiere usar. No puede ser RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.
-   *dwImpLevel debe* ser RPC \_ C IMP LEVEL \_ \_ \_ IMPERSONATE.
-   *pAuthList* debe tener los siguientes parámetros [**SOLE \_ AUTHENTICATION \_ INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) como miembro de la lista:
    -   *dwAuthnSvc* debe ser RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL.
    -   *dwAuthzSvc* debe ser RPC \_ C \_ AUTHZ \_ NONE.
    -   *pAuthInfo* es un puntero a [**UN CONTEXTO \_ DE CERT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)que se convierte como puntero a void, que representa el certificado X.509 del cliente. Si el cliente no tiene un certificado o no quiere presentar su certificado al servidor, *pAuthInfo* debe ser **NULL** y se intenta una conexión anónima con el servidor.
-   *dwCapabilities es* un conjunto de marcas que indican funcionalidades de cliente adicionales. Consulte [**CoInitializeSecurity para**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) obtener información sobre qué marcas se deben establecer.

Para obtener más información sobre el [**uso de CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)vea Establecer la seguridad [de todo el proceso con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Cómo cambia un cliente el problema de seguridad

Si un cliente quiere usar TLS pero cambiar la seguridad después de llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), debe llamar a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) o [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) con parámetros similares a los usados en la llamada a **CoInitializeSecurity**, con las siguientes diferencias:

-   *pServerPrincName* indica el nombre principal del servidor, en formato msstd o fullsic. Para obtener información sobre estos formatos, vea [Nombres principales](/windows/desktop/Rpc/principal-names). Si el cliente tiene el certificado X.509 del servidor, puede encontrar el nombre principal llamando a [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).
-   *pAuthInfo* es un puntero a [**UN CONTEXTO \_ DE CERT,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)que se convierte como puntero a RPC AUTH IDENTITY HANDLE, que representa el certificado \_ \_ \_ X.509 del cliente. Si el cliente no tiene un certificado o no quiere presentar su certificado al servidor, *pAuthInfo* debe ser **NULL** y se intenta una conexión anónima con el servidor.
-   *dwCapabilities consta* de marcas que indican funcionalidades de cliente adicionales. Solo se pueden usar cuatro marcas para cambiar la configuración de la omisión de seguridad: EOAC \_ DEFAULT, EOAC MUTUAL AUTH, EOAC ANY AUTHORITY (esta marca está en desuso) y \_ \_ \_ \_ EOAC \_ MAKE \_ FULLSIC. Para obtener más información, [**vea CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Para obtener más información sobre el [**uso de CoSetProxyBlanket, vea**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)Establecer la seguridad en el nivel de proxy de [interfaz.](setting-security-at-the-interface-proxy-level.md)

### <a name="example-client-changes-the-security-blanket"></a>Ejemplo: El cliente cambia el nivel de seguridad

En el ejemplo siguiente se muestra cómo un cliente puede cambiar el nivel de seguridad para dar cabida a una solicitud del servidor para que el cliente proporcione su certificado X.509. El código de control de errores se omite por brevedad.


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

[Com y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 