---
title: Ejemplos de capas de canales de seguridad
description: En los siguientes ejemplos se muestra la seguridad en la capa del canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- ejemplos de seguridad
- ejemplos de seguridad, configuración
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704713"
---
# <a name="security-channel-layer-examples"></a>Ejemplos de capas de canales de seguridad

En los siguientes ejemplos se muestra la seguridad en el [nivel de canal](channel-layer-overview.md) .

Seguridad de transporte de Windows a través de TCP: cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Seguridad de transporte de Windows a través de canalizaciones con nombre: cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Seguridad de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nombre de usuario sobre SSL en modo mixto: cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nombre de usuario sobre SSL en modo mixto: cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nombre de usuario sobre la seguridad de modo mixto de SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido sobre seguridad de modo mixto de SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre seguridad de modo mixto de SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time el programa de instalación de ejemplos de seguridad

Para ejecutar ejemplos de seguridad de WWSAPI, debe configurar los certificados de cliente y de servidor para SSL, así como una cuenta de usuario local para la autenticación de encabezados HTTP. Antes de empezar, necesita las siguientes herramientas:

-   MakeCert.exe (disponible en el SDK de Windows 7).
-   CertUtil.exe o CertMgr.exe (CertUtil.exe está disponible en los SDK de Windows a partir de Windows Server 2003. CertMgr.exe está disponible en el SDK de Windows 7. Solo se necesita una de estas herramientas).
-   HttpCfg.exe: (solo es necesario si usa Windows 2003 o Windows XP. Esta herramienta está disponible en las herramientas de soporte de Windows XP SP2 y también se incluye en el CD de herramientas del kit de recursos de Windows Server 2003.

Si obtiene los ejemplos de WWSAPI instalando el SDK de Windows 7, puede encontrar los MakeCert.exe y CertMgr.exe en% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.

Realice la siguiente configuración en cinco pasos desde el símbolo del sistema (elevado si usa Windows Vista y versiones posteriores):

1.  Genere un certificado autofirmado para que sea la entidad de certificación (CA) o el emisor: **MakeCert.exe-SS root-Sr LocalMachine-n "CN = falsificate-test-CA"-CY Authority-r-SK "CAKeyContainer"**
2.  Genere un certificado de servidor con el certificado anterior como emisor: **MakeCert.exe-SS My-Sr LocalMachine-n "CN = localhost"-Sky Exchange-is root-ir LocalMachine-in falsificate-test-CA-SK "ServerKeyContainer"**
3.  Busque la huella digital (un hash SHA-1 de 40 caracteres) del certificado de servidor mediante la ejecución de cualquiera de los siguientes comandos y busque el certificado denominado localhost con el emisor falso-test-CA:
    -   **CertUtil.exe: almacenar mi localhost**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  Registre la huella digital del certificado de servidor sin espacios con HTTP.SYS:
    -   En Windows Vista y versiones posteriores (la opción "AppID" es un GUID arbitrario): **Netsh.exe http Add sslcert ipport = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint>
    -   En Windows XP o 2003: **HttpCfg.exe Set SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**
5.  Cree un usuario local: **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**

Para limpiar los certificados, el enlace de certificado SSL y la cuenta de usuario creada en los pasos anteriores, ejecute los siguientes comandos. Nota: si hay varios certificados con el mismo nombre, CertMgr.exe necesitará la entrada antes de eliminarlos.

-   **CertMgr.exe-del-c-n Falsificate-test-CA-s-r LocalMachine raíz**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe http Delete sslcert ipport = 0.0.0.0:8443 (o HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**
-   **Net user "TestUserForBasicAuth"/Delete**

Asegúrese de que solo hay un certificado raíz denominado falso-test-CA. Si no está seguro, es siempre seguro que intente limpiar estos certificados con los comandos de limpieza anteriores (y omitir los errores) antes de iniciar la configuración de cinco pasos.

 

 




