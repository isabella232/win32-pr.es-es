---
description: Obtenga información sobre cómo desarrollar controladores de filtro en Windows Search. La búsqueda usa filtros para extraer elementos para su inclusión en un índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desarrollar controladores de filtro para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cb8fe61ce85c86d0b8397d81303014ed1268bc0aef96b22e7b7bab335b7f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597825"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Desarrollar controladores de filtro para Windows Search

Microsoft Windows Search usa filtros para extraer el contenido de los elementos para su inclusión en un índice de texto completo. Puede ampliar Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo filtros para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.

En esta sección se proporciona el marco conceptual necesario para implementar un controlador de filtro (una implementación de la [**interfaz IFilter).**](/windows/win32/api/filter/nn-filter-ifilter)

- [Descripción de los controladores de filtros en Windows Search](-search-ifilter-about.md)
- [Procedimientos recomendados para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)
- [Devolver propiedades de un controlador de filtros](-search-ifilter-property-filtering.md)
- [Controladores de filtro que se envían con Windows](-search-ifilter-implementations.md)
- [Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)
- [Registro de controladores de filtro](-search-ifilter-registering-filters.md)
- [Probar controladores de filtro](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Recursos adicionales

- El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), muestra cómo crear una clase base IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
