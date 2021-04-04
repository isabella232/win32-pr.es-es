---
description: Puede cambiar los gráficos de audio en cualquier momento para agregar o quitar voces o subgráficos completos.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Cómo: agregar o quitar voces de un gráfico de audio dinámicamente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154613"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="d73fa-103">Cómo: agregar o quitar voces de un gráfico de audio dinámicamente</span><span class="sxs-lookup"><span data-stu-id="d73fa-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="d73fa-104">Puede cambiar los gráficos de audio en cualquier momento para agregar o quitar voces o subgráficos completos.</span><span class="sxs-lookup"><span data-stu-id="d73fa-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="d73fa-105">En este tema se muestra cómo agregar o quitar voces de submezcla de un grafo creado siguiendo los pasos descritos en [Cómo: compilar un gráfico básico de procesamiento de audio](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="d73fa-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="d73fa-106">Una sola voz puede enviar su salida a varias voces o a una cadena larga de voces.</span><span class="sxs-lookup"><span data-stu-id="d73fa-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="d73fa-107">Quitar o agregar una sola voz puede tener un gran efecto en un gráfico de audio.</span><span class="sxs-lookup"><span data-stu-id="d73fa-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="d73fa-108">Para cambiar dinámicamente un gráfico de audio</span><span class="sxs-lookup"><span data-stu-id="d73fa-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="d73fa-109">Agregar y quitar voces de un gráfico de audio es muy similar a agregar o quitar nodos de un gráfico o una lista de un solo vínculo.</span><span class="sxs-lookup"><span data-stu-id="d73fa-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="d73fa-110">Para agregar una voz o un subgráfico a un gráfico de audio</span><span class="sxs-lookup"><span data-stu-id="d73fa-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="d73fa-111">Establezca el resultado de una voz en el gráfico, la voz primaria, en la voz que se va a agregar con la función [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) .</span><span class="sxs-lookup"><span data-stu-id="d73fa-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="d73fa-112">Establezca el resultado de la nueva voz en el elemento secundario original de la voz primaria.</span><span class="sxs-lookup"><span data-stu-id="d73fa-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="d73fa-113">Para quitar una voz o un subgráfico de un gráfico de audio</span><span class="sxs-lookup"><span data-stu-id="d73fa-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="d73fa-114">Establezca la voz de salida del elemento primario de la voz que se va a quitar en el elemento secundario de la voz que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d73fa-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="d73fa-115">Si la voz que se va a quitar está al final del gráfico, la voz primaria debe cambiarse para que apunte a la voz maestra.</span><span class="sxs-lookup"><span data-stu-id="d73fa-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="d73fa-116">Tenga en cuenta que, para mayor claridad, cada elemento primario solo tiene un elemento secundario en estos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="d73fa-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="d73fa-117">Si un nodo primario tiene varios elementos secundarios, su sendlist contendrá una matriz de voces en lugar de un puntero a una sola voz.</span><span class="sxs-lookup"><span data-stu-id="d73fa-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d73fa-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d73fa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d73fa-119">Gráficos de audio</span><span class="sxs-lookup"><span data-stu-id="d73fa-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="d73fa-120">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="d73fa-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="d73fa-121">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="d73fa-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="d73fa-122">Cómo: usar voces de submezcla</span><span class="sxs-lookup"><span data-stu-id="d73fa-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="d73fa-123">Cómo: crear un efecto en cadena</span><span class="sxs-lookup"><span data-stu-id="d73fa-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
