---
description: Interfaz del proveedor de servicios (SPI) de Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652721"
---
# <a name="winsock-spi"></a>SPI de Winsock

La interfaz del proveedor de servicios Winsock, o Winsock SPI, es una disciplina especializada de Winsock que se usa para crear proveedores. los proveedores de transporte, como las pilas de protocolo TCP/IP o IPX/SPX, usan el SPI de Winsock, al igual que los proveedores de espacios de nombres, como el sistema de nombres de dominio (DNS) de Internet.

La programación de red tradicional, como permitir que las aplicaciones se comuniquen a través de la red, no requiere el uso de interfaces de Winsock SPI; Use las interfaces de [Winsock](winsock-reference.md) estándar en su lugar.

 

El SPI de Winsock usa la siguiente Convención de nomenclatura de prefijos de función.



| Prefijo | Significado                          | Descripción                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Proveedor de servicios de Windows Sockets | Puntos de entrada del proveedor de servicios de transporte           |
| WPU    | Llamada al proveedor de Windows Sockets  | Ws2 \_32.dll puntos de entrada para proveedores de servicios    |
| WSC    | Configuración de Windows Sockets    | WS2 \_32.dll puntos de entrada para applets de instalación |
| NSP    | Proveedor de espacios de nombres               | Puntos de entrada del proveedor de espacios de nombres                   |



 

 

 



