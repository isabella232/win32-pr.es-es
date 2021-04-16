---
description: XAPOFX es una colección de efectos de audio que implementan las interfaces XAPO para su uso en XAudio2. XAPOFX contiene varios efectos y un mecanismo común para crear instancias de efectos.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Información general de XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8979b5de50406d46bc472e18ca4a6479679e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542523"
---
# <a name="xapofx-overview"></a>Información general de XAPOFX

XAPOFX es una colección de efectos de audio que implementan las interfaces [XAPO](xapo-overview.md) para su uso en XAudio2. XAPOFX contiene varios efectos y un mecanismo común para crear instancias de efectos.

## <a name="included-effects"></a>Efectos incluidos

En la tabla siguiente se describen los efectos incluidos en XAPOFX. 

| Efecto             | Descripción                                                                                                                                                                                           | Estructura del parámetro                                                     | Constantes de parámetro                                              | Requisitos                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Efecto de eco.                                                                                                                                                                                       | [**parámetros de FXECHO \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Constantes de FXECHO**](fxecho-constants.md)                     | Solo admite formatos de audio FLOAT32.                                                                                      |
| FXEQ               | Ecualizador de cuatro bandas.                                                                                                                                                                                | [**parámetros de FXEQ \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Constantes de FXEQ**](fxeq-constants.md)                         | Solo admite formatos de audio FLOAT32. La velocidad de muestreo debe ser de entre 22.000 Hz y 48.000 Hz.                             |
| FXMasteringLimiter | Un límite de volumen.                                                                                                                                                                                     | [**parámetros de FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Constantes de FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Solo admite formatos de audio FLOAT32.                                                                                      |
| FXReverb           | Efecto de reverberación simple.<br/> XAudio2 también proporciona un efecto que implementa la reverberación digital de Princeton, de la que se pueden crear instancias con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**parámetros de FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Constantes de FXREVERB**](fxreverb-constants.md)                 | Solo admite formatos de audio FLOAT32. Además, solo admite la entrada mono en la salida mono y la entrada estéreo en la salida estéreo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Crear una instancia de un efecto incluido en XAPOFX

XAPOFX proporciona la función [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) como un mecanismo común para crear instancias de efectos. **CreateFX** toma el CLSID de un efecto y devuelve un puntero de interfaz IUnknown a una instancia del efecto.

## <a name="using-xapofx-in-xaudio2"></a>Uso de XAPOFX en XAudio2

Los efectos con instancias de [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) se usan en XAudio2 mediante su asociación a las voces. Cada voz de XAudio2 tiene una cadena de efectos que contiene cero o más efectos de audio. Los datos de audio enviados a una voz se pasan a través de cada efecto de la cadena antes de que se envíen a los destinos de salida de la voz. La voz toma el resultado de cada efecto y lo alimenta en el siguiente efecto de la cadena hasta que no quede ningún efecto en la cadena. Para adjuntar un efecto de XAPOFX a una voz de XAudio2, rellene una estructura de [**\_ \_ cadena de efectos de xaudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con la información del efecto y páselo a [**IXAudio2Voice:: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Para más información sobre las cadenas de efectos de XAudio2, consulte [efectos de audio de xaudio2](xaudio2-audio-effects.md).

Para obtener un ejemplo del uso de XAPOFX en XAudio2, consulte [Cómo: usar XAPOFX en xaudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="xaudio2-implicit-effects"></a>Efectos implícitos de XAudio2

Además de la biblioteca de XAPOs proporcionada por XAPOFX, XAudio2 tiene efectos de audio de reverberación integrados y de medición de volumen. Puede crear estos efectos integrados con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) y [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter). Consulte [Cómo: crear una cadena de efectos](how-to--create-an-effect-chain.md) para obtener un ejemplo del uso de uno de estos efectos integrados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> </dl>

 

 
