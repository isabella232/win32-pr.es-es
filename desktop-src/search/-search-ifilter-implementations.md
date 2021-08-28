---
description: Microsoft proporciona varios filtros estándar con Windows Search. Los clientes llaman a estos controladores de filtro (que son implementaciones de la interfaz IFilter) para extraer texto y propiedades de un documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Controladores de filtro que se envían con Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a245978482e0334d91e35031aa80186fd2cb32
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624371"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Controladores de filtro que se envían con Windows

Microsoft proporciona varios filtros estándar con Windows Search. Los clientes llaman a estos controladores de filtro (que son implementaciones de la [**interfaz IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) para extraer texto y propiedades de un documento.

Este tema se organiza de la siguiente manera:

- [Windows Notas de implementación de búsqueda](#windows-search-implementation-notes)
  - [Windows implementación de 7 y 10](#windows-7-and-10-implementation)
  - [Windows Implementación de Vista](#windows-vista-implementation)
  - [Implementación heredada](#legacy-implementation)
- [Windows Filtros de búsqueda](#filter-handlers-that-ship-with-windows)
  - [Controlador de filtros MIME](#mime-filter-handler)
  - [Controlador de filtros HTML](#html-filter-handler)
  - [Controlador de filtro de documentos](#document-filter-handler)
  - [Controlador de filtro de texto sin formato](#plain-text-filter-handler)
  - [Controlador de filtro binario o nulo](#binary-or-null-filter-handler)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="windows-search-implementation-notes"></a>Windows Notas de implementación de búsqueda

En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente. Los filtros DEBEN escribirse en código nativo debido a posibles problemas de control de versiones clr con el proceso en el que se ejecutan varios complementos.

### <a name="windows-7-and-10-implementation"></a>Windows implementación de 7 y 10

En Windows 7 y versiones posteriores, hay un nuevo comportamiento que se produce al registrar un controlador de filtro, un controlador de propiedades o una nueva extensión. Cuando se instala un nuevo controlador de propiedades o un controlador de filtro, los archivos con las extensiones correspondientes se indexa automáticamente.

En Windows 7 y versiones posteriores, se recomienda instalar un controlador de filtro junto con sus controladores de propiedades correspondientes y registrar el controlador de filtro antes que el controlador de propiedades. El registro del controlador de propiedades inicia la re indexación inmediata de los archivos indexados previamente sin necesidad de reiniciar primero y aprovecha los controladores de filtro registrados previamente para la indexación de contenido.

Si solo se instala un controlador de filtros sin un controlador de propiedades correspondiente, la re indexación automática se produce después de reiniciar el servicio de indexación o de reiniciar el sistema.

Para obtener marcas de descripción de propiedades específicas de Windows 7, vea los temas de referencia siguientes: [GETPROPERTYSTOREFLAGS,](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) y [PROPDESC \_ SEARCHINFO \_ FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Windows Implementación de Vista

En Windows Vista y versiones anteriores, la instalación de un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o un controlador de propiedades no inicia una nueva indexación de los elementos existentes a menos que un proveedor de software independiente (ISV) llame explícitamente a una recompilación o nueva indexación de direcciones URL correspondientes.

Hay dos diferencias principales entre las aplicaciones heredadas, como Indexing Service, y las aplicaciones más recientes, como Windows Search, que debe tener en cuenta al implementar filtros:

- Uso de la [interfaz IPersistStream.](/windows/win32/api/objidl/nn-objidl-ipersiststream)
- Uso de controladores de propiedades.

En primer lugar, Windows Vista y Windows Search 3.0 y versiones posteriores requieren [que use IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) por los siguientes motivos:

- Para garantizar el rendimiento y la compatibilidad futura.
- Para ayudar a aumentar la seguridad. Los filtros [implementados con IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) son más seguros porque el contexto en el que se ejecuta el filtro no necesita los derechos para abrir archivos en el disco o a través de la red.

Aunque Windows Search solo usa [IPersistStream,](/windows/win32/api/objidl/nn-objidl-ipersiststream)también puede incluir implementaciones de [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) en los filtros por motivos de compatibilidad con versiones anteriores.

La segunda diferencia principal es que Windows Vista y Windows Search 3.0 y versiones posteriores tienen un nuevo sistema de propiedades que usa controladores de propiedades para enumerar las propiedades de los elementos. [](../properties/building-property-handlers.md)

Sin embargo, hay ocasiones en las que es necesario implementar un filtro que controle el contenido y las propiedades para:

- Compatibilidad con implementaciones heredadas de MSSearch.
- Recorrer vínculos.
- Conservar la información de idioma.
- Filtrar de forma recursiva los elementos incrustados.

En estas situaciones, necesita una implementación de filtro completa, incluido el método [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) para acceder a los valores de propiedad.

### <a name="legacy-implementation"></a>Implementación heredada

Como se indicó anteriormente, Windows Vista y Windows Search incluyen un nuevo sistema de propiedades que encapsula las propiedades de un elemento que es independiente del contenido de un elemento. Este sistema de propiedades no existe en versiones anteriores de Microsoft Windows Desktop Search (WDS) 2.x. Si el filtro debe admitir otras aplicaciones como se describió anteriormente, puede que tenga que controlar el contenido y las propiedades.

Para obtener más información sobre el desarrollo de un filtro compatible, vea los temas [siguientes, IFilter (para](/windows/win32/api/filter/nn-filter-ifilter)aplicaciones heredadas) y Desarrollo de complementos de filtro (para aplicaciones [heredadas).](../lwef/-search-2x-wds-ifilteraddins.md)

## <a name="windows-search-filters"></a>Windows Filtros de búsqueda

Microsoft proporciona varios filtros estándar con Windows Search. El contenido del archivo DLL de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  se resume en la tabla siguiente. Al hacer clic en el nombre de un controlador de filtro, se le lleva a la descripción de esa **implementación de IFilter.**

| Controlador de filtros                                                  | Archivos filtrados                              | IFilter DLL  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Controlador de filtros MIME](#mime-filter-handler)                     | Multipurpose Internet Mail Extension (MIME) | mimefilt.dll |
| [Controlador de filtros HTML](#html-filter-handler)                     | HTML 3.0 o versiones anteriores                         | nlhtml.dll   |
| [Controlador de filtro de documentos](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Controlador de filtro de texto sin formato](#plain-text-filter-handler)         | Archivos de texto sin formato: IFilter predeterminado          | query.dll    |
| [Controlador de filtro binario o nulo](#binary-or-null-filter-handler) | Archivos binarios: IFilter nulo                 | query.dll    |

### <a name="mime-filter-handler"></a>Controlador de filtros MIME

El controlador de filtros MIME (en mimefilt.dll) extrae texto y información de propiedades de archivos con las extensiones .eml, .mht y .mhtml.

### <a name="html-filter-handler"></a>Controlador de filtros HTML

El controlador de filtros HTML (en nlhtml.dll) extrae información de texto y propiedades de la clase "htmlfiles" para que se pueda indexar mediante Windows Search. Para obtener una descripción de la asociación entre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y el tipo de archivo, vea "Finding the IFilter DLL for a File" (Buscar el archivo DLL de IFilter para un archivo) en [Registering Filter Handlers](-search-ifilter-registering-filters.md).

Puede usar la característica de etiqueta de documentos HTML para transmitir solicitudes de `META` control especiales al [**IFilter HTML.**](/windows/win32/api/filter/nn-filter-ifilter) `META` Las etiquetas se producen cerca del principio de un archivo HTML dentro de las etiquetas, como `HEAD ... /HEAD` se muestra en el ejemplo siguiente.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Algunas etiquetas HTML se asignan automáticamente a valores conocidos de conjunto de propiedades e identificador de propiedad (identificador de propiedad (PID)) para que las consultas en estas propiedades busquen el `META` contenido asignado. En la tabla siguiente se enumeran algunos ejemplos. Para obtener una lista de las propiedades del sistema que puede usar para los formatos de archivo, vea Propiedades definidas por el sistema [para formatos de archivo personalizados.](-shell-systemdefinedpropertiesforfileformats.md)

| Ejemplo de propiedad                              | Asignada a                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name="author" content="rut"             | Propiedad author del conjunto de propiedades Información de resumen.            |
| meta name="subject" content="word processing" | Propiedad subject del conjunto de propiedades Información de resumen.           |
| meta name="keywords" content="fonts, serif"   | Propiedad de palabra clave del conjunto de propiedades Información de resumen.           |
| meta name="ms.category" content="lanálisis"     | Propiedad de categoría del conjunto de propiedades Información de resumen del documento. |

Algunas características de HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se enumeran en la tabla siguiente.

[comment]: # (Esta tabla debe ser HTML para que los ejemplos tengan el formato correcto.)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Creación de resúmenes especiales a partir de archivos</td>
<td>Use la etiqueta para indicar al IFilter que use la cadena que sigue a <code>META NAME=&quot;DESCRIPTION&quot;...</code> la palabra clave como el documento <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong></strong></a> <code>CONTENT</code> abstracto.
<blockquote>
[!Note]<br />
El proceso de filtrado puede generar resúmenes para cada archivo filtrado, que de forma predeterminada es un conjunto de caracteres al principio del archivo.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<col  />
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
<td>Establecer el código de idioma de un archivo (para asegurarse de que el sistema elige los separadores de palabras de idioma y los archivos de palabras ruido correctos)</td>
<td>Agregue la etiqueta siguiente al archivo , donde el campo de contenido especifica el código de idioma adecuado (ya sea en caracteres o <code>meta name</code> mediante el valor de configuración regional).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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

### <a name="document-filter-handler"></a>Controlador de filtro de documentos

El controlador de filtros de documentos (en offilt.dll) filtra los archivos para algunas extensiones de documentos en Microsoft Office. Estos incluyen archivos con las extensiones .doc, .mdb, .ppt y .xlt, por ejemplo.

### <a name="plain-text-filter-handler"></a>Controlador de filtro de texto sin formato

En el caso de los archivos de texto sin formato, Windows Search usa el controlador de filtro de texto, que filtra las propiedades del sistema (como los nombres de archivo) y el contenido de un archivo. Cuando un tipo de archivo no tiene una asociación [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en el Registro, Windows buscar solo indexa las propiedades de Shell para el archivo. Sin embargo, el usuario puede usar opciones avanzadas  **en** el panel de **control** Opciones de indexación para Propiedades de índice o Propiedades de índice y Contenido **del archivo**.

![captura de pantalla que muestra el cuadro de diálogo opciones avanzadas](images/ifilteradvancedoptions.png)

Si el usuario elige esta opción para un tipo de archivo sin un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)asociado, se usa el controlador de filtro de texto para extraer el contenido del archivo. El controlador de filtro de texto no "entiende" ningún formato de documento; al filtrar el contenido de un archivo, trata el archivo como una secuencia de caracteres. Comprueba la marca de orden de bytes Unicode al principio del archivo.

### <a name="binary-or-null-filter-handler"></a>Controlador de filtro binario o nulo

Cuando se encuentra un archivo binario registrado, se usa el controlador de filtro NULL. El controlador de filtro NULL recupera solo las propiedades del sistema. El contenido de un archivo binario no se filtra. Algunos ejemplos de propiedades del sistema **son FileName**, **LastWriteTime,** **FileSize** y **Attributes**.

## <a name="additional-resources"></a>Recursos adicionales

- El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), muestra cómo crear una clase base de IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Procedimientos recomendados para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtros](-search-ifilter-property-filtering.md)

[Implementación de controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Registro de controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
