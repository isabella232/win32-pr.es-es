---
description: Los conjuntos de cifrado solo se pueden negociar para las versiones de TLS que los admiten.
ms.assetid: 283CB634-25EA-47F5-A2E3-0913F7D3D9DC
title: Conjuntos de cifrado TLS en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dadd86877f6e2c09ba46d34ec3a3abf5ff04d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000912"
---
# <a name="tls-cipher-suites-in-windows-7"></a>Conjuntos de cifrado TLS en Windows 7

Los conjuntos de cifrado solo se pueden negociar para las versiones de TLS que los admiten. Siempre se prefiere la versión de TLS más alta admitida en el protocolo de enlace de TLS. Por ejemplo, SSL \_ CK \_ RC4 \_ 128 \_ con \_ MD5 solo se puede usar cuando el cliente y el servidor no admiten TLS 1,2, 1,1 & 1,0 o SSL 3,0, ya que solo se admite con SSL 2,0.

La disponibilidad de los conjuntos de cifrado debe controlarse de una de estas dos maneras:

-   El orden de prioridad predeterminado se invalida cuando se configura una lista de prioridades. No se usarán los conjuntos de cifrado que no estén en la lista de prioridades.
-   Se permite cuando la aplicación pasa SCH \_ usar \_ \_ Criptografía segura: el proveedor de Microsoft Schannel filtrará los conjuntos de cifrado débil conocidos cuando la aplicación use la \_ marca de \_ \_ cifrado Strong usar. En Windows 7, se filtran los conjuntos de cifrado RC4.

> [!IMPORTANT]
> Los servicios Web HTTP/2 producen un error con conjuntos de cifrado no compatibles con HTTP/2. Para asegurarse de que los servicios web funcionan con clientes y exploradores HTTP/2, consulte [cómo implementar el orden personalizado de conjuntos de cifrado](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

El cumplimiento de FIPS se ha vuelto más complejo con la adición de curvas elípticas que hacen que la columna del modo FIPS habilitado en las versiones anteriores de esta tabla sea engañosa. Por ejemplo, un conjunto de cifrado como TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 solo es compatible con FIPS cuando se usan curvas elípticas de NIST. Para averiguar qué combinaciones de las curvas elípticas y los conjuntos de cifrado se habilitarán en modo FIPS, consulte la sección 3.3.1 de [directrices para la selección, la configuración y el uso de implementaciones de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Los Windows Update actualizan Windows 7, Windows 8 y Windows Server 2012 mediante la actualización 3042058, que cambia el orden de prioridad. Consulte el [aviso de seguridad de Microsoft 3042058](/security-updates/SecurityAdvisories/2015/3042058) para obtener más información. Los siguientes conjuntos de cifrado están habilitados y en este orden de prioridad de forma predeterminada por el proveedor de Microsoft Schannel:



| Cadena de conjunto de cifrado                                                                                            | Permitido por SCH \_ usar \_ \_ Criptografía segura | Versiones del protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ clave p384<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ clave p384<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                     | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ clave p384<br/>                                                     | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                     | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ clave p384<br/>                                                     | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                                  | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                                  | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384 \_ clave p384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256 \_ clave p384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ clave p384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ clave p384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                   | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ clave p384<br/>                                                   | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                   | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ clave p384<br/>                                                   | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ 3DES \_ Ede \_ CBC \_ Sha<br/>                                                                 | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ 3DES \_ Ede \_ CBC \_ Sha<br/>                                                            | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ RC4 \_ 128 \_ Sha<br/>                                                                       | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ null \_ SHA256 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>            | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ \_ Sha nulo <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>               | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ con \_ MD5 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/> | Sí<br/>                      | SSL 2.0<br/>                            |



 

Los siguientes conjuntos de cifrado son compatibles con el proveedor de Microsoft Schannel, pero no están habilitados de forma predeterminada:



| Cadena de conjunto de cifrado                                             | Permitido por SCH \_ usar \_ \_ Criptografía segura | Versiones del protocolo TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>      | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>      | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>    | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>    | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ des \_ CBC \_ Sha<br/>                        | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_EXPORT1024 RSA \_ TLS \_ con \_ RC4 \_ 56 \_ Sha<br/>             | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_ \_ EXPORT1024 de RSA TLS \_ con \_ des \_ CBC \_ Sha<br/>            | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportación RSA \_ TLS \_ con \_ RC4 \_ 40 \_ MD5<br/>                 | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ \_ MD5 nulo<br/>                            | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ con \_ des \_ CBC \_ Sha<br/>                   | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha<br/>       | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ des \_ 64 \_ CBC \_ con \_ MD5<br/>                     | Sí<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ con \_ MD5<br/>               | No<br/>                       | SSL 2.0<br/>                            |



 

Para agregar conjuntos de cifrado, use la configuración de directiva de grupo orden SSL del conjunto de cifrado en configuración del equipo > Plantillas administrativas > red > opciones de configuración de SSL para configurar una lista de prioridades para todos los conjuntos de cifrado que desee habilitar.

 

 
