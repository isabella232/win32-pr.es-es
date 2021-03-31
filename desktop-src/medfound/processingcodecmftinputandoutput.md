---
description: Procesamiento de entrada y salida de MFT de códecs
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Procesamiento de entrada y salida de MFT de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275823"
---
# <a name="processing-codec-mft-input-and-output"></a>Procesamiento de entrada y salida de MFT de códecs

Cuando haya configurado el tipo de entrada y el tipo de salida de una MFT, puede empezar a procesar las muestras de datos. Pase ejemplos a la MFT para su procesamiento mediante el método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y, a continuación, recupere el ejemplo procesado llamando a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Debe establecer las marcas de tiempo y duraciones precisas para todos los ejemplos de entrada pasados. Las marcas de tiempo no son estrictamente necesarias pero ayudan a mantener la sincronización de audio y vídeo. Si no dispone de las marcas de tiempo para los ejemplos, es mejor dejarlas de usar valores inciertos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



