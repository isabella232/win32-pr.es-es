---
description: Trabajar con tipos de medios MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Trabajar con tipos de medios MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ead31c4291cf41cff62f4341227bf0ee1ad22d12e96a6c9eff87ff5a3e6faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886955"
---
# <a name="working-with-mft-media-types"></a>Trabajar con tipos de medios MFT

Un tipo de medio es una manera de describir el formato de una secuencia multimedia. En Media Foundation, los tipos de medios se representan mediante la **interfaz IMFMediaType.** Esta interfaz hereda la **interfaz DEATTRIBUTEAttributes.** Los detalles de un tipo de medio se especifican como atributos.

Para crear un nuevo tipo de medio, llame a **la función MFCreateMediaType.** Esta función devuelve un puntero a la **interfaz IMFMediaType.** El tipo de medio inicialmente no tiene atributos.

El SDK Media Foundation proporciona varias funciones auxiliares para inicializar tipos multimedia a partir de estructuras de formato. Por ejemplo, la función **MFInitMediaTypeFromVideoInfoHeader** inicializa un tipo de vídeo a partir de una estructura **VIDEOINFOHEADER,** y la función **MFInitMediaTypeFromWaveFormatEx** inicializa un tipo de vídeo a partir de una estructura **DETENTEATEX** o **UNATEXTENSIBLE.**

Los tipos de formato que usan los códecs suelen limitarse a los descritos por las estructuras **VIDEOINFOHEADER** **y MPEGATEX.**

Puede encontrar más información sobre cómo crear y Media Foundation tipos de medios en la documentación Media Foundation SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códecs MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



