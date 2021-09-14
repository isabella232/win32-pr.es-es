---
description: En este tema se describe una nueva vista en Windows Explorer, denominada vista Contenido, que muestra el contenido más relevante para cada elemento.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256928"
---
# <a name="content-view-by-file-type-or-kind"></a>Vista de contenido por tipo de archivo o tipo

En este tema se describe una nueva vista en Windows Explorer, denominada vista Contenido, que muestra el contenido más relevante para cada elemento. Con un conjunto de claves del Registro, los elementos pueden definir una lista de propiedades y un diseño que el Shell usa para la vista Contenido. El Shell recupera las claves del Registro mediante la matriz de asociación [del elemento](fa-perceivedtypes.md).

## <a name="how-does-the-content-view-work"></a>¿Cómo funciona la vista de contenido?

En Windows 7 y versiones posteriores, la vista Contenido usa una lógica de cambiar el tamaño que quita las propiedades cuando el tamaño de la ventana disminuye, para asegurarse de que las propiedades más críticas todavía tienen espacio para ser claramente legibles. En la captura de pantalla siguiente se muestra la vista Contenido de los resultados de búsqueda que contienen música, imágenes y documentos.

![vista de contenido de los resultados de búsqueda que contienen música, imágenes y documentos](images/content-view/contentviewsearchresults.png)

Algunos orígenes de datos de Shell usan la vista Contenido de forma predeterminada, pero los usuarios pueden seleccionar la vista Contenido haciendo clic en el botón **Ver control** en Windows Explorador. Un origen de datos de Shell amplía el espacio de nombres de Shell y expone los elementos de un almacén de datos. Los elementos de un almacén de datos se pueden indexar mediante el sistema Windows Search mediante un controlador de protocolo.

## <a name="how-to-implement-the-content-view"></a>Cómo implementar la vista de contenido

Al registrar un nuevo tipo [de archivo](fa-file-types.md) o controlador de [protocolo,](../search/-search-3x-wds-extidx-prot-implementing.md)puede aprovechar la vista Contenido mediante cualquiera de los dos enfoques diferentes. Puede usar un conjunto existente de propiedades y un patrón de diseño, o bien puede crear su propia combinación.

Puede usar una entrada del Registro para asociar el tipo de archivo o elemento a un tipo [predefinido,](../properties/building-property-handlers-user-friendly-kind-names.md)que es una propiedad que se puede pensar como una categoría de contenido. Al asociar el tipo de archivo o elemento a algunos de estos tipos, hereda automáticamente las listas de propiedades y los patrones de diseño de la vista Contenido de esa clase. Windows modelos de diseño de vista de contenido y listas de propiedades para los siguientes tipos: documentos, correo electrónico, carpeta, música, imagen y genéricos. Se recomienda este tipo de asociación. Permite proporcionar la experiencia coherente que un usuario espera para elementos similares.

Para obtener más información, [](../properties/building-property-handlers-user-friendly-kind-names.md) vea [Tipos](fa-file-types.md) de archivo y nombres de tipo y Cómo registrar un conjunto de propiedades de vista de contenido único y Patrón de diseño para el tipo [de archivo o elemento](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener documentación de referencia de propiedades, [vea System.Kind](../properties/props-system-kind.md)y [System.KindText.](../properties/props-system-kindtext.md)
-   Para obtener documentación de referencia de PropList, vea [System.PropList.ContentViewModeForBrowse y](../properties/props-system-proplist-contentviewmodeforbrowse.md) [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).

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

[Controladores de tipos de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores mediante programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
