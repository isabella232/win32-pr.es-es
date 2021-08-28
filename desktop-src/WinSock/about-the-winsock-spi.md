---
description: Winsock proporciona una interfaz de proveedor de servicios para crear servicios winsock, lo que se conoce normalmente como SPI de Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Acerca del SPI de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f321aabfd6345e3209414f96dedfaca4b9ab0acfa1629d49883a72ab8199cfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996945"
---
# <a name="about-the-winsock-spi"></a>Acerca del SPI de Winsock

Winsock proporciona una interfaz de proveedor de servicios para crear servicios winsock, lo que se conoce normalmente como SPI de Winsock. Existen dos tipos de proveedores de servicios: proveedores de transporte y proveedores de espacios de nombres. Algunos ejemplos de proveedores de transporte son las pilas de protocolos como TCP/IP o IPX/SPX, mientras que un ejemplo de un proveedor de espacios de nombres sería una interfaz para el Sistema de nomenclatura de dominios (DNS) de Internet. Las secciones independientes de la especificación de la interfaz del proveedor de servicios se aplican a cada tipo de proveedor de servicios.

[Los](transport-service-providers-2.md) proveedores [de servicios de](name-space-service-providers-2.md) transporte y espacio de nombres deben estar registrados con la32.dll Ws2 en el momento en que se \_ instalan. Este registro solo debe realizarse una vez para cada proveedor, ya que la información necesaria se conserva en el almacenamiento persistente.

 

 



