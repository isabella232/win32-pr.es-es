---
description: 'El codificador Windows Media Audio codifica secuencias de audio. El codificador admite tres categorías de salida codificada: Windows Media Audio estándar, Windows Media Audio Professional y Windows Media Audio sin pérdida de información.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Codificador Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718940"
---
# <a name="windows-media-audio-encoder"></a>Codificador Windows Media Audio

El codificador Windows Media Audio codifica secuencias de audio. El codificador admite tres categorías de salida codificada: Windows Media Audio estándar, Windows Media Audio Professional y Windows Media Audio sin pérdida de información.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador Windows Media Audio se representa mediante la constante CWMAEncMediaObject de **CLSID \_**. Puede crear una instancia del codificador de audio llamando a **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de entrada admitidas por el codificador de Windows Media Audio. Para obtener información sobre cómo establecer los tipos de entrada y salida para el codificador, consulte [configuración](configuringaudioencoding.md)de la codificación de audio.



| Format (constante de etiqueta)       | Valor de etiqueta de formato | Formato de audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM con formato de onda \_         | 0x0001           | Formato PCM                                            |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Punto flotante IEEE                                   |
| formato de onda \_ \_ extensible  | 0xFFFE           | Formato PCM/IEEE en la estructura **WAVEFORMATEXTENSIBLE** |



 

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de salida admitidas por el codificador de Windows Media Audio.



| Format (constante de etiqueta)             | Valor de etiqueta de formato | Formato de audio                     |
|---------------------------------|------------------|----------------------------------|
| Formato de onda \_ \_ WMAUDIO2          | 0x0161           | Estándar Windows Media Audio     |
| Formato de onda \_ \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| formato de onda \_ \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio sin pérdida de     |



 

## <a name="interfaces"></a>Interfaces

Un objeto endoder de audio expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz **IMFTransform** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un codificador de Windows Media Audio se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un codificador de audio se comporta como un DMO o una MFT.



| Sistema operativo | Comportamiento del codificador                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un codificador Windows Media Audio siempre se comporta como DMO.                                                                                                                                |
| Windows Vista    | De forma predeterminada, un codificador de Windows Media Audio se comporta como un DMO. Si obtiene una interfaz **IMFTransform** o una interfaz **IPropertyStore** en un codificador de audio, se comporta como una MFT. |
| Windows 7        | De forma predeterminada, un codificador de Windows Media Audio se comporta como un DMO. Si obtiene una interfaz **IMFTransform** en un codificador de audio, se comporta como una MFT.                                    |



 

## <a name="encoder-properties"></a>Propiedades del codificador

El codificador Windows Media Audio admite las siguientes propiedades.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Especifica si el codificador utiliza la codificación VBR de promedio controlable.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en su velocidad de bits máxima.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Especifica si el codificador debe comprobar la coherencia de los datos entre las pasadas al realizar la codificación VBR de dos pasos. <br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Especifica si el codificador está restringido por un requisito máximo de latencia del descodificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Especifica si la complejidad del algoritmo de codificación está restringida.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Especifica si el codificador está restringido por un requisito de latencia máximo.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica si los modos enumerados por el codificador están limitados a aquellos que cumplen un requisito de calidad.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica el perfil de complejidad del contenido codificado.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad deseado para la codificación VBR.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Especifica si el codificador utiliza la sustitución de ruido.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Especifica si el codificador utiliza la limitación de intervalo PCM.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Especifica el ancho de banda máximo codificado permitido por el truncamiento de banda en el codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Especifica el ancho de banda mínimo codificado permitido por el truncamiento de banda en el codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Especifica la calidad con la que se permite el ancho de banda mínimo codificado. <br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Especifica la calidad con la que se permite el ancho de banda máximo codificado.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Especifica si el codificador realiza el truncamiento de la banda.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Especifica si el codificador usa el estilo de cálculo de máscara realizado por la versión 7 del codificador Windows Media Audio.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Especifica si el codificador realiza el procesamiento de imágenes estéreo. <br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de media controlable.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Especifica la velocidad de bits promedio, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de tamaño medio.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Especifica la complejidad del algoritmo de codificación.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica el final de una fase de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Especifica si el codificador básico usa la &quot; característica Plus &quot; .<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Especifica la latencia máxima del descodificador, en milisegundos.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Especifica la latencia máxima del codificador, en milisegundos.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad VBR del tipo de salida enumerado más recientemente.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica el número máximo de pasos admitidos por el codificador.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica el número de pasos que usará el codificador para codificar el contenido.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Especifica si el codificador está restringido por una velocidad de bits máxima.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>Especifica el número preferido de muestras por fotograma.<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>Especifica si el codificador debe usar un tamaño de marco preferido.<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos restringidos. <br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Especifica la ventana de búfer promedio, en milisegundos, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Especifica la ventana de búfer máxima, en milisegundos, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Especifica la velocidad de bits media, en bits por segundo, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica si el codificador utiliza la codificación VBR.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Esta propiedad no se usa actualmente en el códec de Windows Media Audio.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Especifica el nivel de volumen medio del contenido de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Especifica el nivel de volumen más alto que tiene lugar en el contenido de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Especifica el promedio de bytes por segundo para el audio codificado VBR.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Especifica si el codificador debe producir 1 paquete WMA por fotograma.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Especifica si el codificador debe generar parámetros de control de intervalo dinámicos.<br/> <dl> Windows Vista y versiones posteriores.<br />
Standard, Professional y Lossless.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Especifica la estructura <strong>WAVEFORMATEX</strong> que describe el contenido de audio de entrada.<br/> <dl> Windows XP y versiones posteriores.<br />
Standard, Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Especifica si el codificador debe habilitar la codificación S/PDIF en tiempo real.<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> </dl>

 

 




