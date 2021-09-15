---
description: A partir Windows Server 2008 y Windows Vista, la API WinHTTP se ha mejorado para incluir las siguientes características.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Novedades de Windows Server 2008 y Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0f274b45e1db79fb79340b7f490de96f57e8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568165"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Novedades de Windows Server 2008 y Windows Vista

A partir Windows Server 2008 y Windows Vista, la API WinHTTP se ha mejorado para incluir las siguientes características.

## <a name="greater-than-4-gb-upload"></a>Más de 4 GB de Upload.

[**WinHttpSendRequest solo**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) puede enviar 4 GB de datos debido a limitaciones en el tamaño del parámetro de longitud total DWORD. Para permitir que las aplicaciones envíen más de 4 GB de datos, el encabezado Content-Length se agrega a la solicitud especificando datos tan grandes como un ENTERO GRANDE \_ (2^64 bytes). Para obtener más información, **vea WinHttpSendRequest**. Esta característica no se admite en el objeto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="transfer-encoding-header"></a>Transfer-Encoding encabezado

El Transfer-Encoding permite a las aplicaciones enviar datos fragmentados al servidor. Cuando el Transfer-Encoding está presente en la solicitud, la aplicación envía la solicitud con un cuerpo de entidad de longitud cero en la llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). El cuerpo de la entidad se envía en llamadas posteriores [**a WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata). Esta característica no se admite en el objeto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Recuperación de la lista de emisores de certificados de cliente SSL

La aplicación puede recuperar la lista de emisores del certificado de cliente SSL cuando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) produce un **error \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED**. Una nueva opción, **WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ ISSUER \_ LIST,** permite a las aplicaciones recuperar la lista de emisores de certificados y filtrar la lista para obtener el certificado óptimo. Para obtener más información, vea los temas [**Marcas de opción**](option-flags.md) y Recuperación de lista de [emisores para la autenticación de cliente SSL.](ssl-in-winhttp.md) Esta característica no se admite en el objeto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="optional-client-certificates"></a>Certificados de cliente opcionales

Cuando [**WinHttpSendRequest produce**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) un **error \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED**, es posible que el servidor no requiera el certificado de cliente SSL. Es posible que el servidor pueda revertir a otra forma de autenticación o permitir que el cliente continúe con el acceso anónimo. La aplicación establece la opción **WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ CONTEXT** y especifica una macro que WinHttp usa para determinar si se requiere el certificado de cliente. Para obtener más información, vea [**Marcas de opción**](option-flags.md). Esta característica no se admite en el objeto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="source-and-destination-ip-addresses"></a>Direcciones IP de origen y destino

Cuando [**Se completa WinHttpReceiveResponse,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) la aplicación puede recuperar la dirección IP de origen y destino y el puerto de la solicitud que generó la respuesta. Se proporciona una nueva estructura para recibir las direcciones de origen y destino cuando se establece la opción **WINHTTP \_ OPTION CONNECTION \_ \_ INFO.** Para obtener más información, vea [**Marcas de opción**](option-flags.md). Esta característica no se admite en el objeto COM [**IWinHttpRequest.**](iwinhttprequest-interface.md)

## <a name="additional-ssl-client-authentication-errors"></a>Errores de autenticación de cliente SSL adicionales

Los errores de autenticación de cliente SSL adicionales proporcionan más información sobre el certificado de cliente SSL. **ERROR \_ Los errores de certificado de cliente WINHTTP \_ CLIENT CERT NO PRIVATE \_ \_ \_ \_ KEY** y **ERROR \_ WINHTTP CERT NO ACCESS \_ \_ PRIVATE \_ \_ \_ KEY** son nuevos para Windows Server 2008 y Windows Vista. El objeto COM [**IWinHttpRequest**](iwinhttprequest-interface.md) devuelve estos errores en un HRESULT.

 

 



