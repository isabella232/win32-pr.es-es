---
title: Acerca de Windows Connect Now
description: Windows Connect Now (WCN) proporciona un mecanismo sencillo y seguro para que los puntos de acceso a la red y los dispositivos (como impresoras, cámaras y equipos) conecten e intercedán la configuración.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46e0acbf2d2eb728b0b62610040aaa08e06d466c5bbd5ab47237c46a8612ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593715"
---
# <a name="about-windows-connect-now"></a>Acerca de Windows Connect Now

Windows Connect Now (WCN) proporciona un mecanismo sencillo y seguro para que los puntos de acceso a la red y los dispositivos (como impresoras, cámaras y equipos) conecten e intercedán la configuración. Esta API es la implementación de Microsoft del protocolo de configuración simple de Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC), creado por Wi-Fi Alliance como solución para redes locales y pequeñas empresas. Esta tecnología no está pensada para escenarios empresariales.

> [!Note]  
> El nombre de especificación ha cambiado entre la versión 1.0h y la versión 2. La especificación de la versión 1.0h se denominaba Wi-Fi protected setup (WPS). A partir de la especificación de la versión 2, la especificación se denomina Wi-Fi Simple Configuration (WSC). En nuestra documentación, los términos WPS y WSC se usan indistintamente a menos que se indique.

 

Windows Connect Now permite a las aplicaciones buscar dispositivos compatibles con WCN mediante [function discovery API](/previous-versions/windows/desktop/fundisc/fd-portal). El ámbito de una búsqueda se puede restringir a un SSID, estado, categoría o incluso ampliarse para incluir todos los dispositivos compatibles con WCN. Una vez que se encuentran los dispositivos, la API de WCN permite la comunicación con el dispositivo compatible con WCN con el fin de facilitar la configuración o la conectividad.

 

 