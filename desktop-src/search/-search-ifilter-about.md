---
description: Los controladores de filtro, que son implementaciones de la interfaz IFilter, analizan documentos en busca de texto y propiedades.
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: Descripción de los controladores de filtros en Windows búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a331770fba1ed0103a770209348b4dc33a1bf17b7c3e7cfa7c3e9eb78f4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680920"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>Descripción de los controladores de filtros en Windows búsqueda

Los controladores de filtro, que son implementaciones de la [**interfaz IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) analizan documentos en busca de texto y propiedades. Los controladores de filtro extraen fragmentos de texto de estos elementos, filtran el formato incrustado y conservan información sobre la posición del texto. También extraen fragmentos de valores, que son propiedades del documento. **IFilter** es la base para crear aplicaciones de nivel superior, como indexadores de documentos y visores independientes de la aplicación.

Este tema se organiza de la siguiente manera:

- [Acerca de la interfaz IFilter](#about-the-ifilter-interface)
  - [Proceso de aislamiento](#isolation-process)
  - [Archivos DLL de IFilter](#ifilter-dlls)
  - [IFilter (estructura)](#ifilter-structure)
  - [Código nativo](#native-code)
- [Buscar el identificador de clase IFilter](#finding-the-ifilter-class-identifier)
  - [IFilter::GetChunk y identificadores de código de configuración regional](#ifiltergetchunk-and-locale-code-identifiers)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="about-the-ifilter-interface"></a>Acerca de la interfaz IFilter

Microsoft Windows Search usa filtros para extraer el contenido de los elementos para su inclusión en un índice de texto completo. Puede extender Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo filtros para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.

La [**interfaz IFilter**](/windows/win32/api/filter/nn-filter-ifilter) está diseñada para satisfacer las necesidades específicas de los motores de búsqueda de texto completo. Los motores de búsqueda de texto completo como Windows Search llaman a los métodos **IFilter** para extraer texto y la información de propiedades y agregarlos a un índice. Windows La búsqueda divide los resultados del método [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelto en palabras, los normaliza y los guarda en un índice. Si está disponible, el motor de búsqueda usa el identificador de código de idioma (LCID) de un fragmento de texto para realizar la separación y normalización de palabras específicas del idioma.

Windows La búsqueda usa tres funciones, descritas en la tabla siguiente, para acceder a los controladores de filtro registrados (implementaciones de la [**interfaz IFilter).**](/windows/win32/api/filter/nn-filter-ifilter) Estas funciones son especialmente útiles al cargar y enlazar al controlador de filtro de un objeto incrustado.

| Función               | Descripción                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LoadIFilter            | Obtiene un puntero al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) más adecuado para el tipo de contenido especificado.                                                                                            |
| BindIFilterFromStorage | Obtiene un puntero al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) más adecuado para el contenido contenido en un [objeto IStorage Interface.](/windows/win32/api/objidl/nn-objidl-istorage) |
| BindIFilterFromStream  | Obtiene un puntero al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) más adecuado para un identificador de clase especificado (CLSID) recuperado de una variable de secuencia.                                                 |

La [**interfaz IFilter**](/windows/win32/api/filter/nn-filter-ifilter) tiene cinco métodos, que se describen en la tabla siguiente.

| Método                                                    | Descripción                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | Inicializa una sesión de filtrado.                                                                                   |
| [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | Coloca [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) al principio del primer fragmento o el siguiente y devuelve un descriptor. |
| [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | Recupera texto del fragmento actual.                                                                             |
| [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | Recupera valores del fragmento actual.                                                                           |
| [**IFilter::BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Recupera una interfaz que representa la parte especificada del objeto . Reservado para uso futuro.                      |

### <a name="isolation-process"></a>Proceso de aislamiento

Windows La búsqueda ejecuta IFilters en el contexto de seguridad del sistema local con derechos restringidos. En este proceso de aislamiento de host de [**IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) se quitan varios derechos:

- Código restringido
- Todos.
- Local
- Interactive
- Usuarios autenticados
- Usuarios integrados
- Identificador de seguridad (SID) de los usuarios

La eliminación de estos derechos significa que la [**interfaz IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no tiene acceso al sistema de disco o a la red ni a ninguna interfaz de usuario o funciones del Portapapeles. Además, el proceso de aislamiento se ejecuta en un objeto de trabajo que impide que se cree procesos secundarios e impone un límite de 100 MB en el espacio de trabajo. El proceso de aislamiento de host de interfaz **IFilter** aumenta la estabilidad de la plataforma de indexación, debido a la posibilidad de que se implementen filtros de terceros incorrectamente.

> [!NOTE]  
> Los controladores de filtro deben escribirse para administrar búferes y apilar correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para protegerse frente a saturaciones del búfer. Siempre debe comprobar el tamaño asignado del búfer. Siempre debe probar el tamaño de los datos con respecto al tamaño del búfer.

### <a name="ifilter-dlls"></a>Archivos DLL de IFilter

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Los archivos DLL implementan la **interfaz IFilter** para permitir que un cliente extraiga información de texto y valor de propiedad de un tipo de archivo, clase o tipo percibido. El Windows de filtrado  deSearchFilterHost.exebúsqueda se enlaza al **IFilter** registrado para la clase, el tipo percibido o la extensión de nombre del elemento.

### <a name="ifilter-structure"></a>IFilter (estructura)

Cada [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es un archivo DLL que implementa un servidor del Modelo de objetos componentes (COM) en proceso para proporcionar las funcionalidades de filtrado especificadas. En la ilustración siguiente se muestra la estructura general de los archivos **DLL de IFilter** típicos. Un ejemplo más complejo podría implementar más de una **clase IFilter.**

![diagrama de la estructura de un archivo DLL típico de ifilter](images/ifilter-structure.png)

### <a name="native-code"></a>Código nativo

Los filtros deben escribirse en código nativo debido a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos. En Windows 7 y versiones posteriores y posteriores, los filtros escritos en código administrado se bloquean explícitamente.

## <a name="finding-the-ifilter-class-identifier"></a>Buscar el identificador de clase IFilter

La clase del archivo DLL [**de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se registra en la clave del Registro PersistentHandler. En el ejemplo siguiente, para los archivos HTML, se muestra cómo buscar el archivo DLL **de IFilter** para un documento HTML. Este ejemplo sigue una lógica similar a la usada por el sistema para buscar el **IFilter** asociado a un elemento.

1. Compruebe si la extensión para el tipo de archivos que filtra el archivo DLL tiene un PersistentHandler registrado en la entrada del Registro \\ HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes. Deje que esta clave sea `Value1` . Si esa entrada ya existe, vaya al paso 4 de este procedimiento y use `Value1` en esa clave. Los valores son de tipo REG \_ SZ.

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. Como alternativa, si no hay un PersistentHandler registrado para la extensión, busque el CLSID asociado al tipo de documento en la entrada del Registro \\ HKEY LOCAL MACHINE SOFTWARE Classes (Clases DE SOFTWARE de HKEY \_ LOCAL \_ \\ \\ MACHINE). Deje que esta clave sea `Value2` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. Determine si persistenthandler está registrado para el CLSID. Con determinado en el paso 2, busque PersistentHandler para la entrada `Value2` \\ \_ \_ \\ \\ \\ CLSID \\ Value2 de las clases DE SOFTWARE HKEY LOCAL MACHINE. Deje que esta clave sea `Value3` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determine el GUID del controlador persistente [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) Con `Value1` y , busque el GUID del controlador persistente `Value3` **IFilter** para el tipo de documento. El valor de la entrada del Registro \\ HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID \\ Value1 or 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF"/>  produce el GUID de IFilter PersistentHandler para este tipo de documento. Deje que esta clave sea `Value4` . En este ejemplo, el GUID de la **interfaz IFilter** es 89BCB740-6119-101A-BCB7-00DD010655AF.

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
> En este ejemplo, se muestra el archivo DLL [**de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para documentos HTML nlhtml.dll.

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>IFilter::GetChunk y identificadores de código de configuración regional

El LCID del texto puede cambiar dentro de un único archivo. Por ejemplo, el texto de un manual de instrucciones puede alternar entre inglés (en-us) y español (es) o el texto puede incluir una sola palabra en un idioma distinto del idioma principal. En cualquier caso, el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) debe comenzar un nuevo fragmento cada vez que cambia el LCID. Dado que el LCID se usa para elegir un separador de palabras adecuado, es muy importante que lo identifique correctamente. Si el **IFilter** no puede determinar la configuración regional del texto, debe devolver un LCID de cero con el fragmento. Devolver un LCID de cero hace que Windows Search use la tecnología de detección automática de idioma (LAD) para determinar el identificador de configuración regional del fragmento. Si Windows búsqueda no encuentra una coincidencia, el valor predeterminado es la configuración regional predeterminada del sistema (mediante una llamada a la función [GetSystemDefaultLocaleName Function).](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) Para obtener más información, [**vea IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**CHUNK \_ BREAKTYPE,**](/windows/win32/api/filter/ne-filter-chunk_breaktype) [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)y [**STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).

Si controla el formato de archivo y actualmente no contiene información de configuración regional, debe agregar una característica de usuario para habilitar la identificación de la configuración regional adecuada. El uso de un separador de palabras no coincidente puede dar lugar a una experiencia de consulta deficiente para el usuario. Para obtener más información, [**vea IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).

> [!NOTE]  
> Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o CLSID. Aunque un filtro puede controlar varios tipos de archivo, cada tipo funciona con un solo filtro.

## <a name="additional-resources"></a>Recursos adicionales

- El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7), muestra cómo crear una clase base IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Procedimientos recomendados para crear controladores de filtro en Windows búsqueda](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtros](-search-ifilter-property-filtering.md)

[Controladores de filtro que se envían con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en la Windows búsqueda](-search-ifilter-constructing-filters.md)

[Registro de controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
