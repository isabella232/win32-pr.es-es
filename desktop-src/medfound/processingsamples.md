---
description: Procesamiento de entradas y salidas de códecs DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Procesamiento de entradas y salidas de códecs DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360481"
---
# <a name="processing-codec-dmo-input-and-output"></a>Procesamiento de entradas y salidas de códecs DMO

Cuando haya configurado el tipo de entrada y de salida para un DMO, puede empezar a procesar los ejemplos de datos. Pase ejemplos a DMO para su procesamiento mediante el método **IMediaObject::P rocessinput** y, a continuación, recupere el ejemplo procesado llamando a **IMediaObject::P rocessoutput**. Debe establecer las marcas de tiempo y duraciones precisas para todos los ejemplos de entrada pasados. Las marcas de tiempo no son estrictamente necesarias pero ayudan a mantener la sincronización de audio y vídeo. Si no dispone de las marcas de tiempo para los ejemplos, es mejor dejarlas de usar valores inciertos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



