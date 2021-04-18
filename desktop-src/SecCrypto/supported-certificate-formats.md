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
# <a name="supported-certificate-formats"></a><span data-ttu-id="ef5c3-103">Formatos de certificado compatibles</span><span class="sxs-lookup"><span data-stu-id="ef5c3-103">Supported Certificate Formats</span></span>

<span data-ttu-id="ef5c3-104">Los servicios de Certificate Server pueden emitir los siguientes tipos de certificados.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="ef5c3-105">Término</span><span class="sxs-lookup"><span data-stu-id="ef5c3-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="ef5c3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef5c3-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5c3-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de cliente compatible con SSL de [*X. 509*](../secgloss/x-gly.md) versión 3</span><span class="sxs-lookup"><span data-stu-id="ef5c3-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="ef5c3-108">Este certificado de autenticación de cliente identifica un cliente y lo usan los servidores para autenticar un cliente que solicita acceso al servidor.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="ef5c3-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificado de autenticación de servidor compatible con SSL de X. 509 V3</span><span class="sxs-lookup"><span data-stu-id="ef5c3-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="ef5c3-110">Este certificado de autenticación de servidor identifica un servidor y lo usan los clientes para autenticar un servidor al que el cliente desea tener acceso.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="ef5c3-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificado [*S/MIME*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="ef5c3-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="ef5c3-112">Los clientes usan este certificado para proteger el correo electrónico en el protocolo S/MIME (extensiones seguras multipropósito de correo Internet).</span><span class="sxs-lookup"><span data-stu-id="ef5c3-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="ef5c3-113">Además de estos certificados, los servicios de Certificate Server también se pueden usar para emitir otros certificados X. 509 escribiendo un módulo de directivas personalizado.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="ef5c3-114">"Certificado de autenticación de servidor" y "certificado de servidor", así como "certificado de autenticación del cliente" y "certificado de cliente" son términos intercambiables.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="ef5c3-115">Además, servicios de Certificate Server incluye plantillas de certificado en la configuración de la entidad de certificación empresarial de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="ef5c3-116">Consulte la documentación de ayuda de Windows para obtener información sobre las plantillas de certificado para comprender cómo definen los propósitos del certificado.</span><span class="sxs-lookup"><span data-stu-id="ef5c3-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
