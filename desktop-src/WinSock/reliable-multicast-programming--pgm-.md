---
description: En esta sección se describe la implementación del Protocolo de multidifusión PGM (multidifusión general pragmática) en Windows, que a menudo se conoce como multidifusión confiable. La multidifusión confiable se implementa a través de Windows Sockets en Windows Server 2003 y versiones posteriores.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programación de multidifusión confiable (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706195"
---
# <a name="reliable-multicast-programming-pgm"></a>Programación de multidifusión confiable (PGM)

En esta sección se describe la implementación del Protocolo de multidifusión PGM (multidifusión general pragmática) en Windows, que a menudo se conoce como multidifusión confiable. La multidifusión confiable se implementa a través de Windows Sockets en Windows Server 2003 y versiones posteriores.

**Windows XP:** PGM solo se admite cuando se instala Microsoft Message Queuing (MSMQ) 3,0.

PGM es un protocolo de multidifusión confiable y escalable que permite a los receptores detectar la pérdida, solicitar la retransmisión de datos perdidos o notificar a una aplicación de una pérdida irrecuperable. PGM es un protocolo de confianza del receptor, lo que significa que el receptor es responsable de garantizar que se reciban todos los datos, absolving el remitente de la responsabilidad de la recepción.

PGM es adecuado para aplicaciones que requieren la entrega de datos de multidifusión sin duplicar desde varios orígenes a varios receptores. PGM no admite la entrega confirmada, ni garantiza el orden de los paquetes de varios remitentes.

Para obtener más información sobre PGM, consulte RFC 3208 disponible en [www.ietf.org](https://www.ietf.org/).

En esta sección se describe cómo usar la multidifusión confiable en Windows. En los temas siguientes se explican los diversos aspectos de la creación de una aplicación de multidifusión confiable mediante Windows Sockets:

-   [Receptores y remitentes de PGM](pgm-senders-and-receivers.md)
-   [Opciones del remitente de PGM](pgm-sender-options.md)
-   [Envío y recepción de datos PGM](sending-and-receiving-pgm-data.md)
-   [Host múltiple y PGM](multihoming-and-pgm.md)
-   [Opciones de socket PGM](pgm-socket-options.md)

 

 



