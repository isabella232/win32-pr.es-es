---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player tiendas en línea, list.csv
- tiendas en línea, list.csv
- Escriba 1 tiendas en línea, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149072"
---
# <a name="listcsv"></a>list.csv

Este archivo contiene una entrada para cada una de las listas que contiene el catálogo. Las listas pueden ser listas de pistas, álbumes, intérpretes, géneros, subgéneros o fuentes de radio. o bien, pueden ser listas de otras listas. Cada entrada de la lista es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Obligatorio</th>
<th>Formato</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ListID</td>
<td>Sí</td>
<td>Entero no negativo.</td>
<td>Identificador de lista, único en list.csv. No debe ser negativo y menor que 2 ^ 32. <strong>Mostrar un nodo de lista en el control de vista de árbol:</strong> Si ListID es 0, 1, 2, 3, 4, 5, 6 o 7, la lista aparecerá como un nodo personalizado en el nodo de nivel superior de la tienda en línea en el control de vista de árbol del reproductor. Los nodos personalizados aparecen antes que los nodos estándar en el nodo de nivel superior de la tienda en línea y se colocan en orden ascendente por ListID. Por ejemplo, si hay tres nodos personalizados, con Listid de 1, 3 y 5, se mostrarán primero, segundo y tercero en el nodo de nivel superior de la tienda en línea.<br/></td>
</tr>
<tr class="even">
<td>ListTitle</td>
<td>No</td>
<td>Cadena Unicode. Ejemplo: diez golpes principales<br/></td>
<td>Título de la lista.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>No</td>
<td>Cadena de Unicode</td>
<td>Mostrar el título alternativo, que se muestra en la segunda línea de la vista de mosaico.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Sí</td>
<td>Cadena de Unicode</td>
<td>Muestra el texto para mostrar descriptivo (mostrado en páginas de propiedades).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Sí</td>
<td>Cadena Unicode. Formato: [T | P | Un | L | G | S | C<br/> Ejemplo: T<br/></td>
<td>Indica el tipo de los elementos vinculados.
<ul>
<li>T = pista</li>
<li>P = rendimiento</li>
<li>A = álbum</li>
<li>L = lista</li>
<li>G = Género</li>
<li>S = subgénero</li>
<li>R = radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Sí</td>
<td>Cadena Unicode. Ejemplo: $9,99<br/></td>
<td>Precio de la lista. Se debe incluir el símbolo de moneda. Un cero significa que la lista es gratuita. Ningún valor significa que se desconoce el precio. Un guion significa que la lista no se puede comprar.<br/></td>
</tr>
<tr class="odd">
<td>Popularidad</td>
<td>Sí</td>
<td>Valor entero o decimal. Ejemplo: 1259,3<br/></td>
<td>Indica la categoría de popularidad cuando esta lista aparece en otras listas. Puede ser cero si no es aplicable.</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Sí</td>
<td>Booleano. formato: [0 | 1]<br/> Ejemplo: 0<br/></td>
<td>Indica si la lista se ha agregado recientemente.</td>
</tr>
<tr class="odd">
<td>IsFeatured</td>
<td>Sí</td>
<td>Booleano. formato: [0 | 1]<br/> Ejemplo: 0<br/></td>
<td>Indica si la lista está destacada. Se puede usar para determinar el criterio de ordenación.</td>
</tr>
<tr class="even">
<td>EditorialGlyph</td>
<td>Sí</td>
<td>Entero no negativo. Debe ser 0.</td>
<td>No se usa en esta versión. Debe ser 0.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Sí</td>
<td>Cadena Unicode. Formato: [I | T | R | L | O] ejemplo: T<br/></td>
<td>Indica el tipo de vista que se va a utilizar para la lista.
<ul>
<li>I = icono</li>
<li>T = icono</li>
<li>R = informe</li>
<li>L = lista</li>
<li>O = Lista ordenada</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Sí</td>
<td>Entero no negativo. Ejemplo: 180<br/></td>
<td>Tamaño en el que se muestra la imagen de la lista. Si es 0, el tamaño se determina automáticamente.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Sí</td>
<td>Cadena Unicode. Formato: [-| P | Un | C | R | D<br/> Ejemplo: P<br/></td>
<td>Indica el campo que se utiliza para agrupar los elementos de la lista.
<ul>
<li>- = Automático</li>
<li>P = rendimiento</li>
<li>A = álbum</li>
<li>C = compositor</li>
<li>R = clasificación</li>
<li>D = fecha</li>
</ul></td>
</tr>
<tr class="even">
<td>ListItemsAreDynamic</td>
<td>Sí</td>
<td>booleano. Puede ser 0 o 1.</td>
<td>Indica si la lista se genera dinámicamente. Las listas dinámicas no tienen elementos en listitem.csv. Si una lista está marcada como dinámica, <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner:: GetListContents</a> proporciona los elementos.</td>
</tr>
</tbody>
</table>



 

 

 





