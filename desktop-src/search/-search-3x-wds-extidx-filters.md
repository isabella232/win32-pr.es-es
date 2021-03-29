---
description: Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Prácticas recomendadas para los controladores de filtro en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540742"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Prácticas recomendadas para crear controladores de filtro en Windows Search

Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo. Puede extender Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo controladores de filtro para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos. Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLSID). Aunque un filtro puede controlar varios tipos de archivo, cada tipo funciona con un solo filtro.

Este tema contiene las siguientes secciones:

-   [Código nativo](#native-code)
-   [Prácticas de código seguro para Windows Search](#secure-code-practices-for-windows-search)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="native-code"></a>Código nativo

En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente. Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan varios complementos.

## <a name="secure-code-practices-for-windows-search"></a>Prácticas de código seguro para Windows Search

A continuación se indican los procedimientos para escribir aplicaciones seguras para su uso con Windows Search.

**Para las aplicaciones de consulta:**

-   Al escribir clientes de búsqueda, debe elegir la API que se ejecuta en un contexto de seguridad que permite al usuario el privilegio mínimo. Por ejemplo, las páginas ASP pueden utilizar el objeto de consulta IXSSO, que se ejecuta como un proceso de usuario.

**Para IFilters y recursos de idioma:**

-   Si se va a instalar un nuevo controlador de filtro para un tipo de archivo como sustituto de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro. No hay ningún mecanismo para encadenar filtros. Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.
-   Los IFilters, los separadores de palabras y lematizadores para Windows Search se ejecutan en el contexto de seguridad local. Se deben escribir para administrar los búferes y para apilarlos correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para evitar las saturaciones del búfer. Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con respecto al tamaño del búfer. Las saturaciones de búfer son una técnica común para aprovechar el código que no impone restricciones de tamaño de búfer.
-   Los componentes de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), separador de palabras y lingüísticos nunca deben llamar a la función de [función ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o a una API similar que termine un proceso y todos sus subprocesos.
-   No asigne ni libere recursos en el punto de entrada de DllMain. Esto puede conducir a errores durante las pruebas de esfuerzo de recursos insuficientes.
-   Codifique todos los objetos para que sean seguros para subprocesos. Windows Search llama a cualquier instancia de un separador de palabras o un analizador lingüístico en un subproceso cada vez, pero puede llamar a varias instancias al mismo tiempo en varios subprocesos.
-   Evite la creación de archivos temporales o la escritura en el registro.
-   Si usa el compilador Microsoft Visual C++, asegúrese de compilar la aplicación con la opción **/GS** . La opción **/GS** se usa para detectar saturaciones del búfer. La opción/GS coloca las comprobaciones de seguridad en el código compilado. Para obtener más información, vea la [función de DllGetClassObject](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (comprobación de seguridad del búfer) en la sección de opciones del compilador Visual C++ del SDK de la plataforma.

## <a name="additional-resources"></a>Recursos adicionales

-   En el ejemplo [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
-   Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
-   Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
-   Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)
</dt> <dt>

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)
</dt> <dt>

[Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)
</dt> <dt>

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
