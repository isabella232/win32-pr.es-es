---
description: Trabajar con tipos de medios de MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Trabajar con tipos de medios de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279784"
---
# <a name="working-with-mft-media-types"></a>Trabajar con tipos de medios de MFT

Un tipo de medio es una manera de describir el formato de un flujo multimedia. En Media Foundation, los tipos de medios se representan mediante la interfaz **IMFMediaType** . Esta interfaz hereda la interfaz **IMFAttributes** . Los detalles de un tipo de medio se especifican como atributos.

Para crear un nuevo tipo de archivo multimedia, llame a la función **MFCreateMediaType** . Esta función devuelve un puntero a la interfaz **IMFMediaType** . El tipo de medio no tiene inicialmente ningún atributo.

El SDK de Media Foundation proporciona varias funciones auxiliares para inicializar los tipos de medios desde las estructuras de formato. Por ejemplo, la función **MFInitMediaTypeFromVideoInfoHeader** Inicializa un tipo de vídeo a partir de una estructura **VIDEOINFOHEADER** , y la función **MFInitMediaTypeFromWaveFormatEx** Inicializa un tipo de vídeo a partir de una estructura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** .

Los tipos de formato que usan los códecs generalmente se limitan a los descritos por las estructuras **VIDEOINFOHEADER** y **WAVEFORMATEX** .

Puede encontrar más información sobre cómo crear y obtener acceso a los tipos de medios Media Foundation en la documentación del SDK de Media Foundation.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



