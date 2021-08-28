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
ms.openlocfilehash: ee7237afb37b30ccf8c96ddac95f0e81e148703d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480791"
---
# <a name="listcsv"></a>list.csv

Este archivo contiene una entrada para cada una de las listas que contiene el catálogo. Las listas pueden ser listas de pistas, álbumes, intérpretes, géneros, subgéneos o fuentes de radio. o pueden ser listas de otras listas. Cada entrada de lista es una fila formada por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si integer se indica en la columna Formato, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.




| Campo | Requerido | Formato | Descripción | 
|-------|----------|--------|-------------|
| ListID | Sí | Entero no negativo. | Identificador de lista, único en list.csv. Debe ser no negativo y menor que 2^32. <strong>Mostrar un nodo de lista en el control de vista de árbol:</strong> Si listID es 0, 1, 2, 3, 4, 5, 6 o 7, la lista aparecerá como un nodo personalizado en el nodo de nivel superior de la tienda en línea en el control de vista de árbol del reproductor. Los nodos personalizados aparecen delante de los nodos estándar en el nodo de nivel superior del almacén en línea y listID los coloca en orden ascendente. Por ejemplo, si hay tres nodos personalizados, con listIDs de 1, 3 y 5, se mostrarán primero, segundo y tercero bajo el nodo de nivel superior de la tienda en línea.<br /> | 
| ListTitle | No | Cadena Unicode. Ejemplo: Diez aciertos principales<br /> | Título de la lista. | 
| ListSubtitle | No | Cadena de Unicode | Muestra el título alternativo, que se muestra en la segunda línea de la vista Icono. | 
| ListDescription | Sí | Cadena de Unicode | Enumerar texto descriptivo para mostrar (que se muestra en las páginas de propiedades). | 
| Linked_ItemType | Sí | Cadena Unicode. Formato: [T|P|A|L|G|S|R]<br /> Ejemplo: T<br /> | Indica el tipo de los elementos vinculados.<ul><li>T= Seguimiento</li><li>P = Performer</li><li>A = Álbum</li><li>L = Lista</li><li>G = Género</li><li>S = Subgenre</li><li>R = Radio</li></ul> | 
| ListPrice | Sí | Cadena Unicode. Ejemplo: 9,99 USD<br /> | Precio de la lista. Se debe incluir el símbolo de moneda. Un cero significa que la lista es libre. Ningún valor significa que se desconoce el precio. Un guión significa que no se puede comprar la lista.<br /> | 
| Popularidad | Sí | Valor entero o decimal. Ejemplo: 1259.3<br /> | Indica la clasificación de popularidad cuando esta lista aparece en otras listas. Puede ser cero si no es aplicable. | 
| IsRecentlyAdded | Sí | Boolean.Format: [0|1]<br /> Ejemplo: 0<br /> | Indica si la lista se ha agregado recientemente. | 
| IsFeatured | Sí | Boolean.Format: [0|1]<br /> Ejemplo: 0<br /> | Indica si la lista aparece como destacado. Se puede usar para determinar el criterio de ordenación. | 
| EditorialGlyph | Sí | Entero no negativo. Debe ser 0. | No se usa en esta versión. Debe ser 0. | 
| ViewType | Sí | Cadena Unicode. Formato: [I|T|R|L|O]Ejemplo: T<br /> | Indica el tipo de vista que se usará para la lista.<ul><li>I = Icono</li><li>T = Icono</li><li>R = Informe</li><li>L = Lista</li><li>O = Lista ordenada</li></ul> | 
| ViewImageSize | Sí | Entero no negativo. Ejemplo: 180<br /> | Tamaño con el que se muestra la imagen de lista. Si es 0, el tamaño se determina automáticamente. | 
| GroupBy | Sí | Cadena Unicode. Formato: [-|P|A|C|R|D]<br /> Ejemplo: P<br /> | Indica qué campo se usa para agrupar los elementos de la lista.<ul><li>- = Automático</li><li>P = Performer</li><li>A = Álbum</li><li>C = Composer</li><li>R = Clasificación</li><li>D = Fecha</li></ul> | 
| ListItemsAreDynamic | Sí | booleano. Puede ser 0 o 1. | Indica si la lista se genera dinámicamente. Las listas dinámicas no tienen elementos en listitem.csv. Si una lista está marcada como dinámica, <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a> proporciona sus elementos. | 




 

 

 





