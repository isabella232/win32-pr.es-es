---
description: 'Hay dos tipos fundamentales de aplicaciones de red: transaccional y streaming. Estos tipos de aplicación también se denominan tipos de aplicación interactivos y de procesamiento por lotes, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Transaccional frente a aplicaciones de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e55a21ba552ed768b29b784a557633edfc5734ec266893ede04fded76e538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559506"
---
# <a name="transactional-versus-streaming-applications"></a>Transaccional frente a aplicaciones de streaming

Hay dos tipos fundamentales de aplicaciones de red: *transaccional* y *de streaming.* Estos tipos de aplicación también se denominan *tipos de* aplicación interactivos y *de procesamiento* por lotes, respectivamente.

Las aplicaciones transaccionales son aplicaciones de stop-and-go. Normalmente realizan operaciones de solicitud/respuesta, a menudo ordenadas. Algunos ejemplos de aplicaciones transaccionales son la llamada a procedimiento remoto sincrónico (RPC), así como algunas implementaciones de HTTP y del Sistema de nombres de dominio (DNS).

Las aplicaciones de streaming mueven datos. Para describir las aplicaciones de streaming con un término paralelo, las aplicaciones de streaming se adhieren a una filosofía de transmisión de datos de velocidad a metal, normalmente con poca preocupación por el orden de los datos. Algunos ejemplos de aplicaciones de streaming son la copia de seguridad de red y el protocolo de transferencia de archivos (FTP).

Una vez determinado el tipo de aplicación, también se determinan sus características de red y protocolo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensiones de rendimiento](performance-dimensions-2.md)
</dt> </dl>

 

 



