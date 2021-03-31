---
description: Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desarrollar controladores de filtro para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082021"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Desarrollar controladores de filtro para Windows Search

Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo. Puede extender Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo filtros para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.

En esta sección se proporciona el marco conceptual que es necesario para implementar un controlador de filtro (una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

- [Descripción de los controladores de filtro en Windows Search](-search-ifilter-about.md)
- [Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)
- [Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)
- [Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)
- [Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)
- [Registrar controladores de filtro](-search-ifilter-registering-filters.md)
- [Probar controladores de filtro](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
