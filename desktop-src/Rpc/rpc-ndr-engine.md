---
title: Motor de NDR de RPC (RPC)
description: El motor de representación de datos de red (NDR) de la llamada a procedimiento remoto (RPC) es el motor de serialización de los componentes RPC y DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bf7ba92a74d2d7dc8c394c561f65337db13af99
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078728"
---
# <a name="rpc-ndr-engine-rpc"></a>Motor de NDR de RPC (RPC)

El motor de representación de datos de red (NDR) de la llamada a procedimiento remoto (RPC) es el motor de serialización de los componentes RPC y DCOM. El motor NDR controla todos los problemas relacionados con el código auxiliar de una llamada remota. Como proceso, el cálculo de referencias de NDR está controlado por el código C de los códigos auxiliares generados por MIDL, un generador de tipos JIT de MIDL o por códigos auxiliares generados por otras herramientas o escritos manualmente. A su vez, el motor NDR impulsa el tiempo de ejecución subyacente (DCOM o RPC) que se comunica con transportes específicos.

Aunque los códigos auxiliares son código de C generado por MIDL, se recomienda que las aplicaciones traten los códigos auxiliares como opacos y se desaconseja encarecidamente que no modifiquen nada en el código auxiliar. El comportamiento es indefinido si se llama a estas rutinas de NDR fuera de contexto.

El motor de NDR de RPC se describe con más detalle en los temas siguientes:

-   [Sintaxis de transfer y NDR64](transfer-syntax-and-ndr64.md)
-   [Cadenas de formato NDR de RPC](rpc-ndr-format-strings.md)
-   [Referencia de la interfaz NDR de RPC](rpc-ndr-interface-reference.md)

 

 




