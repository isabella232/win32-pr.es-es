---
title: Desarrollo de un servidor RPC de alto rendimiento
description: La información de esta sección se aplica a las secuencias de protocolo remoto ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np y a Windows 2000 y Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, desarrollar un servidor de alto rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488158"
---
# <a name="developing-a-high-performance-rpc-server"></a>Desarrollo de un servidor RPC de alto rendimiento

La información de esta sección se aplica a las secuencias de protocolo remoto: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**NCACN \_ NP**](/windows/desktop/Midl/ncacn-np)y a Windows 2000 y Windows XP.

En esta sección se tratan tres aspectos principales del rendimiento del servidor RPC:

-   [Latencia y rendimiento de la red](network-latency-and-throughput.md)
-   [Escalabilidad](scalability.md)
-   [Sugerencias de rendimiento de RPC varias](miscellaneous-rpc-performance-tips.md)

La longitud de la ruta de acceso del código es otra consideración de rendimiento principal de RPC. La longitud de la ruta de acceso del código es generalmente entendida y, como la bibliografía y las herramientas están ampliamente disponibles en ese tema, en este artículo no se aborda.

Una regla de rendimiento general importante y establecida que se debe recordar al considerar el rendimiento de RPC es la siguiente: encontrar el cuello de botella en el sistema y trabajar para resolverlo. Es posible que el cuello de botella de la puerta no sea la programación RPC y, en ese caso, el ajuste del rendimiento en RPC no dará lugar a un rendimiento mejorado hasta que se solucione el cuello de botella. Por ejemplo, un sistema plagado por la contención de recursos no necesita hacer un uso más eficaz de la red.

Si el sistema está implementado en varios entornos, es una buena idea asegurarse de que todos los aspectos del mismo estén bien optimizados, ya que los distintos entornos pueden producir cuellos de botella de rendimiento diversos.

 

 