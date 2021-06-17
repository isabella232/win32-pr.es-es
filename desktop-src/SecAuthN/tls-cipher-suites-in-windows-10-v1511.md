---
description: Obtenga información sobre los conjuntos de cifrado TLS Windows 10 v1511. Los conjuntos de cifrado solo se pueden negociar para las versiones TLS que los admiten.
ms.assetid: E17F8C61-6985-43D7-8AAA-5300D1AA7028
title: Conjuntos de cifrado TLS en Windows 10 v1511
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644417cc4af531049c0c09f7c06dd6c5f92ca3e0
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262537"
---
# <a name="tls-cipher-suites-in-windows-10-v1511"></a>Conjuntos de cifrado TLS en Windows 10 v1511

Los conjuntos de cifrado solo se pueden negociar para las versiones TLS que los admiten. Siempre se prefiere la versión de TLS más alta admitida en el protocolo de enlace TLS. Por ejemplo, SSL CK RC4 128 WITH MD5 solo se puede usar cuando el cliente y el servidor no admiten \_ \_ TLS \_ \_ \_ 1.2, 1.1 & 1.0 o SSL 3.0, ya que solo se admite con SSL 2.0.

La disponibilidad de los conjuntos de cifrado debe controlarse de una de estas dos maneras:

-   El orden de prioridad predeterminado se invalida cuando se configura una lista de prioridad. No se usarán los conjuntos de cifrado que no están en la lista de prioridades.
-   Permitido cuando la aplicación pasa SCH USE STRONG CRYPTO: el proveedor de Microsoft Schannel filtrará los conjuntos de cifrado débiles conocidos cuando la aplicación use la marca \_ \_ SCH USE STRONG \_ \_ \_ \_ CRYPTO. En Windows 10, versión 1511, además de RC4, se filtran los conjuntos de cifrado DES, export y NULL.

> [!IMPORTANT]
> Se producirá un error en los servicios web HTTP/2 con conjuntos de cifrado no compatibles con HTTP/2. Para asegurarse de que los servicios web funcionan con clientes y exploradores HTTP/2, consulte Implementación de la ordenación de conjuntos de [cifrado personalizados.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

El cumplimiento de FIPS se ha vuelto más complejo con la adición de curvas elípticas, lo que hace que la columna habilitada para el modo FIPS en versiones anteriores de esta tabla sea confusa. Por ejemplo, un conjunto de cifrado como TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 solo es una queja de FIPS cuando se usan curvas elípticas NIST. Para averiguar qué combinaciones de curvas elípticas y conjuntos de cifrado se habilitarán en el modo FIPS, consulte la sección 3.3.1 de Directrices para la selección, configuración y uso de implementaciones [de TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Para Windows 10 versión 1511, los siguientes conjuntos de cifrado están habilitados y en este orden de prioridad de forma predeterminada mediante el proveedor de Microsoft Schannel:



| Cadena de conjunto de cifrado                                                                                            | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versiones del protocolo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                      | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                      | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                        | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                        | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                                      | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                      | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                                        | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                        | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                         | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                         | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                           | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                           | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Sí<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ SHA256 NULL <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>            | No<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA CON SHA \_ \_ \_ NULL <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>               | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ CON \_ MD5 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/> | Sí<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>            | No<br/>                       | SSL 2.0<br/>                            |



 

El proveedor de Microsoft Schannel admite los siguientes conjuntos de cifrado, pero no está habilitado de forma predeterminada:



| Cadena de conjunto de cifrado                                                                              | Permitido por SCH \_ USE \_ STRONG \_ CRYPTO | Versiones del protocolo TLS/SSL                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ RSA \_ CON \_ DES \_ CBC \_ SHA<br/>                                                         | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA<br/>                                              | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ DES \_ CBC \_ SHA<br/>                                             | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT \_ WITH \_ RC4 \_ 40 \_ MD5<br/>                                                  | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ MD5 NULL <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/> | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ CON \_ DES \_ CBC \_ SHA<br/>                                                    | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ CON \_ DES \_ CBC \_ SHA<br/>                                        | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC \_ WITH \_ MD5<br/>                                                      | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5<br/>                                                | No<br/>                       | SSL 2.0<br/>                            |



 

Para agregar conjuntos de cifrado, implemente una directiva de grupo o use los cmdlets TLS:

-   Para usar la directiva de grupo, configure el orden del conjunto de cifrado SSL en Configuración del equipo > Plantillas administrativas > Network > Opciones de configuración de SSL con la lista de prioridad de todos los conjuntos de cifrado que quiera habilitar.
-   Para usar PowerShell, consulte [Cmdlets de TLS.](/powershell/module/tls/?view=win10-ps)

> [!Note]  
> Antes de Windows 10, las cadenas del conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva. Windows 10 admite una configuración de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la directiva de grupo para configurar distintas versiones de Windows con los mismos conjuntos de cifrado.

 

> [!IMPORTANT]
> Los servicios web HTTP/2 no son compatibles con los pedidos personalizados del conjunto de cifrado TLS. Para obtener más información, [vea Cómo implementar la ordenación de conjuntos de cifrado personalizados.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

 

 
