---
description: Obtenga información sobre los conjuntos de cifrado TLS en Windows 7. Los conjuntos de cifrado solo se pueden negociar para las versiones TLS que los admiten.
ms.assetid: 283CB634-25EA-47F5-A2E3-0913F7D3D9DC
title: Conjuntos de cifrado TLS en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cbb6905c2505e53b3083e86cb04084eff824b1
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262387"
---
# <a name="tls-cipher-suites-in-windows-7"></a>Conjuntos de cifrado TLS en Windows 7

Los conjuntos de cifrado solo se pueden negociar para las versiones TLS que los admiten. Siempre se prefiere la versión de TLS más alta admitida en el protocolo de enlace TLS. Por ejemplo, SSL CK RC4 128 WITH MD5 solo se puede usar cuando el cliente y el servidor no admiten \_ \_ TLS \_ \_ \_ 1.2, 1.1 & 1.0 o SSL 3.0, ya que solo se admite con SSL 2.0.

La disponibilidad de los conjuntos de cifrado debe controlarse de una de estas dos maneras:

-   El orden de prioridad predeterminado se invalida cuando se configura una lista de prioridad. No se usarán los conjuntos de cifrado que no están en la lista de prioridades.
-   Permitido cuando la aplicación pasa SCH USE STRONG CRYPTO: el proveedor de Microsoft Schannel filtrará los conjuntos de cifrado débiles conocidos cuando la aplicación use la marca \_ \_ SCH USE STRONG \_ \_ \_ \_ CRYPTO. En Windows 7, los conjuntos de cifrado RC4 se filtran.

> [!IMPORTANT]
> Se producirá un error en los servicios web HTTP/2 con conjuntos de cifrado no compatibles con HTTP/2. Para asegurarse de que los servicios web funcionan con clientes y exploradores HTTP/2, consulte Implementación de la ordenación de conjuntos de [cifrado personalizados.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

El cumplimiento de FIPS se ha vuelto más complejo con la adición de curvas elípticas, lo que hace que la columna habilitada para el modo FIPS en versiones anteriores de esta tabla sea confusa. Por ejemplo, un conjunto de cifrado como TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 solo es compatible con FIPS cuando se usan curvas elípticas NIST. Para averiguar qué combinaciones de curvas elípticas y conjuntos de cifrado se habilitarán en el modo FIPS, consulte la sección 3.3.1 de Directrices para la selección, configuración y uso de implementaciones [de TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Windows 7, Windows 8 y Windows Server 2012 se actualizan mediante el Windows Update mediante la actualización 3042058, que cambia el orden de prioridad. Consulte [El aviso de seguridad de Microsoft 3042058](/security-updates/SecurityAdvisories/2015/3042058) para obtener más información. Los siguientes conjuntos de cifrado están habilitados y en este orden de prioridad de forma predeterminada el proveedor de Microsoft Schannel:



| Cadena de conjunto de cifrado                                                                                            | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versiones del protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>                                                     | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>                                                     | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>                                                     | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>                                                     | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                   | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                   | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>                                                   | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>                                                   | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ SHA256 NULL <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>            | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA CON SHA \_ \_ \_ NULL <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>               | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ CON \_ MD5 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/> | Sí<br/>                      | SSL 2.0<br/>                            |



 

El proveedor de Schannel de Microsoft admite los siguientes conjuntos de cifrado, pero no está habilitado de forma predeterminada:



| Cadena del conjunto de cifrado                                             | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versiones del protocolo TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>      | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>      | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>    | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>    | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ DES \_ CBC \_ SHA<br/>                        | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA<br/>             | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ DES \_ CBC \_ SHA<br/>            | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| EXPORTACIÓN DE RSA DE TLS \_ \_ CON \_ \_ RC4 \_ 40 \_ MD5<br/>                 | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ MD5 NULL<br/>                            | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ CON \_ DES \_ CBC \_ SHA<br/>                   | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ CON \_ DES \_ CBC \_ SHA<br/>       | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC \_ WITH \_ MD5<br/>                     | Sí<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5<br/>               | No<br/>                       | SSL 2.0<br/>                            |



 

Para agregar conjuntos de cifrado, use la configuración de directiva de grupo Orden del conjunto de cifrado SSL en Configuración del equipo > Plantillas administrativas > Network > Opciones de configuración de SSL para configurar una lista de prioridad para todos los conjuntos de cifrado que quiera habilitar.

 

 
