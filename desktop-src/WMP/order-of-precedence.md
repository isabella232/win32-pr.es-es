---
title: Orden de precedencia
description: Orden de precedencia
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Metarchivos multimedia, orden de prioridad
- Windows Metarchivos multimedia, prioridad
- metarchivos, orden de prioridad
- metarchivos, prioridad
- Windows Multimedia, metarchivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476213"
---
# <a name="order-of-precedence"></a>Orden de precedencia

No todos los atributos de elemento de metarchivo se crean iguales. Algunos atributos de elemento de metarchivo invalidan otros atributos de elemento. Los atributos de elemento se pueden reemplazar por atributos de elemento similares en función de la posición y el orden. Los atributos de una lista de reproducción de metarchivo reemplazan a los contenidos en un archivo Windows media. Un atributo que invalida otro tiene mayor prioridad.

En la tabla siguiente se muestra la jerarquía, la prioridad más alta a la más baja. El elemento de prioridad más alta nunca se invalida.



| Ámbito                    | Hierarchy                                   |
|--------------------------|---------------------------------------------|
| "Contenido DRM firmado"     | Nunca se invalida.                           |
| **Ámbito del** elemento REF    | Solo se reemplaza por contenido DRM firmado.      |
| **Ámbito del** elemento ENTRY  | Invalida los elementos de las categorías siguientes. |
| **Ámbito de ASX**            | Invalida los elementos del archivo multimedia.              |
| Windows Ámbito del archivo multimedia | Se reemplaza por todos los anteriores.             |



 

-   "Contenido drm firmado": objeto de firma digital.

    Los atributos del contenido drm firmado reemplazarán a todos los demás. Por ejemplo, no se invalidará la información de copyright del "contenido DRM firmado". Siempre se transmitirá y presentará.

-   **Ámbito del** elemento REF

    Los atributos del **elemento REF** invalidarán otros atributos de elemento, pero no el contenido DRM firmado.

-   **Ámbito ENTRY**

    Los atributos del **elemento ENTRY** se reemplazarán por el atributo de elemento **REF,** pero invalidarán otros atributos de elemento. **Los** metadatos TITLE del **elemento ENTRY** se muestran en lugar de la información de título del archivo multimedia.

-   **Ámbito de ASX**

    Las propiedades que se introducen en el metarchivo invalidan las contenidas en el Windows multimedia. Los atributos del **elemento ENTRY** invalidan los atributos del elemento **ASX.** Mientras se **reproduce el** clip multimedia al que se hace referencia del elemento **ENTRY,** se muestran los metadatos TITLE del **elemento ENTRY** en lugar de la información de título del **elemento ASX.**

-   Windows Ámbito del archivo multimedia

    Los atributos del archivo Windows multimedia se reemplazan por cualquier atributo de metarchivo. Los metadatos del archivo multimedia solo se muestran si no hay ningún metadato definido para ese elemento en el metarchivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




