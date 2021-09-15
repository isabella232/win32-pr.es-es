---
title: Integración de bibliotecas
description: Integración de bibliotecas
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Reproductor de Windows Media en línea, integración de bibliotecas
- tiendas en línea, integración de bibliotecas
- tiendas en línea de tipo 1, integración de bibliotecas
- Reproductor de Windows Media en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tiendas en línea de tipo 1, paneles de tareas
- Reproductor de Windows Media,paneles de tareas
- Reproductor de Windows Media, integración
- library,integrating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360560"
---
# <a name="library-integration"></a>Integración de bibliotecas

La Reproductor de Windows Media de usuario se organiza en áreas de características, denominadas paneles de tareas , que encapsulan las *distintas* características de alto nivel del programa. Estos incluyen los paneles  de **tareas** **Biblioteca,** Sincronización y Grabación (entre otros). El **panel de** tareas Biblioteca permite a los usuarios trabajar con la biblioteca; el **panel de** tareas Sincronizar permite a los usuarios sincronizar archivos multimedia digitales con un dispositivo portátil. y el **panel de** tareas Grabar permite a los usuarios grabar archivos multimedia digitales en un CD o DVD.

> [!Note]  
> El **panel de** tareas Biblioteca a veces se denomina panel **de** tareas Examinar.

 

Cada uno de estos paneles de tareas tiene algún nivel de integración con la biblioteca. Por ejemplo, si el usuario quiere grabar música en un CD, tiene sentido dejar que el usuario elija la música que se va a grabar explorando la biblioteca y simplemente arrastrando y colocando elementos multimedia en una lista. Esto significa que los usuarios pueden ver y usar un catálogo de tiendas en  línea que esté totalmente integrado en la biblioteca cuando trabajen en los paneles de tareas **Biblioteca,** Sincronización y Grabación. La [enumeración WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) contiene valores que representan estos tres paneles de tareas para que se puedan identificar mediante programación.

Cada uno de estos tres paneles de tareas se organiza en tres partes principales. La primera parte es el control de vista de árbol de biblioteca. Este control proporciona al usuario una vista jerárquica de la biblioteca Reproductor de Windows Media, incluidas las características de categorización por canción, intérprete, álbum, etc. La segunda parte del panel de tareas es el panel de detalles. Este panel proporciona información detallada organizada según la categoría seleccionada actualmente en el control de vista de árbol de biblioteca. Por ejemplo, si el usuario ha hecho clic en **Canciones** en la vista de árbol, el panel de detalles mostrará los títulos de las canciones actualmente en la biblioteca, junto con otra información como la longitud y el título del álbum. La tercera parte es el panel de lista o *cesta.* Los usuarios pueden arrastrar y colocar elementos multimedia en la cesta para crear listas de reproducción, listas de reproducción, listas de sincronización y listas de grabación.

Cuando un catálogo de tiendas en línea se integra con la biblioteca, el almacén en línea aparece como una categoría de nivel superior, o nodo *,* en el control de vista de árbol de la biblioteca. (Solo un catálogo de tiendas en línea es visible para el usuario a la vez). Cuando un usuario decide ver el catálogo de tiendas en línea haciendo clic en el nodo, el panel de detalles muestra información sobre la música en el catálogo de tiendas en línea. Esto incluye música que el usuario ha comprado o alquilado, y también música que el usuario aún no ha adquirido.

El nodo de almacén en línea de nivel superior tiene un conjunto de nodos secundarios proporcionados por Reproductor de Windows Media. Por ejemplo, el nodo de la tienda en línea de nivel superior tiene los nodos secundarios Radio, Artist y Album, entre otros. El nodo de la tienda en línea de nivel superior también puede tener hasta ocho nodos secundarios personalizados proporcionados por la tienda en línea. Reproductor de Windows Media crea un nodo secundario personalizado para cualquier lista que tenga un identificador de lista en el intervalo de 0 a 7. La tienda en línea especifica el identificador de una lista en ellist.csv[ que ](list-csv.md) forma parte del catálogo de la tienda.

Reproductor de Windows Media recupera un icono para cada uno de los nodos de árbol personalizados de la tienda en línea llamando a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando CPListIDIcon en el *parámetro bstrInfoName.*

A medida que el usuario navega por el catálogo, Reproductor de Windows Media realiza llamadas a **IWMPContentPartner::GetItemInfo** para recuperar metadatos del complemento del asociado de contenido sobre los elementos de música que el usuario selecciona. Estos metadatos proporcionan información al reproductor para que el reproductor pueda mostrar detalles sobre los elementos del catálogo. Por ejemplo, si el usuario selecciona un álbum, Reproductor de Windows Media la dirección URL del álbum para que el usuario pueda ver la portada del álbum.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




