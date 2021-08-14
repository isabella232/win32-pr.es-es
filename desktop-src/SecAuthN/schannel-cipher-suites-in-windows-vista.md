---
description: Conjunto de algoritmos criptográficos. Los protocolos de Schannel usan algoritmos de un conjunto de cifrado para crear claves y cifrar la información.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Conjuntos de cifrado TLS en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf77d821612093e3015a0f8dee4cf51ae5bd9b95c653b61fe7a36271ba81ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918658"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Conjuntos de cifrado TLS en Windows Vista

Un conjunto de cifrado es un conjunto de algoritmos criptográficos. Los protocolos de Schannel usan algoritmos de un conjunto de cifrado para crear claves y cifrar la información. Un conjunto de cifrado especifica un algoritmo para cada una de las siguientes tareas:

-   Intercambio de claves
-   Cifrado masivo
-   Autenticación de mensajes

[*Los algoritmos de intercambio*](../secgloss/k-gly.md) de claves protegen la información necesaria para crear claves compartidas. Estos algoritmos son [*asimétricos (algoritmos de clave*](../secgloss/p-gly.md)pública) y tienen un buen rendimiento para cantidades relativamente pequeñas de datos.

Los algoritmos de cifrado masivo cifran los mensajes intercambiados entre clientes y servidores. Estos algoritmos son [*simétricos*](../secgloss/s-gly.md) y tienen un buen rendimiento para grandes cantidades de datos.

[Los algoritmos de](message-authentication-codes-in-schannel.md) autenticación de mensajes [*generan hashes*](../secgloss/h-gly.md) de mensajes y firmas que garantizan la [*integridad*](../secgloss/i-gly.md) de un mensaje.

Los desarrolladores especifican estos elementos mediante tipos de datos de ID de [**ALG. \_**](../seccrypto/alg-id.md) Para obtener más información, vea [Especificar cifrados de Schannel y intensidades de cifrado.](specifying-schannel-ciphers-and-cipher-strengths.md)

Schannel admite los siguientes conjuntos de cifrado. Los conjuntos se muestran en el orden predeterminado en el que los elige el proveedor de Microsoft Schannel.

> [!IMPORTANT]
> Se producirá un error en los servicios web HTTP/2 con conjuntos de cifrado no compatibles con HTTP/2. Para asegurarse de que los servicios web funcionan con clientes y exploradores HTTP/2, consulte Implementación de la ordenación de conjuntos de [cifrado personalizados.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 



| Conjunto de cifrado                                                 | Modo FIPS habilitado | Exchange              | Cifrado      | Hash            | Protocolos                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Sí<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Sí<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>               | Sí<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/> | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/> | Sí<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/> | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/> | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/> | Sí<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/> | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>   | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>   | Sí<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>   | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>   | Sí<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>   | Sí<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>   | Sí<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Sí<br/>    | Dh<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Sí<br/>    | Dh<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>          | Sí<br/>    | Dh<br/>         | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ CON \_ MD5<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA \_ CON \_ \_ MD5 NULL<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA CON SHA \_ \_ \_ NULL<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Schannel admite los siguientes conjuntos de cifrado; sin embargo, no están presentes de forma predeterminada. Se deben agregar según sea necesario. Para obtener información sobre cómo agregar conjuntos de cifrado al proveedor de Schannel, consulte [Priorización de conjuntos de cifrado de Schannel.](prioritizing-schannel-cipher-suites.md)

-   TLS \_ RSA \_ EXPORT \_ WITH \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA
-   TLS \_ RSA \_ EXPORT1024 \_ CON \_ DES \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ DES \_ 64 \_ CBC \_ WITH \_ MD5
-   TLS \_ RSA \_ CON \_ DES \_ CBC \_ SHA
-   TLS \_ RSA \_ CON \_ \_ MD5 NULL
-   TLS \_ RSA CON SHA \_ \_ \_ NULL
-   TLS \_ DHE \_ DSS \_ EXPORT1024 \_ CON \_ DES \_ CBC \_ SHA
-   TLS \_ DHE \_ DSS \_ CON \_ DES \_ CBC \_ SHA

**Windows Server 2003 y Windows XP:** Para obtener información sobre los conjuntos de cifrado admitidos, consulte los temas siguientes.

| Tema                                                                         | Descripción                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjuntos de cifrado TLS](tls-cipher-suites.md)<br/>                         | Información sobre los conjuntos de cifrado disponibles con el protocolo TLS en Windows Server 2003 y Windows XP.<br/>              |
| [Capa de sockets seguros protocolo](secure-sockets-layer-protocol.md)<br/> | Información general sobre SSL 2.0 y 3.0, incluidos los conjuntos de cifrado disponibles en Windows Server 2003 y Windows XP.<br/> |



 

 

 
