---
description: Los equipos personales que ejecutan Microsoft Windows a menudo tienen numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes o una conexión de red física y una conexión de acceso telefónico.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Proveedor de servicios de reconocimiento de ubicación de red (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7378aff6f51f2785671f1d424a4721f9cd77fad22d60554746f9427d7f24f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132098"
---
# <a name="network-location-awareness-service-provider-nla"></a>Proveedor de servicios de reconocimiento de ubicación de red (NLA)

Los equipos personales que ejecutan Microsoft Windows a menudo tienen numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes o una conexión de red física y una conexión de acceso telefónico. Windows Los sockets han sido capaces de enumerar las interfaces de red disponibles durante algún tiempo, pero cierta información crítica sobre las conexiones de red no estaba disponible anteriormente. Esto incluye información como la red lógica a la que está conectado un equipo Windows o si hay varias interfaces conectadas a la misma red.

El proveedor de servicios de reconocimiento de ubicación de red, que se conoce normalmente como NLA, permite a las aplicaciones de Windows Sockets 2 identificar la red lógica a la que está asociado Windows equipo. Además, NLA permite a Windows Sockets identificar a qué interfaz de red física una aplicación determinada ha guardado información específica. NLA se implementa como un proveedor Windows servicio de resolución de nombres sockets 2.

 

 



