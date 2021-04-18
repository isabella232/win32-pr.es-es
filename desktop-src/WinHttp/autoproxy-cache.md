---
description: Caché de AutoProxy
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: Caché de AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0492bec116bad8a82da0e961cf6d851d27c787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716993"
---
# <a name="autoproxy-cache"></a>Caché de AutoProxy

La función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) realiza la búsqueda de proxy automática en función de la solicitud de la dirección URL especificada. Si se devuelven varios servidores proxy, las aplicaciones cliente deben probar cada proxy antes de enviar la solicitud (para obtener más información, vea la sección [solo se admite un servidor proxy](autoproxy-issues-in-winhttp.md) en problemas de AutoProxy en WinHTTP). La información de este tema se aplica a las llamadas a **WinHttpGetProxyForUrl** cuando el cliente especifica la detección automática del proxy.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , opcionalmente, localiza la dirección URL de AutoProxy y descarga el script de AutoProxy de ese sitio. WinHttp usa el script de AutoProxy para ubicar los servidores proxy. Tanto la dirección URL de AutoProxy como el script de AutoProxy se almacenan en caché para la sesión especificada. Solo se almacenan en caché una dirección URL y un script de AutoProxy para cada sesión. Normalmente, el script y la dirección URL de AutoProxy se almacenan en caché hasta que cambia la dirección IP asociada al equipo. Si se detecta una nueva dirección IP durante una llamada a **WinHttpGetProxyForUrl**, la llamada intentará localizar una nueva dirección URL de proxy AutoProxy y el script y almacenar en caché los resultados. Solo se debe permitir un usuario por sesión, de modo que los datos almacenados en caché no se compartan con otros usuarios del equipo. Para obtener más información, vea [información general sobre las sesiones de WinHTTP](winhttp-sessions-overview.md).

Si el servicio fuera de proceso está activo cuando se llama a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , el script y la dirección URL de proxy automático almacenados en caché estarán disponibles para todo el equipo. Sin embargo, si se usa el servicio fuera de proceso y la marca **fAutoLogonIfChallenged** en la estructura *pAutoProxyOptions* es true, el script y la dirección URL de AutoProxy no se almacenan en caché. Por lo tanto, al llamar a **WinHttpGetProxyForUrl** con el miembro **FAutoLogonIfChallenged** establecido en **true** , se producen operaciones de sobrecarga adicionales que pueden afectar al rendimiento. Los siguientes pasos se pueden usar para mejorar el rendimiento.

**Para mejorar el rendimiento**

1.  Llame a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con el parámetro fAutoLogonIfChallenged establecido en **false**. La dirección URL y el script de AutoProxy se almacenan en caché para futuras llamadas a **WinHttpGetProxyForUrl**.
2.  Si se produce un error en el paso 1, con **errores de inicio de sesión de \_ WinHTTP \_ \_**, llame a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con el miembro **fAutoLogonIfChallenged** establecido en **true**.

 

 



