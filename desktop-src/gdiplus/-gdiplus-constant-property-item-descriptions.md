---
description: En la lista siguiente se proporcionan descripciones de los elementos de propiedad admitidos por GDI+ de Windows.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descripciones de elementos de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636127"
---
# <a name="property-item-descriptions"></a>Descripciones de elementos de propiedad

En la lista siguiente se proporcionan descripciones de los elementos de propiedad admitidos por GDI+ de Windows. Las descripciones son breves y generales para que se apliquen a una variedad de formatos de archivo de imagen. Para obtener una descripción detallada de cómo se usa un elemento de propiedad en un formato de archivo determinado, vea la especificación de ese formato de archivo. Para obtener vínculos a varias especificaciones de archivo y otros documentos que describen los metadatos en detalle, vea [Especificaciones de formato de archivo de imagen](-gdiplus-constant-image-file-format-specifications.md).

El formato de archivo de imagen intercambiable (EXIF) es un estándar de la Asociación de desarrollo en el sector electrónico (JEIDA) de Japón, revisado el 1998 de junio como versión 2,1. Las partes de la especificación EXIF se usan con el permiso de JEIDA.

## <a name="propertytaggpsver"></a>PropertyTagGpsVer

Versión de la IFD del sistema de posicionamiento global (GPS), proporcionada como 2.0.0.0. Esta etiqueta es obligatoria cuando la etiqueta PropertyTagGpsIFD está presente. Cuando la versión es 2.0.0.0, el valor de la etiqueta es 0x02000000.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0000              |
| Tipo  | PropertyTagTypeByte |
| Count | 4                   |



 

## <a name="propertytaggpslatituderef"></a>PropertyTagGpsLatitudeRef

Cadena de caracteres terminada en null que especifica si la latitud es North o South. `N` especifica North latitud y `S` especifica South latitud.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0001                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpslatitude"></a>PropertyTagGpsLatitude

Latitud. La latitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente. Cuando se expresan los grados, los minutos y los segundos, el formato es DD/1, mm/1, SS/1. Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DD/1, mmmm/100, 0/1.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0002                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytaggpslongituderef"></a>PropertyTagGpsLongitudeRef

Cadena de caracteres terminada en null que especifica si la longitud es East o West longitud. `E` Especifica la longitud del este y `W` especifica la longitud oeste.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0003                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpslongitude"></a>PropertyTagGpsLongitude

Longitud. La longitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente. Cuando se expresan grados, minutos y segundos, el formato es DDD/1, mm/1, SS/1. Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DDD/1, mmmm/100, 0/1.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0004                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytaggpsaltituderef"></a>PropertyTagGpsAltitudeRef

Altitud de referencia, en metros.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0005              |
| Tipo  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytaggpsaltitude"></a>PropertyTagGpsAltitude

Altitud, en metros, en función de la altitud de referencia especificada por PropertyTagGpsAltitudeRef.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0006                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsgpstime"></a>PropertyTagGpsGpsTime

Hora en hora universal coordinada (UTC). El valor se expresa como tres números racionales que proporcionan la hora, el minuto y el segundo.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0007                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytaggpsgpssatellites"></a>PropertyTagGpsGpsSatellites

Cadena de caracteres terminada en null que especifica los satélites de GPS usados para las mediciones. Esta etiqueta se puede usar para especificar el número de identificación, el ángulo de elevación, Azimuth, SNR y otra información sobre cada satélite. No se ha especificado el formato. Si el receptor de GPS no es capaz de tomar medidas, el valor de la etiqueta debe establecerse en **null**.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0008                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytaggpsgpsstatus"></a>PropertyTagGpsGpsStatus

Cadena de caracteres terminada en null que especifica el estado del receptor de GPS cuando se graba la imagen. `A` significa que la medida está en curso y `V` significa que la medida es la interoperabilidad.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0009                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsgpsmeasuremode"></a>PropertyTagGpsGpsMeasureMode

Cadena de caracteres terminada en null que especifica el modo de medición del GPS. `2` Especifica la medida 2D y `3` especifica la medida 3D.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x000A                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsgpsdop"></a>PropertyTagGpsGpsDop

GPS DOP (grado de datos de precisión). Un valor HDOP se escribe durante la medida 2D y se escribe un valor PDOP durante la medida 3D.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x000B                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsspeedref"></a>PropertyTagGpsSpeedRef

Cadena de caracteres terminada en null que especifica la unidad utilizada para expresar la velocidad de movimiento del receptor GPS. `K`, `M` y `N` representan kilómetros por hora, kilómetros por hora y nudos respectivamente.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x000C                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsspeed"></a>PropertyTagGpsSpeed

Velocidad del movimiento del receptor GPS.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x000D                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpstrackref"></a>PropertyTagGpsTrackRef

Cadena de caracteres terminada en null que especifica la referencia para ofrecer la dirección del movimiento del receptor GPS. `T` Especifica la dirección verdadera y `M` especifica la dirección magnética.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x000E                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpstrack"></a>PropertyTagGpsTrack

Dirección del movimiento del receptor de GPS. El intervalo de valores está comprendido entre 0,00 y 359,99.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x000F                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsimgdirref"></a>PropertyTagGpsImgDirRef

Cadena de caracteres terminada en null que especifica la referencia para la dirección de la imagen cuando se captura. `T` Especifica la dirección verdadera y `M` especifica la dirección magnética.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0010                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsimgdir"></a>PropertyTagGpsImgDir

Dirección de la imagen cuando se capturó. El intervalo de valores está comprendido entre 0,00 y 359,99.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0011                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsmapdatum"></a>PropertyTagGpsMapDatum

Cadena de caracteres terminada en null que especifica los datos de encuesta de geodésico utilizados por el receptor de GPS. Si los datos de la encuesta están restringidos a Japón, el valor de esta etiqueta es `TOKYO` o `WGS-84` .



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0012                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytaggpsdestlatref"></a>PropertyTagGpsDestLatRef

Cadena de caracteres terminada en null que especifica si la latitud del punto de destino es North o South latitud. `N` especifica North latitud y `S` especifica South latitud.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0013                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsdestlat"></a>PropertyTagGpsDestLat

Latitud del punto de destino. La latitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente. Cuando se expresan los grados, los minutos y los segundos, el formato es DD/1, mm/1, SS/1. Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DD/1, mmmm/100, 0/1.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0014                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytaggpsdestlongref"></a>PropertyTagGpsDestLongRef

Cadena de caracteres terminada en null que especifica si la longitud del punto de destino es la longitud oriental o oeste. `E` Especifica la longitud del este y `W` especifica la longitud oeste.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0015                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsdestlong"></a>PropertyTagGpsDestLong

Longitud del punto de destino. La longitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente. Cuando se expresan los grados, los minutos y los segundos, el formato es DDD/1, mm/1, SS/1. Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DDD/1, mmmm/100, 0/1.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0016                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytaggpsdestbearref"></a>PropertyTagGpsDestBearRef

Cadena de caracteres terminada en null que especifica la referencia usada para asignar el cojinete al punto de destino. `T` Especifica la dirección verdadera y `M` especifica la dirección magnética.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0017                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsdestbear"></a>PropertyTagGpsDestBear

Cojinete hasta el punto de destino. El intervalo de valores está comprendido entre 0,00 y 359,99.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0018                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsdestdistref"></a>PropertyTagGpsDestDistRef

Cadena de caracteres terminada en null que especifica la unidad utilizada para expresar la distancia al punto de destino. K, M y N representan kilómetros, millas y nudos respectivamente.



| Información de propiedad | Value |
|-------|--------------------------------------------|
| Etiqueta   | 0x0019                                     |
| Tipo  | PropertyTagTypeASCII                       |
| Count | 2 (un carácter más el terminador nulo) |



 

## <a name="propertytaggpsdestdist"></a>PropertyTagGpsDestDist

Distancia al punto de destino.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x001A                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagnewsubfiletype"></a>PropertyTagNewSubfileType

Tipo de datos de un subarchivo.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x00FE              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagsubfiletype"></a>PropertyTagSubfileType

Tipo de datos de un subarchivo.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x00FF               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagimagewidth"></a>PropertyTagImageWidth

Número de píxeles por fila.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0100                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagimageheight"></a>PropertyTagImageHeight

Número de filas de píxeles.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0101                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagbitspersample"></a>PropertyTagBitsPerSample

Número de bits por componente de color. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0102                                   |
| Tipo  | PropertyTagTypeShort                     |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagcompression"></a>PropertyTagCompression

Esquema de compresión utilizado para los datos de la imagen.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0103               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagphotometricinterp"></a>PropertyTagPhotometricInterp

Cómo se interpretarán los datos de píxeles.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0106               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthreshholding"></a>PropertyTagThreshHolding

Técnica usada para convertir de píxeles grises a píxeles negros y blancos.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0107               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagcellwidth"></a>PropertyTagCellWidth

Ancho de la matriz de tramas o semitonos.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0108               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagcellheight"></a>PropertyTagCellHeight

Alto de la matriz de tramas o semitonos.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0109               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagfillorder"></a>PropertyTagFillOrder

Orden lógico de bits en bytes.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x010A               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagdocumentname"></a>PropertyTagDocumentName

Cadena de caracteres terminada en null que especifica el nombre del documento desde el que se examinó la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x010D                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagimagedescription"></a>PropertyTagImageDescription

Cadena de caracteres terminada en null que especifica el título de la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x010E                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagequipmake"></a>PropertyTagEquipMake

Cadena de caracteres terminada en null que especifica el fabricante del equipo usado para grabar la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x010F                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagequipmodel"></a>PropertyTagEquipModel

Cadena de caracteres terminada en null que especifica el nombre del modelo o el número de modelo del equipo usado para grabar la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0110                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagstripoffsets"></a>PropertyTagStripOffsets

Para cada franja, el desplazamiento de bytes de esa franja. Vea también [PropertyTagRowsPerStrip](#propertytagrowsperstrip) y [PropertyTagStripBytesCount](#propertytagstripbytescount).



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0111                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | Número de bandas                            |



 

## <a name="propertytagorientation"></a>PropertyTagOrientation

Orientación de imagen visualizada en términos de filas y columnas.



Etiqueta

0x0112

Tipo

PropertyTagTypeShort

Count

1

1: la fila situada en la parte superior de la imagen visual y la columna de la izquierda es el lado izquierdo del visual. 2-la fila situada en la parte superior de la imagen y la columna 0 es el lado derecho visual. 3-la fila de la 0 en la parte inferior de la imagen y la columna de la derecha es el lado derecho del visual. 4: la fila de la 0 en la parte inferior de la imagen y la columna de la izquierda es el lado izquierdo del visual. 5: la fila de la izquierda es el lado izquierdo visual de la imagen y la columna 0 es la parte superior del visual. 6-la fila de la derecha es el lado derecho visual de la imagen y la columna 0 es la parte superior del visual. 7: la fila de la derecha es el lado derecho visual de la imagen y la columna de la 0 es la parte inferior del visual. 8: la fila de la izquierda es el lado izquierdo visual de la imagen y la columna de la derecha es la parte inferior del visual.



 

## <a name="propertytagsamplesperpixel"></a>PropertyTagSamplesPerPixel

Número de componentes de color por píxel.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0115               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagrowsperstrip"></a>PropertyTagRowsPerStrip

Número de filas por franja. Vea también [PropertyTagStripBytesCount](#propertytagstripbytescount) y [PropertyTagStripOffsets](#propertytagstripoffsets).



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0116                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagstripbytescount"></a>PropertyTagStripBytesCount

Para cada franja, el número total de bytes de esa franja.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0117                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | Número de bandas                            |



 

## <a name="propertytagminsamplevalue"></a>PropertyTagMinSampleValue

Para cada componente de color, el valor mínimo asignado a ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0118                                   |
| Tipo  | PropertyTagTypeShort                     |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagmaxsamplevalue"></a>PropertyTagMaxSampleValue

Para cada componente de color, el valor máximo asignado a ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0119                                   |
| Tipo  | PropertyTagTypeShort                     |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagxresolution"></a>PropertyTagXResolution

Número de píxeles por unidad en la dirección de ancho de la imagen (x). La unidad se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x011A                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagyresolution"></a>PropertyTagYResolution

Número de píxeles por unidad en la dirección del alto de la imagen (y). La unidad se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x011B                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagplanarconfig"></a>PropertyTagPlanarConfig

Si los componentes de píxeles se registran en formato plano o fragmentado.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x011C               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagpagename"></a>PropertyTagPageName

Cadena de caracteres terminada en null que especifica el nombre de la página desde la que se examinó la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x011D                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagxposition"></a>PropertyTagXPosition

Desplazamiento desde el lado izquierdo de la página hasta el lado izquierdo de la imagen. La unidad de medida se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x011E                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagyposition"></a>PropertyTagYPosition

Desplazamiento desde la parte superior de la página hasta la parte superior de la imagen. La unidad de medida se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x011F                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagfreeoffset"></a>PropertyTagFreeOffset

Para cada cadena de bytes contiguos no utilizados, el desplazamiento de bytes de esa cadena.



| Información de propiedad | Value |
|------|---------------------|
| Etiqueta  | 0x0120              |
| Tipo | PropertyTagTypeLong |



 

## <a name="propertytagfreebytecounts"></a>PropertyTagFreeByteCounts

Para cada cadena de bytes contiguos no utilizados, el número de bytes de esa cadena.



| Información de propiedad | Value |
|-------|-----------------------------------------------|
| Etiqueta   | 0x0121                                        |
| Tipo  | PropertyTagTypeLong                           |
| Count | Número de cadenas de bytes no usados contiguos. |



 

## <a name="propertytaggrayresponseunit"></a>PropertyTagGrayResponseUnit

Precisión del número especificado por PropertyTagGrayResponseCurve. 1 especifica décimas, 2 especifica centésimas, 3 especifica milésimas, etc.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0122               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaggrayresponsecurve"></a>PropertyTagGrayResponseCurve

Para cada valor de píxel posible de una imagen de escala de grises, la densidad óptica de ese valor de píxel.



| Información de propiedad | Value |
|-------|---------------------------------|
| Etiqueta   | 0x0123                          |
| Tipo  | PropertyTagTypeShort            |
| Count | Número de valores de píxeles posibles |



 

## <a name="propertytagt4option"></a>PropertyTagT4Option

Conjunto de marcas relacionadas con la codificación T4.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0124              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagt6option"></a>PropertyTagT6Option

Conjunto de marcas relacionadas con la codificación T6.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0125              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagresolutionunit"></a>PropertyTagResolutionUnit

Unidad de medida para la resolución horizontal y la resolución vertical.



Etiqueta

0x0128

Tipo

PropertyTagTypeShort

Count

1

2 pulgadas 3-centímetro



 

## <a name="propertytagpagenumber"></a>PropertyTagPageNumber

Número de página de la página desde la que se examinó la imagen.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0129               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagtransferfunction"></a>PropertyTagTransferFunction

Tablas que especifican funciones de transferencia para la imagen.



| Información de propiedad | Value |
|-------|------------------------------------------------------|
| Etiqueta   | 0x012D                                               |
| Tipo  | PropertyTagTypeShort                                 |
| Count | Número total de palabras de 16 bits necesarias para las tablas |



 

## <a name="propertytagsoftwareused"></a>PropertyTagSoftwareUsed

Cadena de caracteres terminada en null que especifica el nombre y la versión del software o firmware del dispositivo usado para generar la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0131                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagdatetime"></a>PropertyTagDateTime

Fecha y hora en que se creó la imagen.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0132               |
| Tipo  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagartist"></a>PropertyTagArtist

Cadena de caracteres terminada en null que especifica el nombre de la persona que creó la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x013B                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytaghostcomputer"></a>PropertyTagHostComputer

Cadena de caracteres terminada en null que especifica el equipo o sistema operativo usado para crear la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x013C                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagpredictor"></a>PropertyTagPredictor

Tipo de esquema de predicción que se aplicó a los datos de imagen antes de que se aplicara el esquema de codificación.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x013D               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagwhitepoint"></a>PropertyTagWhitePoint

Cromaticidad del punto blanco de la imagen.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x013E                  |
| Tipo  | PropertyTagTypeRational |
| Count | 2                       |



 

## <a name="propertytagprimarychromaticities"></a>PropertyTagPrimaryChromaticities

Para cada uno de los tres colores primarios de la imagen, la cromaticidad de ese color.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x013F                  |
| Tipo  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytagcolormap"></a>PropertyTagColorMap

Paleta de colores (tabla de búsqueda) para una imagen indizada en una paleta.



| Información de propiedad | Value |
|-------|-------------------------------------------------|
| Etiqueta   | 0x0140                                          |
| Tipo  | PropertyTagTypeShort                            |
| Count | Número de palabras de 16 bits necesarias para la paleta |



 

## <a name="propertytaghalftonehints"></a>PropertyTagHalftoneHints

Información usada por la función de semitono



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0141               |
| Tipo  | PropertyTagTypeShort |
| Count | 2                    |



 

## <a name="propertytagtilewidth"></a>PropertyTagTileWidth

Número de columnas de píxeles en cada mosaico.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0142                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagtilelength"></a>PropertyTagTileLength

Número de filas de píxeles en cada mosaico.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0143                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagtileoffset"></a>PropertyTagTileOffset

Para cada mosaico, el desplazamiento de bytes de ese mosaico.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0144              |
| Tipo  | PropertyTagTypeLong |
| Count | Número de mosaicos     |



 

## <a name="propertytagtilebytecounts"></a>PropertyTagTileByteCounts

Para cada mosaico, el número de bytes de ese mosaico.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0145                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | Número de mosaicos                             |



 

## <a name="propertytaginkset"></a>PropertyTagInkSet

Conjunto de tintas utilizadas en una imagen separada.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x014C               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaginknames"></a>PropertyTagInkNames

Secuencia de cadenas de caracteres concatenadas y terminadas en null que especifican los nombres de las tintas utilizadas en una imagen separada.



| Información de propiedad | Value |
|-------|------------------------------------------------------------------------|
| Etiqueta   | 0x014D                                                                 |
| Tipo  | PropertyTagTypeASCII                                                   |
| Count | Longitud total de la secuencia de cadenas, incluidos los terminadores NULL |



 

## <a name="propertytagnumberofinks"></a>PropertyTagNumberOfInks

Número de tintas.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x014E               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagdotrange"></a>PropertyTagDotRange

Valores de componente de color que corresponden a un punto de 0% y un punto de 100%.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x0150                                      |
| Tipo  | PropertyTagTypeByte o PropertyTagTypeShort |
| Count | 2 o 2 × PropertyTagSamplesPerPixel           |



 

## <a name="propertytagtargetprinter"></a>PropertyTagTargetPrinter

Cadena de caracteres terminada en null que describe el entorno de impresión previsto.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0151                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagextrasamples"></a>PropertyTagExtraSamples

Número de componentes de color adicionales. Por ejemplo, un componente adicional podría contener un valor alfa.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0152               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagsampleformat"></a>PropertyTagSampleFormat

Para cada componente de color, el formato numérico (sin signo, firmado, punto flotante) de ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0153                                   |
| Tipo  | PropertyTagTypeShort                     |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagsminsamplevalue"></a>PropertyTagSMinSampleValue

Para cada componente de color, el valor mínimo de ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|-----------------------------------------------------|
| Etiqueta   | 0x0154                                              |
| Tipo  | El tipo que mejor coincide con los datos del componente de píxeles |
| Count | Número de muestras (componentes) por píxel            |



 

## <a name="propertytagsmaxsamplevalue"></a>PropertyTagSMaxSampleValue

Para cada componente de color, el valor máximo de ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|-----------------------------------------------------|
| Etiqueta   | 0x0155                                              |
| Tipo  | El tipo que mejor coincide con los datos del componente de píxeles |
| Count | Número de muestras (componentes) por píxel            |



 

## <a name="propertytagtransferrange"></a>PropertyTagTransferRange

Tabla de valores que extiende el intervalo de la función de transferencia.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0156               |
| Tipo  | PropertyTagTypeShort |
| Count | 6                    |



 

## <a name="propertytagjpegproc"></a>PropertyTagJPEGProc

Proceso de compresión JPEG.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0200               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagjpeginterformat"></a>PropertyTagJPEGInterFormat

Desplazamiento al inicio de un fragmentada JPEG.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0201              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagjpeginterlength"></a>PropertyTagJPEGInterLength

Longitud, en bytes, del fragmentada JPEG.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x0202              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagjpegrestartinterval"></a>PropertyTagJPEGRestartInterval

Longitud del intervalo de reinicio.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0203               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagjpeglosslesspredictors"></a>PropertyTagJPEGLosslessPredictors

Para cada componente de color, valor de la selección de predictor sin pérdida para ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0205                                   |
| Tipo  | PropertyTagTypeShort                     |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagjpegpointtransforms"></a>PropertyTagJPEGPointTransforms

Para cada componente de color, un valor de transformación de punto para ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0206                                   |
| Tipo  | PropertyTagTypeShort                     |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagjpegqtables"></a>PropertyTagJPEGQTables

Para cada componente de color, el desplazamiento a la tabla de cuantificación de ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0207                                   |
| Tipo  | PropertyTagTypeLong                      |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagjpegdctables"></a>PropertyTagJPEGDCTables

Para cada componente de color, el desplazamiento a la tabla Huffman del DC (o tabla Huffman sin pérdida) para ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0208                                   |
| Tipo  | PropertyTagTypeLong                      |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagjpegactables"></a>PropertyTagJPEGACTables

Para cada componente de color, el desplazamiento a la tabla de la tabla de alimentación de CA para ese componente. Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Información de propiedad | Value |
|-------|------------------------------------------|
| Etiqueta   | 0x0209                                   |
| Tipo  | PropertyTagTypeLong                      |
| Count | Número de muestras (componentes) por píxel |



 

## <a name="propertytagycbcrcoefficients"></a>PropertyTagYCbCrCoefficients

Coeficientes para la transformación de datos de imagen de RGB a YCbCr.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0211                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytagycbcrsubsampling"></a>PropertyTagYCbCrSubsampling

Relación de muestreo de los componentes de crominancia en relación con el componente de luminancia.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0212               |
| Tipo  | PropertyTagTypeShort |
| Count | 2                    |



 

## <a name="propertytagycbcrpositioning"></a>PropertyTagYCbCrPositioning

Posición de los componentes de crominancia en relación con el componente de luminancia.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x0213               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagrefblackwhite"></a>PropertyTagREFBlackWhite

Valor de punto negro de referencia y valor de punto blanco de referencia.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0214                  |
| Tipo  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytaggamma"></a>PropertyTagGamma

Valor gamma asociado a la imagen. El valor gamma se almacena como un número racional (par de **Long**) con un numerador de 100000. Por ejemplo, un valor gamma de 2,2 se almacena como el par (100000, 45455).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x0301                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagiccprofiledescriptor"></a>PropertyTagICCProfileDescriptor

Cadena de caracteres terminada en null que identifica un perfil ICC.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0302                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagsrgbrenderingintent"></a>PropertyTagSRGBRenderingIntent

Cómo debe mostrarse la imagen tal como la define el International color Consortium (ICC). Si un objeto de  [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ se construye con el parámetro *UseEmbeddedColorManagement* establecido en **true**, GDI+ representa la imagen según el intento de representación especificado. La intención se puede establecer en perceptual, relative colorimétrica, saturación o colorimétrico absoluto.

-   La intención perceptual, que es adecuada para las fotografías, proporciona una buena adaptación a la gama de la pantalla del dispositivo a costa de la precisión colorimétrica.
-   La intención colorimétrica relativa es adecuada para las imágenes (por ejemplo, logotipos) que requieren una coincidencia de aspecto de color relativa al punto blanco del dispositivo de pantalla.
-   La intención de saturación, que es adecuada para gráficos y gráficos, conserva la saturación a costa del matiz y la luminosidad.
-   La intención de colorimétrico absoluto es adecuada para las pruebas (vistas previas de imágenes destinadas a un dispositivo de pantalla diferente) que requieran la preservación de la colorimétrico absoluta.



Etiqueta

0x0303

Tipo

BYTE

Count

1

0-percepción 1-colorimétrico relativo 2-saturación 3-colorimétrico absoluto



 

## <a name="propertytagimagetitle"></a>PropertyTagImageTitle

Cadena de caracteres terminada en null que especifica el título de la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x0320                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagresolutionxunit"></a>PropertyTagResolutionXUnit

Unidades en las que se va a mostrar la resolución horizontal.



Etiqueta

0x5001

Tipo

PropertyTagTypeShort

Count

1

1-píxeles por pulgada 2-píxeles por centímetro



 

## <a name="propertytagresolutionyunit"></a>PropertyTagResolutionYUnit

Unidades en las que se va a mostrar la resolución vertical.



Etiqueta

0x5002

Tipo

PropertyTagTypeShort

Count

1

1-píxeles por pulgada 2-píxeles por centímetro



 

## <a name="propertytagresolutionxlengthunit"></a>PropertyTagResolutionXLengthUnit

Unidades en las que se va a mostrar el ancho de la imagen.



Etiqueta

0x5003

Tipo

PropertyTagTypeShort

Count

1

1 PDA 2-centímetros 3 puntos 4-picas 5-columnas



 

## <a name="propertytagresolutionylengthunit"></a>PropertyTagResolutionYLengthUnit

Unidades en las que se va a mostrar el alto de la imagen.



Etiqueta

0x5004

Tipo

PropertyTagTypeShort

Count

1

1 PDA 2-centímetros 3 puntos 4-picas 5-columnas



 

## <a name="propertytagprintflags"></a>PropertyTagPrintFlags

Secuencia de valores booleanos de un byte que especifican las opciones de impresión.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5005               |
| Tipo  | PropertyTagTypeASCII |
| Count | Número de marcas      |



 

## <a name="propertytagprintflagsversion"></a>PropertyTagPrintFlagsVersion

Versión de marcas de impresión.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5006               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagprintflagscrop"></a>PropertyTagPrintFlagsCrop

Marcas de recorte del centro de marcas de impresión.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5007              |
| Tipo  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagprintflagsbleedwidth"></a>PropertyTagPrintFlagsBleedWidth

Ancho de sangría de marcas de impresión



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5008              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a>PropertyTagPrintFlagsBleedWidthScale

Escala de ancho de sangría de marcas de impresión



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5009               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaghalftonelpi"></a>PropertyTagHalftoneLPI

Frecuencia de la pantalla de la tinta, en líneas por pulgada.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x500A                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaghalftonelpiunit"></a>PropertyTagHalftoneLPIUnit

Unidades para la frecuencia de la pantalla.



Etiqueta

0x500B

Tipo

PropertyTagTypeShort

Count

1

1-líneas por pulgada de 2 líneas por centímetro



 

## <a name="propertytaghalftonedegree"></a>PropertyTagHalftoneDegree

Ángulo de la pantalla.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x500C                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaghalftoneshape"></a>PropertyTagHalftoneShape

Forma de los puntos de semitono.



Etiqueta

0x500D

Tipo

PropertyTagTypeShort

Count

1

0-redondo 1-elipse 2-línea 3-cuadrado 4-Cruz 6-rombo



 

## <a name="propertytaghalftonemisc"></a>PropertyTagHalftoneMisc

Información de semitono diversa.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x500E              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytaghalftonescreen"></a>PropertyTagHalftoneScreen

Valor booleano que especifica si se van a utilizar las pantallas predeterminadas de la impresora.



Etiqueta

0x500F

Tipo

PropertyTagTypeByte

Count

1

1-usar las pantallas predeterminadas de la impresora 2-otras



 

## <a name="propertytagjpegquality"></a>PropertyTagJPEGQuality

Etiqueta privada utilizada por el formato de Adobe Photoshop. No disponible para uso público.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5010               |
| Tipo  | PropertyTagTypeShort |
| Count | Any                  |



 

## <a name="propertytaggridsize"></a>PropertyTagGridSize

Bloque de información sobre cuadrículas y guías.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x5011                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

## <a name="propertytagthumbnailformat"></a>PropertyTagThumbnailFormat

Formato de la imagen en miniatura.



Etiqueta

0x5012

Tipo

PropertyTagTypeLong

Count

1

0-RGB sin formato 1-JPEG



 

## <a name="propertytagthumbnailwidth"></a>PropertyTagThumbnailWidth

Ancho, en píxeles, de la imagen en miniatura.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5013              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailheight"></a>PropertyTagThumbnailHeight

Alto, en píxeles, de la imagen en miniatura.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5014              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailcolordepth"></a>PropertyTagThumbnailColorDepth

bits por píxel (BPP) para la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5015               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailplanes"></a>PropertyTagThumbnailPlanes

Número de planos de color de la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5016               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrawbytes"></a>PropertyTagThumbnailRawBytes

Desplazamiento de bytes entre filas de datos de píxeles.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5017              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailsize"></a>PropertyTagThumbnailSize

Tamaño total, en bytes, de la imagen en miniatura.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5018              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailcompressedsize"></a>PropertyTagThumbnailCompressedSize

Tamaño comprimido, en bytes, de la imagen en miniatura.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5019              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagcolortransferfunction"></a>PropertyTagColorTransferFunction

Tabla de valores que especifican las funciones de transferencia de color.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x501A                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

## <a name="propertytagthumbnaildata"></a>PropertyTagThumbnailData

Bits de miniaturas sin formato en formato JPEG o RGB. Depende de PropertyTagThumbnailFormat.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x501B              |
| Tipo  | PropertyTagTypeByte |
| Count | Variable            |



 

## <a name="propertytagthumbnailimagewidth"></a>PropertyTagThumbnailImageWidth

Número de píxeles por fila de la imagen en miniatura.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x5020                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailimageheight"></a>PropertyTagThumbnailImageHeight

Número de filas de píxeles de la imagen en miniatura.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x5021                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailbitspersample"></a>PropertyTagThumbnailBitsPerSample

Número de bits por componente de color de la imagen en miniatura. Vea también [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).



| Información de propiedad | Value |
|-------|-----------------------------------------------------------------|
| Etiqueta   | 0x5022                                                          |
| Tipo  | PropertyTagTypeShort                                            |
| Count | Número de muestras (componentes) por píxel en la imagen en miniatura |



 

## <a name="propertytagthumbnailcompression"></a>PropertyTagThumbnailCompression

Esquema de compresión utilizado para los datos de imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5023               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a>PropertyTagThumbnailPhotometricInterp

Cómo se interpretarán los datos de píxeles en miniatura.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5024               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailimagedescription"></a>PropertyTagThumbnailImageDescription

Cadena de caracteres terminada en null que especifica el título de la imagen.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x5025                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagthumbnailequipmake"></a>PropertyTagThumbnailEquipMake

Cadena de caracteres terminada en null que especifica el fabricante del equipo usado para grabar la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x5026                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagthumbnailequipmodel"></a>PropertyTagThumbnailEquipModel

Cadena de caracteres terminada en null que especifica el nombre del modelo o el número de modelo del equipo usado para grabar la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x5027                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagthumbnailstripoffsets"></a>PropertyTagThumbnailStripOffsets

Para cada franja de la imagen en miniatura, el desplazamiento de bytes de esa franja. Vea también [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) y [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x5028                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | Número de bandas                            |



 

## <a name="propertytagthumbnailorientation"></a>PropertyTagThumbnailOrientation

Orientación de la imagen en miniatura en términos de filas y columnas. Vea también [PropertyTagOrientation](#propertytagorientation).



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5029               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a>PropertyTagThumbnailSamplesPerPixel

Número de componentes de color por píxel en la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x502A               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a>PropertyTagThumbnailRowsPerStrip

Número de filas por franja en la imagen en miniatura. Vea también [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) y [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x502B                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a>PropertyTagThumbnailStripBytesCount

Para cada franja de imagen en miniatura, el número total de bytes de esa franja.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0x502C                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | Número de bandas en la imagen en miniatura     |



 

## <a name="propertytagthumbnailresolutionx"></a>PropertyTagThumbnailResolutionX

Resolución de miniaturas en la dirección de ancho. La unidad de resolución se proporciona en [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Información de propiedad | Value |
|-----|--------|
| Etiqueta | 0x502D |



 

## <a name="propertytagthumbnailresolutiony"></a>PropertyTagThumbnailResolutionY

Resolución de miniaturas en la dirección de alto. La unidad de resolución se proporciona en [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Información de propiedad | Value |
|-----|--------|
| Etiqueta | 0x502E |



 

## <a name="propertytagthumbnailplanarconfig"></a>PropertyTagThumbnailPlanarConfig

Si los componentes de píxeles de la imagen en miniatura se registran en formato plano o fragmentado. Vea también [PropertyTagPlanarConfig](#propertytagplanarconfig).



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x502F               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailresolutionunit"></a>PropertyTagThumbnailResolutionUnit

Unidad de medida para la resolución horizontal y la resolución vertical de la imagen en miniatura. Vea también [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5030               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailtransferfunction"></a>PropertyTagThumbnailTransferFunction

Tablas que especifican funciones de transferencia para la imagen en miniatura. Vea también [PropertyTagTransferFunction](#propertytagtransferfunction).



| Información de propiedad | Value |
|-------|------------------------------------------------------|
| Etiqueta   | 0x5031                                               |
| Tipo  | PropertyTagTypeShort                                 |
| Count | Número total de palabras de 16 bits necesarias para las tablas |



 

## <a name="propertytagthumbnailsoftwareused"></a>PropertyTagThumbnailSoftwareUsed

Cadena de caracteres terminada en null que especifica el nombre y la versión del software o firmware del dispositivo usado para generar la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x5032                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagthumbnaildatetime"></a>PropertyTagThumbnailDateTime

Fecha y hora en que se creó la imagen en miniatura. Vea también [PropertyTagDateTime](#propertytagdatetime).



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5033               |
| Tipo  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagthumbnailartist"></a>PropertyTagThumbnailArtist

Cadena de caracteres terminada en null que especifica el nombre de la persona que creó la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x5034                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagthumbnailwhitepoint"></a>PropertyTagThumbnailWhitePoint

Cromaticidad del punto blanco de la imagen en miniatura. Vea también [PropertyTagWhitePoint](#propertytagwhitepoint).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x5035                  |
| Tipo  | PropertyTagTypeRational |
| Count | 2                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a>PropertyTagThumbnailPrimaryChromaticities

Para cada uno de los tres colores primarios de la imagen en miniatura, la cromaticidad de ese color. Vea también [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x5036                  |
| Tipo  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a>PropertyTagThumbnailYCbCrCoefficients

Coeficientes para la transformación de datos de RGB a YCbCr para la imagen en miniatura. Vea también [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x5037                  |
| Tipo  | PropertyTagTypeRational |
| Count | 3                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a>PropertyTagThumbnailYCbCrSubsampling

Relación de muestreo de los componentes de crominancia en relación con el componente de luminancia de la imagen en miniatura. Vea también [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5038               |
| Tipo  | PropertyTagTypeShort |
| Count | 2                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a>PropertyTagThumbnailYCbCrPositioning

Posición de los componentes de crominancia en relación con el componente de luminancia de la imagen en miniatura. Vea también [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5039               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a>PropertyTagThumbnailRefBlackWhite

Valor de punto negro de referencia y valor de punto blanco de referencia para la imagen en miniatura. Vea también [PropertyTagREFBlackWhite](#propertytagrefblackwhite).



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x503A                  |
| Tipo  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytagthumbnailcopyright"></a>PropertyTagThumbnailCopyRight

Cadena de caracteres terminada en null que contiene información de copyright para la imagen en miniatura.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x503B                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagluminancetable"></a>PropertyTagLuminanceTable

Tabla de luminancia. La tabla luminancia y la tabla crominancia se utilizan para controlar la calidad JPEG. Una tabla de luminancia o crominancia válida tiene 64 entradas de tipo PropertyTagTypeShort. Si una imagen tiene una tabla de luminancia o una tabla de crominancia, debe tener ambas tablas.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5090               |
| Tipo  | PropertyTagTypeShort |
| Count | 64                   |



 

## <a name="propertytagchrominancetable"></a>PropertyTagChrominanceTable

Tabla de crominancia. La tabla luminancia y la tabla crominancia se utilizan para controlar la calidad JPEG. Una tabla de luminancia o crominancia válida tiene 64 entradas de tipo PropertyTagTypeShort. Si una imagen tiene una tabla de luminancia o una tabla de crominancia, debe tener ambas tablas.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5091               |
| Tipo  | PropertyTagTypeShort |
| Count | 64                   |



 

## <a name="propertytagframedelay"></a>PropertyTagFrameDelay

Tiempo de retardo, en centésimas de segundo, entre dos marcos en una imagen GIF animada.



| Información de propiedad | Value |
|-------|-------------------------------|
| Etiqueta   | 0x5100                        |
| Tipo  | PropertyTagTypeLong           |
| Count | Número de fotogramas de la imagen |



 

## <a name="propertytagloopcount"></a>PropertyTagLoopCount

En el caso de una imagen GIF animada, el número de veces que se va a mostrar la animación. Un valor de 0 especifica que la animación debe mostrarse infinitamente.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x5101               |
| Tipo  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagglobalpalette"></a>PropertyTagGlobalPalette

Paleta de colores para un mapa de bits indizado en una imagen GIF.



| Información de propiedad | Value |
|-------|-------------------------------|
| Etiqueta   | 0x5102                        |
| Tipo  | PropertyTagTypeByte           |
| Count | 3 x número de entradas de la paleta |



 

## <a name="propertytagindexbackground"></a>PropertyTagIndexBackground

Índice del color de fondo de la paleta de una imagen GIF.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5103              |
| Tipo  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagindextransparent"></a>PropertyTagIndexTransparent

Índice del color transparente en la paleta de una imagen GIF.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5104              |
| Tipo  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagpixelunit"></a>PropertyTagPixelUnit

Unidad para PropertyTagPixelPerUnitX y PropertyTagPixelPerUnitY.



Etiqueta

0x5110

Tipo

PropertyTagTypeByte

Count

1

0: desconocido



 

## <a name="propertytagpixelperunitx"></a>PropertyTagPixelPerUnitX

Píxeles por unidad en la dirección x.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5111              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagpixelperunity"></a>PropertyTagPixelPerUnitY

Píxeles por unidad en la dirección y.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x5112              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagpalettehistogram"></a>PropertyTagPaletteHistogram

Histograma de la paleta.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x5113                  |
| Tipo  | PropertyTagTypeByte     |
| Count | Longitud del histograma |



 

## <a name="propertytagcopyright"></a>PropertyTagCopyright

Cadena de caracteres terminada en null que contiene información de copyright.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x8298                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagexifexposuretime"></a>PropertyTagExifExposureTime

Tiempo de exposición, medido en segundos.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x829A                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffnumber"></a>PropertyTagExifFNumber

F número.



| Información de propiedad | Value |
|-------|----------|
| Etiqueta   | 0x829D   |
| Tipo  | LÓGICO |
| Count | 1        |



 

## <a name="propertytagexififd"></a>PropertyTagExifIFD

Etiqueta privada utilizada por GDI+. No disponible para uso público. GDI+ utiliza esta etiqueta para buscar información específica de EXIF.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x8769              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagiccprofile"></a>PropertyTagICCProfile

Perfil ICC incrustado en la imagen.



| Información de propiedad | Value |
|-------|-----------------------|
| Etiqueta   | 0x8773                |
| Tipo  | PropertyTagTypeByte   |
| Count | Longitud del perfil |



 

## <a name="propertytagexifexposureprog"></a>PropertyTagExifExposureProg

Clase del programa que usa la cámara para establecer la exposición cuando se toma la imagen.



Etiqueta

0x8822

Tipo

SHORT

Count

1

Valor predeterminado

0

0-no definido 1-manual 2-programa normal 3-apertura prioridad 4-valor de obturación 5-Programa creativo (sesgado hacia la profundidad de campo) 6-Action Program (sesgado hacia la velocidad rápida). velocidad de obturación) 7: modo vertical (para las fotografías de primer plano con el fondo desenfocado) en modo de 8 horizontal (para las fotos horizontales con el foco de fondo) de 9 a 255: reservado



 

## <a name="propertytagexifspectralsense"></a>PropertyTagExifSpectralSense

Cadena de caracteres terminada en null que especifica la sensibilidad espectral de cada canal de la cámara utilizada. La cadena es compatible con el estándar desarrollado por el Comité técnico de ASTM.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x8824                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytaggpsifd"></a>PropertyTagGpsIFD

Desplazamiento a un bloque de elementos de propiedad GPS. Los elementos de propiedad cuyas etiquetas tienen el prefijo PropertyTagGps se almacenan en el bloque de GPS. Los elementos de propiedad de GPS se definen en la especificación EXIF. GDI+ utiliza esta etiqueta para buscar información GPS, pero GDI+ no expone esta etiqueta para su uso público.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0x8825              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagexifisospeed"></a>PropertyTagExifISOSpeed

Velocidad ISO e ISO latitud de la cámara o dispositivo de entrada tal y como se especifica en ISO 12232.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x8827               |
| Tipo  | PropertyTagTypeShort |
| Count | Any                  |



 

## <a name="propertytagexifoecf"></a>PropertyTagExifOECF

Función de conversión Optoelectronic (OECF) especificada en ISO 14524. OECF es la relación entre los valores de entrada óptica de cámara y de imagen.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x8828                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

## <a name="propertytagexifver"></a>PropertyTagExifVer

Versión del estándar EXIF compatible. La no existencia de este campo se toma para hacer referencia a la no conformidad con el estándar. La conformidad con el estándar se indica grabando 0210 como una cadena ASCII de 4 bytes. Dado que el tipo es PropertyTagTypeUndefined, no hay ningún terminador nulo.



| Información de propiedad | Value |
|---------|--------------------------|
| Etiqueta     | 0x9000                   |
| Tipo    | PropertyTagTypeUndefined |
| Count   | 4                        |
| Valor predeterminado | 0210                     |



 

## <a name="propertytagexifdtorig"></a>PropertyTagExifDTOrig

Fecha y hora en que se generaron los datos de imagen originales. Para un DSC, la fecha y la hora en que se tomó la imagen. El formato es AAAA: MM: DD HH: MM: SS con la hora que se muestra en formato de 24 horas y la fecha y hora separadas por un carácter en blanco (0x2000). La longitud de la cadena de caracteres es de 20 bytes, incluido el terminador NULL. Cuando el campo está vacío, se trata como desconocido.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x9003               |
| Tipo  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagexifdtdigitized"></a>PropertyTagExifDTDigitized

Fecha y hora en que se almacenó la imagen como datos digitales. Por ejemplo, si DSC ha capturado una imagen y, al mismo tiempo, se grabó el archivo, DateTimeOriginal y DateTimeDigitized tendrán el mismo contenido.

El formato es AAAA: MM: DD HH: MM: SS con la hora que se muestra en formato de 24 horas y la fecha y hora separadas por un carácter en blanco (0x2000). La longitud de la cadena de caracteres es de 20 bytes, incluido el terminador NULL. Cuando el campo está vacío, se trata como desconocido.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0x9004               |
| Tipo  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagexifcompconfig"></a>PropertyTagExifCompConfig

Información específica de los datos comprimidos. Los canales de cada componente se organizan en orden desde el primer componente hasta el cuarto. En el caso de los datos sin comprimir, la organización de datos se proporciona en la etiqueta PropertyTagPhotometricInterp.

Sin embargo, dado que PropertyTagPhotometricInterp solo puede expresar el orden de Y, CB y CR, esta etiqueta se proporciona para los casos en los que los datos comprimidos usan componentes distintos de Y, CB y CR, y para admitir otras secuencias.



Etiqueta

0x9101

Tipo

PropertyTagTypeUndefined

Count

4

Valor predeterminado

4 5 6 0 (si RGB no comprimido) 1 2 3 0 (otros casos)

0: no existe 1-Y 2-CB 3-CR 4-R 5-G 6-B Other-Reserved



 

## <a name="propertytagexifcompbpp"></a>PropertyTagExifCompBPP

Información específica de los datos comprimidos. El modo de compresión utilizado para una imagen comprimida se indica en unidad BPP.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x9102                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifshutterspeed"></a>PropertyTagExifShutterSpeed

Velocidad del obturador. La unidad es el sistema aditivo de valor de exposición fotográfica (vértice).



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x9201                   |
| Tipo  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifaperture"></a>PropertyTagExifAperture

Abertura de la lente. La unidad es el valor de APEX.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x9202                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifbrightness"></a>PropertyTagExifBrightness

Valor de brillo. La unidad es el valor de APEX. Normalmente, se proporciona en el intervalo de-99,99 a 99,99.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x9203                   |
| Tipo  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifexposurebias"></a>PropertyTagExifExposureBias

Tendencia de exposición. La unidad es el valor de APEX. Normalmente, se proporciona en el intervalo de-99,99 a 99,99.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x9204                   |
| Tipo  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifmaxaperture"></a>PropertyTagExifMaxAperture

Número F más pequeño de la lente. La unidad es el valor de APEX. Normalmente, se proporciona en el intervalo de 00,00 a 99,99, pero no se limita a este intervalo.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x9205                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifsubjectdist"></a>PropertyTagExifSubjectDist

Distancia al asunto, medida en metros.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x9206                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifmeteringmode"></a>PropertyTagExifMeteringMode

Modo de medición.



Etiqueta

0x9207

Tipo

PropertyTagTypeShort

Count

1

Valor predeterminado

0

0-desconocido 1-promedio 2-CenterWeightedAverage 3-punto 4-multiposición 5-patrón 6-parcial 7 a 254-reservado 255-otro



 

## <a name="propertytagexiflightsource"></a>PropertyTagExifLightSource

Tipo de fuente de luz.



Etiqueta

0x9208

Tipo

PropertyTagTypeShort

Count

1

Valor predeterminado

0

0-desconocido 1-horario de verano 2-Flourescent 3-Tungsten 17-luz estándar A 18-estándar Light B 19-estándar claro C 20-D55 21-D65 22-D75 23 a 254-reservado 255-otro



 

## <a name="propertytagexifflash"></a>PropertyTagExifFlash

Estado de Flash. Esta etiqueta se registra cuando se toma una imagen mediante una luz estroboscópica (Flash). Bit 0 indica el estado de activación de Flash y los bits 1 y 2 indican el estado de retorno de Flash.



Etiqueta

0x9209

Tipo

PropertyTagTypeShort

Count

1

Valores de bit 0 que indican si el flash activado: 0B-Flash no se ha desencadenado 1B-flash activado

Valores de los bits 1 y 2 que indican el estado de devuelto Light: 00B-no se detectó la función de detección de devoluciones estroboscópica 01B-Reserved 10B-luz de retorno de luz estroboscópica no detectada 11b-luz de retorno de luz estroboscópica detectada

Valores de etiqueta Flash resultantes: 0x0000-Flash no activó 0x0001-Flash 0x0005-luz de retorno de luz estroboscópica no detectada



 

## <a name="propertytagexiffocallength"></a>PropertyTagExifFocalLength

La longitud focal real, en milímetros, de la lente. La conversión no se realiza en la longitud focal de una cámara de película 35 milímetros.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0x920A                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifmakernote"></a>PropertyTagExifMakerNote

Etiqueta de nota. Etiqueta utilizada por los fabricantes de escritores EXIF para registrar información. El contenido depende del fabricante.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x927C                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

## <a name="propertytagexifusercomment"></a>PropertyTagExifUserComment

Etiqueta de comentario. Una etiqueta utilizada por los usuarios EXIF para escribir palabras clave o comentarios sobre la imagen, además de los de PropertyTagImageDescription y sin las limitaciones de código de carácter de la etiqueta PropertyTagImageDescription.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0x9286                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

El código de carácter que se usa en la etiqueta PropertyTagExifUserComment se identifica en función de un código de identificador en un área fija de 8 bytes al principio del área de datos de etiqueta. La parte no utilizada del área se rellena con caracteres nulos (0). Los códigos de identificador se asignan por medio del registro. Dado que el tipo no es ASCII, no es necesario utilizar un terminador nulo.

## <a name="propertytagexifdtsubsec"></a>PropertyTagExifDTSubsec

Cadena de caracteres terminada en null que especifica una fracción de segundo para la etiqueta PropertyTagDateTime.



| Información de propiedad | Value |
|-------|----------------------------------------------------|
| Etiqueta   | 0x9290                                             |
| Tipo  | PropertyTagTypeASCII                               |
| Count | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagexifdtorigss"></a>PropertyTagExifDTOrigSS

Cadena de caracteres terminada en null que especifica una fracción de segundo para la etiqueta PropertyTagExifDTOrig.



| Información de propiedad | Value |
|------|----------------------------------------------------|
| Etiqueta  | 0x9291                                             |
| Tipo | PropertyTagTypeASCII                               |
| N    | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagexifdtdigss"></a>PropertyTagExifDTDigSS

Cadena de caracteres terminada en null que especifica una fracción de segundo para la etiqueta PropertyTagExifDTDigitized.



| Información de propiedad | Value |
|------|----------------------------------------------------|
| Etiqueta  | 0x9292                                             |
| Tipo | ASCII                                              |
| N    | Longitud de la cadena, incluido el terminador NULL |



 

## <a name="propertytagexiffpxver"></a>PropertyTagExifFPXVer

Versión de formato de FlashPix compatible con un archivo FPXR. Si la función FPXR admite el formato de FlashPix versión 1,0, esto se indica de forma similar a PropertyTagExifVer grabando 0100 como una cadena ASCII de 4 bytes. Dado que el tipo es PropertyTagTypeUndefined, no hay ningún terminador nulo.



Etiqueta

0xA000

Tipo

PropertyTagTypeUndefined

Count

4

Valor predeterminado

0100

0100: formato FlashPix versión 1,0 otros: reservados



 

## <a name="propertytagexifcolorspace"></a>PropertyTagExifColorSpace

Especificador de espacio de colores. Normalmente, sRGB (= 1) se usa para definir el espacio de colores en función del entorno y las condiciones del monitor de PC. Si se utiliza un espacio de colores distinto de sRGB, se establece sin calibración (= 0xFFFF). Los datos de imagen grabados como no calibrados se pueden tratar como sRGB cuando se convierten en FlashPix.



Etiqueta

0xA001

Tipo

PropertyTagTypeShort

Count

1

0x1-sRGB 0xFFFF-otro no calibrado: reservado



 

## <a name="propertytagexifpixxdim"></a>PropertyTagExifPixXDim

Información específica de los datos comprimidos. Cuando se graba un archivo comprimido, se debe grabar el ancho válido de la imagen significativa en esta etiqueta, independientemente de si hay datos de relleno o un marcador de reinicio. Esta etiqueta no debe existir en un archivo sin comprimir.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0xA002                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagexifpixydim"></a>PropertyTagExifPixYDim

Información específica de los datos comprimidos. Cuando se graba un archivo comprimido, se debe grabar el alto válido de la imagen significativa en esta etiqueta independientemente de si hay datos de relleno o un marcador de reinicio. Esta etiqueta no debe existir en un archivo sin comprimir. Dado que el relleno de datos no es necesario en la dirección vertical, el número de líneas registradas en esta etiqueta de alto de imagen válida será el mismo que se registró en Soft.



| Información de propiedad | Value |
|-------|---------------------------------------------|
| Etiqueta   | 0xA003                                      |
| Tipo  | PropertyTagTypeShort o PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagexifrelatedwav"></a>PropertyTagExifRelatedWav

Nombre de un archivo de audio relacionado con los datos de la imagen. La única información relacional registrada es el nombre y la extensión de archivo de audio EXIF (una cadena ASCII que consta de 8 caracteres más un punto (.), más 3 caracteres). La ruta de acceso no se registra. Cuando se usa esta etiqueta, los archivos de audio deben registrarse de acuerdo con el formato de audio EXIF. Los escritores también pueden almacenar datos de audio dentro de APP2 como datos de flujo de extensión de FlashPix.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0xA004               |
| Tipo  | PropertyTagTypeASCII |
| Count | 13                   |



 

## <a name="propertytagexifinterop"></a>PropertyTagExifInterop

Desplazamiento a un bloque de elementos de propiedad que contienen información de interoperabilidad.



| Información de propiedad | Value |
|-------|---------------------|
| Etiqueta   | 0xA005              |
| Tipo  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagexifflashenergy"></a>PropertyTagExifFlashEnergy

Energía de luz estroboscópica, en la vela de luz de los segundos (BCPS), en el momento en que se capturó la imagen.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0xA20B                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifspatialfr"></a>PropertyTagExifSpatialFR

Valores de tabla y SFR de frecuencia espacial del dispositivo de entrada y de cámara en el ancho de la imagen, el alto de la imagen y la dirección diagonal, tal como se especifica en ISO 12233.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0xA20C                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

## <a name="propertytagexiffocalxres"></a>PropertyTagExifFocalXRes

Número de píxeles en la dirección de ancho de la imagen (x) por unidad en el plano focal de la cámara. La unidad se especifica en PropertyTagExifFocalResUnit.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0xA20E                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffocalyres"></a>PropertyTagExifFocalYRes

Número de píxeles en la dirección de alto (y) de la imagen por unidad en el plano focal de la cámara. La unidad se especifica en PropertyTagExifFocalResUnit.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0xA20F                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffocalresunit"></a>PropertyTagExifFocalResUnit

Unidad de medida para PropertyTagExifFocalXRes y PropertyTagExifFocalYRes.



Etiqueta

0xA210

Tipo

PropertyTagTypeShort

Count

1

2 pulgadas 3-centímetro



 

## <a name="propertytagexifsubjectloc"></a>PropertyTagExifSubjectLoc

Ubicación del asunto principal de la escena. El valor de esta etiqueta representa el píxel del centro del asunto principal relativo al borde izquierdo. El primer valor indica el número de columna y el segundo valor indica el número de fila.



| Información de propiedad | Value |
|-------|----------------------|
| Etiqueta   | 0xA214               |
| Tipo  | PropertyTagTypeShort |
| Count | 2                    |



 

## <a name="propertytagexifexposureindex"></a>PropertyTagExifExposureIndex

Índice de exposición seleccionado en la cámara o dispositivo de entrada en el momento en que se capturó la imagen.



| Información de propiedad | Value |
|-------|-------------------------|
| Etiqueta   | 0xA215                  |
| Tipo  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifsensingmethod"></a>PropertyTagExifSensingMethod

Tipo de sensor de imagen en la cámara o dispositivo de entrada.



Etiqueta

0xA217

Tipo

PropertyTagTypeShort

Count

1

1: sensor de área de color de dos chips de 3 a 2: sensor de área de color de dos chips 4-tres-chip sensor de área de color 5-sensor de área 3D de sensor trilineal de 8 colores sensor lineal de color 2-reservado



 

## <a name="propertytagexiffilesource"></a>PropertyTagExifFileSource

Origen de la imagen. Si un DSC grabó la imagen, el valor de esta etiqueta es 3.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0xA300                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | 1                        |



 

## <a name="propertytagexifscenetype"></a>PropertyTagExifSceneType

Tipo de escena. Si un DSC grabó la imagen, el valor de esta etiqueta debe establecerse en 1, lo que indica que la imagen se ha fotografiado directamente.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0xA301                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | 1                        |



 

## <a name="propertytagexifcfapattern"></a>PropertyTagExifCfaPattern

El patrón geométrico de matriz de filtro de colores (CFA) del sensor de imagen cuando se usa un sensor de área de color de un solo chip. No se aplica a todos los métodos de detección.



| Información de propiedad | Value |
|-------|--------------------------|
| Etiqueta   | 0xA302                   |
| Tipo  | PropertyTagTypeUndefined |
| Count | Any                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificaciones de formato de archivo de imagen](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Constantes de etiqueta de propiedad de imagen](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[**Constantes de tipo de etiqueta de propiedad de imagen**](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[Etiquetas de propiedad en orden alfabético](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[Etiquetas de propiedad en orden numérico](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[Leer y escribir metadatos](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



