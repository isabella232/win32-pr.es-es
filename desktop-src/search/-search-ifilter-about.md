---
description: Los controladores de filtro, que son implementaciones de la interfaz de IFilter, analizan documentos en busca de texto y propiedades.
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: Descripción de los controladores de filtro en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540718"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>Descripción de los controladores de filtro en Windows Search

Los controladores de filtro, que son implementaciones de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , analizan documentos en busca de texto y propiedades. Los controladores de filtro extraen fragmentos de texto de estos elementos, filtran el formato incrustado y conservan información sobre la posición del texto. También extraen fragmentos de valores, que son propiedades del documento. **IFilter** es la base para la creación de aplicaciones de nivel superior como indexadores de documentos y visores independientes de la aplicación.

Este tema se organiza de la siguiente manera:

- [Acerca de la interfaz IFilter](#about-the-ifilter-interface)
  - [Proceso de aislamiento](#isolation-process)
  - [Archivos dll de IFilter](#ifilter-dlls)
  - [Estructura de IFilter](#ifilter-structure)
  - [Código nativo](#native-code)
- [Buscar el identificador de clase de IFilter](#finding-the-ifilter-class-identifier)
  - [IFilter:: GetChunk y identificadores de código de configuración regional](#ifiltergetchunk-and-locale-code-identifiers)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="about-the-ifilter-interface"></a>Acerca de la interfaz IFilter

Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo. Puede extender Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo filtros para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.

La interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) está diseñada para satisfacer las necesidades específicas de los motores de búsqueda de texto completo. Los motores de búsqueda de texto completo, como Windows Search, llaman a los métodos de **IFilter** para extraer información de texto y de propiedades y agregarlas a un índice. Windows Search rompe los resultados del método [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelto en palabras, los normaliza y los guarda en un índice. Si está disponible, el motor de búsqueda utiliza el identificador de código de idioma (LCID) de un fragmento de texto para realizar la separación y normalización de palabras específicas del idioma.

Windows Search usa tres funciones, que se describen en la tabla siguiente, para tener acceso a los controladores de filtro registrados (implementaciones de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ). Estas funciones son especialmente útiles cuando se carga y se enlaza a un controlador de filtro de un objeto incrustado.

| Función               | Descripción                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LoadIFilter            | Obtiene un puntero al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que es más adecuado para el tipo de contenido especificado.                                                                                            |
| BindIFilterFromStorage | Obtiene un puntero al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que es más adecuado para el contenido incluido en un objeto de [interfaz IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . |
| BindIFilterFromStream  | Obtiene un puntero al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que es más adecuado para un identificador de clase especificado (CLSID) recuperado de una variable de flujo.                                                 |

La interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) tiene cinco métodos, que se describen en la tabla siguiente.

| Método                                                    | Descripción                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | Inicializa una sesión de filtrado.                                                                                   |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | Coloca [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) al principio del primer fragmento o siguiente y devuelve un descriptor. |
| [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | Recupera texto del fragmento actual.                                                                             |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | Recupera los valores del fragmento actual.                                                                           |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Recupera una interfaz que representa la parte especificada del objeto. Reservado para uso futuro.                      |

### <a name="isolation-process"></a>Proceso de aislamiento

Windows Search ejecuta IFilters en el contexto de seguridad del sistema local con derechos restringidos. En este proceso de aislamiento de host de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , se quitan varios derechos:

- Código restringido
- Todos
- Local
- Interactive
- Usuarios autenticados
- Usuarios integrados
- Identificador de seguridad (SID) de los usuarios

La eliminación de estos derechos significa que la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no tiene acceso al sistema de disco o a la red, ni a ninguna función de interfaz de usuario o portapapeles. Además, el proceso de aislamiento se ejecuta bajo un objeto de trabajo que impide que se creen procesos secundarios e impone un límite de 100 MB en el espacio de trabajo. el proceso de aislamiento de host de interfaz **IFilter** aumenta la estabilidad de la plataforma de indexación, debido a la posibilidad de que los filtros de terceros se implementen incorrectamente.

> [!NOTE]  
> Los controladores de filtro se deben escribir para administrar los búferes y apilarse correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para evitar las saturaciones del búfer. Siempre debe comprobar el tamaño asignado del búfer. Siempre debe probar el tamaño de los datos con respecto al tamaño del búfer.

### <a name="ifilter-dlls"></a>Archivos dll de IFilter

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de Los archivos dll implementan la interfaz **IFilter** para permitir que un cliente Extraiga información de texto y valores de propiedad de un tipo de archivo, una clase o un tipo percibido. El proceso de filtrado de Windows Search **SearchFilterHost.exe** enlaza con el **IFilter** registrado para la clase, el tipo percibido o la extensión de nombre del elemento.

### <a name="ifilter-structure"></a>Estructura de IFilter

Cada [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es un archivo DLL que implementa un servidor de modelo de objetos componentes (com) en proceso para proporcionar las capacidades de filtrado especificadas. En la ilustración siguiente se muestra la estructura general de una DLL de **IFilter** típica. Un ejemplo más complejo podría implementar más de una clase de **IFilter** .

![diagrama de la estructura de un archivo dll de IFilter típico](images/ifilter-structure.png)

### <a name="native-code"></a>Código nativo

Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos. En Windows 7 y versiones posteriores y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente.

## <a name="finding-the-ifilter-class-identifier"></a>Buscar el identificador de clase de IFilter

La clase del archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se registra en la clave del registro PersistentHandler. En el ejemplo siguiente, para los archivos HTML, se muestra cómo buscar el archivo dll de **IFilter** para un documento HTML. Este ejemplo sigue una lógica similar a la utilizada por el sistema para buscar el **IFilter** asociado a un elemento.

1. Compruebe si la extensión para el tipo de archivos que los filtros de DLL tiene un PersistentHandler registrado en la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Permita que esta clave sea `Value1` . Si esa entrada ya existe, vaya al paso 4 de este procedimiento y úselo `Value1` en esa clave. Los valores son de tipo REG \_ SZ.

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. Como alternativa, si no hay un PersistentHandler registrado para la extensión, busque el CLSID asociado con el tipo de documento en la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Permita que esta clave sea `Value2` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. Determinar si un PersistentHandler está registrado para el CLSID. Con `Value2` el valor determinado en el paso 2, busque PersistentHandler para la \\ \_ entrada HKEY local \_ Machine \\ software \\ classes \\ CLSID \\ value2. Permita que esta clave sea `Value3` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determine el GUID del controlador persistente de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Con `Value1` y `Value3` , busque el GUID del controlador persistente de **IFilter** para el tipo de documento. El valor de la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ Value1 o 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF "/> da como resultado el GUID PersistentHandler de **IFilter** para este tipo de documento. Permita que esta clave sea `Value4` . En este ejemplo, el GUID de la interfaz de **IFilter** es 89BCB740-6119-101A-BCB7-00DD010655AF.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> En este ejemplo, el archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para documentos HTML es nlhtml.dll.

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>IFilter:: GetChunk y identificadores de código de configuración regional

El LCID del texto puede cambiar en un único archivo. Por ejemplo, el texto de un manual de instrucciones podría alternar entre inglés (en-US) y español (es), o bien el texto puede incluir una sola palabra en un idioma distinto del idioma principal. En cualquier caso, el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) debe comenzar un nuevo fragmento cada vez que cambie el LCID. Dado que el LCID se utiliza para elegir un separador de palabras adecuado, es muy importante que lo identifique correctamente. Si el **IFilter** no puede determinar la configuración regional del texto, debe devolver un LCID de cero con el fragmento. Al devolver un LCID de cero, la búsqueda de Windows usa la tecnología de detección automática de idioma (LAD) para determinar el ID. de configuración regional del fragmento. Si Windows Search no encuentra ninguna coincidencia, toma como valor predeterminado la configuración regional predeterminada del sistema (llamando a la función de [función GetSystemDefaultLocaleName](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) ). Para obtener más información, vea [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**fragmentos \_ BREAKTYPE**](/windows/win32/api/filter/ne-filter-chunk_breaktype), [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)y [**\_ fragmento STAT**](/windows/win32/api/filter/ns-filter-stat_chunk).

Si controla el formato de archivo y actualmente no contiene información de configuración regional, debe agregar una característica de usuario para habilitar la identificación de configuración regional adecuada. El uso de un separador de palabras no coincidente puede dar lugar a una mala experiencia de consulta para el usuario. Para obtener más información, vea [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).

> [!NOTE]  
> Los filtros se asocian a los tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o CLSID. Aunque un filtro puede controlar varios tipos de archivo, cada tipo funciona con un solo filtro.

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)

[Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
