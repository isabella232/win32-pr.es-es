---
description: La configuración y la desmontaje de conexiones de punto a punto y punto a punto de ATM son compatibles de forma nativa con la especificación Windows Sockets 2.
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Controles de ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed891f24c16f01025d0bd06da1ea3ec9c0cca01abdcaf3c9950229bf512f0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051453"
---
# <a name="winsock-atm-controls"></a>Controles de ATM de Winsock

La configuración y la desmontaje de conexiones de punto a punto y punto a punto de ATM son compatibles de forma nativa con la especificación Windows Sockets 2. De hecho, Windows especificación de QoS sockets 2 y mecanismos multipunto/multidifusión independientes del protocolo se diseñaron pensando en ATM, junto con otros protocolos. Consulte la sección 2.7 y el Apéndice D de la especificación de api Windows Sockets 2 para Windows Sockets 2, Calidad de servicio y Compatibilidad con varios puntos, respectivamente. Por lo tanto, no es necesario introducir ninguna ioctls específica de ATM en este documento.

 

 



