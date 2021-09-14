---
description: En este tema se muestra cómo puede agrupar métodos XAudio2 para que suenen efecto al mismo tiempo.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Cómo: agrupar métodos de audio como un conjunto de operaciones'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255968"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>Cómo: agrupar métodos de audio como un conjunto de operaciones

En este tema se muestra cómo puede agrupar métodos XAudio2 para que suenen efecto al mismo tiempo.

## <a name="to-group-audio-methods-as-an-operation-set"></a>Para agrupar métodos de audio como un conjunto de operaciones

1.  Declare un contador de conjunto de operaciones global.

    El [contador del conjunto](operation-sets.md) de operaciones garantiza que cada conjunto de operaciones sea único.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Incremente el contador global.

    Cada vez que envíe un nuevo conjunto [de operaciones,](operation-sets.md)el contador global debe incrementarse para asegurarse de que cada conjunto es único.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Agrupa las llamadas de método estableciendo sus [parámetros de conjunto de](operation-sets.md) operaciones.

4.  Establezca los [parámetros del conjunto de](operation-sets.md) operaciones en el valor actual del contador global.

    En este caso, cuatro llamadas a [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) se agrupan como un [conjunto de operaciones](operation-sets.md). La agrupación de las llamadas hace que los cuatro sonidos se inicien exactamente al mismo tiempo.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Inicie el [conjunto de operaciones](operation-sets.md).

    Después de llamar a todos los métodos del conjunto, inicie el conjunto llamando a [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el valor actual del contador global.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de operaciones](operation-sets.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Conjuntos de operaciones XAudio2](xaudio2-operation-sets.md)
</dt> </dl>

 

 
