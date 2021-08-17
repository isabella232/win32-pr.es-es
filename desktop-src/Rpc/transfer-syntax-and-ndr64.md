---
title: Sintaxis de transferencia y QL64
description: El protocolo de conexión LDA, también conocido como sintaxis de transferencia, permite que las llamadas RPC atraviese la red.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433e68689ec4c960adbb43ddc19ec3e9e37765db57cfe6bf87c86c096720b771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011233"
---
# <a name="transfer-syntax-and-ndr64"></a>Sintaxis de transferencia y QL64

El protocolo de conexión LDA, también conocido como sintaxis de transferencia, permite que las llamadas RPC atraviese la red. El protocolo de conexión define la representación de conexión de una llamada RPC, como el orden en que se serializan los miembros de datos, la alineación de los datos en la conexión, la información adicional incluida con los datos y otros problemas. El protocolo UNIX64 es una extensión de la sintaxis de transferencia de QL basada en 32 bits, creada específicamente para permitir que los desarrolladores que tienen como destino sistemas de 64 bits consigan un rendimiento optimizado.

Las diferencias entre el formato de conexión de MOUSE y el formato de conexión MOUSE64 abordan el diferente tamaño de los punteros en un entorno de 64 bits, así como otros problemas. Rpc controla la mecánica de RPC. Los desarrolladores solo necesitan usar [**el**](/windows/desktop/Midl/-protocol)modificador de línea de comandos **/all** MIDL para obtener las ventajas de UNIX64 en plataformas de 64 bits. UNIX64 solo está disponible en plataformas de 64 bits.

 

 