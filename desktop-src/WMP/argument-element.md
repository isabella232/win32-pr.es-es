---
title: Elemento argument
description: El elemento argument contiene una parte de una cadena de condición.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Elemento argument de Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699801"
---
# <a name="argument-element"></a>Elemento argument

El elemento **argument** contiene una parte de una cadena de condición. Normalmente, una cadena de condición tiene una parte de condición y una parte de valor. Por ejemplo, en la cadena de condición "artista Equals Joe", la parte de la condición es "Equals" y la parte del valor es "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Atributos

**nombre** (obligatorio)

Nombre de una parte de la cadena de condición.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                         |
|-----------|----------------------------------|
| Parent    | [Fragment](fragment-element.md) |
| Elemento secundario     | None                             |



 

## <a name="remarks"></a>Observaciones

Cuando el atributo **Name** de un elemento **Fragment** es una característica de elemento multimedia como el intérprete del álbum, o el género, el elemento **Fragment** debe contener dos elementos **argument** : uno que especifique una condición y otro que especifique un valor. En la tabla siguiente se muestran dos valores posibles para el atributo **Name** y cómo se usan los elementos **argument** para especificar condiciones y valores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>El contenido del elemento <strong>argument</strong> es la parte de la condición de una cadena de condición. Por ejemplo, en el intérprete de la cadena de condición es &quot; igual a Joe &quot; , la parte de la condición es &quot; igual a &quot; . La parte de la condición de una cadena de condición debe ser uno de los siguientes: es igual a, no es igual a, contiene, no contiene, es menor que, es mayor que, es, no es, es anterior, es posterior a, es más reciente que, más abajo, ascendente, descendente, aleatorio, es al menos, no es más que.</td>
</tr>
<tr class="even">
<td>Value</td>
<td>El contenido del elemento <strong>argument</strong> es la parte del valor de una cadena de condición. Por ejemplo, en el intérprete de la cadena de condición es &quot; igual a Joe &quot; , la parte del valor es &quot; Joe &quot; . Ejemplo<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Cuando el atributo **Name** de un elemento **Fragment** es "Limit total size to" o "Limit total Duration to", el elemento **Fragment** debe contener dos elementos **argument** : uno que especifique un formato y otro que especifique un número. En la tabla siguiente se muestran dos valores posibles para el atributo **Name** y cómo se usan los elementos **argument** para limitar el tamaño o la duración de una lista de reproducción.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Cuando el atributo <strong>Name</strong> del elemento <strong>Fragment</strong> tiene el &quot; límite de tamaño total en &quot; , el contenido del elemento <strong>argument</strong> debe ser uno de los siguientes: kilobytes, megabytes o gigabytes. cuando el atributo <strong>Name</strong> del elemento <strong>Fragment</strong> es &quot; Limit total Duration to &quot; , el contenido del elemento <strong>argument</strong> debe ser uno de los siguientes: segundos, minutos, horas o días.<br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>El contenido del elemento <strong>argument</strong> es un número que limita el tamaño o la duración de la lista de reproducción. Example<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Cuando el atributo **Name** de un elemento **Fragment** es "Limit Number of items", el elemento **Fragment** debe contener un elemento **argument** que especifique el número de elementos. En la tabla siguiente se muestra cómo utilizar el valor numérico del atributo **Name** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>El contenido del elemento <strong>argument</strong> es un número que limita el número de elementos de una lista de reproducción. Ejemplo<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





