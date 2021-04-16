---
description: Entrelazado de vídeo
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelazado de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705887"
---
# <a name="video-interlacing"></a>Entrelazado de vídeo

En este tema se describe cómo los orígenes y descodificadores multimedia deben controlar el contenido de vídeo entrelazado.

Para descodificar y representar correctamente el vídeo entrelazado, se necesita la siguiente información:

-   Progresiva o entrelazada. Un flujo de vídeo puede contener fotogramas progresivos, fotogramas entrelazados o una combinación de ambos.

-   Dominio de campo. Dominio de campo describe el campo que aparece en primer lugar, el campo superior o el campo inferior.

-   Repite el primer campo. Esta marca se usa en el desplegable 3:2, cuando el fotograma es progresivo, pero la secuencia está entrelazada. En este contexto, el primer campo puede ser el campo superior o inferior.

-   Campos intercalados o un solo campo. Un ejemplo puede contener un solo campo o dos campos intercalados. Si un ejemplo contiene un solo campo, el alto de ejemplo es la mitad del alto del marco, ya que el ejemplo solo contiene la mitad de las líneas de recorrido de un fotograma. Los campos intercalados se recomiendan a menos que las características del contenido de origen dicten lo contrario.

Cualquiera de estas características puede cambiar de una muestra a la siguiente. Sin embargo, los componentes de vídeo deben saber algo sobre el contenido general antes de comenzar la transmisión por secuencias. Por ejemplo, si el vídeo está entrelazado, el representador de vídeo mejorado (EVR) debe reservar la memoria de vídeo para el desentrelazado. Si el vídeo es totalmente fotogramas progresivos, por otro lado, el EVR puede optimizar la canalización de representación. Agregar un paso de desentrelazado a la canalización aumenta la latencia de representación.

La información sobre el entrelazado se almacena en dos lugares:

-   La información general sobre el entrelazado en una secuencia se coloca en el tipo de medio. Para obtener más información sobre los tipos de medios, consulte [tipos de medios](media-types.md).

-   La información que puede cambiar con cada ejemplo se coloca en el ejemplo como un atributo. Para obtener más información acerca de los ejemplos, vea [ejemplos de medios](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Información de entrelazado en el tipo de medio

El atributo de [**\_ \_ \_ modo entrelazado MF MT**](mf-mt-interlace-mode-attribute.md) en el tipo de medio describe cómo se entrelaza la secuencia en su conjunto. El valor de este atributo es un miembro de la enumeración [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) . Un tipo de medio de vídeo siempre debe tener este atributo.

-   Si la secuencia contiene solo fotogramas progresivos, sin fotogramas entrelazados, use MFVideoInterlace \_ progresivo.
-   Si la secuencia contiene solo fotogramas entrelazados y cada ejemplo contiene dos campos intercalados, use MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Si la secuencia contiene solo fotogramas entrelazados y cada ejemplo contiene un solo campo, utilice MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower. Si los campos alternan entre la parte superior e inferior, no importa cuál de estos dos valores se use. Si el formato contiene solo los campos superiores, o simplemente los campos inferiores, establezca el valor que se corresponda con el contenido.
-   Si la secuencia contiene una mezcla de fotogramas entrelazados y progresivos, o si el campo domina, establezca el tipo de medio en MFVideoInterlace \_ MixedInterlaceOrProgressive. Use los atributos de ejemplo para describir cada fotograma.

En la tabla siguiente se resume este atributo.



| \_ \_ modo entrelazado MF MT \_                       | Entrelazadas? | Ejemplos                                  | Primer campo    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| \_Progresiva MFVideoInterlace                 | No          | Fotograma progresivo                        | No aplicable |
| MFVideoInterlace \_ FieldInterleavedUpperFirst  | Sí         | Campos intercalados                       | Primero en primer lugar    |
| MFVideoInterlace \_ FieldInterleavedLowerFirst  | Sí         | Campos intercalados                       | Inferior primero    |
| MFVideoInterlace \_ FieldSingleUpper            | Sí         | Campo único                             | Primero en primer lugar    |
| MFVideoInterlace \_ FieldSingleLower            | Sí         | Campo único                             | Inferior primero    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | Puede variar    | Campos intercalados o fotogramas progresivos | Puede variar       |



 

Los campos intercalados y los campos únicos no se pueden mezclar. Cambiar de uno a otro requiere un cambio de tipo de medio.

## <a name="interlace-flags-on-samples"></a>Marcas de entrelazado en ejemplos

La información que puede cambiar de una muestra a la siguiente se indica mediante los atributos de ejemplo. Use la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para obtener o establecer estos atributos.

Todos los atributos de entrelazado que aparecen en esta sección tienen valores booleanos. En realidad, cada uno de estos atributos puede tener tres valores: **true**, **false** o Not Set. Si no se establece un atributo, el valor se toma del tipo de medio. Si se establece un atributo, el valor invalida el tipo de medio. Algunas combinaciones de marcas y tipos de medios no son válidas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></td>
<td>Si es <strong>true</strong>, el marco está entrelazado. Si es <strong>false</strong>, el marco es progresivo.<br/> Establezca este atributo en cada ejemplo si el tipo de medio es MFVideoInterlace_MixedInterlaceOrProgressive.<br/></td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></td>
<td>El significado de esta marca depende de si los ejemplos contienen campos intercalados o campos individuales.<br/>
<ul>
<li>Campos intercalados: si es <strong>true</strong>, el campo inferior es el primero. Si es <strong>false</strong>, el campo superior es primero.<br/></li>
<li>Campos únicos: Si <strong>es true</strong>, el ejemplo contiene un campo inferior. Si <strong>es false</strong>, el ejemplo contiene un campo superior.<br/></li>
</ul>
Establezca este atributo en cada ejemplo entrelazado si el tipo de medio es MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower o MFVideoInterlace_MixedInterlaceOrProgressive.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></td>
<td>Si es <strong>true</strong>, el primer campo se repite. Si es <strong>false</strong> o no se establece, el primer campo no se repite.</td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></td>
<td>Si <strong>es true</strong>, el ejemplo contiene un solo campo. Si <strong>es false</strong>, el ejemplo contiene campos intercalados.</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se muestra qué marcas son necesarias, opcionales o prohibidas, en función del tipo de medio.



| Tipo de soporte         | Marca entrelazada                      | Marca BottomFieldFirst                    | Marca RepeatFirstField | Marca SingleField                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| progresivo        | Opta Si se establece, debe ser **false**. | No lo establezca.                              | No lo establezca.           | No lo establezca.                          |
| Campos intercalados | Opta Si se establece, debe ser **true**.  | Opta Si se establece, debe coincidir con el tipo de medio. | No lo establezca.           | Opta Si se establece, debe ser **false**. |
| Campos únicos      | Opta Si se establece, debe ser **true**.  | Obligatorio.                                | No lo establezca.           | Establézcalo en **true**.                     |
| Mixto              | Obligatorio.                            | Obligatorio.                                | Obligatorio.             | Opta Si se establece, debe ser **false**. |



 

En los casos en los que el atributo es opcional, el tipo de medio ya define la información. Es válido establecer el atributo para que coincida, pero no es necesario.

Por ejemplo, si el tipo de medio es MFVideoInterlace \_ progresivo, implica que todos los marcos de la secuencia son progresivos. Por lo tanto, puede establecer el **atributo \_ entrelazado MFSampleExtension** en **false** o dejar el atributo como no establecido.

## <a name="recommendations"></a>Recomendaciones

Esta sección contiene recomendaciones para varios tipos de contenido.

1. El vídeo es todos los fotogramas progresivos.

-   Establezca el tipo de medio en MFVideoInterlace \_ progresivo.

-   No establezca el atributo **\_ entrelazado MFSampleExtension** o establézcalo en **false** en cada fotograma.

-   No establezca los atributos **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** o **MFSampleExtension \_ SingleField** .

2. El vídeo son todos los campos entrelazados con el mismo dominio de campo. Los ejemplos contienen campos intercalados.

-   Establezca el tipo de medio en MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.

-   No establezca el atributo **\_ entrelazado MFSampleExtension** o establézcalo en **true** en cada fotograma.

-   No establezca el atributo **\_ BottomFieldFirst de MFSampleExtension** o establezca el valor en cada fotograma para que coincida con el tipo de medio.

-   No establezca el atributo **\_ RepeatFirstField de MFSampleExtension** o establézcalo en **false** en cada fotograma.

-   No establezca el atributo **\_ SingleField de MFSampleExtension** o establézcalo en **false** en cada fotograma.

3. El vídeo contiene una mezcla de fotogramas entrelazados y progresivos, con campos repetidos y una superposición de campo variable (por ejemplo, vídeo DVD).

-   Establezca el tipo de medio en MFVideoInterlace \_ MixedInterlaceOrProgressive.

-   En cada fotograma, establezca los atributos **MFSampleExtension \_ entrelazad**, **MFSampleExtension \_ BottomFieldFirst** y **MFSampleExtension \_ RepeatFirstField** .

-   No establezca el atributo **\_ SingleField de MFSampleExtension** o establézcalo en **false** en cada fotograma.

4. El vídeo está entrelazado y los ejemplos contienen campos únicos.

-   Establezca el tipo de medio en MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.

-   En cada fotograma, establezca el atributo **\_ BottomFieldFirst de MFSampleExtension** .

-   No establezca el atributo **\_ entrelazado MFSampleExtension** o establézcalo en **true** en cada fotograma.

-   No establezca el atributo **\_ RepeatFirstField de MFSampleExtension** o establézcalo en **false** en cada fotograma.

-   No establezca el atributo **\_ SingleField de MFSampleExtension** o establézcalo en **true** en cada fotograma.

La mayoría del contenido de vídeo se encuentra en una de estas categorías.

## <a name="mpeg-2-mappings"></a>Asignaciones MPEG-2

En el caso de contenido MPEG-2, utilice las siguientes asignaciones para convertir las marcas MPEG-2 en Media Foundation atributos de ejemplo.

**estructura de la imagen \_**



| Value         | Atributo de ejemplo                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ SingleField**  =  **false**                                                                          |
| \_campo superior    | **MFSampleExtension \_ SingleField**  =  **true**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**<br/> |
| \_campo inferior | **MFSampleExtension \_ SingleField**  =  **true**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**<br/>  |



 

**fotograma progresivo \_**



| Value | Atributo de ejemplo                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ True entrelazado**  =    |
| 1     | **MFSampleExtension \_ FALSE entrelazado**  =   |



 

**\_primer campo \_ primero**



| Value | Atributo de ejemplo                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **true**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **false** |



 

**repetir \_ primer \_ campo**



| Value | Atributo de ejemplo                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **false** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **true**  |



 

## <a name="single-field-samples"></a>Ejemplos de Single-Field

Si el tipo de medio es MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower, significa que cada ejemplo contiene un solo campo. Sin embargo, el tipo de medio describe todo el marco. Por lo tanto, cada búfer contiene solo la mitad del número de líneas de campo que se proporcionan en el tipo de medio. Por ejemplo, si el tipo de medio describe el vídeo como 720 × 480, cada campo contiene 240 líneas de análisis y, por tanto, cada búfer contiene solo 240 filas de píxeles. Si escribe un componente que acepta tipos de medios con muestras de un solo campo, debe tener en cuenta este hecho al tener acceso a los datos del búfer.

La misma regla se aplica a la abertura geométrica (atributo de[ \_ \_ \_ abertura geométrica de MF MT](mf-mt-geometric-aperture-attribute.md) ) y a la abertura mínima de pantalla (el atributo de[ \_ \_ \_ \_ abertura de pantalla mínima MF MT](mf-mt-minimum-display-aperture-attribute.md) ). Estas regiones se especifican en términos de todo el marco, no de los campos individuales.

## <a name="directshow-mappings"></a>Asignaciones de DirectShow

En DirectShow, la información de entrelazado por muestra se incluye en el miembro **dwTypeSpecificFlags** de la estructura de **\_ \_ propiedades AM SAMPLE2** . En la tabla siguiente se muestran los atributos equivalentes para Media Foundation.



| Marca de ejemplo de DirectShow              | Media Foundation atributo de ejemplo                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_marca de vídeo AM \_ \_ FOTOgrama intercalado \_ | **MFSampleExtension \_ SingleField**  =  **false**.                                                                                                                                    |
| \_Marca de vídeo AM \_ \_ Campo1             | **MFSampleExtension \_ True entrelazado**  =  .<br/> **MFSampleExtension \_ SingleField**  =  **true**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**.<br/> |
| \_FIELD2 de \_ marca de vídeo AM \_             | **MFSampleExtension \_ True entrelazado**  =  .<br/> **MFSampleExtension \_ SingleField**  =  **true**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**.<br/>  |
| trama de la \_ marca de vídeo AM \_ \_              | **MFSampleExtension \_ FALSE entrelazado**  =  . (Este marcador indica que el controlador no debe Desentrelazar los dos campos).                                                        |
| \_Marca de vídeo AM \_ \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. Si el contenido está entrelazado y la marca de la \_ marca de vídeo AM \_ \_ FIELD1FIRST no está presente, establezca este atributo en **true**.        |
| \_campo de \_ repetición de marca de vídeo AM \_ \_      | **MFSampleExtension \_ RepeatFirstField**  =  **true**. Si el indicador de repetición de la \_ marca de vídeo AM \_ \_ \_ no está presente, establezca este atributo en **false**.                                    |



 

Si el ejemplo de DirectShow no contiene marcas de ejemplo, use el valor de **dwInterlaceFlags** de la estructura **VIDEOINFOHEADER2** :



| Marca de entrelazado de DirectShow    | Media Foundation atributo de ejemplo                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ IsInterlaced    | **MFSampleExtension \_ True entrelazado**  =  .        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_ SingleField**  =  **true**.       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




