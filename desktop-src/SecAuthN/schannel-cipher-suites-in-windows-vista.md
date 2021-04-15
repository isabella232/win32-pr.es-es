---
description: Un conjunto de algoritmos criptográficos. Los protocolos de Schannel usan algoritmos de un conjunto de cifrado para crear claves y cifrar la información.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Conjuntos de cifrado TLS en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cf270f0608666b7d766e3f063f24ea39204fd1
ms.sourcegitcommit: b022a50bc0d11975dad6337b8f399c47234dffcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105649317"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Conjuntos de cifrado TLS en Windows Vista

Un conjunto de cifrado es un conjunto de algoritmos criptográficos. Los protocolos de Schannel usan algoritmos de un conjunto de cifrado para crear claves y cifrar la información. Un conjunto de cifrado especifica un algoritmo para cada una de las siguientes tareas:

-   Intercambio de claves
-   Cifrado masivo
-   Autenticación de mensajes

Los [*algoritmos de intercambio de claves*](../secgloss/k-gly.md) protegen la información necesaria para crear claves compartidas. Estos algoritmos son asimétricos ([*algoritmos de clave pública*](../secgloss/p-gly.md)) y funcionan bien para cantidades de datos relativamente pequeñas.

Los algoritmos de cifrado masivo cifran los mensajes intercambiados entre clientes y servidores. Estos algoritmos son [*simétricos*](../secgloss/s-gly.md) y funcionan bien para grandes cantidades de datos.

Los algoritmos de [autenticación de mensajes](message-authentication-codes-in-schannel.md) generan [*hashes*](../secgloss/h-gly.md) de mensajes y firmas que garantizan la [*integridad*](../secgloss/i-gly.md) de un mensaje.

Los desarrolladores especifican estos elementos mediante tipos de datos de [**\_ identificador de alg**](../seccrypto/alg-id.md) . Para obtener más información, consulte [especificar cifrados Schannel y intensidades de cifrado](specifying-schannel-ciphers-and-cipher-strengths.md).

Schannel admite los siguientes conjuntos de cifrado. Los conjuntos se enumeran en el orden predeterminado en el que los elige el proveedor de Microsoft Schannel.

> [!IMPORTANT]
> Los servicios Web HTTP/2 producen un error con conjuntos de cifrado no compatibles con HTTP/2. Para asegurarse de que los servicios web funcionan con clientes y exploradores HTTP/2, consulte [cómo implementar el orden personalizado de conjuntos de cifrado](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 



| Conjunto de cifrado                                                 | Modo FIPS habilitado | Exchange              | Cifrado      | Hash            | Protocolos                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| \_RSA TLS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                | Sí<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                | Sí<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ RC4 \_ 128 \_ Sha<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ 3DES \_ Ede \_ CBC \_ Sha<br/>               | Sí<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/> | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ clave p384<br/> | Sí<br/>    | ECDH \_ clave p384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/> | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/> | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ clave p384<br/> | Sí<br/>    | ECDH \_ clave p384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/> | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>   | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ clave p384<br/>   | Sí<br/>    | ECDH \_ clave p384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>   | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>   | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ clave p384<br/>   | Sí<br/>    | ECDH \_ clave p384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>   | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>           | Sí<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>           | Sí<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ 3DES \_ Ede \_ CBC \_ Sha<br/>          | Sí<br/>    | DH<br/>         | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ RC4 \_ 128 \_ MD5<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ con \_ MD5<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| \_RSA TLS \_ con \_ \_ MD5 nulo<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ \_ Sha nulo<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Los siguientes conjuntos de cifrado son compatibles con Schannel; sin embargo, no están presentes de forma predeterminada. Se deben agregar según sea necesario. Para obtener información sobre cómo agregar conjuntos de cifrado al proveedor de Schannel, consulte [priorización de conjuntos de cifrado de Schannel](prioritizing-schannel-cipher-suites.md).

-   \_Exportación RSA \_ TLS \_ con \_ RC4 \_ 40 \_ MD5
-   \_EXPORT1024 RSA \_ TLS \_ con \_ RC4 \_ 56 \_ Sha
-   \_ \_ EXPORT1024 de RSA TLS \_ con \_ des \_ CBC \_ Sha
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ des \_ 64 \_ CBC \_ con \_ MD5
-   \_RSA TLS \_ con \_ des \_ CBC \_ Sha
-   \_RSA TLS \_ con \_ \_ MD5 nulo
-   \_RSA TLS \_ con \_ \_ Sha nulo
-   TLS \_ DHE \_ DSS \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha
-   TLS \_ DHE \_ DSS \_ con \_ des \_ CBC \_ Sha

**Windows Server 2003 y Windows XP:** Para obtener información acerca de los conjuntos de cifrado compatibles, vea los temas siguientes.

| Tema                                                                         | Descripción                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjuntos de cifrado TLS](tls-cipher-suites.md)<br/>                         | Información sobre los conjuntos de cifrado disponibles con el protocolo TLS en Windows Server 2003 y Windows XP.<br/>              |
| [Protocolo Capa de sockets seguros](secure-sockets-layer-protocol.md)<br/> | Información general sobre SSL 2,0 y 3,0, incluidos los conjuntos de cifrado disponibles en Windows Server 2003 y Windows XP.<br/> |



 

 

 
