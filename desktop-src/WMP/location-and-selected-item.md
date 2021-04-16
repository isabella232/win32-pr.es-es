---
title: Ubicación y elemento seleccionado
description: Ubicación y elemento seleccionado
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player tiendas en línea, ubicaciones
- tiendas en línea, ubicaciones
- tipo 1 almacenes en línea, ubicaciones
- Windows Media Player tiendas en línea, ubicaciones de biblioteca
- tiendas en línea, ubicaciones de biblioteca
- tipo 1 almacenes en línea, ubicaciones de biblioteca
- Windows Media Player tiendas en línea, elementos seleccionados
- tiendas en línea, elementos seleccionados
- tipo 1 tiendas en línea, elementos seleccionados
- Biblioteca Media Player de Windows, ubicaciones
- Biblioteca de Media Player de Windows, elementos seleccionados
- Biblioteca, ubicaciones
- Biblioteca, elementos seleccionados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268688"
---
# <a name="location-and-selected-item"></a>Ubicación y elemento seleccionado

Windows Media Player usa los cinco elementos siguientes para caracterizar su vista actual del contenido de la tienda en línea:

-   task
-   tipo de ubicación de la biblioteca
-   ID. de ubicación de biblioteca
-   tipo de elemento seleccionado
-   IDENTIFICADOR del elemento seleccionado

Normalmente, puede pensar en la vista de Windows Media Player como un contenedor de elementos. El contenedor tiene un tipo y un elemento tiene un tipo. Todos los elementos de un contenedor tienen el mismo tipo. Los tipos de ubicación y los tipos de elemento se especifican mediante las [constantes de ubicación](library-location-constants.md)de la biblioteca. Por ejemplo, si la vista actual muestra un álbum individual, el tipo de ubicación de la biblioteca es CPAlbumID y, dado que un álbum contiene pistas, el tipo de elemento seleccionado es CPTrackID.

En la tabla siguiente se muestran los tipos de ubicación y elemento de varios contenedores.



| Descripción del contenedor                              | Tipo de ubicación de la biblioteca | Tipo de elemento seleccionado |
|-------------------------------------------------------|-----------------------|--------------------|
| Un álbum que es un contenedor de pistas                | CPAlbumID             | CPTrackID          |
| Una lista que es un contenedor de pistas                  | CPListID              | CPTrackID          |
| Una lista que es un contenedor de álbumes                  | CPListID              | CPAlbumID          |
| Una emisora de radio que es un contenedor de listas          | CPRadioID             | CPListID           |
| Conjunto de todos los álbumes, que es un contenedor de álbumes. | AllCPAlbumIDs         | CPAlbumID          |
| Conjunto de todos los géneros, que es un contenedor de géneros | AllCPGenreIDs         | CPGenreID          |



 

Las pestañas de Windows Media Player representan diferentes tareas. El reproductor muestra el contenido de la tienda en línea en tres paneles de tareas diferentes: **biblioteca**, **grabación** y **sincronización**. El panel de tareas biblioteca también se denomina panel de tareas **examinar** . A veces, un panel de tareas se denomina *característica*, por lo que puede ver términos como característica de *grabación* y *característica de sincronización* en esta documentación.

En los siguientes ejemplos se muestra cómo Windows Media Player usa las cinco piezas de información (tarea, tipo de ubicación de biblioteca, identificador de ubicación de biblioteca, tipo de elemento seleccionado, ID. de elemento seleccionado) para caracterizar distintas vistas.

En el panel de tareas **grabar** , el reproductor muestra un álbum como un contenedor de pistas. El álbum tiene un identificador de 250. En la vista, el elemento seleccionado es la pista que tiene un identificador de 800. Tenga en cuenta que 800 es el identificador de la pista en el catálogo de la tienda en línea, no el número de la pista en el álbum.



| Elemento                  | Value     |
|-----------------------|-----------|
| task                  | Burn      |
| tipo de ubicación de la biblioteca | CPAlbumID |
| ID. de ubicación de biblioteca   | 250       |
| tipo de elemento seleccionado    | CPTrackID |
| IDENTIFICADOR del elemento seleccionado      | 800       |



 

En el panel de tareas de **sincronización** , el reproductor muestra el conjunto de todos los álbumes, que es un contenedor de álbumes. En la vista, el elemento seleccionado es el álbum que tiene un identificador de 300. Tenga en cuenta que el identificador de ubicación de la biblioteca no es aplicable a esta vista.



| Elemento                  | Value         |
|-----------------------|---------------|
| task                  | Sync          |
| tipo de ubicación de la biblioteca | AllCPAlbumIDs |
| ID. de ubicación de biblioteca   | N/D           |
| tipo de elemento seleccionado    | CPAlbumID     |
| IDENTIFICADOR del elemento seleccionado      | 300           |



 

En el control de vista de árbol, se selecciona el nodo raíz de la tienda en línea. En este caso, no hay ningún contenedor y, por consiguiente, no hay elementos. El panel de tareas **biblioteca** completa muestra una página de detección.



| Elemento                  | Value           |
|-----------------------|-----------------|
| task                  | Examinar          |
| tipo de ubicación de la biblioteca | RootLocation    |
| ID. de ubicación de biblioteca   | N/D             |
| tipo de elemento seleccionado    | UnknownLocation |
| IDENTIFICADOR del elemento seleccionado      | N/D             |



 

En el panel de tareas de **sincronización** , el reproductor muestra el año 2002 como un contenedor de pistas. En la vista, el elemento seleccionado es la pista que tiene un identificador de 450.



| Elemento                  | Value           |
|-----------------------|-----------------|
| task                  | Sync            |
| tipo de ubicación de la biblioteca | ReleaseDateYear |
| ID. de ubicación de biblioteca   | 2002            |
| tipo de elemento seleccionado    | CPTrackID       |
| IDENTIFICADOR del elemento seleccionado      | 450             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Páginas de detección**](discovery-pages.md)
</dt> </dl>

 

 




