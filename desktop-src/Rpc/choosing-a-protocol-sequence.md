---
title: Elección de una secuencia de protocolo
description: Los procedimientos recomendados para elegir una secuencia de protocolos implican el uso de ncacn \_ IP \_ TCP y ncalrpc, no ncacn \_ NP, ncacn \_ SPX y ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078285"
---
# <a name="choosing-a-protocol-sequence"></a>Elección de una secuencia de protocolo

**Procedimiento recomendado:** Use [**\_ \_ TCP IP de ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) al efectuar una llamada remota. Use [**ncalrpc**](/windows/desktop/Midl/ncalrpc) para llamadas locales. No use [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)ni ninguna de las secuencias de protocolo **ncadg \_ \*** ; son menos eficientes y tienen funcionalidades inferiores.

 

 