---
description: Microsoft Windows Search usa controladores de propiedades para extraer los valores de las propiedades de los elementos y utiliza el esquema del sistema de propiedades para determinar cómo se debe indizar una propiedad concreta.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Desarrollar controladores de propiedades para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275271"
---
# <a name="developing-property-handlers-for-windows-search"></a>Desarrollar controladores de propiedades para Windows Search

Microsoft Windows Search usa controladores de propiedades para extraer los valores de las propiedades de los elementos y utiliza el esquema del sistema de propiedades para determinar cómo se debe indizar una propiedad concreta. Para leer e indexar los valores de propiedad, la búsqueda de Windows invoca los controladores de propiedades para mejorar la seguridad y la solidez. En cambio, el explorador de Windows invoca los controladores de propiedades en proceso para leer y escribir valores de propiedad.

En este tema se complementa el tema [del sistema de propiedades](../properties/building-property-handlers.md) con información específica de Windows Search y contiene las siguientes secciones:

-   [Decisiones de diseño para los controladores de propiedades](#design-decisions-for-property-handlers)
    -   [Decisiones de propiedades](#property-decisions)
    -   [Compatibilidad con texto completo](#full-text-support)
    -   [Consideraciones de Implementatation del sistema operativo](#operating-system-implementatation-considerations)
-   [Escribir archivos de descripción de propiedades](#writing-property-description-files)
-   [Implementar controladores de propiedades](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Asegurarse de que los elementos se indexan](#ensuring-your-items-get-indexed)
-   [Instalar y registrar controladores de propiedades](#installing-and-registering-property-handlers)
-   [Probar y solucionar problemas de controladores de propiedades](#testing-and-troubleshooting-property-handlers)
    -   [Pruebas de instalación y configuración](#installation-and-setup-tests)
    -   [Solucionar problemas de controladores de propiedades](#troubleshooting-property-handlers)
-   [Usar controladores de propiedades de System-Supplied](#using-system-supplied-property-handlers)
-   [Temas relacionados](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Decisiones de diseño para los controladores de propiedades

La implementación de controladores de propiedades implica los siguientes pasos:

1.  Tomar decisiones de diseño con respecto a las propiedades que desea admitir.
2.  Crear un archivo de descripción de propiedad (. propDesc) para las propiedades que ya no están en el sistema de propiedades.
3.  Implementar y probar el controlador de propiedad.
4.  Instalación y registro de los archivos de descripción de propiedades y controladores de propiedades.
5.  Prueba de la instalación y el registro del controlador de propiedades.

Antes de comenzar, debe tener en cuenta las siguientes preguntas de diseño:

-   ¿Qué propiedades tiene o debe admitir el formato de archivo?
-   ¿Estas propiedades ya están en el esquema del sistema?
-   ¿Puedo usar un controlador de propiedades proporcionado por el sistema existente?
-   ¿Qué propiedades se pueden mostrar a los usuarios finales?
-   ¿Qué propiedades pueden editar los usuarios?
-   ¿La compatibilidad con la búsqueda de texto completo procede de un controlador de propiedades o un filtro?
-   ¿Necesito compatibilidad con aplicaciones heredadas? Si es así, ¿qué puedo implementar?

> [!Note]  
> Antes de continuar, vea [usar System-Supplied controladores de propiedades](#using-system-supplied-property-handlers) para ver si puede usar un controlador de propiedades proporcionado por el sistema, lo que le ahorra tiempo y recursos de desarrollo.

 

Después de tomar estas decisiones, puede escribir descripciones formales de las propiedades personalizadas para que el motor de búsqueda de Windows pueda empezar a indizar los archivos y las propiedades. Estas descripciones formales son archivos XML, que se describen en el [esquema de descripción de propiedad](/previous-versions//cc144127(v=vs.85)).

### <a name="property-decisions"></a>Decisiones de propiedades

Al considerar las propiedades que se deben admitir, debe identificar las necesidades de indexación y búsqueda de los usuarios. Por ejemplo, puede identificar 100 propiedades potencialmente útiles para el tipo de archivo, pero es posible que los usuarios estén interesados en buscar solo en un puñado. Además, puede que desee mostrar un grupo diferente, mayor o menor, de esas propiedades a los usuarios en el explorador de Windows y permitir que los usuarios modifiquen solo un subconjunto de las propiedades mostradas.

El tipo de archivo puede admitir cualquier propiedad personalizada que defina, así como un conjunto de propiedades definidas por el sistema. Antes de crear una propiedad personalizada, revise [las propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) para ver si la propiedad que desea admitir ya está definida por una propiedad del sistema. Asegúrese siempre de que admite las propiedades más importantes definidas por el sistema.

Se recomienda usar una matriz para ayudarle a diseñar sus propiedades:



| Nombre de propiedad | ¿Es indexable? | ¿Es visible? | ¿Es editable? |
|---------------|---------------|-----------------|--------------|
| property1     | Y             | Y               | N            |
| propiedad...   | Y             | Y               | N            |
| propiedad     | N             | N               | N            |



 

Para cada una de estas propiedades, debe determinar qué atributos debe tener y, a continuación, describirlos formalmente en archivos XML de descripción de propiedad (. propDesc). Los atributos incluyen el tipo de datos de la propiedad, la etiqueta, la cadena de ayuda y mucho más. En el caso de las propiedades indexables, debe prestar especial atención a los siguientes atributos de propiedad que se encuentran en el elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   del archivo de descripción de la propiedad.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Opcional. Indica si un valor de propiedad de cadena debe dividirse en palabras y en cada palabra almacenada en el índice invertido. El índice invertido permite una búsqueda eficaz de palabras y frases sobre el valor de propiedad mediante Contains o FREETEXT (por ejemplo, SELECT... DONDE contiene &quot; sometext &quot; ). Si se establece en <strong>false</strong>, las búsquedas se realizan en toda la cadena. La mayoría de las propiedades de cadena deben tener esta propiedad establecida en <strong>true</strong>; las propiedades que no son de cadena deben tener esta propiedad establecida en <strong>false</strong>. El valor predeterminado es <strong>false</strong>.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Opcional. Indica si la propiedad debe almacenarse en la base de datos de Windows Search como una columna. Almacenar la propiedad como una columna permite recuperar, ordenar, agrupar y filtrar (es decir, usar cualquier predicado excepto Contains o FREETEXT) en el valor de la columna completa. Las propiedades que se muestran al usuario deben tener este valor establecido en <strong>true</strong> a menos que sea una propiedad de texto muy grande (como el cuerpo de un documento) que se buscaría en el índice invertido. El valor predeterminado es <strong>false</strong>.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Opcional. Indica si una propiedad no necesita espacio si el valor es <strong>null</strong>. Una propiedad no dispersa tiene espacio para cada elemento, incluso si el valor es <strong>null</strong>. Si la propiedad tiene varios valores, este atributo siempre es <strong>true</strong>. Este atributo solo debe ser <strong>false</strong> si hay un valor para cada elemento. El valor predeterminado es <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Opcional. Para optimizar las consultas, el motor de búsqueda de Windows puede crear índices secundarios para propiedades que tienen isColumn =<strong>true</strong>. Esto requiere más procesamiento y espacio en disco durante la indexación, pero mejora el rendimiento durante la consulta. Si la propiedad tiende a ordenarse, agruparse o filtrarse (es decir, usando =,! =, <, >, LIKE, coincide) con frecuencia por usuarios, este atributo debe establecerse en &quot; disco &quot; . El valor predeterminado es &quot; NotIndexed &quot; . Valores válidos son:
<ul>
<li>NotIndexed: no se crea ningún índice secundario.</li>
<li>Disco: cree y almacene un índice secundario en el disco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tamañomáximo</td>
<td>Opcional. Indica el tamaño máximo permitido para el valor de propiedad almacenado en la base de datos de Windows Search. Este límite se aplica a los elementos indvidual de un vector, no al vector en su totalidad. Se truncan los valores que superen este tamaño. El valor predeterminado es &quot; 128 &quot; (bytes).<br/> Actualmente, Windows Search no usa maxSize al calcular la cantidad de datos que acepta de un archivo. En su lugar, el límite que usa Windows Search es el producto del tamaño del archivo y el MaxGrowFactor (tamaño de archivo N * MaxGrowFactor) leído del registro en HKEY_LOCAL_MACHINE->software->Microsoft->Windows Search->Gather Manager->MaxGrowFactor. El valor predeterminado de MaxGrowFactor es cuatro (4). Por lo tanto, si el tipo de archivo tiende a ser pequeño en tamaño total pero tiene propiedades más grandes, es posible que Windows Search no acepte todos los datos de propiedad que desea emitir. Sin embargo, puede aumentar el MaxGrowFactor para que se adapte a sus necesidades. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> En el caso del atributo columnIndexType, la ventaja de las consultas más rápidas debe sopesarse con el mayor tiempo de indización y los costos de espacio que pueden tener los índices secundarios. Sin embargo, este costo solo se paga por los elementos que tienen un valor distinto de **null** , por lo que la mayoría de las propiedades pueden tener este atributo establecido en "disco".

 

### <a name="full-text-support"></a>Compatibilidad con texto completo

En términos generales, la búsqueda de texto completo es compatible con los componentes denominados [filtros](-search-3x-wds-extidx-filters.md); sin embargo, para los tipos de archivos basados en texto con formatos de archivo poco complicados, los controladores de propiedades pueden proporcionar esta funcionalidad con menos esfuerzo de desarrollo. Debe revisar la sección [contenido de texto completo](../properties/building-property-handlers-property-handlers.md) para obtener una comparación de la funcionalidad del filtro y del controlador de propiedades para ayudarle a decidir cuál es el mejor para su tipo de archivo. Una importancia concreta es el hecho de que los filtros pueden controlar varios identificadores de código de idioma (LCID) por archivo, mientras que los controladores de propiedades no pueden.

> [!Note]  
> Dado que los controladores de propiedades no pueden fragmentar el contenido de la manera en que se filtran los filtros, los archivos grandes (incluso si son formatos de archivo no complicados) se deben cargar completamente en la memoria.

 

### <a name="operating-system-implementatation-considerations"></a>Consideraciones de Implementatation del sistema operativo

### <a name="implementation-information-for-windows-7"></a>Información de implementación de Windows 7

En Windows 7 y versiones posteriores, hay un nuevo comportamiento al registrar un controlador de propiedades, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)o una nueva extensión. Cuando se instala un nuevo controlador de propiedades o **IFilter** , los archivos con las extensiones correspondientes se reindexan automáticamente.

En Windows 7 se recomienda instalar un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) junto con sus controladores de propiedades correspondientes y que el **IFilter** se registre antes que el controlador de propiedad. El registro del controlador de propiedades inicia una reindización inmediata de archivos indizados previamente sin requerir primero un reinicio, y aprovecha los IFilter registrados previamente para el propósito de la indización de contenido.

Si solo hay un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) instalado, sin un controlador de propiedades correspondiente, la reindexación automática se produce después de un reinicio del servicio de indización o de un reinicio del sistema.

En el caso de las marcas de descripción de propiedades específicas de Windows 7, vea los temas de referencia siguientes:

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [PROPDESC \_ COLUMNINDEX ( \_ tipo)](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [PROPDESC \_ \_ marcas SEARCHINFO](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Información de implementación de Windows Vista y versiones anteriores

Antes de Windows Vista, los filtros proporcionaban compatibilidad para analizar y enumerar el contenido y las propiedades de los archivos. Con la introducción del sistema de propiedades, los controladores de propiedades controlan las propiedades de archivo mientras que los filtros controlan el contenido del archivo. En Windows Vista, solo necesita desarrollar una implementación parcial de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)en coordinación con un controlador de propiedades, como se describe en [procedimientos recomendados para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md).

Aunque el sistema de propiedades también se incluye con la instalación de Windows Search para Windows XP, las aplicaciones heredadas y de terceros pueden requerir que los filtros controlen tanto el contenido como las propiedades. Por lo tanto, si está desarrollando en la plataforma Windows XP, debe proporcionar una implementación de filtro completa, así como un controlador de propiedades para el tipo de archivo o la propiedad personalizada.

 

## <a name="writing-property-description-files"></a>Escribir archivos de descripción de propiedades

La estructura de los archivos XML de descripción de propiedad (. propDesc) se describe en el tema [propertyDescription](../properties/propdesc-schema-propertydescription.md) . Un interés particular para la búsqueda son los atributos del elemento [searchInfo](../properties/propdesc-schema-searchinfo.md) . Una vez que haya decidido qué propiedades se deben admitir, debe crear y registrar los archivos de descripción de propiedades para cada una de las propiedades. Al registrar los archivos. propDesc, se incluyen en la lista de descripción de la propiedad del esquema y se convierten en nombres de columna en el almacén de propiedades del motor de búsqueda.

Puede registrar las descripciones de propiedades personalizadas mediante la función [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , una API de contenedor que llama a IPropertySystem:: RegisterPropertySchema del subsistema de esquema. Esta función informa al subsistema de esquema de la adición de archivos de esquema de descripción de propiedad (. propDesc), mediante rutas de acceso de archivo a los archivos. propDesc en el equipo local, normalmente el directorio de instalación de la aplicación en "archivos de programa". Normalmente, una instalación o una aplicación (por ejemplo, el instalador del controlador de propiedad) llamará a este método después de instalar los archivos. propDesc.

 

## <a name="implementing-property-handlers"></a>Implementar controladores de propiedades

El desarrollo de un controlador de propiedades implica la implementación de las interfaces siguientes:

-   IInitialzeWithStream: proporciona la inicialización basada en secuencias del controlador de propiedad.
-   IPropertyStore: enumera, obtiene y establece los valores de propiedad.
-   IPropertyStoreCapabilities: opcional. Identifica si los usuarios pueden editar una propiedad desde una interfaz de usuario.

### <a name="iinitializewithstream"></a>IInitializeWithStream

Tal y como se describe en el tema [sistema de propiedades](../properties/building-property-handlers.md) , se recomienda encarecidamente implementar controladores de propiedades con **IInitializeWithStream** para realizar la inicialización basada en secuencias. Si decide no implementar IInitializeWithStream, el controlador de propiedad debe dejar de ejecutarse en el proceso de aislamiento estableciendo la marca DisableProcessIsolation en la clave del registro del controlador de propiedad. Generalmente, la deshabilitación del aislamiento de procesos está destinada únicamente a los controladores de propiedades heredadas y se debe evitar por cualquier nuevo código.

### <a name="ipropertystore"></a>IPropertyStore

Para crear un controlador de propiedades, debe implementar la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con los métodos siguientes.



| Método   | Descripción                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Guarda un cambio de propiedad en el archivo.                                |
| GetAt    | Recupera una clave de propiedad de la matriz de propiedades de un elemento.        |
| GetCount | Obtiene el número de propiedades adjuntas al archivo.                 |
| GetValue | Recupera los datos de una propiedad concreta.                             |
| SetValue | Establece un nuevo valor de propiedad o reemplaza o quita un valor existente. |



 

 

 

En la documentación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) se incluyen consideraciones importantes para implementar esta interfaz.

> [!Note]  
> Si el controlador de propiedad emite varios valores para la misma propiedad para un elemento determinado, solo el último valor emitido se almacena en el catálogo.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

Opcionalmente, los controladores de propiedades pueden implementar esta interfaz para deshabilitar la capacidad de un usuario para editar propiedades específicas. Normalmente, estas propiedades se pueden editar en la página de detalles y el panel, pero no se pueden editar en el controlador de propiedades de implementación. La implementación correcta de esta interfaz proporciona una mejor experiencia de usuario que la alternativa, un error de tiempo de ejecución simple del shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Asegurarse de que los elementos se indexan

Ahora que ha implementado el controlador de propiedad, desea asegurarse de que los elementos que el controlador está registrado para la indexación se han indizado. Puede usar el [Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) para iniciar la reindización y también puede usar el [Administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md) para configurar las reglas predeterminadas que indican las direcciones URL que desea que rastree el indexador. Otra opción es seguir el ejemplo de código REINDEX en los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Para obtener más información, consulte [uso del administrador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) y [uso del administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Instalar y registrar controladores de propiedades

Con el controlador de propiedades implementado, debe estar registrado y su extensión de nombre de archivo asociada al controlador. En el ejemplo siguiente se muestran las claves y los valores del registro necesarios para hacerlo.

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Probar y solucionar problemas de controladores de propiedades

En la lista siguiente se proporcionan consejos sobre los tipos de pruebas que se deben realizar:

-   Pruebe la obtención de resultados de cada propiedad única admitida por el tipo de archivo.
-   Use valores de propiedad grande, por ejemplo, para usar una metaetiqueta grande en documentos HTML.
-   Compruebe que el controlador de propiedad no pierde los identificadores de archivo editándolo después de obtener la salida del controlador de propiedad o mediante una herramienta como oh.exe antes y después de enumerar las propiedades del archivo.
-   Probar todos los tipos de archivo asociados al controlador de propiedades. Por ejemplo, compruebe que el filtro HTML funciona con tipos de archivo. htm y. html.
-   Pruebe con archivos dañados. El controlador de propiedad debe producir un error.
-   Si una aplicación admite el cifrado, compruebe que el controlador de propiedad no genera texto cifrado.
-   Si el controlador de propiedad admite la búsqueda de texto completo:
    -   Use varios caracteres Unicode especiales en el contenido del archivo y pruebe su salida.
    -   Pruebe el control de documentos muy grandes para asegurarse de que el controlador de propiedades funciona según lo previsto.

### <a name="installation-and-setup-tests"></a>Pruebas de instalación y configuración

Por último, debe probar las rutinas de instalación y desinstalación.

-   La instalación se debe recuperar de las instalaciones con error (por ejemplo, cancelar y reiniciar el programa de instalación).
-   La desinstalación debe eliminar todos los archivos asociados con el controlador de propiedades.
-   La desinstalación no debe eliminar archivos que no sean los asociados a la instalación del controlador de propiedades.
-   Se deben quitar las claves del registro asociadas al controlador de propiedades cuando se desinstale.
-   La desinstalación debe funcionar incluso si se eliminan archivos del directorio de instalación.

### <a name="troubleshooting-property-handlers"></a>Solucionar problemas de controladores de propiedades

A continuación se muestran algunos errores comunes que se realizan al desarrollar controladores de propiedades:

-   Instalación de archivos. propDesc o dll en un directorio de usuario.
-   Registrar componentes mediante rutas de acceso relativas.
-   Registrando componentes en HKEY \_ Current \_ User en lugar de HKEY \_ local \_ Machine.
-   Olvidar establecer DisableProcessIsolation para los controladores que no son de secuencia.
-   Colocar el archivo de prueba en una ubicación no indizada.

Si tiene problemas para que el controlador de propiedades funcione con el indexador, aquí tiene algunas sugerencias que le ayudarán a solucionar el problema:

-   Compruebe que las descripciones de propiedad (archivos. propDesc) están marcadas como isColumn = "**true**", isViewable = "**true**" y isQueryable = "**true**", según corresponda.
-   Compruebe que los archivos. propDesc se encuentran en una ubicación global.
-   Compruebe que ha registrado los archivos. propDesc mediante rutas de acceso absolutas.
-   Compruebe que el registro de eventos no registró ningún error al registrar el archivo. propDesc.
-   Compruebe que los archivos dll están en una ubicación global (y no en el perfil de usuario).
-   Compruebe que los archivos dll estén registrados en HKEY \_ local \_ Machine \\ software \\ classes.
-   Compruebe que los archivos DLL se registran mediante rutas de acceso completas (o \_ cadenas de expansión \_ SZ que se expanden a rutas de acceso absolutas mediante variables de entorno conocidas por la cuenta del sistema).
-   Compruebe que el controlador de propiedades funciona en el explorador de Windows.
-   Aunque se recomienda usar IInitializeWithStream, si debe usar IInitializeWithFile o IInitializeWithItem, compruebe que especifica DisableProcessIsolation.
-   Compruebe que el panel de control opciones de indización muestra el tipo de archivo como un tipo de archivo indexado.
-   Compruebe que el archivo de prueba se encuentra en una ubicación indizada.
-   Compruebe que el archivo de prueba se ha modificado desde que instaló el controlador de propiedad.

Si el archivo de prueba está en una ubicación indizada y el indexador ya ha rastreado esa ubicación, debe modificar el archivo de alguna manera para desencadenar una reindexación del archivo.

 

## <a name="using-system-supplied-property-handlers"></a>Usar controladores de propiedades de System-Supplied

Windows incluye varios controladores de propiedades proporcionados por el sistema que puede usar si el formato del tipo de archivo es compatible. Si define una nueva extensión de archivo que usa uno de estos formatos, puede usar los controladores proporcionados por el sistema registrando el identificador de clase del controlador (CLSID) para la extensión de archivo.

Puede usar el CLSID que se muestra en la tabla siguiente para registrar los controladores de propiedades proporcionados por el sistema para el tipo de formato de archivo.



| Formato          | CLSID                                  |
|-----------------|----------------------------------------|
| OLE     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Guardar el XML del juego   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| Controlador de XPS/OPC | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Antes de crear una propiedad personalizada, debe asegurarse de que no haya una propiedad definida por el sistema que pueda usar en su lugar. Puede enumerar las propiedades definidas por el sistema llamando a [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) o mediante la herramienta de línea de comandos prop.exe.

El esquema del sistema define cómo interactúan estas propiedades con el indizador y no se puede cambiar. Además, la aplicación que se usa para crear, editar y guardar el tipo de archivo también debe ajustarse a cierto comportamiento. Por ejemplo, si la aplicación implementa el guardado seguro (en el que se crea un archivo temporal durante la edición y, a continuación, se usa ReplaceFile () para intercambiar la nueva versión del antiguo), debe transferir todas las propiedades del archivo original al nuevo archivo. Si no lo hace, el archivo pierde las propiedades agregadas por los usuarios u otras aplicaciones.

 

**Ejemplo**

A continuación se muestra el registro del controlador de archivos OLE de archivo proporcionado por el sistema para un tipo de archivo con un. Extensión OLEDocFile.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

A continuación se muestra el registro de la información de la lista de propiedades para las propiedades de. Los archivos OLEDocFile se muestran en la pestaña detalles y el panel.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Asignaciones de propiedades](-search-3x-wds-propertymappings.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[Proceso de indización](-search-indexing-process-overview.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Propiedades definidas por el sistema para formatos de archivo personalizados](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Sistema de propiedades](../properties/building-property-handlers.md)
</dt> <dt>

[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
