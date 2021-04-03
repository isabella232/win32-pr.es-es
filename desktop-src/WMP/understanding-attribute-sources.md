---
title: Descripción de los orígenes de atributos
description: Descripción de los orígenes de atributos
ms.assetid: 83274fea-233d-40dc-b587-99e99ddcd92b
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, orígenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b7266b75f8f506b1f06e822fbbb40a85d8f2dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779314"
---
# <a name="understanding-attribute-sources"></a>Descripción de los orígenes de atributos

Los atributos, o metadatos, que puede utilizar proceden de diversos orígenes. En este tema se describen esos orígenes, pasando de escenarios con menos atributos potenciales a los que tienen más atributos potenciales.

Mientras el usuario reproduce un CD o DVD, tiene acceso a muy pocos metadatos sobre el propio disco o el contenido multimedia del disco. Normalmente, los discos comerciales no incluyen metadatos de atributos.

Si el usuario ha reproducido un CD o DVD mientras estaba conectado a Internet, es posible que tenga acceso a más atributos cuando dicho disco esté en la unidad de CD o DVD. Aunque Windows Media Player está conectado a Internet y reproduciendo un CD o DVD, el reproductor recupera los metadatos de ese disco de una base de datos en línea. El reproductor muestra esta información en **reproducción** en curso y en un nodo independiente de la biblioteca. Los atributos no se almacenan en la base de datos de biblioteca, pero se almacenan en caché. Si la memoria caché no se ha vaciado todavía, la aplicación tendrá acceso a los atributos mientras el disco está en la unidad.

> [!Note]  
> Los usuarios pueden optar por no permitir la recuperación de información multimedia de una base de datos en línea. En ese caso, los únicos atributos disponibles son los de un archivo multimedia digital, los que el usuario ha escrito manualmente en la biblioteca y los generados por el propio reproductor (por ejemplo, los atributos relacionados con la frecuencia de reproducción de un elemento).

 

Si el usuario reproduce un archivo multimedia digital que no se agrega a la biblioteca, tiene acceso a los atributos que se encuentran en el archivo.

Si el usuario reproduce un archivo multimedia digital que se ha agregado a la biblioteca, tiene acceso a los atributos que solo se almacenan en la biblioteca, los atributos que solo se almacenan en el archivo y los atributos que se almacenan en la biblioteca y en el archivo.

Los atributos que están disponibles para los elementos multimedia que se agregan a la biblioteca varían en función de cómo se creó el archivo multimedia digital de origen y las acciones que ha realizado el usuario desde que se agregó.

-   El creador de contenido puede insertar información de atributos en el archivo cuando se crea por primera vez. Por ejemplo, si crea y distribuye un archivo multimedia digital con la aplicación, tendrá control sobre los atributos que se insertaron originalmente en el archivo.
-   Si el usuario modifica los datos de atributos de un elemento multimedia que se ha agregado a la biblioteca, mediante el editor de etiquetas avanzado o la interfaz de usuario de la biblioteca, Windows Media Player agrega los datos a la base de datos de la biblioteca. El reproductor agrega algunos atributos directamente al archivo porque solo se almacenan en el archivo. En algún momento indeterminado, los atributos de lectura y escritura se sincronizan con el archivo para que los atributos que se almacenan tanto en la biblioteca como en el archivo tengan el mismo valor.
-   Si el usuario copia una pista desde un CD mediante Windows Media Player mientras está conectado a Internet, el efecto es casi el mismo que si el usuario hubiera modificado atributos mediante Windows Media Player. Los atributos se agregan a la base de datos de biblioteca, que se extraen del archivo en sí y de una base de datos en línea. Algunos atributos solo se almacenan en el archivo. En algún momento indeterminado, la base de datos de biblioteca se sincroniza con el archivo.
-   Si escribe código mediante el control Media Player de Windows para cambiar el valor de un atributo de lectura/escritura existente en un elemento multimedia que se ha agregado a la biblioteca, el efecto es casi el mismo que si el usuario hubiera modificado el atributo mediante Media Player de Windows. El valor se escribe en la base de datos de biblioteca y, en algún momento indeterminado, la base de datos se sincroniza con el archivo.
-   [!Note]  
    > Si incrusta el control en la aplicación, los atributos de archivo que cambie no se escribirán en el propio archivo multimedia digital hasta que el usuario ejecute Windows Media Player. Si utiliza el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios. En cualquier caso, los cambios están disponibles inmediatamente a través de la biblioteca.

     

-   Si escribe código mediante el control Media Player de Windows para insertar un atributo personalizado en un elemento multimedia, el atributo y su valor se conservarán solo mientras la aplicación tenga una referencia al objeto **multimedia** . Ni el atributo ni su valor se almacenarán en la base de datos de biblioteca ni en el archivo multimedia digital, si hay alguno.

La situación más sencilla es cuando se trabaja con archivos multimedia digitales que ha proporcionado. En ese escenario, sabrá que hay atributos específicos en el archivo. Al agregar el elemento multimedia a la biblioteca, sabe que puede trabajar con esos atributos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elemento multimedia**](media-item-attributes.md)
</dt> </dl>

 

 




