---
description: La arquitectura de Windows Sockets 2 (Winsock) es compatible con la arquitectura de Windows Open System (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Arquitectura de Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155261"
---
# <a name="windows-sockets-2-architecture"></a>Arquitectura de Windows Sockets 2

La arquitectura de Windows Sockets 2 es compatible con la arquitectura de Windows Open System (WOSA), como se muestra a continuación:

![arquitectura de Windows Sockets 2](images/ovrvw2-1.png)

Winsock define una interfaz de proveedor de servicios estándar (SPI) entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas desde WS2 \_32.dll y las pilas de protocolos. Por lo tanto, la compatibilidad con Winsock no se limita a las pilas del protocolo TCP/IP, como es el caso de Windows Sockets 1,1.

Con la arquitectura de Windows Sockets 2, no es necesario o deseable, para que los proveedores de pila suministren su propia implementación de WS2 \_32.dll, ya que un único WS2 \_32.dll debe funcionar en todas las pilas. El \_32.dll WS2 y las correcciones de compatibilidad (shim) se deben ver de la misma manera que un componente del sistema operativo.

 

 



