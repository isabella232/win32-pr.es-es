---
description: El codificador Windows Media Video 7/8 implementa versiones anteriores del codificador Windows Media Video.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Codificador Windows Media Video 7/8 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700272"
---
# <a name="windows-media-video-78-encoder"></a>Codificador Windows Media Video 7/8

El codificador Windows Media Video 7/8 implementa versiones anteriores del codificador Windows Media Video.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador Windows Media Video 7/8 es **CLSID \_ CWMVXEncMediaObject**. Puede crear una instancia del codificador llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto de codificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto pueda usarse como un objeto multimedia de DirectX (DMO) y expone la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un codificador de vídeo se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un codificador de vídeo se comporta como un DMO o una MFT.



| Sistema operativo            | Comportamiento del codificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un codificador de vídeo de Windows Media siempre se comporta como DMO.                                                                                                                |
| Windows Vista y Windows 7 | De forma predeterminada, un codificador de vídeo de Windows Media se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un codificador de vídeo, se comporta como una MFT. |



 

## <a name="input-formats"></a>Formatos de entrada

El codificador Windows Media Video admite los siguientes subtipos de medios de entrada cuando actúa como DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ i420
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8
-   fotomovimiento MEDIASUBTYPE \_

El codificador Windows Media Video admite los siguientes subtipos de medios de entrada cuando actúa como MFT.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ i420
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8
-   fotomovimiento MEDIASUBTYPE \_

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCCs) para los tipos de salida admitidos por el codificador Windows Media Video 7/8.



| Category              | FOURCC |
|-----------------------|--------|
| Windows Media Video 7 | "WMV1" |
| Windows Media Video 8 | "WMV2" |



 

## <a name="properties"></a>Propiedades

El codificador Windows Media Video 7/8 admite las siguientes propiedades.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Especifica la velocidad media de fotogramas del contenido de vídeo, en fotogramas por segundo.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo codificados por el códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Esta propiedad se sustituye por <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Especifica la complejidad del algoritmo del codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen en la salida del códec.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica la plantilla de conformidad del dispositivo a la que se ajusta el contenido codificado.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica el final de una fase de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Especifica el FOURCC que identifica el codificador que se desea utilizar.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Especifica si la salida del códec se entrelazará.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica el número máximo de pasos admitidos por el códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica el número de pasos que el códec usará para codificar el contenido.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Especifica QP.<br/> <dl> Windows Vista y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la velocidad de bits variable (VBR) limitada de dos pasos.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo pasados al codificador durante el proceso de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica si el códec usará la codificación de velocidad de bits variable (VBR).<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo que se omitieron porque eran duplicados de fotogramas anteriores.<br/> <dl> Windows XP y versiones posteriores.<br />
Solo lectura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> <dt>

[GUID de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 
