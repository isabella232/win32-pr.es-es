---
description: XAPOFX es una colección de efectos de audio que implementan las interfaces XAPO para su uso en XAudio2. XAPOFX contiene varios efectos y un mecanismo común para crear instancias de efecto.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Información general de XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae339a022ae5e2e880dcd130dbe055d0fde9cd28a95ea52c1238e2ade080ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005725"
---
# <a name="xapofx-overview"></a>Información general de XAPOFX

XAPOFX es una colección de efectos de audio que implementan las interfaces [XAPO](xapo-overview.md) para su uso en XAudio2. XAPOFX contiene varios efectos y un mecanismo común para crear instancias de efecto.

## <a name="included-effects"></a>Efectos incluidos

En la tabla siguiente se describen los efectos incluidos en XAPOFX. 

| Efecto             | Descripción                                                                                                                                                                                           | Estructura de parámetros                                                     | Constantes de parámetro                                              | Requisitos                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Efecto de eco.                                                                                                                                                                                       | [**PARÁMETROS \_ FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Constantes FXECHO**](fxecho-constants.md)                     | Solo admite formatos de audio FLOAT32.                                                                                      |
| FXEQ               | Un igualador de cuatro bandas.                                                                                                                                                                                | [**PARÁMETROS \_ FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Constantes FXEQ**](fxeq-constants.md)                         | Solo admite formatos de audio FLOAT32. La frecuencia de muestreo debe estar entre 22 000 Hz y 48 000 Hz.                             |
| FXMasteringLimiter | Limitador de volumen.                                                                                                                                                                                     | [**PARÁMETROS DE FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Constantes FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Solo admite formatos de audio FLOAT32.                                                                                      |
| FXReverb           | Un efecto de reverberación simple.<br/> XAudio2 también proporciona un efecto al implementar La reverberación digital de Noé que se puede crear con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**PARÁMETROS FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Constantes FXREVERB**](fxreverb-constants.md)                 | Solo admite formatos de audio FLOAT32. Además, solo admite la entrada mono en la salida mono y la entrada estéreo a la salida estéreo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Crear una instancia de un efecto incluido en XAPOFX

XAPOFX proporciona la [**función CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) como un mecanismo común para crear instancias de efecto. **CreateFX** toma el CLSID de un efecto y devuelve un puntero de interfaz IUnknown a una instancia del efecto.

## <a name="using-xapofx-in-xaudio2"></a>Uso de XAPOFX en XAudio2

Los efectos creados con [**CreateFX se**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) usan en XAudio2 asociándolos a voces. Cada voz XAudio2 tiene una cadena de efectos que contiene cero o más efectos de audio. Los datos de audio enviados a una voz se pasan a través de cada efecto de la cadena antes de que se envíen a los destinos de salida de la voz. La voz toma la salida de cada efecto y la alimenta al siguiente efecto de la cadena hasta que no se deja ningún efecto en la cadena. Para asociar un efecto XAPOFX a una voz XAudio2, rellene una estructura [**\_ EFFECT \_ CHAIN de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con la información del efecto y páserala a [**IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Para obtener más información sobre las cadenas de efectos de XAudio2, vea [Efectos de audio XAudio2](xaudio2-audio-effects.md).

Para obtener un ejemplo del uso de XAPOFX en XAudio2, vea [Cómo: Usar XAPOFX en XAudio2.](how-to--use-xapofx-in-xaudio2.md)

## <a name="xaudio2-implicit-effects"></a>Efectos implícitos de XAudio2

Además de la biblioteca de XAPOs proporcionada por XAPOFX, XAudio2 tiene efectos de audio integrados de reverberación y medidor de volumen. Puede crear estos efectos integrados con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) y [**XAudio2CreateVolumeMeter.**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) Vea [Cómo: Crear una cadena de efectos](how-to--create-an-effect-chain.md) para obtener un ejemplo del uso de uno de estos efectos integrados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> </dl>

 

 
