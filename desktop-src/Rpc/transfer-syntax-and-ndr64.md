---
title: Sintaxis de transfer y NDR64
description: El protocolo de conexión NDR, también conocido como sintaxis de transferencia, habilita las llamadas RPC para atravesar la red.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077789"
---
# <a name="transfer-syntax-and-ndr64"></a>Sintaxis de transfer y NDR64

El protocolo de conexión NDR, también conocido como sintaxis de transferencia, habilita las llamadas RPC para atravesar la red. El protocolo de conexión define la representación de conexión de una llamada RPC, como el orden en el que se serializan los miembros de datos, la alineación de los datos en la conexión, la información adicional incluida con los datos y otros problemas. El protocolo NDR64 es una extensión de la sintaxis de transferencia de NDR basada en 32 bits, creada específicamente para permitir que los desarrolladores que tienen como destino sistemas de 64 bits logren un rendimiento optimizado.

Las diferencias entre el formato de conexión de NDR y el formato de NDR64 se dirigen al tamaño diferente de los punteros en un entorno de 64 bits, así como a otros problemas. La mecánica de NDR64 se controla mediante RPC. Los desarrolladores solo necesitan usar el modificador de línea de comandos/[**Protocol**](/windows/desktop/Midl/-protocol)**All** MIDL para obtener las ventajas de NDR64 en plataformas de 64 bits. NDR64 solo está disponible en plataformas de 64 bits.

 

 