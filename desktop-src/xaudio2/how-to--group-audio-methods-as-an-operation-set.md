---
description: En este tema se muestra cómo agrupar los métodos de XAudio2 para que se apliquen al mismo tiempo.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Cómo: agrupar métodos de audio como un conjunto de operaciones'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911102"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="6d056-103">Cómo: agrupar métodos de audio como un conjunto de operaciones</span><span class="sxs-lookup"><span data-stu-id="6d056-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="6d056-104">En este tema se muestra cómo agrupar los métodos de XAudio2 para que se apliquen al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6d056-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="6d056-105">Para agrupar métodos de audio como un conjunto de operaciones</span><span class="sxs-lookup"><span data-stu-id="6d056-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="6d056-106">Declare un contador de conjunto de operaciones global.</span><span class="sxs-lookup"><span data-stu-id="6d056-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="6d056-107">El contador [conjunto de operaciones](operation-sets.md) garantiza que cada conjunto de operaciones sea único.</span><span class="sxs-lookup"><span data-stu-id="6d056-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="6d056-108">Incremente el contador global.</span><span class="sxs-lookup"><span data-stu-id="6d056-108">Increment the global counter.</span></span>

    <span data-ttu-id="6d056-109">Cada vez que envía un [conjunto de operaciones](operation-sets.md)nuevo, el contador global debe incrementarse para asegurarse de que cada conjunto sea único.</span><span class="sxs-lookup"><span data-stu-id="6d056-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="6d056-110">Agrupe las llamadas de método estableciendo los parámetros del [conjunto de operaciones](operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="6d056-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="6d056-111">Establezca los parámetros del [conjunto de operaciones](operation-sets.md) en el valor actual del contador global.</span><span class="sxs-lookup"><span data-stu-id="6d056-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="6d056-112">En este caso, se agrupan cuatro llamadas a [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) como un [conjunto de operaciones](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="6d056-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="6d056-113">Al agrupar las llamadas, los cuatro sonidos se inician exactamente al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6d056-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="6d056-114">Inicie el [conjunto de operaciones](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="6d056-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="6d056-115">Después de llamar a todos los métodos del conjunto, inicie el conjunto mediante una llamada a [**IXAudio2:: commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el valor actual del contador global.</span><span class="sxs-lookup"><span data-stu-id="6d056-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="6d056-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d056-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d056-117">Conjuntos de operaciones</span><span class="sxs-lookup"><span data-stu-id="6d056-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="6d056-118">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="6d056-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6d056-119">Conjuntos de operaciones de XAudio2</span><span class="sxs-lookup"><span data-stu-id="6d056-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
