---
title: Elegir una secuencia de protocolo
description: Los procedimientos recomendados para elegir una secuencia de protocolo implican el uso de ncacn ip tcp y \_ \_ ncalrpc, no ncacn \_ np, ncacn \_ spx y ncadg \_ \ .
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932228"
---
# <a name="choosing-a-protocol-sequence"></a>Elegir una secuencia de protocolo

**Procedimiento recomendado:** Use [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) al realizar una llamada remota. Use [**ncalrpc para**](/windows/desktop/Midl/ncalrpc) las llamadas locales. No use [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ spx**](/windows/desktop/Midl/ncacn-spx)ni ninguna de las secuencias de protocolo **ncadg; \_ \*** son menos eficaces y tienen funcionalidades inferiores.

 

 