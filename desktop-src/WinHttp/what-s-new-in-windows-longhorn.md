---
description: A partir de Windows Server 2008 y Windows Vista, la API de WinHTTP se ha mejorado para incluir las características siguientes.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Novedades de Windows Server 2008 y Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0f274b45e1db79fb79340b7f490de96f57e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497500"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Novedades de Windows Server 2008 y Windows Vista

A partir de Windows Server 2008 y Windows Vista, la API de WinHTTP se ha mejorado para incluir las características siguientes.

## <a name="greater-than-4-gb-upload"></a>Carga superior a 4 GB.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) solo puede enviar 4 GB de datos debido a limitaciones en el tamaño del parámetro de longitud total de DWORD. Para permitir que las aplicaciones envíen más de 4 GB de datos, se agrega el encabezado Content-Length a la solicitud especificando datos como grandes como un \_ entero grande (2 ^ 64 bytes). Para obtener más información, vea **WinHttpSendRequest**. Esta característica no se admite en el objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="transfer-encoding-header"></a>Encabezado Transfer-Encoding

El encabezado Transfer-Encoding permite a las aplicaciones enviar datos fragmentados al servidor. Cuando el encabezado Transfer-Encoding está presente en la solicitud, la aplicación envía la solicitud con un cuerpo de entidad de longitud cero en la llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). El cuerpo de la entidad se envía en llamadas posteriores a [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata). Esta característica no se admite en el objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Recuperación de lista de emisores de certificados de cliente SSL

La aplicación puede recuperar la lista de emisores de certificados de cliente SSL cuando se produce un error de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) con un **certificado de autenticación de \_ \_ cliente WinHTTP \_ \_ \_ necesario**. Una nueva opción, **la \_ opción \_ WinHTTP \_ \_ \_ lista de emisores de certificados de cliente**, permite a las aplicaciones recuperar la lista de emisores de certificados y filtrar la lista para obtener el certificado óptimo. Para obtener más información, consulte los temas de [**Opciones marcas**](option-flags.md) y [recuperación de listas de emisores para la autenticación de cliente SSL](ssl-in-winhttp.md) . Esta característica no se admite en el objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="optional-client-certificates"></a>Certificados de cliente opcionales

Cuando se produce un error de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) con un certificado de **\_ \_ autenticación de cliente \_ \_ \_ WinHTTP**, es posible que el servidor no requiera el certificado de cliente SSL. Es posible que el servidor pueda revertir a otra forma de autenticación, o bien permitir que el cliente continúe con el acceso anónimo. La aplicación establece la opción de contexto de certificado de cliente de la **\_ opción \_ \_ \_ WinHTTP** y especifica una macro que WinHTTP usa para determinar si el certificado de cliente es necesario. Para obtener más información, vea [**marcas de opciones**](option-flags.md). Esta característica no se admite en el objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="source-and-destination-ip-addresses"></a>Direcciones IP de origen y de destino

Cuando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) se completa, la aplicación puede recuperar la dirección IP de origen y de destino y el puerto de la solicitud que generó la respuesta. Se proporciona una nueva estructura para recibir las direcciones de origen y de destino cuando se establece la opción de información de conexión de la **\_ opción \_ \_ WinHTTP** . Para obtener más información, vea [**marcas de opciones**](option-flags.md). Esta característica no se admite en el objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="additional-ssl-client-authentication-errors"></a>Errores de autenticación de cliente SSL adicionales

Los errores adicionales de autenticación del cliente SSL proporcionan más información sobre el certificado de cliente SSL. **Error \_ de El certificado WINHTTP \_ Client \_ \_ no \_ Private \_ key** y **error \_ WinHTTP \_ CERT \_ no \_ Access \_ private \_ key** Certificate Errors son nuevas para Windows Server 2008 y Windows Vista. El objeto com [**IWinHttpRequest**](iwinhttprequest-interface.md) devuelve estos errores en HRESULT.

 

 



