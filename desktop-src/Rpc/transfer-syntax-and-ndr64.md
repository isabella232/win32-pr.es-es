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
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="d5485-103">Sintaxis de transfer y NDR64</span><span class="sxs-lookup"><span data-stu-id="d5485-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="d5485-104">El protocolo de conexión NDR, también conocido como sintaxis de transferencia, habilita las llamadas RPC para atravesar la red.</span><span class="sxs-lookup"><span data-stu-id="d5485-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="d5485-105">El protocolo de conexión define la representación de conexión de una llamada RPC, como el orden en el que se serializan los miembros de datos, la alineación de los datos en la conexión, la información adicional incluida con los datos y otros problemas.</span><span class="sxs-lookup"><span data-stu-id="d5485-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="d5485-106">El protocolo NDR64 es una extensión de la sintaxis de transferencia de NDR basada en 32 bits, creada específicamente para permitir que los desarrolladores que tienen como destino sistemas de 64 bits logren un rendimiento optimizado.</span><span class="sxs-lookup"><span data-stu-id="d5485-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="d5485-107">Las diferencias entre el formato de conexión de NDR y el formato de NDR64 se dirigen al tamaño diferente de los punteros en un entorno de 64 bits, así como a otros problemas.</span><span class="sxs-lookup"><span data-stu-id="d5485-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="d5485-108">La mecánica de NDR64 se controla mediante RPC.</span><span class="sxs-lookup"><span data-stu-id="d5485-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="d5485-109">Los desarrolladores solo necesitan usar el modificador de línea de comandos/[**Protocol**](/windows/desktop/Midl/-protocol)**All** MIDL para obtener las ventajas de NDR64 en plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d5485-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="d5485-110">NDR64 solo está disponible en plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d5485-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 