---
description: El registro de un tipo de archivo es el primer paso para crear una asociación de archivo, que hace que ese tipo de archivo &\# 0034; conocido&\# 0034; en el shell. Sin embargo, sin controladores de tipo de archivo, el shell no puede exponer información al usuario desde y sobre el archivo.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Controladores de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907849"
---
# <a name="file-type-handlers"></a>Controladores de tipo de archivo

El [registro de un tipo de archivo](fa-how-work.md) es el primer paso para crear una asociación de archivo, que hace que ese tipo de archivo sea "conocido" en el shell. Sin embargo, sin controladores de tipo de archivo, el shell no puede exponer información al usuario desde y sobre el archivo.

Este tema se organiza de la siguiente manera:

-   [Convertir un tipo de archivo en Shell](#make-a-file-type-known-to-shell)
-   [Descripciones del controlador de tipo de archivo](#file-type-handler-descriptions)
-   [Temas relacionados](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Convertir un tipo de archivo en Shell

En la siguiente captura de pantalla del explorador de Windows, el archivo de imagen desierto. conocido aparece en la biblioteca de **imágenes** de Shell y está asociado únicamente a la aplicación Paint.

![captura de pantalla que muestra que el explorador abre una imagen sin tipo de archivo](images/file-assoc/fileassoc-filetypehandler.png)

El archivo desierto. know en la captura de pantalla anterior no tiene la siguiente funcionalidad habilitada por un controlador de tipo de archivo:

-   Miniatura o vista previa
-   Verbos específicos de la imagen en el menú contextual, como:
    -   Rotar vista previa
    -   Establecer como fondo de escritorio
    -   Impresión
-   Propiedades específicas de la imagen en el panel de **detalles** , como:
    -   Fecha de creación
    -   Etiquetas
    -   Rating
-   Indexación del texto del archivo

En la siguiente captura de pantalla, el mismo archivo (desierto. known) tiene la extensión. jpg, que es un tipo de archivo registrado con controladores de tipo de archivo asociados, por lo que se muestra una imagen en miniatura y más propiedades.

![imagen con un tipo de archivo registrado y controladores de tipo de archivo asociados](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Descripciones del controlador de tipo de archivo

La funcionalidad proporcionada por cada controlador de tipo de archivo se muestra en la tabla siguiente:



| Controlador                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menú contextual](context-menu-handlers.md)                   | Un controlador de menú contextual, que a veces se denomina controlador de menú contextual, es un controlador de tipo de archivo que agrega comandos a un menú contextual existente. Estos controladores están asociados a un tipo de archivo determinado y se les llama cada vez que se muestra un menú contextual para un miembro del tipo de archivo.                                                                                                                                                                                                                                                                           |
| [Miniatura](thumbnail-providers.md)                         | Un controlador que proporciona una imagen para representar un elemento de Shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Propiedad](../properties/building-property-handlers-properties.md) | Un controlador de propiedades que proporciona acceso a las propiedades de los elementos de búsqueda de Windows, el explorador de Windows y otras aplicaciones que necesitan tener acceso a las propiedades.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Versión preliminar](preview-handlers.md)                              | Un controlador que genera rápidamente una vista simplificada de solo lectura del elemento que se va a mostrar en el panel de vista previa del explorador de Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtros](../search/-search-3x-wds-extidx-filters.md)              | Un filtro, una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , que examina documentos en busca de texto y propiedades (también denominados atributos). Extrae fragmentos de texto de estos documentos, filtrando el formato incrustado y conservando la información sobre la posición del texto. También extrae fragmentos de valores, que son propiedades de un documento completo o de partes bien definidas de un documento. **IFilter** proporciona la base para la creación de aplicaciones de nivel superior como indexadores de documentos y visores independientes de la aplicación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
