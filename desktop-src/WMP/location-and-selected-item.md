---
title: Ubicación y elemento seleccionado
description: Ubicación y elemento seleccionado
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Reproductor de Windows Media en línea, ubicaciones
- tiendas en línea, ubicaciones
- tiendas en línea de tipo 1, ubicaciones
- Reproductor de Windows Media en línea, ubicaciones de biblioteca
- tiendas en línea, ubicaciones de biblioteca
- tiendas en línea de tipo 1, ubicaciones de biblioteca
- Reproductor de Windows Media en línea,elementos seleccionados
- tiendas en línea, elementos seleccionados
- tiendas en línea de tipo 1, elementos seleccionados
- Reproductor de Windows Media biblioteca, ubicaciones
- Reproductor de Windows Media biblioteca, elementos seleccionados
- library,locations
- library,selected items
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6532c6417b6e95632aa21fa8d4a3a9ed943ad844eb1324f34eb80191043eeb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003385"
---
# <a name="location-and-selected-item"></a>Ubicación y elemento seleccionado

Reproductor de Windows Media usa los cinco elementos siguientes para caracterizar su vista actual del contenido de la tienda en línea:

-   task
-   tipo de ubicación de biblioteca
-   Id. de ubicación de la biblioteca
-   tipo de elemento seleccionado
-   Id. de elemento seleccionado

Normalmente, puede pensar en la vista en Reproductor de Windows Media como un contenedor de elementos. El contenedor tiene un tipo y un elemento tiene un tipo. Todos los elementos de un contenedor tienen el mismo tipo. Tanto los tipos de ubicación como los tipos de elemento se especifican mediante las constantes [de ubicación de la biblioteca](library-location-constants.md). Por ejemplo, si la vista actual muestra un álbum individual, el tipo de ubicación de la biblioteca es CPAlbumID y, como un álbum contiene pistas, el tipo de elemento seleccionado es CPTrackID.

En la tabla siguiente se muestran los tipos de ubicación y elemento de varios contenedores.



| Descripción del contenedor                              | Tipo de ubicación de biblioteca | Tipo de elemento seleccionado |
|-------------------------------------------------------|-----------------------|--------------------|
| Un álbum que es un contenedor de pistas                | CPAlbumID             | CPTrackID          |
| Lista que es un contenedor de pistas                  | CPListID              | CPTrackID          |
| Lista que es un contenedor de álbumes                  | CPListID              | CPAlbumID          |
| Una estación de radio que es un contenedor de listas          | CPRadioID             | CPListID           |
| Conjunto de todos los álbumes, que es un contenedor de álbumes | AllCPAlbumIDs         | CPAlbumID          |
| Conjunto de todos los géneros, que es un contenedor de géneros | AllCPGenreIDs         | CPGenreID          |



 

Las pestañas de Reproductor de Windows Media representan tareas diferentes. El reproductor muestra el contenido de la tienda en línea en tres paneles de tareas diferentes: **Biblioteca,** **Grabar** y **Sincronizar.** El panel de tareas Biblioteca también se denomina **panel de** tareas Examinar. A veces, un panel de tareas se denomina  *característica*, por lo que es posible que vea términos como Característica de grabación y Característica *de sincronización* en esta documentación.

En los ejemplos siguientes se muestra cómo Reproductor de Windows Media utiliza los cinco fragmentos de información (tarea, tipo de ubicación de biblioteca, identificador de ubicación de biblioteca, tipo de elemento seleccionado, id. de elemento seleccionado) para caracterizar distintas vistas.

En el **panel de** tareas Grabar, el reproductor muestra un álbum como un contenedor de pistas. El álbum tiene un identificador de 250. En la vista, el elemento seleccionado es la pista que tiene un identificador de 800. Tenga en cuenta que 800 es el identificador de la pista en el catálogo de la tienda en línea, no el número de la pista del álbum.



| Elemento                  | Value     |
|-----------------------|-----------|
| task                  | Quemar      |
| tipo de ubicación de biblioteca | CPAlbumID |
| Id. de ubicación de la biblioteca   | 250       |
| tipo de elemento seleccionado    | CPTrackID |
| Id. de elemento seleccionado      | 800       |



 

En el **panel de** tareas Sincronizar, el reproductor muestra el conjunto de todos los álbumes, que es un contenedor de álbumes. En la vista, el elemento seleccionado es el álbum que tiene un identificador de 300. Tenga en cuenta que el identificador de ubicación de la biblioteca no es aplicable a esta vista.



| Elemento                  | Value         |
|-----------------------|---------------|
| task                  | Sync          |
| tipo de ubicación de biblioteca | AllCPAlbumIDs |
| Id. de ubicación de la biblioteca   | N/D           |
| tipo de elemento seleccionado    | CPAlbumID     |
| Id. de elemento seleccionado      | 300           |



 

En el control de vista de árbol, se selecciona el nodo raíz del almacén en línea. En este caso, no hay ningún contenedor y, por consiguiente, no hay elementos. Todo el panel **de** tareas Biblioteca muestra una página de detección.



| Elemento                  | Value           |
|-----------------------|-----------------|
| task                  | Examinar          |
| tipo de ubicación de biblioteca | RootLocation    |
| Id. de ubicación de la biblioteca   | N/D             |
| tipo de elemento seleccionado    | UnknownLocation |
| Id. de elemento seleccionado      | N/D             |



 

En el **panel de** tareas Sincronizar, el reproductor muestra el año 2002 como un contenedor de pistas. En la vista, el elemento seleccionado es la pista que tiene un identificador de 450.



| Elemento                  | Value           |
|-----------------------|-----------------|
| task                  | Sync            |
| tipo de ubicación de biblioteca | ReleaseDateYear |
| Id. de ubicación de la biblioteca   | 2002            |
| tipo de elemento seleccionado    | CPTrackID       |
| Id. de elemento seleccionado      | 450             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Páginas de detección**](discovery-pages.md)
</dt> </dl>

 

 




