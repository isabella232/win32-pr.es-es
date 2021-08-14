---
title: Ejemplos de capa de canal de seguridad
description: En los ejemplos siguientes se muestra la seguridad en la capa de canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- ejemplos de seguridad
- ejemplos de seguridad, configuración
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d130bc7e0e4250107c6e331a43f7d5a13786929c37bd998177ee587c2f29049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192776"
---
# <a name="security-channel-layer-examples"></a>Ejemplos de capa de canal de seguridad

En los ejemplos siguientes se muestra la seguridad en la [capa de canal](channel-layer-overview.md)

Windows seguridad de transporte a través de TCP: Cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows seguridad de transporte a través de canalizaciones con nombre: Cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Seguridad de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nombre de usuario sobre seguridad en modo mixto SSL: Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nombre de usuario sobre seguridad en modo mixto SSL: Cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nombre de usuario sobre seguridad en modo mixto SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido sobre seguridad en modo mixto SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre seguridad en modo mixto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time configuración de ejemplos de seguridad

Para ejecutar ejemplos de seguridad de WWSAPI, debe configurar los certificados de cliente y servidor para SSL, así como una cuenta de usuario local para la autenticación de encabezado HTTP. Antes de empezar, necesita las siguientes herramientas:

-   MakeCert.exe (disponible en el SDK Windows 7).
-   CertUtil.exe o CertMgr.exe (CertUtil.exe está disponible en los SDK de Windows a partir de Windows Server 2003. CertMgr.exe está disponible en el SDK Windows 7. Solo necesita una de estas herramientas).
-   HttpCfg.exe: (Solo lo necesita si usa Windows 2003 o Windows XP. Esta herramienta está disponible en Windows herramientas de soporte técnico de XP SP2 y también se incluye con el CD de herramientas del Kit de recursos de Windows Server 2003).

Si obtiene los ejemplos de WWSAPI mediante la instalación del SDK de Windows 7, puede encontrar MakeCert.exe y CertMgr.exe en %Archivos de programa% SDK de \\ Microsoft \\ Windows bin \\ v7.0. \\

Realice la siguiente configuración de cinco pasos desde el símbolo del sistema (con privilegios elevados si usa Windows Vista y versiones posteriores):

1.  Generar un certificado autofirmado para que sea la entidad de certificación (CA) o el emisor: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**
2.  Genere un certificado de servidor con el certificado anterior como emisor: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**
3.  Busque la huella digital (un hash SHA-1 de 40 caracteres) del certificado de servidor mediante la ejecución de cualquiera de los siguientes comandos y busque el certificado denominado localhost con el emisor Fake-Test-CA:
    -   **CertUtil.exe -store My localhost**
    -   **CertMgr.exe -s -r LocalMachine My**
4.  Registre la huella digital del certificado de servidor sin espacios con HTTP.SYS:
    -   En Windows Vista y versiones posteriores (la opción "appid" es un GUID arbitrario): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint>
    -   En Windows XP o 2003: **HttpCfg.exe ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**
5.  Creación de un usuario local: **usuario neto "TestUserForBasicAuth" "TstPWD@ \* 4Bsic" /add**

Para limpiar los certificados, el enlace de certificados SSL y la cuenta de usuario creada en los pasos anteriores, ejecute los siguientes comandos. Tenga en cuenta que si hay varios certificados del mismo nombre, CertMgr.exe necesitará la entrada antes de eliminarlos.

-   **CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**
-   **CertMgr.exe -del -c -n localhost -s -r LocalMachine My**
-   **Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (o HttpCfg.exe eliminar ssl -i 0.0.0.0:8443)**
-   **Usuario neto "TestUserForBasicAuth" /delete**

Asegúrese de que solo hay un certificado raíz denominado Fake-Test-CA. Si no está seguro, siempre es seguro intentar limpiar estos certificados mediante los comandos de limpieza anteriores (y omitir los errores) antes de iniciar la configuración de cinco pasos.

 

 




