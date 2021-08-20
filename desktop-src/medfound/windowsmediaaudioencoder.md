---
description: 'El Windows Media Audio codifica secuencias de audio. El codificador admite tres categorías de salida codificada: Windows Media Audio Standard, Windows Media Audio Professional y Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Windows Codificador de audio multimedia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba1a94ff5867282049521e3ac13ae28f949a7fc3ccd1855962fb9abb2217d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688189"
---
# <a name="windows-media-audio-encoder"></a>Windows Codificador de audio multimedia

El Windows Media Audio codifica secuencias de audio. El codificador admite tres categorías de salida codificada: Windows Media Audio Standard, Windows Media Audio Professional y Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador Windows media audio se representa mediante la constante **CLSID \_ CWMAEncMediaObject**. Puede crear una instancia del codificador de audio llamando a **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de entrada admitidas por el codificador Windows Media Audio. Para obtener información sobre cómo establecer los tipos de entrada y salida para el codificador, vea [Configuring Audio Encoding](configuringaudioencoding.md).



| Constante de etiqueta de formato       | Valor de etiqueta de formato | Formato de audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| FORMATO \_ \_ WAVE PCM         | 0x0001           | Formato PCM                                            |
| FORMATO WAVE \_ \_ IEEE \_ FLOAT | 0x0003           | Punto flotante IEEE                                   |
| FORMATO \_ WAVE \_ EXTENSIBLE  | 0xFFFE           | Formato PCM/IEEE en **la estructura DESATEXTENSIBLE** |



 

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de salida admitidas por el codificador Windows Media Audio.



| Constante de etiqueta de formato             | Valor de etiqueta de formato | Formato de audio                     |
|---------------------------------|------------------|----------------------------------|
| FORMATO \_ \_ WAVE WMAUDIO2          | 0x0161           | Windows Media Audio Standard     |
| FORMATO \_ \_ WAVE WMAUDIO3          | 0x0162           | Windows Audio multimedia Professional |
| FORMATO \_ \_ WAVE WMAUDIO \_ LOSSLESS | 0x0163           | Windows Audio multimedia sin pérdida de datos     |



 

## <a name="interfaces"></a>Interfaces

Un objeto de endoder de audio expone la interfaz **IMediaObject** para que el objeto se pueda usar como objeto multimedia DirectX (DMO) y expone la interfaz **DETRANSFORMTRANSFORM** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un Windows Media Audio se comporta como un DMO o MFT en función de las interfaces que obtenga y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un codificador de audio se comporta como DMO o MFT.



| Sistema operativo | Comportamiento del codificador                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un Windows Media Audio siempre se comporta como un DMO.                                                                                                                                |
| Windows Vista    | De forma predeterminada, un codificador Windows Media Audio se comporta como un DMO. Si obtiene una interfaz **IMFTransform** o **una interfaz IPropertyStore** en un codificador de audio, se comporta como MFT. |
| Windows 7        | De forma predeterminada, un codificador Windows Media Audio se comporta como un DMO. Si obtiene una interfaz **DETRANSFORMTransform** en un codificador de audio, se comporta como MFT.                                    |



 

## <a name="encoder-properties"></a>Propiedades del codificador

El Windows Media Audio admite las siguientes propiedades.



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
<td>Especifica si el codificador usa la codificación VBR de control medio.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia restringida de velocidad de bits variable (VBR) a su velocidad de bits máxima.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Especifica si el codificador debe comprobar la coherencia de los datos entre los pases al realizar la codificación VBR de dos pases. <br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Especifica si el codificador está restringido por un requisito de latencia máxima del descodificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Especifica si la complejidad del algoritmo de codificación está restringida.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Especifica si el codificador está restringido por un requisito de latencia máxima.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica si los modos enumerados por el codificador se limitan a los que cumplen un requisito de calidad.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica el perfil de complejidad del contenido codificado.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad deseado para la codificación VBR.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Especifica si el codificador usa la sustitución de ruido.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Especifica si el codificador usa la limitación del intervalo de PCM.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Especifica el ancho de banda codificado máximo permitido por el truncamiento de banda en el codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Especifica el ancho de banda codificado mínimo permitido por truncamiento de banda en el codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Especifica la calidad con la que se permite el ancho de banda codificado mínimo. <br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Especifica la calidad con la que se permite el ancho de banda máximo codificado.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Especifica si el codificador realiza el truncamiento de banda.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Especifica si el codificador usa el estilo de cálculo de máscara realizado por la versión 7 del codificador Windows Media Audio.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Especifica si el codificador realiza el procesamiento de imágenes estéreo. <br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de control medio.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Especifica la velocidad de bits media, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de control medio.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Especifica la complejidad del algoritmo de codificación.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica el final de un paso de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Especifica si el codificador principal usa la &quot; característica &quot; Plus.<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Especifica la latencia máxima del descodificador, en milisegundos.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Especifica la latencia máxima para el codificador, en milisegundos.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad de VBR del tipo de salida enumerado más recientemente.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica el número máximo de pases admitidos por el codificador.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica el número de pases que usará el codificador para codificar el contenido.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Especifica si el codificador está restringido por una velocidad de bits máxima.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional.<br />
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
<td>Especifica si el codificador debe usar un tamaño de fotograma preferido.<br/> <dl> Windows Vista y versiones posteriores.<br />
Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la codificación restringida de velocidad de bits variable (VBR) de 2 pases. <br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Especifica la ventana de búfer promedio, en milisegundos, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Especifica la ventana de búfer máxima, en milisegundos, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Especifica la velocidad de bits media, en bits por segundo, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, de una secuencia codificada.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica si el codificador usa la codificación VBR.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Esta propiedad no se usa actualmente en el códec Windows Media Audio.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Especifica el nivel medio de volumen del contenido de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Especifica el nivel de volumen más alto que se produce en el contenido de audio.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Especifica el promedio de bytes por segundo para el audio codificado en VBR.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Especifica si el codificador debe generar 1 paquete WMA por fotograma.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Especifica si el codificador debe generar parámetros de control de intervalo dinámico.<br/> <dl> Windows Vista y versiones posteriores.<br />
Estándar, Professional, sin pérdida.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Especifica la estructura <strong>DEDATOX</strong> que describe el contenido de audio de entrada.<br/> <dl> Windows XP y versiones posteriores.<br />
Estándar, Professional.<br />
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



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Implementación de códec](codecimplementation.md)
</dt> </dl>

 

 




