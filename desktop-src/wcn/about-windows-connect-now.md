---
title: Acerca de Windows Connect Now
description: Windows Connect Now (WCN) proporciona un mecanismo sencillo y seguro para puntos de acceso de red y dispositivos (por ejemplo, impresoras, cámaras y PCs) para conectarse y cambiar la configuración.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149546"
---
# <a name="about-windows-connect-now"></a>Acerca de Windows Connect Now

Windows Connect Now (WCN) proporciona un mecanismo sencillo y seguro para puntos de acceso de red y dispositivos (por ejemplo, impresoras, cámaras y PCs) para conectarse y cambiar la configuración. Esta API es la implementación de Microsoft del protocolo Wi-Fi de configuración simple (/Wi-Fi) de configuración protegida (WPS), que creó Wi-Fi Alliance como una solución para redes domésticas y pequeñas empresas. Esta tecnología no está pensada para escenarios empresariales.

> [!Note]  
> El nombre de la especificación cambió entre la versión 1.0 h y la versión 2. La especificación h de la versión 1.0 se llamaba Wi-Fi instalación protegida (WPS). A partir de la especificación de la versión 2, la especificación se denomina Wi-Fi configuración simple (WSC). En nuestra documentación, los términos WPS y WSC se usan indistintamente a menos que se indique.

 

Windows Connect ahora permite que las aplicaciones busquen dispositivos compatibles con WCN mediante la [API de detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal). El ámbito de una búsqueda se puede restringir a un SSID específico, un estado, una categoría o incluso ampliarse para incluir todos los dispositivos compatibles con WCN. Una vez que se encuentran los dispositivos, la API de WCN permite la comunicación con el dispositivo compatible con WCN con el fin de facilitar la configuración o la conectividad.

 

 