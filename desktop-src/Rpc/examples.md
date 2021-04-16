---
title: Ejemplos (RPC)
description: Ejemplos que muestran los conceptos de llamada a procedimiento remoto (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC (llamada a procedimiento remoto), ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676527"
---
# <a name="examples-rpc"></a><span data-ttu-id="ce896-104">Ejemplos (RPC)</span><span class="sxs-lookup"><span data-stu-id="ce896-104">Examples (RPC)</span></span>

<span data-ttu-id="ce896-105">El kit de desarrollo de software (SDK) de la plataforma incluye ejemplos que muestran una variedad de conceptos de llamada a procedimiento remoto (RPC), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ce896-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="ce896-106">ASYNCRPC muestra la estructura de una aplicación RPC que usa llamadas a procedimientos remotos asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="ce896-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="ce896-107">También muestra varios métodos de notificación de la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ce896-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="ce896-108">CLUUID muestra el uso del UUID de objeto de cliente para permitir que un cliente seleccione entre varias implementaciones de un procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="ce896-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="ce896-109">El directorio de datos contiene cuatro programas: DUNION ilustra uniones discriminadas (no encapsuladas); Inout muestra los parámetros [ \[ in \] ](../midl/in.md), [ \[ out \] ](../midl/out-idl.md) ; REPAS muestra el atributo [representated \_ as](/windows/desktop/Midl/represent-as) ; TRANSMISIÓN muestra el atributo [transmitir \_ como](/windows/desktop/Midl/transmit-as) .</span><span class="sxs-lookup"><span data-stu-id="ce896-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="ce896-110">DYNEPT muestra una aplicación cliente que administra su conexión con el servidor a través de extremos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="ce896-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="ce896-111">El directorio FILEREP contiene cuatro ejemplos que muestran cómo los desarrolladores pueden escribir un servicio simple de replicación de archivos, un servicio de replicación de archivos de varios usuarios, un servicio que admite características de seguridad y un servicio que usa canalizaciones asincrónicas de RPC.</span><span class="sxs-lookup"><span data-stu-id="ce896-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="ce896-112">El directorio HANDles contiene tres programas, AUTO, CXHNDL, USRDEF, que muestran el [ \_ identificador automático](/windows/desktop/Midl/auto-handle), el \[ identificador de contexto \_ y los \] identificadores genéricos (definidos por el usuario), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ce896-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="ce896-113">HELLO es una implementación de cliente/servidor de "Hello, World".</span><span class="sxs-lookup"><span data-stu-id="ce896-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="ce896-114">El directorio PICKLE contiene dos programas: PICKLP muestra la serialización del procedimiento de datos; La lista desplegable muestra la serialización del tipo de datos; ambos programas usan los atributos de [ \[ codificación \] ](../midl/encode.md) y [ \[ descodificación \] ](../midl/decode.md) .</span><span class="sxs-lookup"><span data-stu-id="ce896-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="ce896-115">CANALIZAciones muestra el uso del constructor de tipo de canalización.</span><span class="sxs-lookup"><span data-stu-id="ce896-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="ce896-116">RPCSVC muestra la implementación de un servicio con RPC.</span><span class="sxs-lookup"><span data-stu-id="ce896-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="ce896-117">STROUT muestra cómo asignar memoria en un servidor para un objeto bidimensional (una matriz de punteros) y devolverla al cliente como un \[ \] parámetro de solo salida.</span><span class="sxs-lookup"><span data-stu-id="ce896-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="ce896-118">Después, el cliente libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="ce896-118">The client then frees the memory.</span></span> <span data-ttu-id="ce896-119">Esta técnica permite al código auxiliar llamar al servidor sin conocer de antemano la cantidad de datos que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="ce896-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="ce896-120">Este programa también permite al usuario compilar para Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce896-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="ce896-121">Todos los archivos de código fuente y los archivos make de estos programas se encuentran en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="ce896-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="ce896-122">Para obtener ejemplos básicos de desarrollo de aplicaciones RPC y más sencillos, consulte los temas del [tutorial](tutorial.md) .</span><span class="sxs-lookup"><span data-stu-id="ce896-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
