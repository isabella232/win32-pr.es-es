---
description: Enumera los formatos de certificado admitidos por Servicios de certificados.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formatos de certificado admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473450"
---
# <a name="supported-certificate-formats"></a>Formatos de certificado admitidos

Certificate Services puede emitir los siguientes tipos de certificados.



| Término                                                                                                                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de cliente compatible con SSL [*X.509*](../secgloss/x-gly.md) versión 3<br/> | Este certificado de autenticación de cliente identifica un cliente y lo usan los servidores para autenticar un cliente que solicita acceso al servidor.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de servidor compatible con SSL X.509 v3<br/>                                                                                         | Este certificado de autenticación de servidor identifica un servidor y lo usan los clientes para autenticar un servidor al que el cliente desea acceder.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*Certificado S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Los clientes usan este certificado para el correo electrónico seguro en el protocolo S/MIME (Extensiones seguras o multipropósito de Correo electrónico de Internet).<br/>              |



 

Además de estos certificados, los servicios de certificados también se pueden usar para emitir otros certificados X.509 escribiendo un módulo de directivas personalizadas.

> [!Note]  
> "Certificado de autenticación de servidor" y "certificado de servidor", así como "certificado de autenticación de cliente" y "certificado de cliente" son términos intercambiables.

 

Además, Certificate Services incluye plantillas de certificado en la configuración de la entidad de certificación empresarial de Microsoft. Consulte la documentación Windows ayuda para las plantillas de certificado para comprender cómo definen los propósitos del certificado.

 

 
