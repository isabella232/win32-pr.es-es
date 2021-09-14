---
description: 'Hay dos tipos fundamentales de aplicaciones de red: transaccional y streaming. Estos tipos de aplicación también se denominan tipos de aplicación interactivos y de procesamiento por lotes, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Transaccional frente a aplicaciones de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361318"
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

 

 



