---
title: elemento argument
description: El elemento argument contiene una parte de una cadena de condición.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- elemento argument Reproductor de Windows Media
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29b0c234d2410d512e2f034f92cbc4a2d6ad7449
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880266"
---
# <a name="argument-element"></a>elemento argument

El **elemento** argument contiene una parte de una cadena de condición. Normalmente, una cadena de condición tiene una parte de condición y una parte de valor. Por ejemplo, en la cadena de condición "Artist Equals Joe", la parte de la condición es "Equals" y la parte del valor es "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Atributos

**name** (obligatorio)

Nombre de una parte de la cadena de condición.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                         |
|-----------|----------------------------------|
| Parent    | [Fragmento](fragment-element.md) |
| Elemento secundario     | None                             |



 

## <a name="remarks"></a>Observaciones

Cuando el atributo  **name** de un elemento de fragmento es una  característica de elemento  multimedia como Album Artist o Genre, el elemento fragment debe contener dos elementos de argumento: uno que especifica una condición y otro que especifica un valor. En la tabla siguiente se muestran dos valores posibles para el atributo **name** y **cómo** se usan los elementos de argumento para especificar condiciones y valores.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor del atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Condición</td>
<td>El contenido del elemento <strong>de argumento</strong> es la parte de condición de una cadena de condición. Por ejemplo, en la cadena de condición &quot; Artist Equals Joe &quot; , la parte de la condición es Igual a &quot; &quot; . La parte de condición de una cadena de condición debe ser una de las siguientes: equals, does not equal, contains, does not contain, is less than, is, is, is not, is before, is later than, is more recent than, above, below, ascending, descending, random, is at least, is no more than.</td>
</tr>
<tr class="even">
<td>Valor</td>
<td>El contenido del elemento <strong>de argumento</strong> es la parte de valor de una cadena de condición. Por ejemplo, en la cadena de condición &quot; Artist Equals Joe &quot; , la parte del valor es Joe &quot; &quot; . Ejemplo:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals&lt;/argument&gt;
  <argument name = &quot;Value&quot;>Joe&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

Cuando el atributo  **name** de un elemento de fragmento es "Limit Total  Size To"  o "Limit Total Duration To", el elemento fragment debe contener dos elementos de argumento: uno que especifica un formato y otro que especifica un número. En la tabla siguiente se muestran dos  valores posibles para el atributo **name** y cómo se usan los elementos de argumento para limitar el tamaño o la duración de una lista de reproducción.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor del atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Formato</td>
<td>Cuando el atributo <strong></strong> <strong>name</strong> del elemento fragment es Limit Total Size To , el contenido del elemento argument debe ser uno de los &quot; &quot; siguientes: Kilobytes, Megabytes o Gigabytes. <strong></strong> <strong></strong> <strong></strong> Cuando el atributo name del elemento de fragmento es Limit Total Duration To , el contenido del elemento de argumento debe ser uno de los &quot; &quot; siguientes: Segundos, Minutos, Horas o Días. <strong></strong><br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>El contenido del elemento <strong>argument</strong> es un número que limita el tamaño o la duración de la lista de reproducción. Ejemplos:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes&lt;/argument&gt;
  <argument name = &quot;Number&quot;>5&lt;/argument&gt;
&lt;/fragment&gt;

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes&lt;/argument&gt;
  <argument name = &quot;Number&quot;>20&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

Cuando el atributo **name** de un elemento **de** fragmento es "Limit  Number of Items", el elemento **fragment** debe contener un elemento de argumento que especifique el número de elementos. En la tabla siguiente se muestra cómo usar el valor Number del **atributo name.**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor del atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Number</td>
<td>El contenido del elemento <strong>argument</strong> es un número que limita el número de elementos de una lista de reproducción. Ejemplo:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**elemento fragment**](fragment-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





