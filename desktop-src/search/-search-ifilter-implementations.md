---
description: Microsoft proporciona varios filtros estándar con Windows Search. Los clientes llaman a estos controladores de filtro (que son implementaciones de la interfaz de IFilter) para extraer texto y propiedades de un documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Controladores de filtro que se distribuyen con Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153971"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Controladores de filtro que se distribuyen con Windows

Microsoft proporciona varios filtros estándar con Windows Search. Los clientes llaman a estos controladores de filtro (que son implementaciones de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para extraer texto y propiedades de un documento.

Este tema se organiza de la siguiente manera:

- [Notas de implementación de Windows Search](#windows-search-implementation-notes)
  - [Implementación de Windows 7 y 10](#windows-7-and-10-implementation)
  - [Implementación de Windows Vista](#windows-vista-implementation)
  - [Implementación heredada](#legacy-implementation)
- [Filtros de Windows Search](#filter-handlers-that-ship-with-windows)
  - [Controlador de filtro MIME](#mime-filter-handler)
  - [Controlador de filtro HTML](#html-filter-handler)
  - [Controlador de filtro de documento](#document-filter-handler)
  - [Controlador de filtro de texto sin formato](#plain-text-filter-handler)
  - [Controlador de filtro binario o null](#binary-or-null-filter-handler)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="windows-search-implementation-notes"></a>Notas de implementación de Windows Search

En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente. Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan varios complementos.

### <a name="windows-7-and-10-implementation"></a>Implementación de Windows 7 y 10

En Windows 7 y versiones posteriores, hay un nuevo comportamiento que se produce al registrar un controlador de filtro, un controlador de propiedades o una nueva extensión. Cuando se instala un nuevo controlador de propiedades o un controlador de filtro, los archivos con las extensiones correspondientes se vuelven a indizar automáticamente.

En Windows 7 y versiones posteriores, se recomienda instalar un controlador de filtro junto con sus controladores de propiedades correspondientes y registrar el controlador de filtro antes del controlador de propiedad. El registro del controlador de propiedades inicia una reindización inmediata de archivos indizados previamente sin requerir primero un reinicio, y aprovecha los controladores de filtro registrados previamente con el fin de indizar contenido.

Si solo se instala un controlador de filtro sin un controlador de propiedades correspondiente, la reindexación automática se produce después de un reinicio del servicio de indización o de un reinicio del sistema.

En el caso de las marcas de descripción de propiedades específicas de Windows 7, vea los temas de referencia siguientes: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) y [PROPDESC \_ SEARCHINFO \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Implementación de Windows Vista

En Windows Vista y versiones anteriores, si se instala un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o un controlador de propiedades, no se inicia una nueva indexación de los elementos existentes a menos que un fabricante de software independiente (ISV) llame explícitamente a una recompilación o reindexación de las direcciones URL coincidentes.

Hay dos diferencias principales entre las aplicaciones heredadas, como el servicio de Index Server y las aplicaciones más recientes como Windows Search que debe tener en cuenta al implementar filtros:

- Uso de la interfaz [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .
- Uso de controladores de propiedades.

En primer lugar, Windows Vista y Windows Search 3,0 y versiones posteriores requieren [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) por los siguientes motivos:

- Para garantizar el rendimiento y la compatibilidad futura.
- Para ayudar a aumentar la seguridad. Los filtros implementados con [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) son más seguros porque el contexto en el que se ejecuta el filtro no necesita los derechos para abrir archivos en el disco o a través de la red.

Aunque Windows Search solo usa [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), también puede incluir las implementaciones de interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) y/o [IPersistStorage interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) en los filtros para mantener la compatibilidad con versiones anteriores.

La segunda diferencia principal es que Windows Vista y Windows Search 3,0 y versiones posteriores tienen un nuevo [sistema de propiedades](../properties/building-property-handlers.md) que usa controladores de propiedades para enumerar las propiedades de los elementos.

Sin embargo, hay ocasiones en las que es necesario implementar un filtro que controla el contenido y las propiedades para:

- Admitir implementaciones de MSSearch heredadas.
- Atravesar vínculos.
- Conservar la información de idioma.
- Filtrar elementos incrustados de forma recursiva.

En estas situaciones, se necesita una implementación de filtro completa, incluido el método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) para tener acceso a los valores de propiedad.

### <a name="legacy-implementation"></a>Implementación heredada

Como se indicó anteriormente, Windows Vista y Windows Search incluyen un nuevo sistema de propiedades que encapsula las propiedades de un elemento que es independiente del contenido de un elemento. Este sistema de propiedades no existe en versiones anteriores de Microsoft Windows Desktop Search (WDS) 2. x. Si el filtro debe admitir otras aplicaciones como se describió anteriormente, puede que tenga que administrar tanto el contenido como las propiedades.

Para obtener más información sobre el desarrollo de un filtro compatible, vea los siguientes temas, [IFilter (para aplicaciones heredadas)](/windows/win32/api/filter/nn-filter-ifilter)y [desarrollo de complementos de filtro (para aplicaciones heredadas)](../lwef/-search-2x-wds-ifilteraddins.md).

## <a name="windows-search-filters"></a>Filtros de Windows Search

Microsoft proporciona varios filtros estándar con Windows Search. El contenido del archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  se resume en la tabla siguiente. Al hacer clic en el nombre de un controlador de filtro, se le remite a la descripción de esa implementación de **IFilter** .

| Controlador de filtro                                                  | Archivos filtrados                              | DLL de IFilter  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Controlador de filtro MIME](#mime-filter-handler)                     | Extensión multipropósito de correo Internet (MIME) | mimefilt.dll |
| [Controlador de filtro HTML](#html-filter-handler)                     | HTML 3,0 o anterior                         | nlhtml.dll   |
| [Controlador de filtro de documento](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Controlador de filtro de texto sin formato](#plain-text-filter-handler)         | Archivos de texto sin formato: IFilter predeterminado          | query.dll    |
| [Controlador de filtro binario o null](#binary-or-null-filter-handler) | Archivos binarios: IFilter nulo                 | query.dll    |

### <a name="mime-filter-handler"></a>Controlador de filtro MIME

El controlador de filtro MIME (en mimefilt.dll) extrae información de texto y propiedades de los archivos con las extensiones. eml,. mht y. MHTML.

### <a name="html-filter-handler"></a>Controlador de filtro HTML

El controlador de filtro HTML (en nlhtml.dll) extrae información de texto y propiedades de la clase "htmlfiles" para que Windows Search pueda indizarla. Para obtener una descripción de la asociación entre el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y el tipo de archivo, vea "buscar el archivo dll de IFilter para un archivo" en [registrar controladores de filtro](-search-ifilter-registering-filters.md).

Puede usar la `META` característica de etiqueta de los documentos HTML para transmitir solicitudes de control especiales al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML. `META` las etiquetas se producen cerca del principio de un archivo HTML dentro de las `HEAD ... /HEAD` etiquetas, tal como se muestra en el ejemplo siguiente.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Algunas `META` etiquetas HTML se asignan automáticamente a los valores del conjunto de propiedades y del identificador de propiedad (identificador de propiedad (PID)) de forma que las consultas en estas propiedades buscarán en el contenido asignado. En la tabla siguiente se muestran algunos ejemplos. Para obtener una lista de las propiedades del sistema que puede usar para los formatos de archivo, consulte [propiedades definidas por el sistema para formatos de archivo personalizados](-shell-systemdefinedpropertiesforfileformats.md).

| Ejemplo de propiedad                              | Asignada a                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name = "author" Content = "Ruth"             | Propiedad de autor del conjunto de propiedades de información de resumen.            |
| meta name = "Subject" Content = "procesamiento de texto" | Propiedad de asunto del conjunto de propiedades de información de resumen.           |
| meta name = "keywords" Content = "fuentes, Serif"   | Propiedad de palabra clave en el conjunto de propiedades de información de resumen.           |
| meta name = "MS. Category" Content = "ficción"     | Propiedad de categoría del conjunto de propiedades información de resumen del documento. |

En la tabla siguiente se enumeran algunas características de HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

[comment]: # (Esta tabla debe ser HTML para que las muestras estén formateadas correctamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarea</th>
<th>Acción</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crear resúmenes especiales de archivos</td>
<td>Use la <code>META NAME=&quot;DESCRIPTION&quot;...</code> etiqueta para indicar al <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> que use la cadena que sigue a la <code>CONTENT</code> palabra clave como resumen del documento.
<blockquote>
[!Note]<br />
El proceso de filtrado puede generar resúmenes para cada archivo filtrado, que de forma predeterminada es un juego de caracteres al principio del archivo.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Impedir que se filtren archivos individuales</td>
<td>Agregue una <code>meta name</code> etiqueta al archivo.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Establecer el código de idioma de un archivo (para asegurarse de que el sistema elige los separadores de palabras de idioma correctos y los archivos de palabras irrelevantes)</td>
<td>Agregue la siguiente <code>meta name</code> etiqueta al archivo, donde el campo de contenido especifica el código de idioma adecuado (en caracteres o mediante el valor de configuración regional).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>Controlador de filtro de documento

El controlador de filtro de documento (en offilt.dll) filtra los archivos de algunas extensiones de documentos en Microsoft Office. Estos archivos de inclusión con las extensiones. doc,. mdb,. ppt y. xlt, por ejemplo.

### <a name="plain-text-filter-handler"></a>Controlador de filtro de texto sin formato

En el caso de los archivos de texto sin formato, Windows Search utiliza el controlador de filtro de texto, que filtra las propiedades del sistema (por ejemplo, los nombres de archivo) y el contenido de un archivo. Cuando un tipo de archivo no tiene una asociación [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en el registro, Windows Search solo indiza las propiedades del shell para el archivo. Sin embargo, el usuario puede usar las **Opciones avanzadas** del panel de control **Opciones de indización** para **indizar propiedades** o **índices, así** como el contenido del archivo.

![captura de pantalla que muestra el cuadro de diálogo Opciones avanzadas](images/ifilteradvancedoptions.png)

Si el usuario elige esta opción para un tipo de archivo sin un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)asociado, el controlador de filtro de texto se utiliza para extraer el contenido del archivo. El controlador de filtro de texto no entiende ningún formato de documento; al filtrar el contenido de un archivo, trata el archivo como una secuencia de caracteres. Comprueba la marca de orden de bytes Unicode al principio del archivo.

### <a name="binary-or-null-filter-handler"></a>Controlador de filtro binario o null

Cuando se encuentra un archivo binario registrado, se utiliza el controlador de filtro null. El controlador de filtro null solo recupera las propiedades del sistema. El contenido de un archivo binario no se filtra. Ejemplos de propiedades del sistema son **filename**, **LastWriteTime**, **archivo** y **atributos**.

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
