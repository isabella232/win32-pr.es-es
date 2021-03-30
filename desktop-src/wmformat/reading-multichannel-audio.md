---
title: Lectura de audio multicanal
description: Lectura de audio multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- SDK de Windows Media Format, lectura de audio multicanal
- Advanced Systems Format (ASF), lectura de audio multicanal
- ASF (formato de sistemas avanzados), lectura de audio multicanal
- Advanced Systems Format (ASF), audio multicanal
- ASF (formato de sistemas avanzados), audio multicanal
- códecs, leer audio multicanal
- audio multicanal, lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793240"
---
# <a name="reading-multichannel-audio"></a>Lectura de audio multicanal

El códec Windows Media Audio 9 Professional puede codificar audio multicanal (más de dos canales). Al leer un archivo con audio multicanal, debe configurar el resultado correctamente o el audio se entregará con una calidad inferior y en estéreo. Para establecer una salida para la entrega de audio multicanal, debe establecer dos configuraciones de salida: g \_ wszEnableDiscreteOutput y g \_ wszSpeakerConfig.

Al establecer g \_ wszEnableDiscreteOutput en **true** , se establece el códec para proporcionar una salida de audio de alta definición. El códec de Windows Media Audio 9 codifica el audio de alta definición con ejemplos de 24 bits en estéreo o en varios canales. Si este valor es **false**, solo se entregará la salida estéreo de 16 bits.

El número de oradores en el equipo que se está configurando está establecido con g \_ wszSpeakerConfig. Esta opción es un valor **DWORD** establecido en una de las constantes de altavoz de DirectSound que se enumeran en la tabla siguiente. Para resolver estos nombres de constantes para el compilador, debe incluir dsound. h.



| Constante             | Value      | Descripción                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | El audio se pasa directamente, sin tener que configurarse para los altavoces. |
| \_auriculares DSSPEAKER | 0x00000001 | El equipo cliente está equipado con auriculares.                             |
| \_mono DSSPEAKER      | 0x00000002 | El equipo cliente está equipado con un altavoz monoaural.                     |
| DSSPEAKER \_ cuádruple      | 0x00000003 | El equipo cliente está equipado con altavoces quadraphonic.                  |
| \_estéreo DSSPEAKER    | 0x00000004 | El equipo cliente está equipado con altavoces estéreo.                        |
| \_envolvente DSSPEAKER  | 0x00000005 | El equipo cliente está equipado con altavoces con sonido envolvente de cuatro canales.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | El equipo cliente está equipado con cinco altavoces y un subwoofer.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | El equipo cliente está equipado con siete altavoces y un subwoofer.         |



 

Para establecer esta configuración, use [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Por último, para que los canales se generen de manera discreta y no se despliegan en estéreo, debe establecer el tipo de medio correcto en la salida siguiendo estos pasos:

1.  Llame a [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obtener el número de formatos admitidos para la salida de audio pertinente. Los índices de formato de salida son de base cero.
2.  Para cada formato admitido, llame a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) para recuperar la interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) en el objeto de propiedades de los medios de salida.
3.  Llame a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) para recuperar el tipo de medio.
4.  Si el tipo de medio recuperado es el tipo multicanal deseado, establézcalo llamando a [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Una vez que haya establecido la salida discreta y la configuración de los altavoces, los formatos de salida enumerados por el lector deben incluir formatos multicanal que utilicen la estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) . Si enumera los formatos de salida antes de establecer las propiedades, se incluirán solo los formatos con 1 o 2 canales y un máximo de 16 bits por canal. Al igual que con otros formatos de audio, solo debe usar los formatos enumerados por el lector; no configure el suyo propio.

> [!Note]  
> Puede generar audio multicanal solo si la aplicación se ejecuta en Microsoft Windows XP o en una versión posterior de Microsoft Windows.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Configuración de salida**](output-settings.md)
</dt> <dt>

[**Trabajar con High-Resolution PCM audio**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 