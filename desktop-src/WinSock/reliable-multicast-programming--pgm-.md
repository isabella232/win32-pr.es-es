---
description: En esta sección se describe la implementación del protocolo de multidifusión general pragmática (PGM) en Windows, a menudo denominada multidifusión confiable. La multidifusión confiable se implementa Windows sockets en Windows Server 2003 y versiones posteriores.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programación de multidifusión confiable (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c34365bdc8db553d24182fcb193dc03177627ccf9b00a03f309ab4cf7bbe01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559957"
---
# <a name="reliable-multicast-programming-pgm"></a>Programación de multidifusión confiable (PGM)

En esta sección se describe la implementación del protocolo de multidifusión general pragmática (PGM) en Windows, a menudo denominada multidifusión confiable. La multidifusión confiable se implementa Windows sockets en Windows Server 2003 y versiones posteriores.

**Windows XP:** PGM solo se admite cuando Microsoft Message Queuing (MSMQ) 3.0.

PGM es un protocolo de multidifusión confiable y escalable que permite a los receptores detectar pérdidas, solicitar la retransmisión de datos perdidos o notificar a una aplicación una pérdida irrecuperable. PGM es un protocolo confiable para el receptor, lo que significa que el receptor es responsable de garantizar que se reciben todos los datos, lo que absuelvía al remitente de la responsabilidad de recepción.

PGM es adecuado para aplicaciones que requieren la entrega de datos de multidifusión sin duplicados desde varios orígenes a varios receptores. PGM no admite la entrega reconocida ni garantiza el orden de los paquetes de varios remitentes.

Para obtener más información sobre PGM, consulte RFC 3208 disponible en [www.ietf.org](https://www.ietf.org/).

En esta sección se describe cómo usar la multidifusión confiable en Windows. En los temas siguientes se explican los distintos aspectos de la creación de una aplicación de multidifusión confiable mediante Windows Sockets:

-   [Remitentes y receptores de PGM](pgm-senders-and-receivers.md)
-   [Opciones del remitente de PGM](pgm-sender-options.md)
-   [Envío y recepción de datos PGM](sending-and-receiving-pgm-data.md)
-   [Multi-host y PGM](multihoming-and-pgm.md)
-   [Opciones de socket de PGM](pgm-socket-options.md)

 

 



