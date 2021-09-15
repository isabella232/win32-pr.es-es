---
description: Caché de AutoProxy
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: Caché de AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0492bec116bad8a82da0e961cf6d851d27c787
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580676"
---
# <a name="autoproxy-cache"></a>Caché de AutoProxy

La [**función WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) realiza la búsqueda de un proxy automático por solicitud para la dirección URL especificada. Si se devuelven varios servidores proxy, las aplicaciones cliente deben probar cada proxy antes de enviar la solicitud (para obtener más información, consulte la sección Only [One Proxy Server is Currently Supported](autoproxy-issues-in-winhttp.md) (Solo un servidor proxy es compatible actualmente) en Problemas de AutoProxy en WinHTTP). La información de este tema se aplica a las llamadas **a WinHttpGetProxyForUrl** cuando el cliente especifica la detección automática de proxy.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) busca opcionalmente la dirección URL del proxy automático y descarga el script de autoproxy desde ese sitio. WinHttp usa el script de proxy automático para buscar los servidores proxy. Tanto la dirección URL del proxy automático como el script de autoproxy se almacenan en caché para la sesión especificada. Solo se almacenan en caché una dirección URL de proxy automático y un script para cada sesión. Normalmente, el script y la dirección URL del proxy automático se almacenan en caché hasta que cambia la dirección IP asociada al equipo. Si se detecta una nueva dirección IP durante una llamada a **WinHttpGetProxyForUrl,** la llamada intentará localizar una nueva dirección URL del proxy automático y crear un script y almacenar en caché los resultados. Solo se debe permitir un usuario por sesión, de modo que los datos almacenados en caché no se compartan con otros usuarios del equipo. Para más información, consulte Información [general sobre las sesiones WinHTTP.](winhttp-sessions-overview.md)

Si el servicio fuera de proceso está activo cuando se llama a [**WinHttpGetProxyForUrl,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) la dirección URL y el script del proxy automático almacenados en caché están disponibles para todo el equipo. Sin embargo, si se usa el servicio fuera de proceso y la marca **fAutoLogonIfProxyLenged** de la estructura *pAutoProxyOptions* es true, la dirección URL del proxy automático y el script no se almacenan en caché. Por lo tanto, llamar **a WinHttpGetProxyForUrl** con el miembro **fAutoLogonIfIferlenged** establecido en **TRUE** da como resultado operaciones de sobrecarga adicionales que pueden afectar al rendimiento. Los pasos siguientes se pueden usar para mejorar el rendimiento.

**Para mejorar el rendimiento**

1.  Llame [**a WinHttpGetProxyForUrl con**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) el parámetro fAutoLogonIfHttplenged establecido en **false.** La dirección URL del proxy automático y el script se almacenan en caché para futuras llamadas **a WinHttpGetProxyForUrl.**
2.  Si se produce un error en el paso 1, con **ERROR \_ WINHTTP \_ LOGIN \_ FAILURE**, llame a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con el miembro **fAutoLogonIfHttplenged** establecido en **TRUE.**

 

 



