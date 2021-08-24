---
description: Las propiedades se extraen de elementos mediante controladores de propiedades registrados o mediante filtros registrados para tipos de archivo específicos. Un controlador de filtro (una implementación de la interfaz IFilter) puede interpretar el contenido de un tipo de archivo de cualquier manera.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Devolver propiedades de un controlador de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1842710af65e22f5a730891ea6e7f32053b92212f8c3ad4c5f0f68f23578d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594864"
---
# <a name="returning-properties-from-a-filter-handler"></a>Devolver propiedades de un controlador de filtros

Las propiedades se extraen de elementos mediante controladores de propiedades registrados o mediante filtros registrados para tipos de archivo específicos. Un controlador de filtro (una implementación de la [**interfaz IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) puede interpretar el contenido de un tipo de archivo de cualquier manera.

Este tema se organiza de la siguiente manera:

- [Filtrado de propiedades](#returning-properties-from-a-filter-handler)
  - [Limitaciones de tamaño de propiedad](#property-size-limitations)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="property-filtering"></a>Filtrado de propiedades

En la tabla siguiente se enumeran los procedimientos recomendados para el filtrado de propiedades.

| Método                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Devuelve la [**enumeración \_ FLAGS de IFILTER.**](/windows/win32/api/filter/ne-filter-ifilter_flags) Si el miembro OLE PROPERTIES de *IFILTER \_ \_ \_ FLAGS* de esta enumeración se establece en uno, Windows Search usa las interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) interfaces para enumerar y acceder a propiedades de tipo de valor externo. |
| [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Devuelve información de un documento en "fragmentos" con tipo de fragmento (texto o valor), nombre y configuración regional. Un fragmento contiene una propiedad de documento.                                                                                                                                                                                                                                                                                                      |
| [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Obtiene una propiedad de tipo de texto de un fragmento.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Obtiene una propiedad de tipo de valor de un fragmento.                                                                                                                                                                                                                                                                                                                                                                                                        |

En la ilustración siguiente se muestra un documento de ejemplo. La propiedad value-type externa (obtenida mediante métodos de las `DocTitle` interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage)](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) y la propiedad de tipo de valor interno (obtenida como resultado de una implementación personalizada de `Book` [**IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) describen el documento en su conjunto. Las propiedades de tipo de `Contents` texto `Chapter` y describen el contenido del documento. Al procesar este documento, el controlador de filtros (una implementación de la **interfaz IFilter)** identifica y extrae estas propiedades.

![diagrama que muestra los elementos de un documento típico](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitaciones de tamaño de propiedad

Hay dos posibles limitaciones en el tamaño de propiedad:

- Tamaño máximo de los datos que Windows Search acepta por archivo.
- Tamaño máximo por propiedad, tal como se define en el archivo de descripción de la propiedad.

Actualmente, Windows Search no usa el tamaño de propiedad definido al calcular la cantidad de datos que acepta de un elemento. En su lugar, el límite Windows Search es el producto del tamaño del archivo y el (tamaño de archivo `MaxGrowFactor` N \* MaxGrowFactor) leídos del Registro. El valor `MaxGrowFactor` predeterminado es cuatro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Por lo tanto, si el tipo de archivo tiende a ser pequeño en tamaño total pero tiene propiedades más grandes, es posible que Windows Search no acepte todos los datos de propiedad que desea emitir. Sin embargo, puede aumentar para `MaxGrowFactor` satisfacer sus necesidades.

## <a name="additional-resources"></a>Recursos adicionales

- El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), muestra cómo crear una clase base IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
- Para obtener información general sobre las propiedades y los controladores de propiedades, y una lista de las propiedades del sistema que puede usar para los formatos de archivo, vea [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Búsqueda](-search-ifilter-about.md)

[Procedimientos recomendados para crear controladores de filtro en Windows búsqueda](-search-3x-wds-extidx-filters.md)

[Controladores de filtro que se envían con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en la Windows búsqueda](-search-ifilter-constructing-filters.md)

[Registro de controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
