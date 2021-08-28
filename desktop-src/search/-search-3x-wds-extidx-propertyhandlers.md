---
description: Microsoft Windows Search usa controladores de propiedades para extraer los valores de las propiedades de los elementos y usa el esquema del sistema de propiedades para determinar cómo se debe indexar una propiedad específica.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Desarrollar controladores de propiedades para la Windows búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3933353d8bf00c3a68a2259daf94a1ce4f13d295
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627331"
---
# <a name="developing-property-handlers-for-windows-search"></a>Desarrollar controladores de propiedades para la Windows búsqueda

Microsoft Windows Search usa controladores de propiedades para extraer los valores de las propiedades de los elementos y usa el esquema del sistema de propiedades para determinar cómo se debe indexar una propiedad específica. Para leer e indexar valores de propiedad, los controladores de propiedades se invocan fuera de proceso mediante Windows Search para mejorar la seguridad y la solidez. Por el contrario, los controladores de propiedades se invocan en proceso Windows Explorer para leer y escribir valores de propiedad.

Este tema complementa el tema [Sistema de](../properties/building-property-handlers.md) propiedades con información específica de Windows Search y contiene las secciones siguientes:

-   [Decisiones de diseño para controladores de propiedades](#design-decisions-for-property-handlers)
    -   [Decisiones de propiedad](#property-decisions)
    -   [Compatibilidad con texto completo](#full-text-support)
    -   [Consideraciones sobre la implementatización del sistema operativo](#operating-system-implementatation-considerations)
-   [Escribir archivos de descripción de propiedades](#writing-property-description-files)
-   [Implementar controladores de propiedades](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Asegurarse de que los elementos se indexa](#ensuring-your-items-get-indexed)
-   [Instalación y registro de controladores de propiedades](#installing-and-registering-property-handlers)
-   [Probar y solucionar problemas de controladores de propiedades](#testing-and-troubleshooting-property-handlers)
    -   [Pruebas de instalación y configuración](#installation-and-setup-tests)
    -   [Solución de problemas de controladores de propiedades](#troubleshooting-property-handlers)
-   [Uso de System-Supplied controladores de propiedades](#using-system-supplied-property-handlers)
-   [Temas relacionados](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Decisiones de diseño para controladores de propiedades

La implementación de controladores de propiedades implica los pasos siguientes:

1.  Tomar decisiones de diseño con respecto a las propiedades que desea admitir.
2.  Crear un archivo de descripción de propiedad (.propdesc) para las propiedades que aún no están en el sistema de propiedades.
3.  Implementar y probar el controlador de propiedades.
4.  Instalar y registrar el controlador de propiedades y los archivos de descripción de propiedades.
5.  Prueba de la instalación y el registro del controlador de propiedades.

Antes de comenzar, debe tener en cuenta las siguientes preguntas de diseño:

-   ¿Qué propiedades admite o debe admitir el formato de archivo?
-   ¿Estas propiedades ya están en el esquema del sistema?
-   ¿Puedo usar un controlador de propiedades proporcionado por el sistema existente?
-   ¿Qué propiedades se pueden mostrar a los usuarios finales?
-   ¿Qué propiedades pueden editar los usuarios?
-   ¿Debe la compatibilidad con la búsqueda de texto completo procede de un controlador de propiedades o un filtro?
-   ¿Es necesario admitir aplicaciones heredadas? Si es así, ¿qué se implementa?

> [!Note]  
> Antes de continuar, [vea Usar System-Supplied controladores](#using-system-supplied-property-handlers) de propiedades para ver si puede usar un controlador de propiedades proporcionado por el sistema, lo que le ahorra tiempo y recursos de desarrollo.

 

Después de tomar estas decisiones, puede escribir descripciones formales de las propiedades personalizadas para que el motor de Windows Search pueda empezar a indexar los archivos y propiedades. Estas descripciones formales son archivos XML, que se describen en [Esquema de descripción de propiedades](/previous-versions//cc144127(v=vs.85)).

### <a name="property-decisions"></a>Decisiones de propiedad

Al considerar qué propiedades admitir, debe identificar las necesidades de indexación y búsqueda de los usuarios. Por ejemplo, es posible que pueda identificar cien propiedades potencialmente útiles para el tipo de archivo, pero es posible que los usuarios estén interesados en buscar solo en unos pocos. Además, es posible que desee mostrar un grupo diferente, mayor o menor, de esas propiedades a los usuarios en el Explorador de Windows y permitir que los usuarios editan solo un subconjunto de esas propiedades mostradas.

El tipo de archivo puede admitir cualquier propiedad personalizada que defina, así como un conjunto de propiedades definidas por el sistema. Antes de crear una propiedad [](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) personalizada, revise Propiedades del sistema para ver si la propiedad que desea admitir ya está definida por una propiedad del sistema. Asegúrese siempre de que admite las propiedades definidas por el sistema más importantes.

Se recomienda usar una matriz para ayudarle a diseñar las propiedades:



| Nombre de propiedad | ¿Es indexable? | ¿Se puede mostrar? | ¿Es editable? |
|---------------|---------------|-----------------|--------------|
| property1     | Y             | Y               | No            |
| Propiedad...   | Y             | Y               | No            |
| propertyn     | No             | No               | No            |



 

Para cada una de estas propiedades, debe determinar qué atributos debe tener y, a continuación, describirlos formalmente en Archivos XML de descripción de propiedad (.propdesc). Los atributos incluyen el tipo de datos de la propiedad, la etiqueta, la cadena de ayuda y mucho más. En el caso de las propiedades indexables, debe prestar especial atención a los siguientes atributos de propiedad que se encuentran en el elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   del archivo Property Description.



<table>
<colgroup>
<col  />
<col  />
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
<td>Opcional. Indica si un valor de propiedad de cadena debe dividirse en palabras y cada palabra almacenada en el índice invertido. El índice invertido permite buscar palabras y frases de forma eficaz sobre el valor de propiedad mediante CONTAINS o FREETEXT (por ejemplo, SELECT ... WHERE CONTAINS &quot; sometext &quot; ). Si se establece en <strong>FALSE,</strong>las búsquedas se realizan en toda la cadena. La mayoría de las propiedades de cadena deben tener este valor establecido en <strong>TRUE</strong>; Las propiedades que no son de cadena deben tener este valor establecido en <strong>FALSE.</strong> El valor predeterminado es <strong>FALSE.</strong></td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Opcional. Indica si la propiedad debe almacenarse en la base de datos Windows Search como una columna. El almacenamiento de la propiedad como columna permite recuperar, ordenar, agrupar y filtrar (es decir, usar cualquier predicado excepto CONTAINS o FREETEXT) en el valor de columna completo. Las propiedades mostradas al usuario deben tener este valor establecido en <strong>TRUE,</strong> a menos que sea una propiedad textual muy grande (como el cuerpo de un documento) que se buscaría en el índice invertido. El valor predeterminado es <strong>FALSE.</strong></td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Opcional. Indica si una propiedad no toma espacio si el valor es <strong>NULL.</strong> Una propiedad no dispersa ocupa espacio para cada elemento, incluso si el valor es <strong>NULL.</strong> Si la propiedad tiene varios valores, este atributo siempre es <strong>TRUE.</strong> Este atributo solo debe <strong>ser FALSE</strong> si hay un valor para cada elemento. El valor predeterminado es <strong>TRUE.</strong></td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Opcional. Para optimizar las consultas, el motor Windows search puede crear índices secundarios para las propiedades que tienen isColumn=<strong>TRUE.</strong> Esto requiere más procesamiento y espacio en disco durante la indexación, pero mejora el rendimiento durante las consultas. Si la propiedad tiende a ordenarse, agruparse o filtrarse (es decir, mediante =, !=, <, >, LIKE, MATCHES) con frecuencia por los usuarios, este atributo debe establecerse en &quot; &quot; OnDisk. El valor predeterminado &quot; es NotIndexed. &quot; Valores válidos son:
<ul>
<li>NotIndexed: no se crea ningún índice secundario.</li>
<li>OnDisk: cree y almacene un índice secundario en el disco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maxsize</td>
<td>Opcional. Indica el tamaño máximo permitido para el valor de propiedad almacenado en la base de Windows de búsqueda. Este límite se aplica a los elementos individuales de un vector, no al vector en su conjunto. Los valores más allá de este tamaño se truncan. El valor predeterminado es &quot; 128 &quot; (bytes).<br/> Actualmente, Windows Search no usa maxSize al calcular la cantidad de datos que acepta de un archivo. En su lugar, el límite que Windows Search usa es el producto del tamaño del archivo y la lectura de MaxGrowFactor (tamaño de archivo N * MaxGrowFactor) del Registro en HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor. El valor predeterminado de MaxGrowFactor es cuatro (4). Por lo tanto, si el tipo de archivo tiende a ser pequeño en tamaño total pero tiene propiedades más grandes, Windows Search puede no aceptar todos los datos de propiedad que desea emitir. Sin embargo, puede aumentar MaxGrowFactor para satisfacer sus necesidades. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Para el atributo columnIndexType, la ventaja de las consultas más rápidas debe sopesarse con el mayor tiempo de indexación y los costos de espacio en los que pueden incurrir los índices secundarios. Sin embargo, este costo solo se paga por los elementos que tienen un valor distinto de **NULL,** por lo que para la mayoría de las propiedades puede tener este atributo establecido en "OnDisk".

 

### <a name="full-text-support"></a>Compatibilidad con texto completo

Por lo general, la búsqueda de texto completo es compatible con componentes denominados [filtros](-search-3x-wds-extidx-filters.md); sin embargo, para los tipos de archivo basados en texto con formatos de archivo sin complicaciones, los controladores de propiedades pueden proporcionar esta funcionalidad con menos esfuerzo de desarrollo. Debe revisar la sección [Contenido](../properties/building-property-handlers-property-handlers.md) de texto completo para ver una comparación de la funcionalidad de filtro y controlador de propiedades para ayudarle a decidir qué es mejor para el tipo de archivo. De particular importancia es el hecho de que los filtros pueden controlar varios identificadores de código de idioma (LCID) por archivo, mientras que los controladores de propiedades no.

> [!Note]  
> Dado que los controladores de propiedades no pueden fragmentar el contenido del modo en que los filtros pueden, los archivos grandes (aunque sean formatos de archivo sin complicaciones) deben cargarse completamente en la memoria.

 

### <a name="operating-system-implementatation-considerations"></a>Consideraciones sobre la implementatización del sistema operativo

### <a name="implementation-information-for-windows-7"></a>Información de implementación para Windows 7

En Windows 7 y versiones posteriores, hay un nuevo comportamiento al registrar un controlador de propiedades, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)o una nueva extensión. Cuando se instala un nuevo controlador de propiedades o **IFilter,** se vuelve a indexar automáticamente los archivos con las extensiones correspondientes.

En Windows 7 se recomienda que se instale un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) junto con sus controladores de propiedades correspondientes y que **el IFilter** se registre antes que el controlador de propiedades. El registro del controlador de propiedades inicia la re indexación inmediata de los archivos indexados previamente sin necesidad de reiniciar primero y aprovecha las ventajas de los IFilter registrados previamente para la indexación de contenido.

Si solo se instala un [**IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) sin un controlador de propiedades correspondiente, se produce la reindexación automática después de reiniciar el servicio de indexación o reiniciar el sistema.

Para obtener marcas de descripción de propiedades específicas de Windows 7, vea los siguientes temas de referencia:

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [MARCAS \_ SEARCHINFO DE PROPDESC \_](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Información de implementación para Windows Vista y versiones anteriores

Antes de Windows Vista, los filtros proporcionaba compatibilidad para analizar y enumerar el contenido y las propiedades del archivo. Con la introducción del sistema de propiedades, los controladores de propiedades controlan las propiedades de archivo mientras que los filtros controlan el contenido del archivo. Para Windows Vista, solo necesita desarrollar una implementación parcial de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)en coordinación con un controlador de propiedades, como se describe en [Procedimientos recomendados](-search-3x-wds-extidx-filters.md)para crear controladores de filtro en Windows Search .

Aunque el sistema de propiedades también se incluye con la instalación de Windows Search para Windows XP, las aplicaciones de terceros y heredadas pueden requerir que los filtros controle el contenido y las propiedades. Por lo tanto, si va a desarrollar en la plataforma Windows XP, debe proporcionar una implementación de filtro completa, así como un controlador de propiedades para el tipo de archivo o la propiedad personalizada.

 

## <a name="writing-property-description-files"></a>Escribir archivos de descripción de propiedades

La estructura de los archivos XML de descripción de propiedad (.propdesc) se describe en el [tema propertyDescription.](../properties/propdesc-schema-propertydescription.md) De particular interés para la búsqueda son los atributos del [elemento searchInfo.](../properties/propdesc-schema-searchinfo.md) Una vez que haya decidido qué propiedades admitir, debe crear y registrar archivos de descripción de propiedades para cada propiedad. Al registrar los archivos .propdesc, se incluyen en la lista de descripción de propiedades del esquema y se convierten en nombres de columna en el almacén de propiedades del motor de búsqueda.

Puede registrar las descripciones de propiedades personalizadas mediante la función [PSRegisterPropertySchema,](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) una API contenedora que llama a IPropertySystem::RegisterPropertySchema del subsistema de esquema. Esta función informa al subsistema de esquema de la adición de archivos de esquema de descripción de propiedad (.propdesc), mediante rutas de acceso de archivo a los archivos .propdesc del equipo local, normalmente el directorio de instalación de la aplicación en "Archivos de programa". Normalmente, una instalación o aplicación (por ejemplo, el instalador del controlador de propiedades) llamará a este método después de instalar los archivos .propdesc.

 

## <a name="implementing-property-handlers"></a>Implementar controladores de propiedades

Desarrollar un controlador de propiedades implica implementar las interfaces siguientes:

-   IInitialzeWithStream: proporciona inicialización basada en secuencias del controlador de propiedades.
-   IPropertyStore: enumera, obtiene y establece los valores de propiedad.
-   IPropertyStoreCapabilities: opcional. Identifica si los usuarios pueden editar una propiedad desde una interfaz de usuario.

### <a name="iinitializewithstream"></a>IInitializeWithStream

Como se describe en el tema [Sistema](../properties/building-property-handlers.md) de propiedades, se recomienda encarecidamente implementar controladores de propiedades con **IInitializeWithStream** para realizar la inicialización basada en secuencias. Si decide no implementar IInitializeWithStream, el controlador de propiedades debe rechazar la ejecución en el proceso de aislamiento estableciendo la marca DisableProcessIsolation en la clave del Registro del controlador de propiedades. Por lo general, deshabilitar el aislamiento de procesos solo está pensado para controladores de propiedades heredados y cualquier código nuevo debe evitarlo.

### <a name="ipropertystore"></a>IPropertyStore

Para crear un controlador de propiedades, debe implementar la [**interfaz IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con los métodos siguientes.



| Método   | Descripción                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Guarda un cambio de propiedad en el archivo.                                |
| GetAt    | Recupera una clave de propiedad de la matriz de propiedades de un elemento.        |
| GetCount | Obtiene el número de propiedades adjuntas al archivo.                 |
| GetValue | Recupera los datos de una propiedad específica.                             |
| SetValue | Establece un nuevo valor de propiedad o reemplaza o quita un valor existente. |



 

 

 

En la documentación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) se incluyen consideraciones importantes para implementar esta interfaz.

> [!Note]  
> Si el controlador de propiedades emite varios valores para la misma propiedad para un elemento determinado, solo el último valor emitido se almacena en el catálogo.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

Opcionalmente, los controladores de propiedades pueden implementar esta interfaz para deshabilitar la capacidad de un usuario de editar propiedades específicas. Normalmente, estas propiedades se pueden editar en la página y el panel Detalles, pero no se permite editarlas en el controlador de propiedades de implementación. La implementación correcta de esta interfaz proporciona una mejor experiencia de usuario que la alternativa: un error en tiempo de ejecución simple del shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Asegurarse de que los elementos se indexa

Ahora que ha implementado el controlador de propiedades, quiere asegurarse de que los elementos para los que está registrado el controlador se indexen. Puede usar [](-search-3x-wds-mngidx-catalog-manager.md) el Administrador de catálogos para iniciar la re indexación y también puede usar el [Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md) para configurar reglas predeterminadas que indiquen las direcciones URL que desea que rastree el indexador. Otra opción es seguir el ejemplo de código ReIndex en los ejemplos [del SDK Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Para obtener más información, consulte [Uso del Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y Uso del [Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Instalación y registro de controladores de propiedades

Con el controlador de propiedades implementado, se debe registrar y su extensión de nombre de archivo asociada al controlador. En el ejemplo siguiente se muestran las claves y los valores del Registro necesarios para hacerlo.

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

En la lista siguiente se proporcionan consejos sobre los tipos de pruebas que debe realizar:

-   Pruebe a obtener la salida de todas las propiedades admitidas por el tipo de archivo.
-   Use valores de propiedad grande, por ejemplo, use una metatag grande en documentos HTML.
-   Compruebe que el controlador de propiedades no pierde identificadores de archivo editándolo después de obtener la salida del controlador de propiedades o mediante una herramienta como oh.exe antes y después de enumerar las propiedades del archivo.
-   Pruebe todos los tipos de archivo asociados al controlador de propiedades. Por ejemplo, compruebe que el filtro HTML funciona con .htm y .html tipos de archivo.
-   Pruebe con archivos dañados. El controlador de propiedades debe producir un error correctamente.
-   Si una aplicación admite el cifrado, compruebe que el controlador de propiedades no genera texto cifrado.
-   Si el controlador de propiedades admite la búsqueda de texto completo:
    -   Use varios caracteres Unicode especiales en el contenido del archivo y pruebe su salida.
    -   Pruebe el control de documentos muy grandes para asegurarse de que el controlador de propiedades funciona según lo previsto.

### <a name="installation-and-setup-tests"></a>Pruebas de instalación y configuración

Por último, debe probar las rutinas de instalación y desinstalación.

-   La instalación debe recuperarse de instalaciones con errores (por ejemplo, de cancelar y reiniciar la instalación).
-   La desinstalación debe eliminar todos los archivos asociados al controlador de propiedades.
-   La desinstalación no debe eliminar archivos distintos de los asociados a la instalación del controlador de propiedades.
-   Las claves del Registro asociadas al controlador de propiedades deben quitarse cuando se desinstale.
-   La desinstalación debe funcionar incluso si los archivos se eliminan del directorio de instalación.

### <a name="troubleshooting-property-handlers"></a>Solución de problemas de controladores de propiedades

Estos son algunos errores comunes que se producen al desarrollar controladores de propiedades:

-   Instalación de archivos .propdesc o ARCHIVOS DLL en un directorio de usuario.
-   Registrar componentes mediante rutas de acceso relativas.
-   Registrar componentes en HKEY \_ CURRENT USER en lugar de \_ HKEY LOCAL \_ \_ MACHINE.
-   Se ha olvidado de establecer DisableProcessIsolation para controladores que no son de secuencia.
-   Colocar el archivo de prueba en una ubicación sin indexar.

Si tiene problemas para que el controlador de propiedades funcione con el indexador, estas son algunas sugerencias para ayudarle a solucionar problemas:

-   Compruebe que las descripciones de propiedades (archivos .propdesc) están marcadas como isColumn="**true**", isViewable="**true**", y isQueryable="**true**" según corresponda.
-   Compruebe que los archivos .propdesc se encuentran en una ubicación global.
-   Compruebe que ha registrado los archivos .propdesc mediante rutas de acceso absolutas.
-   Compruebe que el registro de eventos no registró ningún error al registrar el archivo .propdesc.
-   Compruebe que los archivos DLL están en una ubicación global (y no en el perfil de usuario).
-   Compruebe que los archivos DLL están registrados en clases de software HKEY \_ LOCAL \_ \\ \\ MACHINE.
-   Compruebe que los archivos DLL están registrados mediante rutas de acceso completas (o cadenas REG EXPAND SZ que se expanden a rutas de acceso absolutas mediante variables de \_ \_ entorno conocidas por la cuenta del sistema).
-   Compruebe que el controlador de propiedades funciona en Windows Explorer.
-   Aunque se recomienda usar IInitializeWithStream, si debe usar IInitializeWithFile o IInitializeWithItem, compruebe que especifica DisableProcessIsolation.
-   Compruebe que la página Opciones de Panel de control muestra el tipo de archivo como un tipo de archivo indexado.
-   Compruebe que el archivo de prueba está en una ubicación indizada.
-   Compruebe que el archivo de prueba se ha modificado desde que instaló el controlador de propiedades.

Si el archivo de prueba se encuentra en una ubicación indizada y el indexador ya ha rastreado esa ubicación, debe modificar el archivo de alguna manera para desencadenar una reindexación del archivo.

 

## <a name="using-system-supplied-property-handlers"></a>Uso de System-Supplied controladores de propiedades

Windows incluye una serie de controladores de propiedades proporcionados por el sistema que puede usar si el formato del tipo de archivo es compatible. Si define una nueva extensión de archivo que usa uno de estos formatos, puede usar los controladores proporcionados por el sistema registrando el identificador de clase de controlador (CLSID) para la extensión de archivo.

Puede usar el CLSID que se muestra en la tabla siguiente para registrar los controladores de propiedades proporcionados por el sistema para el tipo de formato de archivo.



| Formato          | CLSID                                  |
|-----------------|----------------------------------------|
| OLE DocFile     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Guardar XML de juego   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| Controlador XPS/OPC | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Antes de crear una propiedad personalizada, debe asegurarse de que no hay ninguna propiedad definida por el sistema que pueda usar en su lugar. Para enumerar las propiedades definidas por el sistema, llame a [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) o use la prop.exe línea de comandos.

El esquema del sistema define cómo interactúan estas propiedades con el indexador y no se puede cambiar. Además, la aplicación que use para crear, editar y guardar el tipo de archivo también debe ajustarse a cierto comportamiento. Por ejemplo, si la aplicación implementa un guardado seguro (en el que se crea un archivo temporal durante la edición y, a continuación, se usa ReplaceFile() para intercambiar la nueva versión por la anterior), debe transferir todas las propiedades del archivo original al nuevo archivo. Si no lo hace, el archivo pierde las propiedades agregadas por los usuarios u otras aplicaciones.

 

**Ejemplo**

A continuación se muestra el registro del controlador OLE DocFile proporcionado por el sistema para un tipo de archivo con . Extensión OLEDocFile.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

A continuación se muestra el registro de la información de la lista de propiedades para las propiedades de . Los archivos OLEDocFile se muestran en la pestaña Detalles y el panel.

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

**Conceptual**
</dt> <dt>

[Procedimientos recomendados para crear controladores de filtro en Windows Búsqueda](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[El proceso de indexación](-search-indexing-process-overview.md)
</dt> <dt>

[Desarrollo de controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Propiedades definidas por el sistema para formatos de archivo personalizados](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Sistema de propiedades](../properties/building-property-handlers.md)
</dt> <dt>

[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Windows Ejemplos del SDK de búsqueda](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
