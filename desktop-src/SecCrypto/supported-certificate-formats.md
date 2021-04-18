---
description: Enumera los formatos de certificado admitidos por servicios de Certificate Server.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formatos de certificado compatibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667531"
---
# <a name="supported-certificate-formats"></a>Formatos de certificado compatibles

Los servicios de Certificate Server pueden emitir los siguientes tipos de certificados.



| Término                                                                                                                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de cliente compatible con SSL de [*X. 509*](../secgloss/x-gly.md) versión 3<br/> | Este certificado de autenticación de cliente identifica un cliente y lo usan los servidores para autenticar un cliente que solicita acceso al servidor.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de servidor compatible con SSL de X. 509 V3<br/>                                                                                         | Este certificado de autenticación de servidor identifica un servidor y lo usan los clientes para autenticar un servidor al que el cliente desea tener acceso.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificado [*S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Los clientes usan este certificado para proteger el correo electrónico en el protocolo S/MIME (extensiones seguras multipropósito de correo Internet).<br/>              |



 

Además de estos certificados, los servicios de Certificate Server también se pueden usar para emitir otros certificados X. 509 escribiendo un módulo de directivas personalizado.

> [!Note]  
> "Certificado de autenticación de servidor" y "certificado de servidor", así como "certificado de autenticación del cliente" y "certificado de cliente" son términos intercambiables.

 

Además, servicios de Certificate Server incluye plantillas de certificado en la configuración de la entidad de certificación empresarial de Microsoft. Consulte la documentación de ayuda de Windows para obtener información sobre las plantillas de certificado para comprender cómo definen los propósitos del certificado.

 

 
