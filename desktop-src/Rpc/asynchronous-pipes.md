---
title: Canalizaciones asincrónicas
description: El uso de parámetros de canalización con RPC asincrónico le permite transmitir datos de forma incremental, a medida que estén disponibles, sin necesidad de utilizar el cliente y el servidor.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793222"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="f3494-103">Canalizaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="f3494-103">Asynchronous Pipes</span></span>

<span data-ttu-id="f3494-104">El uso de parámetros de [canalización](/windows/desktop/Midl/pipe) con RPC asincrónico le permite transmitir datos de forma incremental, a medida que estén disponibles, sin necesidad de utilizar el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="f3494-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="f3494-105">Esto es especialmente útil cuando se tiene una gran cantidad de datos para transferir, combinados con un cliente lento, un servidor lento o una red lenta.</span><span class="sxs-lookup"><span data-stu-id="f3494-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="f3494-106">Si utiliza una canalización en una llamada de función asincrónica, es, por definición, una canalización asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f3494-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="f3494-107">Las canalizaciones sincrónicas no se admiten junto con las funciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="f3494-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="f3494-108">A diferencia de las canalizaciones convencionales (sincrónicas) en las que el servidor controla todos los detalles de envío y recepción de datos de canalización, las canalizaciones asincrónicas son simétricas.</span><span class="sxs-lookup"><span data-stu-id="f3494-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="f3494-109">Es decir, tanto el cliente como el servidor pueden insertar y extraer datos a través de la canalización.</span><span class="sxs-lookup"><span data-stu-id="f3494-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="f3494-110">Los parámetros de canalización solo se pueden pasar por referencia.</span><span class="sxs-lookup"><span data-stu-id="f3494-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="f3494-111">Incluso si el archivo IDL muestra parámetros de [canalización](/windows/desktop/Midl/pipe) que se pasan por valor, el código auxiliar generado aceptará parámetros de canalización solo por referencia.</span><span class="sxs-lookup"><span data-stu-id="f3494-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="f3494-112">En la siguiente explicación de las canalizaciones asincrónicas, se supone que está familiarizado con el constructor de tipo de canalización.</span><span class="sxs-lookup"><span data-stu-id="f3494-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="f3494-113">Para obtener más información sobre los procedimientos de canalización descritos en estos temas, vea [canalizaciones](pipes.md).</span><span class="sxs-lookup"><span data-stu-id="f3494-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 