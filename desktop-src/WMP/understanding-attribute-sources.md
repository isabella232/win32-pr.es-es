---
title: Descripción de los orígenes de atributos
description: Descripción de los orígenes de atributos
ms.assetid: 83274fea-233d-40dc-b587-99e99ddcd92b
keywords:
- Reproductor de Windows Media,attributes para elementos multimedia
- Reproductor de Windows Media modelo de objetos, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Reproductor de Windows Media Móvil, atributos para elementos multimedia
- Reproductor de Windows Media ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media Control de ActiveX móviles, atributos para elementos multimedia
- ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media biblioteca, atributos para elementos multimedia
- library,attributes para elementos multimedia
- attributes,sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b7266b75f8f506b1f06e822fbbb40a85d8f2dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465807"
---
# <a name="understanding-attribute-sources"></a>Descripción de los orígenes de atributos

Los atributos o metadatos que puede usar proceden de diversos orígenes. En este tema se describen esos orígenes, pasando de escenarios con menos atributos potenciales a aquellos con más atributos potenciales.

Mientras el usuario reproduce un CD o DVD, tiene acceso a muy pocos metadatos sobre el propio disco o el contenido multimedia del disco. Los discos comerciales no suelen incluir metadatos de atributo.

Si el usuario ha reproducdo un CD o DVD mientras estaba conectado a Internet, es posible que tenga acceso a más atributos cuando ese disco está en la unidad de CD o DVD. Mientras Reproductor de Windows Media está conectado a Internet y reproduciendo un CD o DVD, el reproductor recupera los metadatos de ese disco de una base de datos en línea. El reproductor muestra esta información en **Reproducción ahora** y en un nodo independiente de la biblioteca. Los atributos no se almacenan en la base de datos de biblioteca, pero se almacenan en caché. Si la memoria caché aún no se ha vaciado, la aplicación tendrá acceso a los atributos mientras el disco está en la unidad.

> [!Note]  
> Los usuarios pueden optar por no permitir la recuperación de información multimedia de una base de datos en línea. En ese caso, los únicos atributos disponibles serán los de un archivo multimedia digital, los que el usuario ha escrito manualmente en la biblioteca y los generados por el propio reproductor (por ejemplo, los atributos relacionados con la frecuencia con la que se ha reproducido un elemento).

 

Si el usuario reproduce un archivo multimedia digital que no se agrega a la biblioteca, tendrá acceso a los atributos que se encuentran en el archivo.

Si el usuario reproduce un archivo multimedia digital que se ha agregado a la biblioteca, tiene acceso a los atributos que se almacenan solo en la biblioteca, los atributos que se almacenan solo en el archivo y los atributos que se almacenan en la biblioteca y el archivo.

Los atributos que están disponibles para los elementos multimedia agregados a la biblioteca varían en función de cómo se creó el archivo multimedia digital de origen y de las acciones que ha llevado a cabo el usuario desde que lo agregó.

-   El creador del contenido puede insertar información de atributos en el archivo cuando se crea por primera vez. Por ejemplo, si crea y distribuye un archivo multimedia digital con la aplicación, tendrá control sobre qué atributos se insertaron originalmente en el archivo.
-   Si el usuario modifica los datos de atributo de un elemento multimedia que se ha agregado a la biblioteca, mediante el Editor de etiquetas avanzado o la interfaz de usuario de la biblioteca, Reproductor de Windows Media agrega los datos a la base de datos de biblioteca. El reproductor agrega algunos atributos directamente al archivo porque solo se almacenan en el archivo. En algún momento indeterminado, los atributos de lectura y escritura se sincronizan con el archivo para que los atributos almacenados en la biblioteca y el archivo tengan el mismo valor.
-   Si el usuario copia una pista de un CD mediante Reproductor de Windows Media mientras está conectado a Internet, el efecto es prácticamente el mismo que si el usuario hubiera modificado atributos mediante Reproductor de Windows Media. Los atributos se agregan a la base de datos de biblioteca, extraídos del propio archivo y de una base de datos en línea. Algunos atributos solo se almacenan en el archivo . En algún momento indeterminado, la base de datos de biblioteca se sincroniza con el archivo .
-   Si escribe código mediante el control Reproductor de Windows Media para cambiar el valor de un atributo de lectura y escritura existente en un elemento multimedia que se ha agregado a la biblioteca, el efecto es prácticamente el mismo que si el usuario hubiera modificado el atributo mediante Reproductor de Windows Media. El valor se escribe en la base de datos de biblioteca y, en algún momento indeterminado, la base de datos se sincroniza con el archivo.
-   [!Note]  
    > Si inserta el control en la aplicación, los atributos de archivo que cambie no se escribirán en el propio archivo multimedia digital hasta que el usuario ejecute Reproductor de Windows Media. Si usa el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios. En cualquier caso, los cambios están disponibles inmediatamente a través de la biblioteca.

     

-   Si escribe código mediante el control Reproductor de Windows Media para insertar un atributo personalizado en un elemento multimedia, el atributo y su valor solo se conservarán siempre que la aplicación tenga una referencia al **objeto Media.** Ni el atributo ni su valor se almacenarán en la base de datos de la biblioteca ni en el archivo multimedia digital, si lo hay.

La situación más sencilla es cuando se trabaja con archivos multimedia digitales que ha proporcionado. En ese escenario, sabe que hay atributos específicos en el archivo. Al agregar el elemento multimedia a la biblioteca, sabe que puede trabajar con esos atributos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elementos multimedia**](media-item-attributes.md)
</dt> </dl>

 

 




