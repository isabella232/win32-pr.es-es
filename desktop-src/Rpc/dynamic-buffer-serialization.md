---
title: Serialización de búfer dinámico
description: Cuando se usa el estilo de búfer dinámico de serialización, el código auxiliar asigna el búfer de serialización, y los datos se codifican en este búfer y se devuelven al usuario. Al calcular las referencias, se proporciona el búfer que contiene los datos.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486791"
---
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="c0f52-104">Serialización de búfer dinámico</span><span class="sxs-lookup"><span data-stu-id="c0f52-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="c0f52-105">Cuando se usa el estilo de búfer dinámico de serialización, el código auxiliar asigna el búfer de serialización, y los datos se codifican en este búfer y se devuelven al usuario.</span><span class="sxs-lookup"><span data-stu-id="c0f52-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="c0f52-106">Al calcular las referencias, se proporciona el búfer que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="c0f52-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="c0f52-107">El estilo de búfer dinámico de serialización utiliza las siguientes rutinas:</span><span class="sxs-lookup"><span data-stu-id="c0f52-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="c0f52-108">**MesEncodeDynBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="c0f52-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="c0f52-109">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="c0f52-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="c0f52-110">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="c0f52-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="c0f52-111">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="c0f52-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="c0f52-112">La función [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) asigna la memoria necesaria para el controlador de codificación y, a continuación, la inicializa.</span><span class="sxs-lookup"><span data-stu-id="c0f52-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="c0f52-113">La aplicación puede llamar a [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar el identificador.</span><span class="sxs-lookup"><span data-stu-id="c0f52-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="c0f52-114">Llama a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar la memoria del controlador.</span><span class="sxs-lookup"><span data-stu-id="c0f52-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="c0f52-115">Para crear un identificador de descodificación que se corresponda con el controlador de codificación dinámica de búfer, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="c0f52-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




