---
description: La arquitectura Windows Sockets 2 (Winsock) es compatible con la arquitectura Windows open system architecture (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows Arquitectura de sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad3dd29f692df94e1f66c13c00c75eeca36fb04d18c5f2e95e67b91773698f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569164"
---
# <a name="windows-sockets-2-architecture"></a>Windows Arquitectura de sockets 2

La arquitectura Windows Sockets 2 es compatible con Windows open system architecture (WOSA), como se muestra a continuación:

![Arquitectura de windows sockets 2](images/ovrvw2-1.png)

Winsock define una interfaz de proveedor de servicios (SPI) estándar entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas desde WS232.dll las pilas \_ de protocolo. Por lo tanto, la compatibilidad con Winsock no se limita a las pilas de protocolo TCP/IP, como es el caso de Windows Sockets 1.1.

Con la arquitectura Windows Sockets 2, no es necesario ni deseable que los proveedores de pila proporcionen su propia implementación de WS232.dll, ya que un único32.dll WS2 debe funcionar en todas las \_ \_ pilas. Las correcciones de compatibilidad32.dll WS2 se deben ver de la misma manera \_ que un componente del sistema operativo.

 

 



