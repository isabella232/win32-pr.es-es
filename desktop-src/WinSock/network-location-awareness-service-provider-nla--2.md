---
description: Los equipos personales que ejecutan Microsoft Windows suelen tener numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes, o una conexión de red física y una conexión de acceso telefónico.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Proveedor de servicios de reconocimiento de ubicación de red (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154259"
---
# <a name="network-location-awareness-service-provider-nla"></a>Proveedor de servicios de reconocimiento de ubicación de red (NLA)

Los equipos personales que ejecutan Microsoft Windows suelen tener numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes, o una conexión de red física y una conexión de acceso telefónico. Windows Sockets es capaz de enumerar las interfaces de red disponibles durante algún tiempo, pero cierta información crítica sobre las conexiones de red no estaba disponible anteriormente. Esto incluye información como la red lógica a la que está conectado un equipo Windows o si varias interfaces están conectadas a la misma red.

El proveedor de servicios de reconocimiento de ubicación de red, comúnmente conocido como NLA, permite que las aplicaciones de Windows Sockets 2 identifiquen la red lógica a la que está conectado un equipo Windows. Además, NLA permite a las aplicaciones de Windows Sockets identificar en qué interfaz de red física una aplicación determinada ha guardado información específica. NLA se implementa como un proveedor de servicios de resolución de nombres genérico de Windows Sockets 2.

 

 



