---
description: El Windows Media Video 9 codifica secuencias de vídeo.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Windows Codificador Media Video 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d3d3e7feb06cfbe9e9149fd9fd55d76ecf5abe2fbe0d6eea6ac961a0561ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398245"
---
# <a name="windows-media-video-9-encoder"></a>Windows Codificador Media Video 9

El Windows Media Video 9 codifica secuencias de vídeo. El codificador admite las cuatro categorías siguientes de salida codificada.

-   Windows Perfil simple de Media Video 9
-   Windows Perfil principal de Media Video 9
-   Windows Perfil avanzado de Media Video 9
-   Windows Imagen de Vídeo multimedia 9.1

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador Windows Media Video se representa mediante la constante **CLSID \_ CWMV9EncMediaObject**. Puede crear una instancia del codificador de vídeo llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto de codificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como objeto multimedia directX (DMO) y expone la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un codificador de vídeo se comporta como un DMO o MFT en función de las interfaces que se obtengan y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un codificador de vídeo se comporta como DMO o MFT.



| Sistema operativo            | Comportamiento del codificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows de vídeo multimedia siempre se comporta como un DMO.                                                                                                                |
| Windows Vista y Windows 7 | De forma predeterminada, un Windows de vídeo multimedia se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un codificador de vídeo, se comporta como MFT. |



 

## <a name="input-formats"></a>Formatos de entrada

El Windows Media Video admite los siguientes subtipos multimedia de entrada cuando actúa como DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ I420
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
-   MEDIASUBTYPE \_ PHOTOMOTION

El Windows Media Video admite los siguientes subtipos multimedia de entrada cuando actúa como MFT.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ I420
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
-   MEDIASUBTYPE \_ PHOTOMOTION

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCC) que corresponden a las categorías de salida codificada.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Perfil simple de Media Video 9   | "WMV3"                                   |
| Windows Perfil principal de Media Video 9     | "WMV3"                                   |
| Windows Perfil avanzado de Media Video 9 | "WVC1"                                   |
| Windows Imagen de Vídeo multimedia 9.1          | "WMVP" para 9.1, "WVP2" para la versión 9.1 versión 2 |



 

Para distinguir entre perfil simple y perfil principal, establezca la [**propiedad MFPKEY \_ DECODERCOMPLEXITYREQUESTED.**](mfpkey-decodercomplexityrequestedproperty.md)

## <a name="properties"></a>Propiedades

El Windows Media Video 9 admite las siguientes propiedades.



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
<td>Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor utilizado para almacenar el contenido comprimido.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Especifica la velocidad media de fotogramas del contenido de vídeo, en fotogramas por segundo.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia restringida de velocidad de bits variable (VBR) a su velocidad de bits media (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Especifica el aumento diferencial entre el cuantificador de imagen del marco delimitador y el cuantificador de imágenes del fotograma B.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica la ventana de búfer, en milisegundos, de una secuencia restringida de velocidad de bits variable (VBR) a su velocidad de bits máxima (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Especifica si la secuencia de bits de vídeo codificada contiene un valor de integridad del búfer con cada fotograma clave.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Especifica el patrón de codificación que se usará al principio de un grupo de imágenes.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo codificados por el códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Esta propiedad se reemplaza <a href="mfpkey-complexityexproperty.md"><strong>por</strong></a>MFPKEY_COMPLEXITYEX .<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Especifica la complejidad del algoritmo del codificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal. Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Especifica el tipo de optimización que se usará para el códec de perfil avanzado Windows Media Video 9.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Especifica una representación numérica del equilibrio entre la suavizado del movimiento y la calidad de la imagen en la salida del códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>No se usa.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica la plantilla de conformidad del dispositivo con la que se ajusta el contenido codificado.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Especifica la plantilla de conformidad de dispositivos que desea usar para la codificación de vídeo.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Especifica el método utilizado para codificar la información del vector de movimiento.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Especifica si el códec usará el filtro de ruido al codificar.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) basada en la calidad (1 paso).<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo descartados durante la codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica el final de un paso de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Especifica un alto de fotograma intermedio para el vídeo codificado.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Especifica un ancho de fotograma intermedio para el vídeo codificado.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Especifica si el códec debe usar el filtrado de mediana durante la codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Especifica el FOURCC que identifica el codificador que desea usar.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Obsoleto.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Especifica si el codificador puede quitar fotogramas.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Especifica si la salida del códec se entrelazará.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Especifica el tiempo máximo, en milisegundos, entre fotogramas clave en la salida del códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>No se usa.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Especifica si el códec debe usar el filtro de desbloqueo en bucle durante la codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Especifica el método de costo utilizado por el códec para determinar qué modo de macrobloqueo se va a usar.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Especifica el método que se usará para la coincidencia de movimiento.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Especifica los tipos de información de vídeo que se usan en las operaciones de búsqueda de movimiento.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Especifica el intervalo utilizado en las búsquedas de movimiento.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Especifica si el códec debe intentar detectar bordes de marco ruidosos y quitarlos.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Especifica el número de subprocesos que usará el códec para la codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica el número máximo de pases admitidos por el códec.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica el número de pases que usará el códec para codificar el contenido.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Especifica si el códec debe usar la optimización perceptual conservadora al codificar.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Especifica si el codificador genera entradas de fotogramas ficticias en la secuencia de bits para fotogramas duplicados.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Especifica QP.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Especifica el grado en que el códec debe reducir el intervalo de colores efectivo del vídeo.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pases.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Especifica si el codificador usa la búsqueda mv de subpíxeles basada en ESCRITORIO remoto. <br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Para la re-codificación de segmentos, especifica el tamaño del búfer.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Para la recodificador de segmentos, especifica la duración del segmento que se va a volver a codificar.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Para volver a codificar el segmento, especifica el cuantificador del fotograma antes del segmento inicial.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Para volver a codificar segmentos, especifica la integridad del búfer inicial.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la velocidad de bits variable de 2 pases restringida (VBR).<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo pasados al codificador durante el proceso de codificación.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica si el códec usará la codificación de velocidad de bits variable (VBR).<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Especifica el nivel de calidad real para la codificación de velocidad de bits variable (VBR) basada en calidad (1 paso).<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Especifica si el códec usará la optimización de escalado de vídeo.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Para volver a codificar segmentos, especifica los datos privados del códec del archivo que se vuelve a codificar.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Especifica el tipo de lógica que usará el códec para detectar vídeo de origen entrelazado.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Especifica el número de fotogramas de vídeo que se omitieron porque eran duplicados de fotogramas anteriores.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Solo lectura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Implementación de códec](codecimplementation.md)
</dt> </dl>

 

 
