---
title: elemento fragment
description: El elemento fragment especifica una condición de la consulta que selecciona elementos de la biblioteca. Las condiciones se especifican mediante cadenas de condición. Normalmente, una cadena de condición tiene una parte de nombre, una parte de condición y una parte de valor.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- fragment Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1010b269302f88f163232bcaf3e37111e5fc219944ff1d141c1189e119bba05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003705"
---
# <a name="fragment-element"></a>elemento fragment

El **elemento fragment** especifica una condición de la consulta que selecciona elementos de la biblioteca. Las condiciones se especifican mediante cadenas de condición. Normalmente, una cadena de condición tiene una parte de nombre, una parte de condición y una parte de valor.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obligatorio) 
</dt> <dd>

Parte de una cadena de condición. Vea la sección Comentarios.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [filter](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Elemento secundario     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Comentarios

Algunas cadenas de condición tienen una parte del atributo de metadatos, una parte de condición y una parte de valor. Por ejemplo, en la cadena de condición "Album Artist Is Joe", la parte del atributo de metadatos es "Album Artist", la parte de condición es "Is" y la parte del valor es "Joe".

Ejemplo:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Para las cadenas de condición de este tipo, en la tabla siguiente se muestran los posibles atributos de metadatos, las condiciones posibles y los valores posibles:



| Atributo de metadatos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Condiciones posibles                                                                                             | Valores posibles                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActorAlbum Artist<br/> Título del álbum<br/> Autor<br/> Caption<br/> Canal<br/> Composer<br/> Director de orquesta<br/> Proveedor de contenido<br/> Género del proveedor de contenido<br/> Colaborador<br/> Texto de copyright<br/> Director<br/> Episodio<br/> Tipo de archivo<br/> Género<br/> Clave<br/> Palabras clave<br/> Lenguaje<br/> Humor<br/> Clasificación parental<br/> Período<br/> Productor<br/> Proveedor<br/> Publisher<br/> Serie<br/> El nombre de la estación<br/> Subgénero<br/> Subtítulo<br/> Título<br/> Escritor<br/> | EqualsDoes Not Equal<br/> Is<br/> No es<br/> Contiene<br/> No contiene<br/> | Cualquier valor de cadena                                                                                                                                                                                                                                                                                                  |
| Velocidad de bits (en kilobytes por segundo).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | EqualsDoes Not Equal<br/> Is<br/> No es<br/> Contiene<br/> No contiene<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1.500<br/> 3000<br/> 4500<br/> 6000<br/> 7500<br/>                                                                            |
| Tipo de medio secundario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | EqualsDoes Not Equal<br/> Is<br/> No es<br/> Contiene<br/> No contiene<br/> | Audio: NewsAudio: Talk Show<br/> Audio: AudioLibros<br/> Audio: Audio Spoken Word<br/> Vídeo: Noticias<br/> Vídeo: Talk Show<br/> Vídeo: Vídeo principal<br/> Vídeo: Película/Película<br/> Vídeo: Programa de TV<br/> Vídeo: Vídeo corporativo<br/> Vídeo: Música Video<br/> |
| Tamaño de archivo (en KB)Alto de la imagen<br/> Ancho de imagen<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales por la mañana<br/> Recuento de reproducción: totales de noche<br/> Recuento de reproducción: total total<br/> Recuento de reproducción: día de la semana total<br/> Recuento de reproducción: fin de semana total<br/>                                                                                                                                                                                                                                                                                                                  | Es menor que Si es mayor que<br/> Is<br/> No es<br/>                                          | Cualquier número                                                                                                                                                                                                                                                                                                        |
| Broadcast timeDate Encoded<br/> Fecha de grabación<br/> Fecha de toma<br/> Año de lanzamiento<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Is BeforeIs After<br/> Is<br/> No es<br/>                                                    | Last week de Ayer<br/> El mes pasado<br/> 6 meses<br/> 1 año<br/> 2 años<br/> 5 años<br/> 2000s<br/> Décadas de 1990<br/> Décadas de 1980<br/> Años 70<br/> Décadas de 1960<br/> Décadas de 1950<br/> Décadas de 1940<br/>                                                            |
| Fecha de adición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Is BeforeIs After<br/> Is<br/> No es<br/>                                                    | Last week de Ayer<br/> El mes pasado<br/> 6 meses<br/> 1 año<br/> 2 años<br/> 5 años<br/>                                                                                                                                                                                   |
| Fecha de última reproducción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Anterior a Más reciente que<br/> Is<br/> No es<br/>                                           | Last week de Ayer<br/> El mes pasado<br/> 6 meses<br/> 1 año<br/> 2 años<br/> 5 años<br/>                                                                                                                                                                                   |
| Mes tomado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Is BeforeIs More Recent Than<br/> Is<br/> No es<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Año realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Is BeforeIs More Recent Than<br/> Is<br/> No es<br/>                                         | Cualquier año                                                                                                                                                                                                                                                                                                          |
| Clasificación automáticaMi clasificación<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Is At LeastIs No More Than<br/> Is<br/> No es<br/>                                           | Unrated1 Star<br/> 2 estrellas<br/> 3 estrellas<br/> 4 estrellas<br/> 5 estrellas<br/>                                                                                                                                                                                                              |
| Campo personalizado \# 1Personalización \# Campo 2<br/> Nombre de archivo<br/> Campos clave<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes Not Contain<br/>                                                                             | Cualquier cadena                                                                                                                                                                                                                                                                                                        |



 

Algunas cadenas de condición tienen una parte del limitador, una parte de número y una parte de formato. Por ejemplo, en la cadena de condición "Limit Total Size To 3 Megabytes", la parte del limitador es "Limit Total Size To", la parte del número es "3" y la parte de formato es "Megabytes".

Ejemplo:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Para las cadenas de condición de este tipo, la tabla siguiente muestra los posibles limitadores y formatos.



| Limitador                 | Números posibles | Formatos posibles                |
|-------------------------|------------------|---------------------------------|
| Limitar el tamaño total a     | Cualquier número       | Kilobytes, Megabytes, Gigabytes |
| Limitar la duración total a | Cualquier número       | Segundos, minutos, horas, días   |



 

Ciertas cadenas de condición tienen una parte del limitador y una parte de número. Por ejemplo, en la cadena de condición "Limitar número de elementos a 25", la parte del limitador es "Limitar número de elementos" y la parte del número es "25".

Ejemplo:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Para las cadenas de condición de este tipo, la tabla siguiente muestra el único limitador posible.



| Limitador               | Números posibles |
|-----------------------|------------------|
| Limitar número de elementos | Cualquier número       |



 

Ciertas cadenas de condición tienen una parte de protección y una parte de condición. Por ejemplo, en la cadena de condición "La protección está presente", la parte de protección es "Protection" y la parte de la condición es "Is".

Ejemplo:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Para las cadenas de condición de este tipo, la tabla siguiente muestra las condiciones posibles.



| Parte de protección | Condiciones posibles             |
|--------------------|---------------------------------|
| Protección         | Is<br/> No es<br/> |



 

Hay un tipo de elemento **de fragmento** que no contiene una cadena de condición. Si el atributo name de un elemento **de fragmento** es "Randomize Playback Order", el elemento **fragment** no contiene elementos **de** argumento. Este **elemento de** fragmento indica al reproductor que reprodgue la lista en orden aleatorio.

Ejemplo:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Algunas cadenas de condición tienen una parte de ordenación, una parte de valor y una parte de condición. Por ejemplo, en la cadena de condición "Ordenar por orden ascendente de título", la parte de ordenación es "Ordenar por", la parte del valor es "Título" y la parte de la condición es "Ascendente". Tenga en cuenta que, en este caso, la parte del valor es un atributo de metadatos.

Ejemplo:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Para las cadenas de condición de este tipo, la tabla siguiente muestra los valores y condiciones posibles.



| Ordenar parte | Valores posibles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Condiciones posibles                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Ordenar por      | GenreTitle<br/> Fecha de adición<br/> Clasificación automática<br/> Mi clasificación<br/> Recuento de reproducción: total general<br/> Recuento de reproducción: totales por la mañana<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de noche<br/> Recuento de reproducción: día de la semana total<br/> Recuento de reproducción: fin de semana total<br/> Actor<br/> Subtítulo<br/> El nombre de la estación<br/> Canal<br/> Hora de difusión<br/> Director<br/> Año de lanzamiento<br/> Escritor<br/> Productor<br/> Fecha de grabación<br/> Fecha codificada<br/> Velocidad de bits<br/> Protección<br/> | AscendingDescending<br/> Random<br/> |



 

Cuando se usa un elemento de fragmento para ordenar una lista de reproducción, debe ordenar por un atributo de metadatos que se aplique al tipo de elementos multimedia que está ordenando. Por ejemplo, si va a ordenar elementos de música, no puede ordenar por Actor. En la tabla siguiente se muestran los atributos de metadatos que puede usar para ordenar los tipos de medios.



| Tipo de medio  | Atributos de metadatos posibles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Música       | GenreTitle<br/> Fecha de adición<br/> Clasificación automática<br/> Mi clasificación<br/> Recuento de reproducción: total general<br/> Recuento de reproducción: totales por la mañana<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de noche<br/> Recuento de reproducción :Total de días laborables<br/> Recuento de reproducción: fin de semana total<br/>                                                                                                                                                                                                                                                                                            |
| Vídeo o televisión | GenreActor<br/> Subtítulo<br/> Título<br/> Fecha de adición<br/> Clasificación automática<br/> El nombre de la estación<br/> Canal<br/> Hora de difusión<br/> Director<br/> Año de lanzamiento<br/> Escritor<br/> Productor<br/> Fecha de grabación<br/> Fecha codificada<br/> Velocidad de bits<br/> Mi clasificación<br/> Protección<br/> Recuento de reproducción: total general<br/> Recuento de reproducción: totales por la mañana<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de noche<br/> Recuento de reproducción: día de la semana total<br/> Recuento de reproducción: fin de semana total<br/> |
| Radio       | TitleDate agregado<br/> Velocidad de bits<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Foto       | Título                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Otros       | GenreTitle<br/> Fecha de adición<br/> Clasificación automática<br/> Mi clasificación<br/> Velocidad de bits<br/> Recuento de reproducción: total general<br/> Recuento de reproducción: totales por la mañana<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de tarde<br/> Recuento de reproducción: totales de noche<br/> Recuento de reproducción: día de la semana total<br/> Recuento de reproducción: fin de semana total<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**elemento argument**](argument-element.md)
</dt> <dt>

[**elemento filter**](filter-element.md)
</dt> <dt>

[**elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





