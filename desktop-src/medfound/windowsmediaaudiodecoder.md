---
description: El descodificador de Windows Media Audio descodifica secuencias de audio codificadas por el codificador Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Descodificador de Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699409"
---
# <a name="windows-media-audio-decoder"></a>Descodificador de Windows Media Audio

El descodificador de Windows Media Audio descodifica secuencias de audio codificadas por el [**codificador Windows Media Audio**](windowsmediaaudioencoder.md). El codificador y el descodificador admiten tres categorías de audio codificado: Windows Media Audio Standard, Windows Media Audio Professional y Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador de Windows Media Audio se representa mediante la constante **\_ CWMADecMediaObject de CLSID**. Puede crear una instancia del descodificador de audio llamando a **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de entrada admitidas por el descodificador de Windows Media Audio. Para obtener información sobre cómo establecer los tipos de entrada y salida para el descodificador, consulte Configuración de la [descodificación de audio](configuringaudiodecoding.md).



| Format (constante de etiqueta)             | Valor de etiqueta de formato | Formato de audio                     |
|---------------------------------|------------------|----------------------------------|
| Formato de onda \_ \_ WMAUDIO2          | 0x0161           | Estándar Windows Media Audio     |
| Formato de onda \_ \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| formato de onda \_ \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio sin pérdida de     |



 

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran las etiquetas de formato de audio que representan los tipos de salida admitidos por el **descodificador de Windows Media Audio**. Para obtener información sobre cómo establecer los tipos de entrada y salida para el descodificador, consulte Configuración de la [codificación de audio](configuringaudioencoding.md).



| Format (constante de etiqueta)       | Valor de etiqueta de formato | Formato de audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM con formato de onda \_         | 0x0001           | Formato PCM                                            |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Punto flotante IEEE                                   |
| formato de onda \_ \_ extensible  | 0xFFFE           | Formato PCM/IEEE en la estructura **WAVEFORMATEXTENSIBLE** |



 

## <a name="interfaces"></a>Interfaces

Un objeto de descodificador de audio expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz **IMFTransform** para que el objeto pueda usarse como una transformación de Media Foundation (MFT).

Un descodificador de Windows Media Audio se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador de audio se comporta como DMO o MFT.



| Sistema operativo | Comportamiento del descodificador                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un descodificador de Windows Media Audio siempre se comporta como DMO.                                                                                                                                |
| Windows Vista    | De forma predeterminada, un descodificador de Windows Media Audio se comporta como un DMO. Si obtiene una interfaz **IMFTransform** o una interfaz **IPropertyStore** en un descodificador de audio, se comporta como una MFT. |
| Windows 7        | De forma predeterminada, un descodificador de Windows Media Audio se comporta como un DMO. Si obtiene una interfaz **IMFTransform** en un descodificador de audio, se comporta como una MFT.                                    |



 

## <a name="properties"></a>Propiedades

El descodificador de Windows Media Audio admite las siguientes propiedades.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>Especifica el número máximo de muestras PCM adicionales que podrían devolverse al final de la descodificación de un archivo.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>Especifica el modo de control de intervalo dinámico que usará el descodificador de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>Especifica los coeficientes de subconjuntos proporcionados por el autor para descodificar el audio multicanal para menos canales de los que contiene la secuencia codificada. <br/> <dl> Windows XP y versiones posteriores.<br />
Profesional<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.<br/> <dl> Windows XP y versiones posteriores.<br />
Profesional, sin pérdida.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>Especifica si el descodificador de audio debe realizar Lt-Rt pliegue.<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>Especifica la configuración de los altavoces en el equipo cliente.<br/> <dl> Windows XP y versiones posteriores.<br />
Professional.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Especifica el nivel de volumen medio del contenido de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Profesional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>Especifica el nivel de volumen medio deseado del contenido de audio de salida.<br/> <dl> Windows XP y versiones posteriores.<br />
Profesional, sin pérdida.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Especifica el nivel de volumen más alto que tiene lugar en el contenido de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Profesional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>Especifica el nivel de volumen máximo deseado del contenido de audio de salida.<br/> <dl> Windows XP y versiones posteriores.<br />
Profesional, sin pérdida.<br />
De solo escritura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> </dl>

 

 




