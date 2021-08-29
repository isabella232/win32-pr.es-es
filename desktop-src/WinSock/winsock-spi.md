---
description: Windows Interfaz del proveedor de servicios (SPI) de Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec29ad26d97b62c884d2944b31d54c94ea1f61b02f74de28c6ff4c84acc6a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051333"
---
# <a name="winsock-spi"></a>Winsock SPI

La interfaz del proveedor de servicios de Winsock, o WINSOCK SPI, es una materia especializada de Winsock que se usa para crear proveedores. Los proveedores de transporte, como las pilas de protocolo TCP/IP o IPX/SPX, usan el SPI de Winsock, al igual que los proveedores de espacios de nombres, como el Sistema de nomenclatura de dominios (DNS) de Internet.

La programación de red tradicional, como permitir que las aplicaciones se comuniquen a través de la red, no requiere el uso de interfaces SPI de Winsock; use interfaces [winsock](winsock-reference.md) estándar en su lugar.

 

El SPI de Winsock usa la siguiente convención de nomenclatura de prefijo de función.



| Prefijo | Significado                          | Descripción                                       |
|--------|----------------------------------|---------------------------------------------------|
| Wsp    | Windows Proveedor de servicios sockets | Puntos de entrada del proveedor de servicios de transporte           |
| WPU    | Windows Llamada upcall del proveedor de sockets  | Puntos de entrada32.dll Ws2 \_ para proveedores de servicios    |
| Wsc    | Windows Configuración de sockets    | Puntos de entrada32.dll WS2 \_ para applets de instalación |
| Nsp    | Proveedor de espacios de nombres               | Puntos de entrada del proveedor de espacios de nombres                   |



 

 

 



