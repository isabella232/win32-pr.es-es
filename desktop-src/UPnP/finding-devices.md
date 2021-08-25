---
title: Buscar dispositivos
description: La arquitectura de UPnP es una arquitectura de red dinámica que permite a los dispositivos unirse a la red y abandonarla en cualquier momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5626f7d941d9e3fa73b6d3d46ef9f51ef256ee8371e7594c312d225bba865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867595"
---
# <a name="finding-devices"></a>Buscar dispositivos

La arquitectura de UPnP es una arquitectura de red dinámica que permite a los dispositivos unirse a la red y abandonarla en cualquier momento. Debido a esta arquitectura dinámica, las aplicaciones no pueden confiar en dispositivos específicos basados en UPnP para estar disponibles en un momento dado. Por esta razón, las aplicaciones (o puntos de control) buscan en la red los dispositivos que coinciden más estrechamente con los criterios especificados. Las aplicaciones también esperan mensajes de anuncio de dispositivos que indican que se han agregado nuevos dispositivos a la red.

Los siguientes son criterios de búsqueda válidos para dispositivos basados en UPnP:

-   Tipo de dispositivo
-   Tipo de servicio
-   Nombre de dispositivo único (UDN)
-   Todos los dispositivos raíz

Las búsquedas de tipo de dispositivo y tipo de servicio se usan normalmente para buscar una clase de dispositivos con características comunes. La búsqueda de UDN se usa para buscar un dispositivo específico.

Para buscar dispositivos, una aplicación debe crear primero una instancia del objeto Device Finder. Este objeto expone la [**interfaz IUPnPDeviceDevice;**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) sus métodos realizan las búsquedas descritas anteriormente.

En las secciones siguientes se describe el proceso de búsqueda de dispositivos:

-   [Creación del buscador de dispositivos](creating-the-device-finder.md)
-   [Búsqueda asincrónica](asynchronous-searching.md)
-   [Búsqueda sincrónica](synchronous-searching.md)
-   [Recopilaciones de dispositivos devueltas por búsquedas sincrónicas](device-collections-returned-by-synchronous-searches.md)

 

 




