---
title: Integración de biblioteca
description: Integración de biblioteca
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Windows Media Player tiendas en línea, integración de bibliotecas
- tiendas en línea, integración de bibliotecas
- tipo 1 almacenes en línea, integración de biblioteca
- Windows Media Player tiendas en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tipo 1 tiendas en línea, paneles de tareas
- Media Player de Windows, paneles de tareas
- Biblioteca de Media Player de Windows, integrar
- Biblioteca, integración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420284"
---
# <a name="library-integration"></a>Integración de biblioteca

La interfaz de usuario de Windows Media Player está organizada en áreas de características, denominadas *paneles de tareas*, que encapsulan las diversas características de alto nivel del programa. Entre ellos se incluyen los paneles de tareas **biblioteca**, **sincronizar** y **grabar** (entre otros). El panel de tareas **biblioteca** permite a los usuarios trabajar con la biblioteca; el panel de tareas **sincronización** permite a los usuarios sincronizar archivos multimedia digitales con un dispositivo portátil. y el panel de tareas **grabar** permite a los usuarios grabar archivos multimedia digitales en un CD o DVD.

> [!Note]  
> El panel de tareas **biblioteca** se denomina a veces panel de tareas **examinar** .

 

Cada uno de estos paneles de tareas tiene cierto nivel de integración con la biblioteca. Por ejemplo, si el usuario desea grabar música en un CD, tiene sentido permitir que el usuario elija la música que se va a grabar examinando la biblioteca y arrastrando y colocando elementos multimedia en una lista. Esto significa que los usuarios pueden ver y usar un catálogo de la tienda en línea que está totalmente integrado en la biblioteca al trabajar en los paneles de tareas **biblioteca**, **sincronizar** y **grabar** . La enumeración [WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) contiene valores que representan estos tres paneles de tareas para que se puedan identificar mediante programación.

Cada uno de estos tres paneles de tareas se organiza en tres partes principales. La primera parte es el control de vista de árbol de la biblioteca. Este control proporciona al usuario una vista jerárquica de la biblioteca de Media Player de Windows, incluidas las características de categorización por canción, intérprete, álbum, etc. La segunda parte del panel de tareas es el panel de detalles. Este panel proporciona información detallada organizada según la categoría seleccionada actualmente en el control de vista de árbol de la biblioteca. Por ejemplo, si el usuario ha seleccionado **canciones** en la vista de árbol, en el panel de detalles se mostrarán los títulos de la canción que se encuentran actualmente en la biblioteca, junto con otra información como el título de la longitud y el álbum. La tercera parte es el panel lista o *cesta*. Los usuarios pueden arrastrar y colocar elementos multimedia en la cesta para crear listas, como listas de reproducción, listas de sincronización y listas de grabación.

Cuando un catálogo de tienda en línea se integra con la biblioteca, la tienda en línea aparece como una categoría de nivel superior, o *nodo*, en el control de vista de árbol de la biblioteca. (Solo un catálogo de tienda en línea es visible para el usuario a la vez). Cuando un usuario elige ver el catálogo de la tienda en línea haciendo clic en el nodo, el panel de detalles muestra información sobre la música en el catálogo de la tienda en línea. Esto incluye la música que el usuario ha comprado o alquilado, y también la música que el usuario aún no ha adquirido.

El nodo de la tienda en línea de nivel superior tiene un conjunto de nodos secundarios que proporciona Windows Media Player. Por ejemplo, el nodo de tienda en línea de nivel superior tiene nodos secundarios de radio, intérprete y álbum, entre otros. El nodo de la tienda en línea de nivel superior también puede tener hasta ocho nodos secundarios personalizados proporcionados por la tienda en línea. Windows Media Player crea un nodo secundario personalizado para cualquier lista que tenga un identificador de lista en el intervalo comprendido entre 0 y 7. La tienda en línea especifica el identificador de una lista en el [list.csv](list-csv.md) archivo que forma parte del catálogo del almacén.

Windows Media Player recupera un icono para cada uno de los nodos de árbol personalizados de la tienda en línea mediante una llamada a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando CPListIDIcon en el parámetro *bstrInfoName* .

A medida que el usuario navega por el catálogo, Windows Media Player realiza llamadas a **IWMPContentPartner:: GetItemInfo** para recuperar los metadatos del complemento de asociado de contenido acerca de los elementos de música que selecciona el usuario. Estos metadatos proporcionan información al reproductor para que el reproductor pueda mostrar detalles sobre los elementos del catálogo. Por ejemplo, si el usuario selecciona un álbum, Windows Media Player recupera la dirección URL de la carátula de álbum para que el usuario pueda ver la portada del álbum.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




