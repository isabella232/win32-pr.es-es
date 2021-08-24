---
description: Puede cambiar los gráficos de audio en cualquier momento para agregar o quitar voces o subgráficos completos.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Cómo: agregar o quitar voces de un gráfico de audio dinámicamente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a49cfc88e89884b63484b7bd58f7f5d96020cd21f8d1147794b840f00258fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082939"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>Cómo: agregar o quitar voces de un gráfico de audio dinámicamente

Puede cambiar los gráficos de audio en cualquier momento para agregar o quitar voces o subgráficos completos. En este tema se muestra cómo agregar o quitar voces de submezcla de un gráfico que se ha creado siguiendo los pasos descritos en [Cómo:](how-to--build-a-basic-audio-processing-graph.md)Compilar un procesamiento de audio básico Graph . Una sola voz puede enviar su salida a varias voces o a una cadena larga de voces. Quitar o agregar una sola voz puede tener un gran efecto en un gráfico de audio.

## <a name="to-dynamically-change-an-audio-graph"></a>Para cambiar dinámicamente un gráfico de audio

Agregar y quitar voces de un gráfico de audio es muy similar a agregar o quitar nodos de una lista o gráfico vinculado único.

-   Para agregar una voz o un subgráfico a un gráfico de audio

    Establezca la salida de una voz en el gráfico, la voz primaria, en la voz que se va a agregar mediante la [**función SetOutputVoices.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) Establezca la salida de la nueva voz en el elemento secundario original de la voz primaria.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   Para quitar una voz o un subgráfico de un gráfico de audio

    Establezca la voz de salida del elemento primario de la voz que se va a quitar en el elemento secundario de la voz que se va a quitar. Si la voz que se quita está al final del gráfico, la voz primaria debe cambiarse para que apunte a la voz maestra.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Tenga en cuenta que, para mayor claridad, cada elemento primario solo tiene un elemento secundario en estos ejemplos. Si un nodo primario tiene varios elementos secundarios, su lista de envío contendrá una matriz de voces en lugar de un puntero a una sola voz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de audio](audio-graphs.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Cómo: usar voces de submezcla](how-to--use-submix-voices.md)
</dt> <dt>

[Cómo: crear un efecto en cadena](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
