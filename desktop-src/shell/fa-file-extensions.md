---
description: El registro de un tipo de archivo es el primer paso para crear una asociación de archivos, lo que hace que ese tipo de archivo &\# 0034;known&\# 0034; en el Shell. Sin embargo, sin controladores de tipo de archivo, el Shell no puede exponer información al usuario desde y sobre el archivo.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Controladores de tipos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404cfd3be4c3e8a600b2f943bda1243ca243b70af411e104000245edd13d94c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459733"
---
# <a name="file-type-handlers"></a>Controladores de tipos de archivo

[El registro de un tipo de](fa-how-work.md) archivo es el primer paso para crear una asociación de archivos, lo que hace que ese tipo de archivo sea "conocido" para el Shell. Sin embargo, sin controladores de tipo de archivo, el Shell no puede exponer información al usuario desde y sobre el archivo.

Este tema se organiza de la siguiente manera:

-   [Hacer que shell conozca un tipo de archivo](#make-a-file-type-known-to-shell)
-   [Descripciones del controlador de tipos de archivo](#file-type-handler-descriptions)
-   [Temas relacionados](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Hacer que shell conozca un tipo de archivo

En la siguiente captura de pantalla de Windows Explorer, el archivo de imagen Desuso.known aparece en la biblioteca **Imágenes** de shell y solo está asociado a la Paint aplicación.

![captura de pantalla que muestra el explorador que abre una imagen sin tipo de archivo](images/file-assoc/fileassoc-filetypehandler.png)

El archivo Momento.conocido de la captura de pantalla anterior carece de la siguiente funcionalidad habilitada por un controlador de tipo de archivo:

-   Miniatura o vista previa
-   Verbos específicos de la imagen en el menú contextual, como:
    -   Girar vista previa
    -   Establecer como fondo de escritorio
    -   Impresión
-   Propiedades específicas de la imagen en **el panel** Detalles, como:
    -   Fecha de toma
    -   Etiquetas
    -   Rating
-   Indexación del texto del archivo

En la siguiente captura de pantalla, el mismo archivo (Mime.known) tiene la extensión .jpg, que es un tipo de archivo registrado que tiene controladores de tipo de archivo asociados, por lo que se muestra una imagen en miniatura y más propiedades.

![imagen con un tipo de archivo registrado y controladores de tipo de archivo asociados](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Descripciones del controlador de tipos de archivo

La funcionalidad proporcionada por cada controlador de tipo de archivo se muestra en la tabla siguiente:



| Controlador                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menú contextual](context-menu-handlers.md)                   | Un controlador de menú contextual, que a veces se conoce como controlador de menú contextual, es un controlador de tipos de archivo que agrega comandos a un menú contextual existente. Estos controladores están asociados a un tipo de archivo determinado y se llaman cada vez que se muestra un menú contextual para un miembro del tipo de archivo.                                                                                                                                                                                                                                                                           |
| [Miniatura](thumbnail-providers.md)                         | Controlador que proporciona una imagen para representar un elemento de Shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Propiedad](../properties/building-property-handlers-properties.md) | Controlador de propiedades que proporciona acceso a las propiedades de elemento para Windows Search, Windows Explorer y otras aplicaciones que necesitan acceder a las propiedades.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Versión preliminar](preview-handlers.md)                              | Controlador que genera rápidamente una vista simplificada y de solo lectura del elemento que se va a mostrar en el panel de vista previa Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtros](../search/-search-3x-wds-extidx-filters.md)              | Filtro, una implementación de la [**interfaz IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) que examina los documentos en busca de texto y propiedades (también denominados atributos). Extrae fragmentos de texto de estos documentos, filtrando el formato incrustado y conservando información sobre la posición del texto. También extrae fragmentos de valores, que son propiedades de un documento completo o de partes bien definidas de un documento. **IFilter** proporciona la base para crear aplicaciones de nivel superior, como indexadores de documentos y visores independientes de la aplicación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo o tipo de archivo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipos de archivo](file-type-verifier.md)
</dt> <dt>

[Identificadores mediante programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
