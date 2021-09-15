---
title: Lectura de audio multicanal
description: Lectura de audio multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows SDK de formato multimedia, lectura de audio multicanal
- Formato de sistemas avanzados (ASF), lectura de audio multicanal
- ASF (formato de sistemas avanzados), lectura de audio multicanal
- Formato de sistemas avanzados (ASF), audio multicanal
- ASF (formato de sistemas avanzados), audio multicanal
- códecs, lectura de audio multicanal
- audio multicanal, lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466664"
---
# <a name="reading-multichannel-audio"></a>Lectura de audio multicanal

El Windows de audio multimedia 9 Professional puede codificar audio multicanal (más de dos canales). Al leer un archivo con audio multicanal, debe configurar la salida correctamente o el audio se entregará con una calidad inferior y en estéreo. Para establecer una salida para la entrega de audio multicanal, debe establecer dos valores de salida: g \_ wszEnableDiscreteOutput y g \_ wszSpeakerConfig.

Al establecer g \_ wszEnableDiscreteOutput en **TRUE,** se establece el códec para proporcionar una salida de audio de alta definición. El audio de alta definición se codifica mediante el códec Windows Media Audio 9 con ejemplos de 24 bits en estéreo o en varios canales. Si esta configuración es **FALSE,** solo se entregará una salida estéreo de 16 bits.

El número de altavoces del equipo que se reproduce se establece con g \_ wszSpeakerConfig. Esta configuración es un **valor DWORD** establecido en una de las constantes de orador de DirectSound enumeradas en la tabla siguiente. Para resolver estos nombres constantes para el compilador, debe incluir dsound.h.



| Constante             | Value      | Descripción                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DIRECTOUT DE DSSPEAKER \_ | 0x00000000 | El audio se pasa directamente, sin configurarse para los altavoces. |
| DSSPEAKER \_ DE LA CAJA DE SEGURIDAD | 0x00000001 | El equipo cliente está equipado con cascos.                             |
| DSSPEAKER \_ MONO      | 0x00000002 | El equipo cliente está equipado con un altavoz de voz.                     |
| DSSPEAKER \_ QUAD      | 0x00000003 | El equipo cliente está equipado con altavoces cuadráticos.                  |
| DSSPEAKER \_ STEREO    | 0x00000004 | El equipo cliente está equipado con altavoces estéreo.                        |
| ENTORNO DE DSSPEAKER \_  | 0x00000005 | El equipo cliente está equipado con altavoces de sonido envolvente de cuatro canales.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | El equipo cliente está equipado con cinco altavoces y un altavoz.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | El equipo cliente está equipado con siete altavoces y un altavoz.         |



 

Para establecer esta configuración, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Por último, para que los canales se puedan generar discretamente, sin plegado a estéreo, debe establecer el tipo de medio correcto en la salida siguiendo estos pasos:

1.  Llame [**a IWMReader::GetOutputFormatCount para**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) obtener el número de formatos admitidos para la salida de audio pertinente. Los índices de formato de salida son de base cero.
2.  Para cada formato admitido, llame a [**IWMReader::GetOutputFormat para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) recuperar la [**interfaz IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) en el objeto de propiedades del medio de salida.
3.  Llame [**a IWMMediaProps::GetMediaType para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) recuperar el tipo de medio.
4.  Si el tipo de medio recuperado es el tipo multicanal deseado, puede establecerlo llamando a [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Después de establecer la salida discreta y la configuración del hablante, los formatos de salida enumerados por el lector deben incluir formatos multicanal que usen la estructura [**DESUSOTEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) Si enumera los formatos de salida antes de establecer las propiedades, solo se incluirán los formatos con 1 o 2 canales y un máximo de 16 bits por canal. Al igual que con otros formatos de audio, solo debe usar los formatos enumerados por el lector; no configure los suyos propios.

> [!Note]  
> Solo puede generar audio multicanal si la aplicación se ejecuta en Microsoft Windows XP o en una versión posterior de Microsoft Windows.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Salida Configuración**](output-settings.md)
</dt> <dt>

[**Trabajar con High-Resolution PCM Audio**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 