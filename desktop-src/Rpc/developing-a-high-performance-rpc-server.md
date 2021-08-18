---
title: Desarrollar un servidor RPC de alto rendimiento
description: La información de esta sección se aplica a las secuencias de protocolo remoto ncacn \_ ip \_ tcp, ncacn \_ http, ncacn np y \_ a Windows 2000 y Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, desarrollo de un servidor de alto rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c52587410b10ae17f2ebd858863327aaf5ab1def92600259c8e49edc87946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021775"
---
# <a name="developing-a-high-performance-rpc-server"></a>Desarrollar un servidor RPC de alto rendimiento

La información de esta sección se aplica a las secuencias de protocolo remoto: [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)y a Windows 2000 y Windows XP.

En esta sección se abordan tres aspectos principales del rendimiento del servidor RPC:

-   [Rendimiento y latencia de red](network-latency-and-throughput.md)
-   [Escalabilidad](scalability.md)
-   [Varias opciones de rendimiento de RPC Sugerencias](miscellaneous-rpc-performance-tips.md)

La longitud de la ruta de acceso del código es otra consideración de rendimiento principal para RPC. La longitud de la ruta de acceso del código suele entenderse bien y, dado que la documentación y las herramientas están ampliamente disponibles en ese tema, este artículo no se aborda.

Una regla de rendimiento general importante y establecida que recordar al considerar el rendimiento de RPC es esta: buscar el cuello de botella en el sistema y trabajar para resolverlo. Es posible que el cuello de botella de acceso no sea la programación rpc y, si es así, el ajuste del rendimiento de RPC no dará como resultado un rendimiento mejorado hasta que se solucione ese cuello de botella. Por ejemplo, un sistema afectado por la contención de recursos no necesita hacer un uso más eficaz de la red.

Si el sistema se implementa en varios entornos, es una buena idea asegurarse de que todos sus aspectos estén bien optimizados, ya que los distintos entornos pueden producir cuellos de botella de rendimiento variados.

 

 