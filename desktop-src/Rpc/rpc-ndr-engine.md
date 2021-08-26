---
title: Motor RPC RPC (RPC)
description: El motor de representación de datos de red (COMPOSICIÓN) de llamada a procedimiento remoto (RPC) es el motor de serialización de los componentes RPC y DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0dd01ae40562528ac89c8b9dcfb0b9009ead5ca1a92b2cde90c3274d574fc1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018425"
---
# <a name="rpc-ndr-engine-rpc"></a>Motor RPC RPC (RPC)

El motor de representación de datos de red (COMPOSICIÓN) de llamada a procedimiento remoto (RPC) es el motor de serialización de los componentes RPC y DCOM. El motor STUB controla todos los problemas relacionados con el código auxiliar de una llamada remota. Como proceso, la serialización de JJ está controlada por el código C de códigos auxiliares generados por MIDL, un generador de tipo JIT de MIDL o por códigos auxiliares generados por otras herramientas o escritos manualmente. A su vez, el motor TIME impulsa el tiempo de ejecución subyacente (DCOM o RPC) que se comunica con transportes específicos.

Aunque los códigos auxiliares son código C generado por MIDL, se recomienda que las aplicaciones traten los códigos auxiliares como opacos y no se recomienda modificar nada dentro del código auxiliar. El comportamiento es indefinido si estas rutinas de BAND se llaman fuera de contexto.

El motor RPC RPC se describe con más detalle en los temas siguientes:

-   [Sintaxis de transferencia y QL64](transfer-syntax-and-ndr64.md)
-   [Cadenas de formato RPC RPC](rpc-ndr-format-strings.md)
-   [Referencia de la interfaz RPC RPC](rpc-ndr-interface-reference.md)

 

 




