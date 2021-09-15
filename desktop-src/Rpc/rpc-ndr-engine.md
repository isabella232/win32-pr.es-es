---
title: Motor RPC RPC (RPC)
description: El motor de representación de datos de red (COMPOSICIÓN) de llamada a procedimiento remoto (RPC) es el motor de serialización de los componentes RPC y DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bf7ba92a74d2d7dc8c394c561f65337db13af99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473589"
---
# <a name="rpc-ndr-engine-rpc"></a>Motor RPC RPC (RPC)

El motor de representación de datos de red (COMPOSICIÓN) de llamada a procedimiento remoto (RPC) es el motor de serialización de los componentes RPC y DCOM. El motor STUB controla todos los problemas relacionados con el código auxiliar de una llamada remota. Como proceso, la serialización de JJ está controlada por el código C de códigos auxiliares generados por MIDL, un generador de tipo JIT de MIDL o por códigos auxiliares generados por otras herramientas o escritos manualmente. A su vez, el motor COMPOSICIÓN impulsa el tiempo de ejecución subyacente (DCOM o RPC) que se comunica con transportes específicos.

Aunque los códigos auxiliares son código C generado por MIDL, se recomienda que las aplicaciones traten los códigos auxiliares como opacos y no se recomienda modificar nada dentro del código auxiliar. El comportamiento es indefinido si estas rutinas BAND se llaman fuera de contexto.

El motor RPC RPC se describe con más detalle en los temas siguientes:

-   [Sintaxis de transferencia y QL64](transfer-syntax-and-ndr64.md)
-   [Cadenas de formato RPC RPC](rpc-ndr-format-strings.md)
-   [Referencia de la interfaz RPC RPC](rpc-ndr-interface-reference.md)

 

 




