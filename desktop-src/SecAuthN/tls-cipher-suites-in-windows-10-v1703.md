---
description: Los conjuntos de cifrado solo se pueden negociar para las versiones de TLS que los admiten. Siempre se prefiere la versión de TLS más alta admitida en el protocolo de enlace de TLS.
ms.assetid: 2933DE68-E14B-48F9-8F31-49529BC883D6
title: Conjuntos de cifrado TLS en Windows 10 v1703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d4f2ca1d0ae07ad0db75a667b34366ba546425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541819"
---
# <a name="tls-cipher-suites-in-windows-10-v1703"></a>Conjuntos de cifrado TLS en Windows 10 v1703

Los conjuntos de cifrado solo se pueden negociar para las versiones de TLS que los admiten. Siempre se prefiere la versión de TLS más alta admitida en el protocolo de enlace de TLS.

La disponibilidad de los conjuntos de cifrado debe controlarse de una de estas dos maneras:

-   El orden de prioridad predeterminado se invalida cuando se configura una lista de prioridades. No se usarán los conjuntos de cifrado que no estén en la lista de prioridades.
-   Se permite cuando la aplicación pasa \_ SCH \_ usar \_ Criptografía segura: el proveedor de Microsoft Schannel filtrará los conjuntos de cifrado débil conocidos cuando la aplicación use la \_ marca de \_ \_ cifrado Strong usar. En Windows 10, la versión 1703, además de RC4, DES, los conjuntos de cifrado de exportación y NULL se filtran.

> [!IMPORTANT]
> Los servicios Web HTTP/2 producen un error con conjuntos de cifrado no compatibles con HTTP/2. Para asegurarse de que los servicios web funcionan con clientes y exploradores HTTP/2, consulte [cómo implementar el orden personalizado de conjuntos de cifrado](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

El cumplimiento de FIPS se ha vuelto más complejo con la adición de curvas elípticas que hacen que la columna del modo FIPS habilitado en las versiones anteriores de esta tabla sea engañosa. Por ejemplo, un conjunto de cifrado como TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 solo es una queja de FIPS cuando se usan curvas elípticas de NIST. Para averiguar qué combinaciones de las curvas elípticas y los conjuntos de cifrado se habilitarán en modo FIPS, consulte la sección 3.3.1 de [directrices para la selección, la configuración y el uso de implementaciones de TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

En Windows 10, versión 1703, los siguientes conjuntos de cifrado están habilitados y en este orden de prioridad de forma predeterminada, mediante el proveedor de Microsoft Schannel:



| Cadena de conjunto de cifrado                                                                                 | Permitido por SCH \_ usar \_ \_ Criptografía segura | Versiones del protocolo TLS/SSL                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                              | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                              | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                    | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Sí<br/>                      | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                       | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                       | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ 3DES \_ Ede \_ CBC \_ Sha<br/>                                                      | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| \_RSA TLS \_ con \_ RC4 \_ 128 \_ Sha<br/>                                                            | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ RC4 \_ 128 \_ MD5<br/>                                                            | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ null \_ SHA256 <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/> | No<br/>                       | TLS 1.2<br/>                            |
| \_RSA TLS \_ con \_ \_ Sha nulo <br/> Solo se usa cuando la aplicación solicita explícitamente.<br/>    | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Los siguientes conjuntos de cifrado son compatibles con el proveedor de Microsoft Schannel, pero no están habilitados de forma predeterminada:



| Cadena de conjunto de cifrado                                                                               | Permitido por SCH \_ usar \_ \_ Criptografía segura | Versiones del protocolo TLS/SSL                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sí<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ con \_ 3DES \_ Ede \_ CBC \_ Sha<br/>                                               | Sí<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ des \_ CBC \_ Sha<br/>                                                          | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ con \_ des \_ CBC \_ Sha<br/>                                                     | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ DHE \_ DSS \_ EXPORT1024 \_ con \_ DES \_ CBC \_ Sha no TLS 1,2, tls 1,1, TLS 1,0, SSL 3,0<br/>   | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ \_ MD5 nulo <br/> Solo se usa cuando la aplicación solicita explícitamente. <br/> | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_EXPORT1024 RSA \_ TLS \_ con \_ RC4 \_ 56 \_ Sha<br/>                                               | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportación RSA \_ TLS \_ con \_ RC4 \_ 40 \_ MD5<br/>                                                   | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_ \_ EXPORT1024 de RSA TLS \_ con \_ des \_ CBC \_ Sha<br/>                                              | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Los siguientes conjuntos de cifrado de PSK están habilitados y en este orden de prioridad de forma predeterminada con el proveedor de Microsoft Schannel:



| Cadena de conjunto de cifrado                              | Permitido por SCH \_ usar \_ \_ Criptografía segura | Versiones del protocolo TLS/SSL |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Sí<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Sí<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Sí<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Sí<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ null \_ SHA384<br/>          | No<br/>                       | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ null \_ SHA256<br/>          | No<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> No hay ningún conjunto de cifrado de PSK habilitado de forma predeterminada. Las aplicaciones necesitan solicitar una PSK mediante \_ SCH \_ use \_ solo PRESHAREDKEY. Para obtener más información sobre las marcas Schannel, consulte [**Schannel \_ CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Para agregar conjuntos de cifrado, implemente una directiva de grupo o use los cmdlets de TLS:

-   Para usar la Directiva de grupo, configure el orden de los conjuntos de cifrado SSL en configuración del equipo > Plantillas administrativas > red > opciones de configuración de SSL con la lista prioridad para todos los conjuntos de cifrado que desee habilitar.
-   Para usar PowerShell, consulte [cmdlets de TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Antes de Windows 10, las cadenas de conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva. Windows 10 admite un valor de orden de prioridad de curva elíptica, por lo que el sufijo de curva elíptica no es necesario y se reemplaza por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la Directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.

 

 

 
