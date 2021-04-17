---
description: Métodos de devolución de llamada asincrónica
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Métodos de devolución de llamada asincrónica
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705429"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="ff29f-103">Métodos de devolución de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="ff29f-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="ff29f-104">Media Foundation proporciona una manera coherente de implementar métodos asincrónicos, mediante una interfaz de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ff29f-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="ff29f-105">En esta sección se describe cómo implementar la interfaz de devolución de llamada y cómo escribir métodos asincrónicos que usan esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="ff29f-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="ff29f-106">Contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff29f-106">It contains the following topics.</span></span>



| <span data-ttu-id="ff29f-107">Tema</span><span class="sxs-lookup"><span data-stu-id="ff29f-107">Topic</span></span>                                                                                | <span data-ttu-id="ff29f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff29f-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff29f-109">Llamar a métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="ff29f-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="ff29f-110">Cómo llamar a métodos asincrónicos en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ff29f-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="ff29f-111">Implementar la devolución de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="ff29f-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="ff29f-112">Cómo implementar el método de devolución de llamada en la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="ff29f-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="ff29f-113">Admitir varias devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="ff29f-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="ff29f-114">Cómo admitir varias devoluciones de llamada dentro de la misma clase de C++.</span><span class="sxs-lookup"><span data-stu-id="ff29f-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="ff29f-115">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="ff29f-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="ff29f-116">Las colas de trabajo proporcionan una manera eficaz de realizar operaciones asincrónicas en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="ff29f-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="ff29f-117">Escribir un método asincrónico</span><span class="sxs-lookup"><span data-stu-id="ff29f-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="ff29f-118">Cómo implementar métodos asincrónicos en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ff29f-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="ff29f-119">Objetos de resultado asincrónicos personalizados</span><span class="sxs-lookup"><span data-stu-id="ff29f-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="ff29f-120">Cómo proporcionar una implementación personalizada de la interfaz [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="ff29f-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="ff29f-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff29f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff29f-122">**Interfaz IMFAsyncCallback**</span><span class="sxs-lookup"><span data-stu-id="ff29f-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="ff29f-123">**Interfaz IMFAsyncResult**</span><span class="sxs-lookup"><span data-stu-id="ff29f-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="ff29f-124">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="ff29f-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



