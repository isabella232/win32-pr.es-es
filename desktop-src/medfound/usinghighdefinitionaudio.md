---
description: Usar High-Definition audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Usar High-Definition audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812578"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Usar High-Definition audio (Microsoft Media Foundation)

El audio de alta definición, en el contexto de los códecs Windows Media Audio, es cualquier tipo de audio con más de dos canales o más de 16 bits por muestra. El audio de alta definición es compatible con las categorías Professional y Lossless del [codificador de Windows Media Audio](windowsmediaaudioencoder.md).

Los tipos de audio sin comprimir de alta definición se definen mediante la estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) . **WAVEFORMATEXTENSIBLE** es una extensión estructurada de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . Cuando se usa DMOs, el miembro de **formatType** de la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que describe un tipo de audio de alta definición debe establecerse en WMCFORMAT \_ WaveFormatEx, del mismo modo que para el audio normal; no hay ningún identificador de formato especial para **WAVEFORMATEXTENSIBLE**. Si un formato usa **WAVEFORMATEXTENSIBLE** , debe establecer el miembro **cbSize** de la estructura **WAVEFORMATEX** en 22.

Al usar Media Foundation, puede crear el tipo de medio correcto a partir de una estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) mediante la función [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

Los tipos de salida de varios canales que admite el códec Windows Media Audio 10 Professional no usan [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), pero notifican el número correcto de canales y bits por muestra en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . Como con todos los tipos de audio que describen el contenido de Windows Media Audio comprimido, hay información adicional anexada a la estructura **WAVEFORMATEX** usada por el descodificador para la descompresión.

## <a name="decoding-high-definition-audio"></a>Descodificar High-Definition audio

Para descodificar el audio de alta definición, debe establecer la propiedad [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) en Variant \_ true. Si no se establece esta propiedad, el descodificador entregará contenido estéreo con un máximo de 16 bits por muestra, independientemente del formato comprimido.

> [!Note]  
> El audio de alta definición solo es compatible con Windows XP, Windows Vista y versiones posteriores. En versiones anteriores de Windows, Windows Media Audio contenido codificado con alta definición se representa como audio de dos canales con un máximo de 16 bits por muestra.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 
