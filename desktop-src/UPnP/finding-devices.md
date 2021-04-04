---
title: Búsqueda de dispositivos
description: La arquitectura de UPnP es una arquitectura de red dinámica que permite a los dispositivos unirse y dejar la red en cualquier momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076187"
---
# <a name="finding-devices"></a>Búsqueda de dispositivos

La arquitectura de UPnP es una arquitectura de red dinámica que permite a los dispositivos unirse y dejar la red en cualquier momento. Debido a esta arquitectura dinámica, las aplicaciones no pueden confiar en que los dispositivos basados en UPnP específicos estén disponibles en un momento dado. Por este motivo, las aplicaciones (o los puntos de control) buscan en la red los dispositivos que coinciden mejor con los criterios especificados. Las aplicaciones también esperan mensajes de anuncios de dispositivo que indican que se han agregado nuevos dispositivos a la red.

Estos son los criterios de búsqueda válidos para dispositivos basados en UPnP:

-   Tipo de dispositivo
-   Tipo de servicio
-   Nombre único del dispositivo (UDN)
-   Todos los dispositivos raíz

Las búsquedas de tipo de dispositivo y tipo de servicio se usan normalmente para buscar una clase de dispositivos con características comunes. La búsqueda de UDN se usa para buscar un dispositivo específico.

Para buscar dispositivos, una aplicación debe crear primero instancias del objeto de buscador de dispositivos. Este objeto expone la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; sus métodos realizan las búsquedas descritas anteriormente.

En las secciones siguientes se describe el proceso de búsqueda de dispositivos:

-   [Crear el buscador de dispositivos](creating-the-device-finder.md)
-   [Búsqueda asincrónica](asynchronous-searching.md)
-   [Búsqueda sincrónica](synchronous-searching.md)
-   [Colecciones de dispositivos devueltas por búsquedas sincrónicas](device-collections-returned-by-synchronous-searches.md)

 

 




