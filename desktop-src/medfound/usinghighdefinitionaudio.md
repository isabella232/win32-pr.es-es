---
description: Uso de High-Definition Audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Usar High-Definition audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3eac918929b6495401a0eeaee31fe6d7a01d2df0eced9866da829381392edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737338"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Usar High-Definition audio (Microsoft Media Foundation)

El audio de alta definición, en el contexto de los códecs Windows Media Audio, es cualquier tipo de audio con más de dos canales o más de 16 bits por muestra. El audio de alta definición es compatible con las categorías Professional y sin pérdida de datos de Windows [codificador de audio multimedia](windowsmediaaudioencoder.md).

Los tipos de audio de alta definición sin comprimir se definen mediante la [**estructura DEDATOATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) **FORMADEDATOSTEXTENSIBLE** es una extensión estructurada de la [**estructura DE FORMA DEDATOSTEX.**](/previous-versions/dd757713(v=vs.85)) Cuando se usan DDO, el miembro **formattype** de la estructura [**\_ media \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) de DMO que describe un tipo de audio de alta definición debe establecerse en WMCFORMAT WaveFormatEx, tal como lo es para el audio normal; no hay ningún identificador de formato especial para \_ **WAVEATEXTENSIBLE.** Si un formato usa **FORMADEDATEXTENSIBLE,** debe establecer el **miembro cbSize** de la estructura **DESACMATEX** en 22.

Al usar Media Foundation, puede construir el tipo de medio correcto a partir de una estructura [**DEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) mediante la función [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

Los tipos de salida de varios canales admitidos por el códec Professional audio multimedia 10 de Windows no usan [**FORMADEDATOSTEXTENSIBLE,**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))sino que informan del número correcto de canales y bits por muestra en la estructura [**DEFORMATEX.**](/previous-versions/dd757713(v=vs.85)) Al igual que con todos los tipos de audio que describen contenido Windows audio multimedia comprimido, hay información adicional anexada a la estructura **DESACTETEX** que usa el descodificador para la descompresión.

## <a name="decoding-high-definition-audio"></a>Decoding High-Definition Audio

Para descodificar el audio de alta definición, debe establecer la propiedad [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) en VARIANT \_ TRUE. Si no se establece esta propiedad, el descodificador entregará contenido estéreo con un máximo de 16 bits por muestra, independientemente del formato comprimido.

> [!Note]  
> El audio de alta definición solo se admite para Windows XP, Windows Vista y versiones posteriores. En versiones anteriores de Windows, Windows contenido de Audio multimedia codificado con alta definición se representa como audio de dos canales con un máximo de 16 bits por muestra.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 
