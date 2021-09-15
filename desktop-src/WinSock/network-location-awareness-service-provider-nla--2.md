---
description: Los equipos personales que ejecutan Microsoft Windows a menudo tienen numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes, o una conexión de red física y una conexión de acceso telefónico.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Proveedor de Servicios de reconocimiento de ubicación de red (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474521"
---
# <a name="network-location-awareness-service-provider-nla"></a>Proveedor de Servicios de reconocimiento de ubicación de red (NLA)

Los equipos personales que ejecutan Microsoft Windows a menudo tienen numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes, o una conexión de red física y una conexión de acceso telefónico. Windows Los sockets han sido capaces de enumerar las interfaces de red disponibles durante un tiempo, pero cierta información crítica sobre las conexiones de red no estaba disponible anteriormente. Esto incluye información como la red lógica a la que está conectado Windows equipo o si hay varias interfaces conectadas a la misma red.

El proveedor de servicios de reconocimiento de ubicación de red, conocido normalmente como NLA, permite que las aplicaciones de sockets de Windows 2 identifiquen la red lógica a la que está conectado un equipo Windows red. Además, NLA permite a Windows Sockets identificar a qué interfaz de red física una aplicación determinada ha guardado información específica. NLA se implementa como un proveedor de servicios de resolución de nombres Windows sockets 2 genéricos.

 

 



