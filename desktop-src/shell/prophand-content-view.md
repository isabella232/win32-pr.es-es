---
description: En este tema se describe una nueva vista en el explorador de Windows, denominada vista de contenido, que muestra el contenido más relevante para cada elemento.
title: Vista de contenido por tipo de archivo o tipo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814838"
---
# <a name="content-view-by-file-type-or-kind"></a>Vista de contenido por tipo de archivo o tipo

En este tema se describe una nueva vista en el explorador de Windows, denominada vista de contenido, que muestra el contenido más relevante para cada elemento. Con un conjunto de claves del registro, los elementos pueden definir una lista de propiedades y un diseño que el shell utiliza para la vista de contenido. El shell recupera las claves del registro mediante la [matriz de asociaciones](fa-perceivedtypes.md)del elemento.

## <a name="how-does-the-content-view-work"></a>¿Cómo funciona la vista de contenido?

En Windows 7 y versiones posteriores, la vista de contenido usa una lógica de cambio de tamaño que quita las propiedades cuando se reduce el tamaño de la ventana, para asegurarse de que las propiedades más críticas todavía tienen espacio para ser legibles claramente. En la captura de pantalla siguiente se muestra la vista de contenido de los resultados de la búsqueda que contienen música, imágenes y documentos.

![vista de contenido de los resultados de la búsqueda que contienen música, imágenes y documentos](images/content-view/contentviewsearchresults.png)

Algunos orígenes de datos de Shell usan la vista de contenido de forma predeterminada, pero los usuarios pueden seleccionar la vista de contenido haciendo clic en el botón **Ver control** en el explorador de Windows. Un origen de datos de Shell extiende el espacio de nombres del shell y expone elementos en un almacén de datos. El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo.

## <a name="how-to-implement-the-content-view"></a>Cómo implementar la vista de contenido

Al registrar un nuevo [tipo de archivo](fa-file-types.md) o [controlador de protocolo](../search/-search-3x-wds-extidx-prot-implementing.md), puede aprovechar la vista de contenido mediante uno de dos enfoques diferentes. Puede usar un conjunto de propiedades y un patrón de diseño existente, o puede crear su propia combinación.

Puede usar una entrada del registro para asociar el tipo de archivo o el elemento a [un tipo predefinido,](../properties/building-property-handlers-user-friendly-kind-names.md)que es una propiedad que se puede considerar como una categoría de contenido. Al asociar el tipo de archivo o el elemento con algunos de estos tipos, se heredan automáticamente los patrones de diseño y las listas de propiedades de la vista de contenido de ese tipo. Windows define los patrones de diseño y las listas de propiedades de la vista de contenido para los siguientes tipos: documentos, correo electrónico, carpeta, música, imagen y genérico. Se recomienda este tipo de asociación. Permite proporcionar la experiencia coherente que un usuario espera para elementos similares.

Para obtener más información, vea [tipos de archivo](fa-file-types.md) y nombres de [tipo](../properties/building-property-handlers-user-friendly-kind-names.md) y [Cómo registrar un conjunto de vistas de contenido único de propiedades y patrones de diseño para el tipo de archivo o el elemento](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener documentación de referencia de propiedades, vea [System. Kind](../properties/props-system-kind.md)y [System. KindText](../properties/props-system-kindtext.md).
-   Para obtener documentación de referencia de proplist, vea [System. proplist. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)y [System. proplist. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
