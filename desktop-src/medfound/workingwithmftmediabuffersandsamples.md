---
description: Trabajar con ejemplos y búferes multimedia de MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Trabajar con ejemplos y búferes multimedia de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964f1c2f2a5fd5f92d5af87213c6977fc51bee76caf3a281861788e2a2fb922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736456"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Trabajar con ejemplos y búferes multimedia de MFT

Los códecs MFT pasan datos multimedia de un lado a otro mediante el uso de ejemplos y búferes multimedia.

Un búfer multimedia es un objeto COM que administra un bloque de memoria, normalmente para contener datos multimedia. Cuando los datos se pasan a o desde un MFT, siempre se pasan en forma de búfer multimedia.

Todos los búferes multimedia exponen la **interfaz IMFMediaBuffer.** Esta interfaz está diseñada para cualquier tipo de datos. Los búferes que contienen datos de vídeo a menudo también **exponen LAN2DBuffer.**

Un búfer multimedia tiene un tamaño máximo, que es la cantidad de memoria asignada para el búfer. Para buscar el tamaño máximo, llame **a IMFMediaBuffer::GetMaxLength**. En cualquier momento, un búfer multimedia también tiene una longitud actual, que es la cantidad de datos válidos en el búfer, que van desde cero bytes hasta el tamaño máximo. Para obtener la longitud actual, llame **a IMFMediaBuffer::GetCurrentLength**. Cuando se crea el búfer, la longitud actual es cero. Si escribe datos en el búfer, llame a **IMFMediaBuffer::SetCurrentLength** para actualizar la longitud actual.

Para acceder a la memoria del búfer, llame **a IMFMediaBuffer::Lock**. Este método devuelve un puntero al inicio del bloque de memoria. Cuando haya terminado de usar el puntero, llame **a IMFMediaBuffer::Unlock**. El **método Lock** no es un mecanismo de sincronización de subprocesos; no garantiza que otros subprocesos no puedan acceder al búfer. El **método Lock** se usa para garantizar que la memoria a la que se accede seguirá siendo válida hasta que llame al método **Unlock.**

Un objeto de ejemplo multimedia (en el contexto del SDK de Media Foundation) es un objeto que contiene una lista ordenada de cero o más búferes. Los ejemplos multimedia exponen la **interfaz DESEJEMPLO.**

Para crear un ejemplo, llame a **la función MFCreateSample.** Inicialmente, la lista de búferes del ejemplo está vacía. Para agregar un búfer al final de la lista, llame **a IMFSample::AddBuffer**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> <dt>

[Trabajar con códecs MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



