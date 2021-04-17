---
title: Elemento Fragment
description: El elemento Fragment especifica una condición de la consulta que selecciona los elementos de la biblioteca. Las condiciones se especifican mediante cadenas de condición. Normalmente, una cadena de condición tiene una parte de nombre, una parte de condición y una parte de valor.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- Elemento Fragment de Windows Media Player
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da4cd18c6286cf2439e310b4e797f6978f3b2395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699919"
---
# <a name="fragment-element"></a>Elemento Fragment

El elemento **Fragment** especifica una condición de la consulta que selecciona los elementos de la biblioteca. Las condiciones se especifican mediante cadenas de condición. Normalmente, una cadena de condición tiene una parte de nombre, una parte de condición y una parte de valor.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nombre** (obligatorio) 
</dt> <dd>

Una parte de una cadena de condición. Vea la sección Comentarios.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [filtrar](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Elemento secundario     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Observaciones

Algunas cadenas de condición tienen una parte del atributo de metadatos, una parte de condición y una parte de valor. Por ejemplo, en la cadena de condición "álbum de álbumes es Joe", la parte del atributo de metadatos es "Album intérprete", la parte de la condición es "es" y la parte del valor es "Joe".

Ejemplo:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



En el caso de las cadenas de condición de este tipo, en la tabla siguiente se muestran los posibles atributos de metadatos, las posibles condiciones y los valores posibles:



| Atributo Metadata                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Condiciones posibles                                                                                             | Valores posibles                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intérprete ActorAlbum<br/> Título del álbum<br/> Autor<br/> Caption<br/> Canal<br/> Composer<br/> Conductor<br/> Proveedor de contenido<br/> Género de proveedor de contenido<br/> Intérprete contribuyente<br/> Texto de copyright<br/> Director<br/> Episodio<br/> Tipo de archivo<br/> Género<br/> Clave<br/> Palabras clave<br/> Idioma<br/> Ánimo<br/> Clasificación parental<br/> Período<br/> Productor<br/> Proveedor<br/> Publicador<br/> Serie<br/> El nombre de la estación<br/> Subgénero<br/> Subtítulo<br/> Title<br/> Escritor<br/> | No es igual a EqualsDoes<br/> Is<br/> No es<br/> Contiene<br/> No contiene<br/> | Cualquier valor de cadena                                                                                                                                                                                                                                                                                                  |
| Velocidad de bits (en kilobytes por segundo).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | No es igual a EqualsDoes<br/> Is<br/> No es<br/> Contiene<br/> No contiene<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1.500<br/> 3000<br/> 4500<br/> 6000<br/> 7500<br/>                                                                            |
| Tipo de medio secundario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | No es igual a EqualsDoes<br/> Is<br/> No es<br/> Contiene<br/> No contiene<br/> | Audio: NewsAudio: Talk Show<br/> Audio: libros de audio<br/> Audio: palabra oral de audio<br/> Vídeo: noticias<br/> Vídeo: Talk Show<br/> Vídeo: vídeo principal<br/> Vídeo: película o película<br/> Vídeo: programa de TV<br/> Vídeo: vídeo corporativo<br/> Vídeo: vídeo musical<br/> |
| Alto de la imagen de tamaño de archivo (en KB)<br/> Ancho de la imagen<br/> Recuento de repeticiones: total de la tarde<br/> Recuento de repeticiones: total de atardecer<br/> Recuento de repeticiones: total de la mañana<br/> Recuento de repeticiones: totales nocturnos<br/> Recuento de repeticiones: total general<br/> Recuento de repeticiones: día de la semana total<br/> Recuento de repeticiones: fin de semana total<br/>                                                                                                                                                                                                                                                                                                                  | Es menor que es mayor que<br/> Is<br/> No es<br/>                                          | Cualquier número                                                                                                                                                                                                                                                                                                        |
| Difundir el código timeDate codificado<br/> Fecha de grabación<br/> Fecha de creación<br/> Año de la versión<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Antes de<br/> Is<br/> No es<br/>                                                    | YesterdayLast semana<br/> El mes pasado<br/> 6 meses<br/> 1 año<br/> 2 años<br/> 5 años<br/> 2000s<br/> comienzos<br/> 80<br/> setenta<br/> años<br/> 1950s<br/> 1940s<br/>                                                            |
| Fecha de adición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Antes de<br/> Is<br/> No es<br/>                                                    | YesterdayLast semana<br/> El mes pasado<br/> 6 meses<br/> 1 año<br/> 2 años<br/> 5 años<br/>                                                                                                                                                                                   |
| Fecha de la última reproducción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Anterior ThanMore más reciente que<br/> Is<br/> No es<br/>                                           | YesterdayLast semana<br/> El mes pasado<br/> 6 meses<br/> 1 año<br/> 2 años<br/> 5 años<br/>                                                                                                                                                                                   |
| Mes tomado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Antes es más reciente que<br/> Is<br/> No es<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Año tomado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Antes es más reciente que<br/> Is<br/> No es<br/>                                         | Cualquier año                                                                                                                                                                                                                                                                                                          |
| Clasificación RatingMy automática<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | No tiene al menos más de<br/> Is<br/> No es<br/>                                           | Estrella Unrated1<br/> 2 estrellas<br/> 3 estrellas<br/> 4 estrellas<br/> 5 estrellas<br/>                                                                                                                                                                                                              |
| Campo personalizado \# 1Custom campo \# 2<br/> Nombre de archivo<br/> Campos clave<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes no contiene<br/>                                                                             | Cualquier cadena                                                                                                                                                                                                                                                                                                        |



 

Algunas cadenas de condición tienen una parte del limitador, una parte del número y una parte del formato. Por ejemplo, en la cadena de condición "limitar tamaño total a 3 megabytes", la parte del límite es "limitar el tamaño total a", la parte del número es "3" y la parte del formato es "megabytes".

Ejemplo:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



En el caso de las cadenas de condición de este tipo, en la tabla siguiente se muestran los posibles límites y formatos.



| Limitador                 | Números posibles | Posibles formatos                |
|-------------------------|------------------|---------------------------------|
| Limitar tamaño total a     | Cualquier número       | Kilobytes, megabytes, gigabytes |
| Limitar la duración total a | Cualquier número       | Segundos, minutos, horas, días   |



 

Algunas cadenas de condición tienen una parte del limitador y una parte del número. Por ejemplo, en la cadena de condición "limitar número de elementos a 25", la parte del limitador es "limitar número de elementos" y la parte del número es "25".

Ejemplo:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



En el caso de las cadenas de condición de este tipo, en la tabla siguiente se muestra el único limitador posible.



| Limitador               | Números posibles |
|-----------------------|------------------|
| Limitar el número de elementos | Cualquier número       |



 

Algunas cadenas de condición tienen una parte de protección y una parte de la condición. Por ejemplo, en la cadena de condición "la protección está presente", la parte de protección es "protección" y la parte de la condición es "es".

Ejemplo:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



En el caso de las cadenas de condición de este tipo, en la tabla siguiente se muestran las posibles condiciones.



| Parte de protección | Condiciones posibles             |
|--------------------|---------------------------------|
| Protección         | Is<br/> No es<br/> |



 

Hay un tipo de elemento **Fragment** que no contiene una cadena de condición. Si el atributo de nombre de un elemento **Fragment** es "aleatorizar el orden de reproducción", el elemento **Fragment** no contiene ningún elemento de **argumento** . Este elemento **Fragment** indica al reproductor que reproduzca la lista en orden aleatorio.

Ejemplo:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Algunas cadenas de condición tienen una parte de ordenación, una parte de valor y una parte de condición. Por ejemplo, en la cadena de condición "ordenar por título ascendente", la parte de ordenación es "ordenar por", la parte del valor es "título" y la parte de la condición es "ascendente". Tenga en cuenta que, en este caso, la parte del valor es un atributo de metadatos.

Ejemplo:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



En el caso de las cadenas de condición de este tipo, en la tabla siguiente se muestran los posibles valores y condiciones.



| Ordenar parte | Valores posibles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Condiciones posibles                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Ordenar por      | GenreTitle<br/> Fecha de adición<br/> Clasificación automática<br/> Mi clasificación<br/> Recuento de repeticiones: total general<br/> Recuento de repeticiones: total de la mañana<br/> Recuento de repeticiones: total de la tarde<br/> Recuento de repeticiones: total de atardecer<br/> Recuento de repeticiones: totales nocturnos<br/> Recuento de repeticiones: día de la semana total<br/> Recuento de repeticiones: fin de semana total<br/> Actor<br/> Subtítulo<br/> El nombre de la estación<br/> Canal<br/> Hora de difusión<br/> Director<br/> Año de la versión<br/> Escritor<br/> Productor<br/> Fecha de grabación<br/> Fecha de codificación<br/> Velocidad de bits<br/> Protección<br/> | AscendingDescending<br/> Random<br/> |



 

Cuando use un elemento Fragment para ordenar una lista de reproducción, debe ordenar por un atributo de metadatos que se aplique al tipo de elementos multimedia que está ordenando. Por ejemplo, si está ordenando elementos de música, no puede ordenar por actor. En la tabla siguiente se muestran los atributos de metadatos que puede usar para ordenar los tipos de medios.



| Tipo de medio  | Posibles atributos de metadatos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Música       | GenreTitle<br/> Fecha de adición<br/> Clasificación automática<br/> Mi clasificación<br/> Recuento de repeticiones: total general<br/> Recuento de repeticiones: total de la mañana<br/> Recuento de repeticiones: total de la tarde<br/> Recuento de repeticiones: total de atardecer<br/> Recuento de repeticiones: totales nocturnos<br/> Recuento de repeticiones: día de la semana total<br/> Recuento de repeticiones: fin de semana total<br/>                                                                                                                                                                                                                                                                                            |
| Vídeo o TV | GenreActor<br/> Subtítulo<br/> Title<br/> Fecha de adición<br/> Clasificación automática<br/> El nombre de la estación<br/> Canal<br/> Hora de difusión<br/> Director<br/> Año de la versión<br/> Escritor<br/> Productor<br/> Fecha de grabación<br/> Fecha de codificación<br/> Velocidad de bits<br/> Mi clasificación<br/> Protección<br/> Recuento de repeticiones: total general<br/> Recuento de repeticiones: total de la mañana<br/> Recuento de repeticiones: total de la tarde<br/> Recuento de repeticiones: total de atardecer<br/> Recuento de repeticiones: totales nocturnos<br/> Recuento de repeticiones: día de la semana total<br/> Recuento de repeticiones: fin de semana total<br/> |
| Radio       | TitleDate agregado<br/> Velocidad de bits<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Foto       | Title                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Otros       | GenreTitle<br/> Fecha de adición<br/> Clasificación automática<br/> Mi clasificación<br/> Velocidad de bits<br/> Recuento de repeticiones: total general<br/> Recuento de repeticiones: total de la mañana<br/> Recuento de repeticiones: total de la tarde<br/> Recuento de repeticiones: total de atardecer<br/> Recuento de repeticiones: totales nocturnos<br/> Recuento de repeticiones: día de la semana total<br/> Recuento de repeticiones: fin de semana total<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento Filter**](filter-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





