---
description: Trabajar con ejemplos y búferes de medios de MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Trabajar con ejemplos y búferes de medios de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361866"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Trabajar con ejemplos y búferes de medios de MFT

Los MFTs de códec pasan datos multimedia hacia atrás y hacia delante mediante los búferes multimedia y ejemplos.

Un búfer multimedia es un objeto COM que administra un bloque de memoria, normalmente para contener datos multimedia. Cuando los datos se pasan a o desde una MFT, siempre se pasan en forma de un búfer multimedia.

Todos los búferes multimedia exponen la interfaz **IMFMediaBuffer** . Esta interfaz está diseñada para cualquier tipo de datos. Los búferes que contienen datos de vídeo a menudo también exponen **IMF2DBuffer**.

Un búfer multimedia tiene un tamaño máximo, que es la cantidad de memoria asignada para el búfer. Para encontrar el tamaño máximo, llame a **IMFMediaBuffer:: GetMaxLength**. En cualquier momento, un búfer multimedia también tiene una longitud actual, que es la cantidad de datos válidos en el búfer, que van desde cero bytes hasta el tamaño máximo. Para obtener la longitud actual, llame a **IMFMediaBuffer:: GetCurrentLength**. Cuando se crea el búfer, la longitud actual es cero. Si escribe datos en el búfer, llame a **IMFMediaBuffer:: SetCurrentLength** para actualizar la longitud actual.

Para tener acceso a la memoria del búfer, llame a **IMFMediaBuffer:: Lock**. Este método devuelve un puntero al principio del bloque de memoria. Cuando haya terminado de usar el puntero, llame a **IMFMediaBuffer:: Unlock**. El método **Lock** no es un mecanismo de sincronización de subprocesos; no garantiza que otros subprocesos no puedan tener acceso al búfer. El método **Lock** se usa para garantizar que la memoria a la que se obtiene acceso permanecerá válida hasta que se llame al método **Unlock** .

Un objeto de ejemplo multimedia (en el contexto del SDK de Media Foundation) es un objeto que contiene una lista ordenada de cero o más búferes. Los ejemplos de medios exponen la interfaz **IMFSample** .

Para crear un nuevo ejemplo, llame a la función **MFCreateSample** . Inicialmente, la lista de búferes del ejemplo está vacía. Para agregar un búfer al final de la lista, llame a **IMFSample:: AddBuffer**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> <dt>

[Trabajar con códec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



