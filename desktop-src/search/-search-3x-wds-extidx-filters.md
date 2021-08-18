---
description: Obtenga información sobre los procedimientos recomendados para crear controladores de filtro en Windows Search. La búsqueda usa filtros para extraer elementos para su inclusión en un índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Procedimientos recomendados para los controladores de filtros en Windows Búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8320cf0f85bf86f7d61df09437271af67d0e4096fc3a917d037914854c9bad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463704"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Procedimientos recomendados para crear controladores de filtro en Windows búsqueda

Microsoft Windows Search usa filtros para extraer el contenido de los elementos para su inclusión en un índice de texto completo. Puede ampliar Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo controladores de filtro para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos. Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLID). Aunque un filtro puede controlar varios tipos de archivo, cada tipo funciona con un solo filtro.

Este tema contiene las siguientes secciones:

-   [Código nativo](#native-code)
-   [Prácticas de código seguro para Windows Search](#secure-code-practices-for-windows-search)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="native-code"></a>Código nativo

En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente. Los filtros DEBEN escribirse en código nativo debido a posibles problemas de control de versiones clr con el proceso en el que se ejecutan varios complementos.

## <a name="secure-code-practices-for-windows-search"></a>Prácticas de código seguro para Windows Search

Estos son los procedimientos para escribir aplicaciones seguras para su uso con Windows Search.

**Para aplicaciones de consulta:**

-   Al escribir clientes de búsqueda, debe elegir la API que se ejecuta en un contexto de seguridad que permita al usuario tener menos privilegios. Por ejemplo, las páginas ASP pueden usar el objeto de consulta IXSSO, que se ejecuta como un proceso de usuario.

**Para IFilters y recursos de lenguaje:**

-   Si se instala un nuevo controlador de filtro para un tipo de archivo como reemplazo de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro. No hay ningún mecanismo para encadenar filtros. Por lo tanto, el nuevo controlador de filtros es responsable de replicar cualquier funcionalidad necesaria del filtro anterior.
-   Los IFilters, separadores de palabras y lematizadores para Windows Search se ejecutan en el contexto de seguridad local. Se deben escribir para administrar búferes y para apilar correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para protegerse frente a saturaciones del búfer. Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con el tamaño del búfer. Las saturaciones de búfer son una técnica común para aprovechar el código que no aplica restricciones de tamaño de búfer.
-   [**Los componentes IFilter**](/windows/win32/api/filter/nn-filter-ifilter), separador de palabras y lematizador nunca deben llamar a la función [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ni a una API similar que finalice un proceso y todos sus subprocesos.
-   No asigne ni libre recursos en el punto de entrada de DllMain. Esto puede provocar errores durante las pruebas de esfuerzo de pocos recursos.
-   Codifie todos los objetos para que sean seguros para subprocesos. Windows Search llama a cualquier instancia de un separador de palabras o lematizador en un subproceso a la vez, pero puede llamar a varias instancias al mismo tiempo en varios subprocesos.
-   Evite crear archivos temporales o escribir en el Registro.
-   Si usa el compilador Microsoft Visual C++, asegúrese de compilar la aplicación mediante la **opción /GS.** La **opción /GS** se usa para detectar saturaciones de búfer. La opción /GS coloca las comprobaciones de seguridad en el código compilado. Para obtener más información, vea [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)GS (Buffer Security Check) (DllGetClassObject Function GS [Comprobación de seguridad del búfer]) en la sección Visual C++ Compiler Options (Opciones del  /  compilador) del SDK de plataforma.

## <a name="additional-resources"></a>Recursos adicionales

-   En [el ejemplo IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) se muestra cómo crear una clase base IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
-   Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
-   Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
-   Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Registro de aplicaciones.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)
</dt> <dt>

[Acerca de los controladores de filtro en Windows Búsqueda](-search-ifilter-about.md)
</dt> <dt>

[Devolver propiedades de un controlador de filtros](-search-ifilter-property-filtering.md)
</dt> <dt>

[Controladores de filtro que se envían con Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementar controladores de filtro en la Windows búsqueda](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)
</dt> <dt>

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
