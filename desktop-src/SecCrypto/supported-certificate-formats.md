---
description: Enumera los formatos de certificado admitidos por Servicios de certificados.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formatos de certificado admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ae0c4d638e957df5ddcf251ca64578a67a58b98890401c68593dd7a12c3952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897636"
---
# <a name="supported-certificate-formats"></a>Formatos de certificado admitidos

Servicios de certificados puede emitir los siguientes tipos de certificados.



| Término                                                                                                                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de cliente compatible con SSL [*X.509*](../secgloss/x-gly.md) versión 3<br/> | Este certificado de autenticación de cliente identifica un cliente y lo usan los servidores para autenticar a un cliente que solicita acceso al servidor.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de servidor compatible con SSL X.509 v3<br/>                                                                                         | Este certificado de autenticación de servidor identifica un servidor y lo usan los clientes para autenticar un servidor al que el cliente desea acceder.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*Certificado S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Los clientes usan este certificado para el correo electrónico seguro en el protocolo S/MIME (Extensiones de correo de Internet seguras o multipropósito).<br/>              |



 

Además de estos certificados, los servicios de certificados también se pueden usar para emitir otros certificados X.509 mediante la escritura de un módulo de directivas personalizadas.

> [!Note]  
> "Certificado de autenticación de servidor" y "certificado de servidor", así como "certificado de autenticación de cliente" y "certificado de cliente" son términos intercambiables.

 

Además, Servicios de certificados incluye plantillas de certificado en la configuración de la entidad de certificación empresarial de Microsoft. Consulte la documentación Windows ayuda de las plantillas de certificado para comprender cómo definen los propósitos del certificado.

 

 
