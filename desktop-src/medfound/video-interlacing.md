---
description: Entrelazado de vídeo
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelazado de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340c727f8faaaf20ff82eff58d0c651601071dea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363631"
---
# <a name="video-interlacing"></a>Entrelazado de vídeo

En este tema se describe cómo los descodificadores y los orígenes multimedia deben controlar el contenido de vídeo entrelazado.

Para descodificar y representar vídeo entrelazado correctamente, se necesita la siguiente información:

-   Progresiva o entrelazada. Una secuencia de vídeo puede contener fotogramas progresivas, entrelazados o una combinación de ambos.

-   Dominación de campo. La dominación de campo describe qué campo aparece primero, el campo superior o el campo inferior.

-   Repita el primer campo. Esta marca se usa en la extracción 3:2, cuando el marco es progresiva pero la secuencia está entrelazada. En este contexto, el primer campo puede ser el campo superior o inferior.

-   Campos intercalados o campo único. Un ejemplo puede contener un solo campo o dos campos intercalados. Si una muestra contiene un solo campo, el alto de la muestra es la mitad del alto del marco, ya que la muestra contiene solo la mitad de las líneas de examen de un marco. Se recomiendan los campos intercalados a menos que las características del contenido de origen indiquen lo contrario.

Cualquiera de estas características puede cambiar de un ejemplo a otro. Sin embargo, los componentes de vídeo deben saber algo sobre el contenido general antes de comenzar el streaming. Por ejemplo, si el vídeo está entrelazado, el representador de vídeo mejorado (EVR) debe reservar memoria de vídeo para el desenlazado. Por otro lado, si el vídeo es totalmente progresiva, la EVR puede optimizar la canalización de representación. Agregar un paso de desenlazado a la canalización aumenta la latencia de representación.

La información sobre el entrelazado se almacena en dos lugares:

-   La información general sobre el entrelazado en una secuencia se coloca en el tipo de medio. Para obtener más información sobre los tipos de medios, vea [Tipos de medios](media-types.md).

-   La información que puede cambiar con cada muestra se coloca en el ejemplo como un atributo. Para obtener más información sobre los ejemplos, vea [Ejemplos de medios](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Información de intercalación en el tipo de medio

El [**atributo MF MT \_ \_ INTERLACE \_ MODE**](mf-mt-interlace-mode-attribute.md) en el tipo de medio describe cómo se entrelaza la secuencia como un todo. El valor de este atributo es un miembro de la [**enumeración MFVideoInterlaceMode.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) Un tipo de medio de vídeo siempre debe tener este atributo.

-   Si la secuencia solo contiene fotogramas progresivas, sin marcos entrelazados, use MFVideoInterlace \_ Progressive.
-   Si la secuencia contiene solo fotogramas entrelazados y cada muestra contiene dos campos intercalados, use MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Si la secuencia contiene solo fotogramas entrelazados y cada muestra contiene un solo campo, use MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower. Si los campos alternan entre superior e inferior, no importa cuál de estos dos valores se utilice. Si el formato contiene solo campos superiores o simplemente campos inferiores, establezca el valor correspondiente al contenido.
-   Si la secuencia contiene una combinación de fotogramas entrelazados y progresivas, o si la dominación de campo cambia, establezca el tipo de medio en MFVideoInterlace \_ MixedInterlaceOrProgressive. Use atributos de ejemplo para describir cada fotograma.

En la tabla siguiente se resume este atributo.



| MODO \_ DE \_ INTERLACE MF \_ MT                       | ¿Entrelazado? | Ejemplos                                  | Primer campo    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ Progressive                 | No          | Marco progresiva                        | No aplicable |
| MFVideoInterlace \_ FieldInterleavedUpperFirst  | Sí         | Campos intercalados                       | Upper first    |
| MFVideoInterlace \_ FieldInterleavedLowerFirst  | Sí         | Campos intercalados                       | Lower first    |
| MFVideoInterlace \_ FieldSingleUpper            | Sí         | Campo único                             | Upper first    |
| MFVideoInterlace \_ FieldSingleLower            | Sí         | Campo único                             | Lower first    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | Puede variar    | Campos intercalados o marcos progresivas | Puede variar       |



 

Los campos intercalados y los campos individuales no se pueden mezclar. Cambiar de uno a otro requiere un cambio de tipo de medio.

## <a name="interlace-flags-on-samples"></a>Marcas de intercalación en ejemplos

La información que puede cambiar de una muestra a la siguiente se indica mediante atributos de ejemplo. Use la [**interfazSAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para obtener o establecer estos atributos.

Todos los atributos de entrelazado enumerados en esta sección tienen valores booleanos. De hecho, cada uno de estos atributos puede tener tres valores: **TRUE,** **FALSE** o no establecido. Si no se establece un atributo, el valor se toma del tipo de medio. Si se establece un atributo, el valor invalida el tipo de medio. Algunas combinaciones de marcas y tipos de medios no son válidas.




| Atributo | Descripción | 
|-----------|-------------|
| <a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a> | Si <strong>es TRUE,</strong>el marco está entrelazado. Si <strong>es FALSE,</strong>el marco es progresiva.<br /> Establezca este atributo en cada ejemplo si el tipo de medio es MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a> | El significado de esta marca depende de si las muestras contienen campos intercalados o campos individuales.<br /><ul><li>Campos intercalados: si <strong>es TRUE,</strong>el campo inferior es el primero. Si <strong>es FALSE,</strong>el campo superior es primero.<br /></li><li>Campos únicos: si <strong>es TRUE,</strong>el ejemplo contiene un campo inferior. Si <strong>es FALSE,</strong>el ejemplo contiene un campo superior.<br /></li></ul>Establezca este atributo en cada ejemplo de intercalación si el tipo de medio es MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower o MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a> | Si <strong>es TRUE</strong>, se repite el primer campo. Si <strong>es FALSE</strong> o no se establece, el primer campo no se repite. | 
| <a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a> | Si <strong>es TRUE,</strong>el ejemplo contiene un solo campo. Si <strong>es FALSE,</strong>el ejemplo contiene campos intercalados. | 




 

En la tabla siguiente se muestran las marcas necesarias, opcionales o prohibidas, según el tipo de medio.



| Tipo de soporte         | Marca entrelazada                      | BottomFieldFirst Flag                    | RepeatFirstField Flag | SingleField Flag                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| progresivo        | Opcional; si se establece, debe ser **FALSE.** | No lo establezca.                              | No lo establezca.           | No lo establezca.                          |
| Campos intercalados | Opcional; si se establece, debe ser **TRUE.**  | Opcional; si se establece, debe coincidir con el tipo de medio. | No lo establezca.           | Opcional; si se establece, debe ser **FALSE.** |
| Campos únicos      | Opcional; si se establece, debe ser **TRUE.**  | Necesario.                                | No lo establezca.           | Establezca en **TRUE.**                     |
| Mixto              | Necesario.                            | Necesario.                                | Necesario.             | Opcional; si se establece, debe ser **FALSE.** |



 

En los casos en los que el atributo es opcional, el tipo de medio ya define la información. Es válido establecer el atributo para que coincida, pero no es necesario.

Por ejemplo, si el tipo de medio es MFVideoInterlace Progressive, implica que todos los \_ fotogramas de la secuencia son progresivas. Por lo tanto, puede establecer el atributo **MFSampleExtension \_ Interlaced** en **FALSE** o dejar el atributo sin establecer.

## <a name="recommendations"></a>Recomendaciones

Esta sección contiene recomendaciones para varios tipos de contenido.

1. Todos los fotogramas del vídeo son progresivas.

-   Establezca el tipo de medio en MFVideoInterlace \_ Progressive.

-   No establezca el atributo **MFSampleExtension \_ Entrelazado** ni estafórelo en **FALSE** en cada fotograma.

-   No establezca los atributos **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** o **MFSampleExtension \_ SingleField.**

2. El vídeo es todos los campos entrelazados con la misma dominación de campo. Los ejemplos contienen campos intercalados.

-   Establezca el tipo de medio en MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.

-   No establezca el atributo **MFSampleExtension \_ Entrelazado** ni estafórelo en **TRUE** en cada fotograma.

-   No establezca el atributo **MFSampleExtension \_ BottomFieldFirst** ni establezca el valor en cada fotograma para que coincida con el tipo de medio.

-   No establezca el atributo **MFSampleExtension \_ RepeatFirstField** ni establezca en **FALSE** en cada fotograma.

-   No establezca el atributo **MFSampleExtension \_ SingleField** ni establezca en **FALSE** en cada fotograma.

3. El vídeo contiene una combinación de fotogramas entrelazados y progresivas, con campos repetidos y una dominación de campo variable (por ejemplo, vídeo de DVD).

-   Establezca el tipo de medio en MFVideoInterlace \_ MixedInterlaceOrProgressive.

-   En cada fotograma, establezca los atributos **MFSampleExtension \_ Interlaced**, **MFSampleExtension \_ BottomFieldFirst** y **MFSampleExtension \_ RepeatFirstField.**

-   No establezca el atributo **MFSampleExtension \_ SingleField** ni establezca en **FALSE** en cada fotograma.

4. El vídeo está entrelazado y los ejemplos contienen campos individuales.

-   Establezca el tipo de medio en MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.

-   En cada fotograma, establezca el **atributo MFSampleExtension \_ BottomFieldFirst.**

-   No establezca el atributo **MFSampleExtension \_ Entrelazado** ni estafórelo en **TRUE** en cada fotograma.

-   No establezca el atributo **MFSampleExtension \_ RepeatFirstField** ni establezca en **FALSE** en cada fotograma.

-   No establezca el atributo **MFSampleExtension \_ SingleField** ni estafórelo en **TRUE** en cada fotograma.

La mayoría del contenido de vídeo se divide en una de estas categorías.

## <a name="mpeg-2-mappings"></a>Asignaciones MPEG-2

Para el contenido MPEG-2, use las siguientes asignaciones para convertir las marcas MPEG-2 en Media Foundation de ejemplo.

**estructura de \_ imagen**



| Value         | Atributo de ejemplo                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ SingleField**  =  **FALSE**                                                                          |
| campo \_ superior    | **MFSampleExtension \_ SingleField**  =  **TRUE**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**<br/> |
| campo \_ inferior | **MFSampleExtension \_ SingleField**  =  **TRUE**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**<br/>  |



 

**marco \_ progresiva**



| Value | Atributo de ejemplo                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ TRUE entrelazado**  =    |
| 1     | **MFSampleExtension \_ FALSE entrelazado**  =   |



 

**primer \_ campo \_ superior**



| Value | Atributo de ejemplo                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE** |



 

**repetir \_ primer \_ campo**



| Value | Atributo de ejemplo                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **FALSE** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE**  |



 

## <a name="single-field-samples"></a>Single-Field ejemplos

Si el tipo de medio es MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace FieldSingleLower, significa que cada ejemplo contiene \_ un solo campo. Sin embargo, el tipo de medio describe todo el marco. Por lo tanto, cada búfer contiene solo la mitad del número de líneas de campo dadas en el tipo de medio. Por ejemplo, si el tipo de medio describe el vídeo como 720 × 480, cada campo contiene 240 líneas de examen y, por tanto, cada búfer contiene solo 240 filas de píxeles. Si escribe un componente que acepta tipos de medios con ejemplos de campo único, debe tener en cuenta este hecho al acceder a los datos del búfer.

La misma regla se aplica a la apertura geométrica (atributo[ \_ MF MT GEOMETRIC \_ \_ APERTURE)](mf-mt-geometric-aperture-attribute.md) y a la apertura de presentación mínima (atributo[MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE).](mf-mt-minimum-display-aperture-attribute.md) Estas regiones se especifican en términos de todo el marco, no de los campos individuales.

## <a name="directshow-mappings"></a>DirectShow Asignaciones

En DirectShow, la información de entrelazado por ejemplo se encuentra en el **miembro dwTypeSpecificFlags** de la estructura **PROPERTIES DE AM \_ SAMPLE2. \_** En la tabla siguiente se muestran los atributos equivalentes para Media Foundation.



| DirectShow de ejemplo              | Media Foundation de ejemplo                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ VIDEO \_ FLAG \_ INTERLEAVED \_ FRAME | **MFSampleExtension \_ SingleField**  =  **FALSE**.                                                                                                                                    |
| CAMPO DE \_ MARCA \_ DE VÍDEO \_ AM1             | **MFSampleExtension \_ TRUE**  =  **entrelazado.**<br/> **MFSampleExtension \_ SingleField**  =  **TRUE**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**.<br/> |
| CAMPO \_ DE LA MARCA DE VÍDEO \_ \_ AM2             | **MFSampleExtension \_ TRUE**  =  **entrelazado.**<br/> **MFSampleExtension \_ SingleField**  =  **TRUE**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE**.<br/>  |
| AM \_ VIDEO \_ FLAG \_ WEAVE              | **MFSampleExtension \_ FALSE**  =  **entrelazado.** (Esta marca indica que el controlador no debe desinterlatar los dos campos).                                                        |
| AM \_ VIDEO \_ FLAG \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**. Si el contenido está entrelazado y la marca FIELD1FIRST de AM VIDEO FLAG no está \_ \_ \_ presente, establezca este atributo en **TRUE.**        |
| CAMPO REPETIR \_ \_ MARCA DE VÍDEO \_ \_ AM      | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE**. Si la marca REPEAT FIELD de AM \_ VIDEO FLAG no está \_ \_ \_ presente, establezca este atributo en **FALSE.**                                    |



 

Si el DirectShow muestra no contiene marcas de ejemplo, use el valor **de dwInterlaceFlags** de la **estructura VIDEOINFOHEADER2:**



| DirectShow de interlace    | Media Foundation de ejemplo                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ IsInterlaced    | **MFSampleExtension \_ TRUE**  =  **entrelazado.**        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_ SingleField**  =  **TRUE**.       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE**. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




