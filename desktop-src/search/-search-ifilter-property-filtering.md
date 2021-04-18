---
description: Las propiedades se extraen de los elementos mediante controladores de propiedad registrados o mediante filtros registrados para tipos de archivo específicos. Un controlador de filtro (una implementación de la interfaz IFilter) puede interpretar el contenido de un tipo de archivo de varias maneras.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Devolver propiedades de un controlador de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df0bfc811176e9b0672dbcbe4ef4f04f3c3a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720335"
---
# <a name="returning-properties-from-a-filter-handler"></a>Devolver propiedades de un controlador de filtro

Las propiedades se extraen de los elementos mediante controladores de propiedad registrados o mediante filtros registrados para tipos de archivo específicos. Un controlador de filtro (una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) puede interpretar el contenido de un tipo de archivo de varias maneras.

Este tema se organiza de la siguiente manera:

- [Filtrado de propiedades](#returning-properties-from-a-filter-handler)
  - [Limitaciones de tamaño de propiedad](#property-size-limitations)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="property-filtering"></a>Filtrado de propiedades

En la tabla siguiente se enumeran los procedimientos recomendados para el filtrado de propiedades.

| Método                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Devuelve la enumeración de [**\_ marcas de IFILTER**](/windows/win32/api/filter/ne-filter-ifilter_flags) . Si el miembro de *\_ \_ \_ propiedades OLE de marcadores de IFILTER* de esta enumeración está establecido en uno, la búsqueda de Windows usa las interfaces de interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) y [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) para enumerar y tener acceso a las propiedades de tipo de valor externo. |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Devuelve información de un documento en "fragmentos" con el tipo de fragmento (texto o valor), el nombre y la configuración regional. Un fragmento contiene una propiedad de documento.                                                                                                                                                                                                                                                                                                      |
| [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Obtiene una propiedad de tipo de texto de un fragmento.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Obtiene una propiedad de tipo de valor de un fragmento.                                                                                                                                                                                                                                                                                                                                                                                                        |

En la ilustración siguiente se muestra un documento de ejemplo. La propiedad de tipo de valor externo `DocTitle` (obtenida con los métodos de las interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) y [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ) y la propiedad de tipo de valor interno `Book` (obtenida como resultado de una implementación de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) personalizada) describen el documento como un todo. Propiedades de tipo de texto `Contents` y `Chapter` describen el contenido del documento. Al procesar este documento, el controlador de filtro (una implementación de la interfaz de **IFilter** ) identifica y extrae estas propiedades.

![diagrama que muestra los elementos de un documento típico](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitaciones de tamaño de propiedad

Hay dos limitaciones posibles para el tamaño de la propiedad:

- El tamaño máximo de datos que la búsqueda de Windows acepta por archivo.
- Tamaño máximo por propiedad tal y como se define en el archivo de descripción de la propiedad.

Actualmente, Windows Search no utiliza el tamaño de propiedad definido al calcular la cantidad de datos que acepta de un elemento. En su lugar, el límite que usa Windows Search es el producto del tamaño del archivo y el `MaxGrowFactor` (tamaño de archivo N \* MaxGrowFactor) leído del registro. El valor predeterminado `MaxGrowFactor` es cuatro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Por lo tanto, si el tipo de archivo tiende a ser pequeño en tamaño total pero tiene propiedades más grandes, es posible que Windows Search no acepte todos los datos de propiedad que desea emitir. Sin embargo, puede aumentar el `MaxGrowFactor` para que se adapte a sus necesidades.

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
- Para obtener información general sobre las propiedades y los controladores de propiedades, así como una lista de propiedades del sistema que puede usar para los formatos de archivo, vea [desarrollar controladores de propiedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
