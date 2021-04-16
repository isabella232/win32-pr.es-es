---
description: 'Hay dos tipos fundamentales de aplicaciones de red: transaccional y de streaming. Estos tipos de aplicaciones también se denominan tipos de aplicación interactivos y de procesamiento por lotes, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Aplicaciones transaccionales frente a streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705591"
---
# <a name="transactional-versus-streaming-applications"></a>Aplicaciones transaccionales frente a streaming

Hay dos tipos fundamentales de aplicaciones de red: *transaccional* y de *streaming*. Estos tipos de aplicaciones también se denominan tipos de aplicación *interactivos* y de *procesamiento por lotes* , respectivamente.

Las aplicaciones transaccionales son aplicaciones STOP y go. Normalmente realizan operaciones de solicitud/respuesta, que a menudo se ordenan. Algunos ejemplos de aplicaciones transaccionales son la llamada a procedimiento remoto (RPC) sincrónica, así como algunas implementaciones de HTTP y del sistema de nombres de dominio (DNS).

Las aplicaciones de streaming mueven datos. Para describir las aplicaciones de streaming con un término paralelo, las aplicaciones de streaming se adhieren a una filosofía de transmisión de datos de pedal a metal, normalmente con poca preocupación para la ordenación de datos. Los ejemplos de aplicaciones de streaming incluyen copia de seguridad de red y Protocolo de transferencia de archivos (FTP).

Una vez que se determina el tipo de aplicación, se determinan también sus características de red y protocolo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensiones de rendimiento](performance-dimensions-2.md)
</dt> </dl>

 

 



