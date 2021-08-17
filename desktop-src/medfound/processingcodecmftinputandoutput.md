---
description: Procesamiento de entrada y salida de MFT de códec
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Procesamiento de entrada y salida de MFT de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cbec9b92ae11d8f1f3722f2cb2540a5b5b01bb5d680e448d298a36ec682ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101844"
---
# <a name="processing-codec-mft-input-and-output"></a>Procesamiento de entrada y salida de MFT de códec

Cuando haya configurado el tipo de entrada y el tipo de salida para un MFT, puede empezar a procesar ejemplos de datos. Se pasan ejemplos al MFT para su procesamiento mediante el método [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y, a continuación, se recupera el ejemplo procesado mediante una llamada a [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Debe establecer marcas de tiempo y duraciones precisas para todas las muestras de entrada pasadas. Las marcas de tiempo no son estrictamente necesarias, pero ayudan a mantener la sincronización de audio y vídeo. Si no tiene las marcas de tiempo de los ejemplos, es mejor dejarlos fuera que usar valores no seguros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códecs MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



