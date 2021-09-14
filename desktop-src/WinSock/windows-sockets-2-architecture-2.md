---
description: La arquitectura Windows Sockets 2 (Winsock) es compatible con la arquitectura Windows open system architecture (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Arquitectura de sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967292"
---
# <a name="windows-sockets-2-architecture"></a>Windows Arquitectura de sockets 2

La arquitectura Windows Sockets 2 es compatible con Windows open system architecture (WOSA), como se muestra a continuación:

![Arquitectura de windows sockets 2](images/ovrvw2-1.png)

Winsock define una interfaz de proveedor de servicios (SPI) estándar entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas desde WS232.dll las pilas \_ de protocolo. Por lo tanto, la compatibilidad con Winsock no se limita a las pilas de protocolo TCP/IP, como es el caso de Windows Sockets 1.1.

Con la arquitectura Windows Sockets 2, no es necesario ni deseable que los proveedores de pila proporcionen su propia implementación de WS232.dll, ya que un único32.dll WS2 debe funcionar en todas las \_ \_ pilas. Las correcciones de compatibilidad32.dll WS2 se deben ver de la misma manera \_ que un componente del sistema operativo.

 

 



