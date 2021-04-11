---
description: Winsock proporciona una interfaz de proveedor de servicios para crear servicios Winsock, lo que se conoce comúnmente como el SPI de Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Acerca de Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154303"
---
# <a name="about-the-winsock-spi"></a>Acerca de Winsock SPI

Winsock proporciona una interfaz de proveedor de servicios para crear servicios Winsock, lo que se conoce comúnmente como el SPI de Winsock. Existen dos tipos de proveedores de servicios: proveedores de transporte y proveedores de espacios de nombres. Entre los ejemplos de proveedores de transporte se incluyen pilas de protocolos como TCP/IP o IPX/SPX, mientras que un ejemplo de proveedor de espacio de nombres sería una interfaz al sistema de nombres de dominio (DNS) de Internet. Las secciones independientes de la especificación de la interfaz del proveedor de servicios se aplican a cada tipo de proveedor de servicios.

Los proveedores de servicios de [transporte](transport-service-providers-2.md) y de [espacio de nombres](name-space-service-providers-2.md) se deben registrar con el \_32.dll Ws2 en el momento en que se instalan. Este registro solo debe realizarse una vez para cada proveedor, ya que la información necesaria se conserva en el almacenamiento persistente.

 

 



