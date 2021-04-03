---
title: Orden de precedencia
description: Orden de precedencia
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Metaarchivos de Windows Media, orden de prioridad
- Metaarchivos de Windows Media, prioridad
- metaarchivos, orden de prioridad
- metaarchivos, prioridad
- Windows Media, metaarchivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075375"
---
# <a name="order-of-precedence"></a>Orden de precedencia

No todos los atributos de elemento de metarchivo se crean igual. Algunos atributos de elemento de metarchivo invalidan otros atributos de elemento. Los atributos de elemento pueden reemplazarse por atributos de elemento similares en función de la posición y el orden. Los atributos de una lista de reproducción de metarchivo invalidan los contenidos en un archivo de Windows Media al que se hace referencia. Un atributo que reemplaza a otro tiene mayor precedencia.

En la tabla siguiente se muestra la jerarquía de prioridad más alta a la más baja. El elemento de prioridad más alto nunca se invalida.



| Ámbito                    | Hierarchy                                   |
|--------------------------|---------------------------------------------|
| "Contenido DRM firmado"     | Nunca se invalida.                           |
| Ámbito del elemento **ref**    | Solo se reemplaza por contenido DRM firmado.      |
| Ámbito del elemento de **entrada**  | Reemplaza los elementos de las categorías siguientes. |
| Ámbito de **ASX**            | Invalida los elementos de archivo multimedia.              |
| Ámbito de archivo de Windows Media | Reemplazado por todo lo anterior.             |



 

-   "Contenido DRM firmado": objeto de firma digital.

    Los atributos de contenido DRM firmado reemplazarán a todos los demás. Por ejemplo, la información de copyright de "contenido DRM firmado" no se invalidará. Siempre se transmitirá por secuencias y se presentará.

-   Ámbito del elemento **ref**

    Los atributos del elemento **ref** reemplazarán a otros atributos de elemento, pero no a contenido DRM firmado.

-   Ámbito de **entrada**

    El atributo de elemento de **referencia** invalidará los atributos del elemento de **entrada** , pero invalidará otros atributos de elemento. Los metadatos de **título** del elemento de **entrada** se muestran en lugar de la información de título del archivo multimedia.

-   Ámbito de **ASX**

    Las propiedades que se escriban en el metarchivo invalidarán las contenidas en el archivo de Windows Media. Los atributos del elemento de **entrada** reemplazan los atributos del elemento **ASX** . Mientras se reproduce el clip multimedia al que se hace referencia del elemento de **entrada** , se muestran los metadatos del **título** del elemento de **entrada** en lugar de la información de título del elemento **ASX** .

-   Ámbito de archivo de Windows Media

    Los atributos de metarchivo reemplazan a los atributos del archivo de Windows Media. Los metadatos del archivo multimedia se muestran solo si no hay metadatos definidos para ese elemento en el metarchivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




