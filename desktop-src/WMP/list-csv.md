---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Reproductor de Windows Media en línea, list.csv
- tiendas en línea, list.csv
- tiendas en línea de tipo 1, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e754f7985fbf59c23cccae5fd9780ff4b4579205ceaf3ef3cc8f74c768d4e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135348"
---
# <a name="listcsv"></a>list.csv

Este archivo contiene una entrada para cada una de las listas que contiene el catálogo. Las listas pueden ser listas de pistas, álbumes, intérpretes, géneros, subgéneos o fuentes de radio. o pueden ser listas de otras listas. Cada entrada de lista es una fila compuesta por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si entero se indica en la columna Formato , significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



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
<th>Requerido</th>
<th>Formato</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ListID</td>
<td>Sí</td>
<td>Entero no negativo.</td>
<td>Identificador de lista, único en list.csv. Debe ser no negativo y menor que 2^32. <strong>Mostrar un nodo de lista en el control de vista de árbol:</strong> Si listID es 0, 1, 2, 3, 4, 5, 6 o 7, la lista aparecerá como un nodo personalizado bajo el nodo de nivel superior de la tienda en línea en el control de vista de árbol del reproductor. Los nodos personalizados aparecen delante de los nodos estándar en el nodo de nivel superior de la tienda en línea y ListID los coloca en orden ascendente. Por ejemplo, si hay tres nodos personalizados, con listIDs de 1, 3 y 5, se mostrarán primero, segundo y tercero bajo el nodo de nivel superior de la tienda en línea.<br/></td>
</tr>
<tr class="even">
<td>ListTitle</td>
<td>No</td>
<td>Cadena Unicode. Ejemplo: Diez aciertos principales<br/></td>
<td>Título de la lista.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>No</td>
<td>Cadena de Unicode</td>
<td>Muestra el título alternativo, que se muestra en la segunda línea de la vista Icono.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Sí</td>
<td>Cadena de Unicode</td>
<td>Enumerar texto descriptivo para mostrar (que se muestra en las páginas de propiedades).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Sí</td>
<td>Cadena Unicode. Formato: [T| P| A| L|G| S| R]<br/> Ejemplo: T<br/></td>
<td>Indica el tipo de los elementos vinculados.
<ul>
<li>T= Seguimiento</li>
<li>P = Performer</li>
<li>A = Album</li>
<li>L = Lista</li>
<li>G = Género</li>
<li>S = Subgenre</li>
<li>R = Radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Sí</td>
<td>Cadena Unicode. Ejemplo: 9,99 USD<br/></td>
<td>Precio de la lista. Se debe incluir el símbolo de moneda. Un cero significa que la lista es gratuita. Ningún valor significa que el precio es desconocido. Un guion significa que no se puede comprar la lista.<br/></td>
</tr>
<tr class="odd">
<td>Popularidad</td>
<td>Sí</td>
<td>Valor entero o decimal. Ejemplo: 1259.3<br/></td>
<td>Indica la clasificación de popularidad cuando esta lista aparece en otras listas. Puede ser cero si no es aplicable.</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Sí</td>
<td>Boolean.Format: [0|1]<br/> Ejemplo: 0<br/></td>
<td>Indica si la lista se ha agregado recientemente.</td>
</tr>
<tr class="odd">
<td>IsFeatured</td>
<td>Sí</td>
<td>Boolean.Format: [0|1]<br/> Ejemplo: 0<br/></td>
<td>Indica si la lista tiene características. Se puede usar para determinar el criterio de ordenación.</td>
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
<td>Cadena Unicode. Formato: [I|T| R| L|O]Ejemplo: T<br/></td>
<td>Indica el tipo de vista que se usará para la lista.
<ul>
<li>I = Icono</li>
<li>T = Icono</li>
<li>R = Informe</li>
<li>L = Lista</li>
<li>O = Lista ordenada</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Sí</td>
<td>Entero no negativo. Ejemplo: 180<br/></td>
<td>Tamaño en el que se muestra la imagen de lista. Si es 0, el tamaño se determina automáticamente.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Sí</td>
<td>Cadena Unicode. Formato: [-| P| A| C|R| D]<br/> Ejemplo: P<br/></td>
<td>Indica qué campo se usa para agrupar los elementos de la lista.
<ul>
<li>- = Automático</li>
<li>P = Performer</li>
<li>A = Album</li>
<li>C = Composer</li>
<li>R = Clasificación</li>
<li>D = Fecha</li>
</ul></td>
</tr>
<tr class="even">
<td>ListItemsAreDynamic</td>
<td>Sí</td>
<td>booleano. Puede ser 0 o 1.</td>
<td>Indica si la lista se genera dinámicamente. Las listas dinámicas no tienen elementos en listitem.csv. Si una lista está marcada como dinámica, <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a> proporciona sus elementos.</td>
</tr>
</tbody>
</table>



 

 

 





