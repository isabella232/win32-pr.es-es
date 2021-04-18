---
title: Url
description: Los elementos de la API de URL de WWSAPI proporcionan mecanismos para dividir y deshacer el escape de las direcciones URL en partes componentes, y para volver a combinar las partes componentes en una dirección URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Servicios Web de URL para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2020
ms.locfileid: "105704909"
---
# <a name="url"></a>Url

Los elementos de la API de URL de WWSAPI proporcionan mecanismos para dividir y deshacer el escape de las direcciones URL en partes componentes, y para volver a combinar las partes componentes en una dirección URL.

-   Para dividir las direcciones URL y unescape en partes componentes, use la función [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .
-   Para escapar y combinar partes de componentes en una dirección URL, use la función [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .
-   Para combinar direcciones URL relativas con una dirección URL base absoluta que forme una dirección URL absoluta, utilice la función [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .

Las enumeraciones siguientes forman parte de la dirección URL:

-   [**\_marcas de URL de WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_tipo de esquema de dirección URL de WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

Las siguientes funciones forman parte de la dirección URL:

-   [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

Las siguientes estructuras forman parte de la dirección URL:

-   [**URL de WS \_ https \_**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**URL de WS \_ http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**URL de WS \_ NETPIPE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**URL de WS \_ NETTCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**URL de WS \_ SOAPUDP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**URL de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




