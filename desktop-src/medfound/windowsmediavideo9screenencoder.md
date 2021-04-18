---
description: El codificador de pantalla de Windows Media Video 9 está optimizado para codificar capturas de pantalla secuenciales desde monitores de equipos.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Codificador de pantalla de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709104"
---
# <a name="windows-media-video-9-screen-encoder"></a>Codificador de pantalla de Windows Media Video 9

El codificador de pantalla de Windows Media Video 9 está optimizado para codificar capturas de pantalla secuenciales desde monitores de equipos.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador de pantalla de Windows Media Video 9 se representa mediante la constante **\_ CMSSCEncMediaObject2 de CLSID**. Puede crear una instancia del codificador llamando a **CoCreateInstance**.

## <a name="input-types"></a>Tipos de entrada

El codificador de pantalla de la versión 9 admite los siguientes tipos de entrada cuando se usa como un objeto multimedia de DirectX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

El codificador de pantalla de la versión 9 admite los siguientes tipos de entrada cuando se usa como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="output-types"></a>Tipos de salida

El código de cuatro caracteres (FOURCC) para el contenido codificado en pantalla de la versión 9 de Windows Media Video es "MSS2".

El codificador de pantalla de la versión 9 admite los siguientes tipos de salida.

-   MEDIASUBTYPE \_ MSS2

## <a name="encoder-properties"></a>Propiedades del codificador

El codificador de pantalla de Windows Media Video 9 admite las siguientes propiedades.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Especifica el número de fotogramas de vídeo codificados por el códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Esta propiedad se sustituye por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Especifica la complejidad del algoritmo del codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen en la salida del códec.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Especifica el final de una fase de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Especifica el FOURCC que identifica el codificador que se desea utilizar.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Obsoleto.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Especifica el número máximo de pasos admitidos por el códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP y versiones posteriores. Lectura/escritura<br/> Especifica el número de pasos que el códec usará para codificar el contenido.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Especifica QP. Los valores posibles son de 1,0 a 31,0.<br/> <dl> Windows Vista y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos restringidos.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Especifica el número de fotogramas de vídeo pasados al codificador durante el proceso de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Especifica si el códec usará la codificación de velocidad de bits variable (VBR).<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>La cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.<br/> <dl> Windows XP y versiones posteriores,<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Especifica el número de fotogramas de vídeo que se omitieron porque eran duplicados de fotogramas anteriores.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Un objeto de codificador de pantalla expone la interfaz **IMediaObject** para que el objeto pueda usarse como un objeto multimedia de DirectX (DMO) y expone la interfaz **IMFTransform** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un codificador de pantalla se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un codificador de pantalla se comporta como un DMO o MFT.



| Sistema operativo            | Comportamiento del codificador                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un codificador de pantalla de Windows Media siempre se comporta como DMO.                                                                                             |
| Windows Vista y Windows 7 | De forma predeterminada, un codificador de pantalla de Windows Media se comporta como un DMO. Si obtiene una interfaz **IMFTransform** en un codificador de pantalla, se comporta como una MFT. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> <dt>

[Usar el códec de pantalla de Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Descodificador de pantalla de Windows Media Video 9](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




