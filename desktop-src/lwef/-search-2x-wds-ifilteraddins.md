---
title: Desarrollo de complementos de IFilter
description: Puede extender Microsoft Windows Desktop Search (WDS) con complementos de filtro, componentes que implementan IFilterinterface, para incluir nuevos tipos de archivo.
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497d4bffdb9564e0737bee3cd0b63fa8026633a2cc81aad37cb989423e460487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480899"
---
# <a name="developing-ifilter-add-ins"></a>Desarrollo de complementos de IFilter

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Puede extender Microsoft Windows Desktop Search (WDS) con complementos de filtro, componentes que implementan la interfaz [**IFilter,**](/windows/desktop/api/filter/nn-filter-ifilter)para incluir nuevos tipos de archivo. Los filtros son responsables de acceder y analizar los datos de los archivos y de devolver pares de propiedades y valores, así como fragmentos de texto para la indexación. Durante el proceso de indexación, WDS llama al filtro adecuado con la dirección URL de cada archivo o elemento. El filtro extrae primero los metadatos que corresponden a las propiedades marcadas como recuperables en el esquema WDS, como el título, el tamaño del archivo y la fecha de última modificación. A continuación, divide el contenido del elemento en fragmentos de texto. WDS agrega las propiedades y el texto devueltos por el filtro al catálogo. WDS puede indexar cualquier tipo de archivo para el que tenga un filtro registrado.

En algunas circunstancias, no es necesario escribir un filtro nuevo. WDS 2.x contiene filtros para más de 200 tipos de elementos (incluidos elementos de texto no cifrado como HTML, XML y archivos de código fuente) y usa la misma tecnología [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Si ya tiene filtros instalados para los tipos de archivo, WDS puede usar esos filtros existentes para indexar estos datos. Además, WDS incluye un filtro general para los tipos de archivo basados en texto no cifrado. Si tiene un tipo de archivo que se puede procesar mediante un filtro de SharePoint Services existente o el filtro de texto no cifrado, puede agregar la extensión de nombre de archivo y filtrar guid al Registro para que WDS pueda localizarlo y usarlo (consulte [Para](#to-register-a-filter-add-in) registrar un complemento de filtro para obtener más información).

Sin embargo, si tiene un formato de archivo o datos no sin formato y de propiedad, escribir una implementación de filtro personalizado es la única manera de asegurarse de que WDS puede indexar el formato de archivo en el catálogo. Solo puede tener un complemento de filtro para un tipo de archivo, por lo que es posible invalidar un filtro existente o hacer que otro filtro invalide el de un tipo de archivo específico.

Esta sección contiene los siguientes temas:

-   [Interfaces de filtro necesarias](#required-filter-interfaces)
    -   [IFilter (interfaz)](#ifilter-interface)
    -   [Ipersiststream](#ipersiststream)
    -   [IPersistFile](#ipersistfile)
    -   [IPersistStorage](#ipersiststorage)
-   [Salida de propiedades con filtros](#outputting-properties-with-filters)
    -   [Valores de propiedad](#property-values)
-   [Filtrar la instalación del complemento](#filter-add-in-installation)
    -   [CLSID necesarios para el registro](#clsids-required-for-registration)
    -   [Modelo de registro](#registration-model)
    -   [Para registrar un complemento de filtro](#to-register-a-filter-add-in)
-   [Temas relacionados](#related-topics)

## <a name="required-filter-interfaces"></a>Interfaces de filtro necesarias

Un complemento de filtro debe implementar la [**interfaz IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)y una de las interfaces siguientes:

-   [IPersistStream:](/windows/win32/api/objidl/nn-objidl-ipersiststream) para cargar datos desde una secuencia. Esto es más seguro que usar archivos porque no se escribe nada en el disco. La interfaz IPersistStream es el método preferido para la compatibilidad con versiones posteriores Windows Vista.
-   [IPersistFile (Interfaz)](/windows/win32/api/objidl/nn-objidl-ipersistfile) : para cargar datos desde un archivo. Esta interfaz no se admite en Windows Vista.
-   [IPersistStorage (Interfaz)](/windows/win32/api/objidl/nn-objidl-ipersiststorage) : para cargar datos desde una estructura OLE COM Storage.

Un complemento de filtro usa estas interfaces para obtener el contenido del elemento y devolverlos iterativamente al índice hasta que se alcanza el final del archivo. Un complemento de filtro debe ser lo más sólido posible para controlar archivos dañados y aquellos que no cumplan los formatos de entrada esperados.

### <a name="ifilter-interface"></a>IFilter (interfaz)

Se trata de una interfaz necesaria para una implementación de filtro. Para más información, consulte la referencia [**de la interfaz IFilter.**](/windows/desktop/api/filter/nn-filter-ifilter)



| Método       | Descripción                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init()       | Inicializa una sesión de filtrado.                                                       |
| GetChunk()   | Coloca el filtro al principio del primer o el siguiente fragmento y devuelve un descriptor. |
| GetText()    | Recupera texto del fragmento actual.                                                 |
| GetValue()   | Recupera los valores de propiedad del fragmento actual.                                      |
| BindRegion() | Actualmente está reservado para uso interno; no implemente. Este método devuelve E \_ NOTIMPL. |



 

### <a name="ipersiststream"></a>Ipersiststream

Esta interfaz carga un archivo desde una secuencia para un procesamiento más seguro que la interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) porque el contexto en el que se ejecuta un filtro [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) no necesita los derechos para abrir ningún archivo en el disco o a través de la red. De los dos métodos para acceder a un único archivo, este es el método preferido para la compatibilidad de reenvío con Windows.



| Método       | Descripción                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty()    | Comprueba si se ha realizado un cambio. Este método devuelve E \_ NOTIMPL en filtros.                                                                      |
| InitNew()    | Crea un nuevo almacenamiento. Este método devuelve E \_ NOTIMPL en filtros.                                                                                  |
| Load()       | Inicializa un objeto desde la secuencia donde se guardó previamente.                                                                               |
| Save()       | Guarda un objeto en la secuencia especificada e indica si el objeto debe restablecer su marca de desajuste. Este método devuelve E \_ NOTIMPL en filtros. |
| GetSizeMax() | Devuelve el tamaño en bytes de la secuencia necesaria para guardar el objeto. Este método devuelve E \_ NOTIMPL en filtros.                                      |



 

### <a name="ipersistfile"></a>IPersistFile

Esta interfaz carga un archivo por ruta de acceso absoluta y no se admite en Windows Vista.



| Método          | Descripción                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| GetCurFile()    | Obtiene el nombre actual del archivo asociado al objeto . Devuelve la ruta de acceso especificada en Load().                          |
| Load()          | Abre el archivo especificado e inicializa un objeto del contenido del archivo. Puede retrasar la apertura del archivo hasta que lo necesite. |
| GetClassID()    | Devuelve el identificador de clase (CLSID) para el nuevo tipo de archivo. Debe usar uuidgen.exe para generar un CLSID único.           |
| IsDirty()       | Solo se necesita devolver E \_ NOTIMPL en los filtros                                                                                       |
| Save()          | Solo se necesita devolver E \_ NOTIMPL en los filtros                                                                                       |
| SaveCompleted() | Solo se necesita devolver E \_ NOTIMPL en los filtros                                                                                       |



 

### <a name="ipersiststorage"></a>IPersistStorage

Esta interfaz admite el modelo de almacenamiento estructurado, en el que cada objeto contenido tiene su propio almacenamiento que está anidado dentro del almacenamiento del contenedor. Al [igual que la interfaz IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile), esta interfaz se carga por ruta de acceso absoluta y no se admite Windows Vista.



| Método            | Descripción                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty()         | Comprueba si se ha realizado un cambio. Este método devuelve E \_ NOTIMPL en filtros.                                 |
| InitNew()         | Crea un nuevo almacenamiento. Este método devuelve E \_ NOTIMPL en filtros.                                             |
| Load()            | Guarda el almacenamiento. Este método devuelve E \_ NOTIMPL en filtros.                                                 |
| Save()            | Devuelve el tamaño en bytes de la secuencia necesaria para guardar el objeto. Este método devuelve E \_ NOTIMPL en filtros. |
| SaveCompleted()   | Reservado para uso interno. Este método devuelve E \_ NOTIMPL en filtros.                                         |
| HandsOffStorage() | Reservado para uso interno. Este método devuelve E \_ NOTIMPL en filtros.                                         |



 

## <a name="outputting-properties-with-filters"></a>Salida de propiedades con filtros

El propósito de un filtro es extraer el contenido y las propiedades de los archivos para su inclusión en el índice de texto completo. WDS llama primero al método Load en las implementaciones IPersistFile, IPersistStream o IPersistStorage y, después, invoca el método Init de la implementación de IFilter. Se llama a **GetChunk** para recuperar fragmentos de texto o datos de valores de propiedad y, a continuación, se llama a **GetText** o **GetValue** tantas veces como sea necesario para recuperar todos los valores de texto o propiedad asociados al fragmento. Este proceso se repite hasta **que GetChunk** informa de que no hay más fragmentos en el documento.

El método **GetChunk** recupera información sobre el primer bloque lógico o siguiente de información del archivo que se filtra y devuelve esa información en una estructura STAT CHUNK, incluido un identificador de fragmento que aumenta de forma monotónica, información de estado sobre cómo se relaciona el fragmento actual con el fragmento anterior, una marca que indica si el fragmento contiene texto o un valor, la configuración regional del fragmento y la especificación de la propiedad del \_ fragmento. La especificación de propiedad es un [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) que consta de un CLSID y un identificador de propiedad de cadena o entero (por ejemplo, D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType). Identifica el tipo de propiedad en lugar del propio valor de propiedad.

El identificador de configuración regional del fragmento se usa para elegir un separador de palabras adecuado y es muy importante que lo identifique correctamente. Si el filtro no puede determinar la configuración regional del texto, debe asumir la configuración regional del sistema predeterminada, disponible mediante **GetSystemDefaultLCID**. Si controla el formato de archivo y actualmente no contiene información de configuración regional, debe agregar una característica de usuario para habilitar la identificación de la configuración regional adecuada. El uso de un separador de palabras no coincidente puede provocar una mala experiencia de consulta para el usuario.

**GetChunk solo** administra el acceso a fragmentos y no devuelve el propio valor de propiedad o texto. En su lugar, las llamadas **posteriores a GetText** **y GetValue** recuperan el cuerpo del fragmento. **GetText** devuelve fragmentos de texto, que son cadenas Unicode, del fragmento CHUNK \_ TEXT actual. Si el fragmento actual es demasiado grande, puede ser necesaria más de una llamada al **método GetText.** Cada llamada al **método GetText** recupera texto que sigue inmediatamente al texto de la última llamada al **método GetText.** Por ejemplo, el último carácter de una llamada puede estar en medio de una palabra y el primer carácter de la siguiente llamada continuaría esa palabra. Los motores de búsqueda deben controlar esta situación.

**GetValue** devuelve valores de propiedad para el fragmento CHUNK VALUE actual en estructuras PROPVARIANT, que pueden \_ contener una amplia variedad de tipos de datos. **GetValue** debe asignar la propia estructura PROPVARIANT mediante CoTaskMemAlloc. El autor de la llamada de **GetValue** es responsable de liberar la memoria a la que apunta propVARIANT mediante PropVariantClear y de liberar la propia estructura con CoTaskMemFree. Para obtener más información sobre PROPVARIANTs, vea la [referencia de PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

### <a name="property-values"></a>Valores de propiedad

Los filtros deben generar como mínimo las siguientes propiedades, que son las columnas predeterminadas en la vista de resultados de WDS.



| GUID                                 | PROPSPEC      | Nombre descriptivo  | Descripción                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | PrimaryTitle   | Título que se muestra para este elemento.                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | PrimaryAuthors | Persona más asociada a este elemento.                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PrimaryDate   | PrimaryDate    | Fecha más importante para el elemento, como la fecha recibida para el correo electrónico o modificada para los archivos.                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PerceivedType | PerceivedType  | Tipo de archivo que se está analizando. Debe coincidir con uno de los Windows búsqueda de escritorio que se enumeran en WdS [Perceived Type](-search-2x-wds-perceivedtype.md). |



 

En el caso de los elementos de texto no cifrado, WDS extrae todo el texto y las propiedades definidas por el sistema, como el tamaño de archivo o la extensión, al incluir nuevos tipos de archivo de texto no cifrado en el índice. Otros tipos de propiedades que se pueden devolver al índice incluyen:

-   Para archivos: author, title, status, keywords
-   Para medios: álbum, género, cámara make, fecha tomada
-   Para las comunicaciones: de, a, cc, importancia
-   Para contactos: puesto de trabajo, teléfono empresarial, empresa

La lista anterior agrupa las propiedades comunes a un tipo percibido especificado; sin embargo, se puede usar cualquier propiedad independientemente del tipo. Por ejemplo, la empresa podría usarse para el nombre del patrón de un contacto y también podría usarse para hacer referencia al nombre de un cliente con el que se relaciona el archivo. Muchas de estas propiedades se usan para mostrar los resultados de la búsqueda en la vista de resultados de WDS. Por ejemplo, la propiedad Title de un archivo se muestra como la columna principal en la vista de resultados predeterminada. Los objetos IFilter deben generar todas las propiedades relacionadas con el tipo de elemento que analizan. No se pueden agregar propiedades personalizadas en WDS 2.x. Para obtener una lista completa de las propiedades disponibles, vea el esquema [de WDS](-search-2x-wds-schematable.md).

## <a name="filter-add-in-installation"></a>Filtrar la instalación del complemento

La instalación del filtro implica copiar el archivo DLL en una ubicación adecuada en el directorio Archivos de programa y registrarlo. Los filtros deben implementar el registro propio para la instalación y deben seguir estas directrices:

-   El instalador debe usar el instalador EXE o MSI.
-   Se deben proporcionar notas de la versión.
-   Se **debe crear una entrada Agregar** o quitar programas para cada complemento instalado.
-   El instalador debe asumir toda la configuración del Registro para el tipo de archivo o almacén determinado que el complemento actual entiende.
-   Si se sobrescribe un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debe haber la capacidad de restaurar la funcionalidad del complemento anterior y convertirla en el complemento predeterminado para ese tipo de archivo o almacenarlo de nuevo.

### <a name="clsids-required-for-registration"></a>CLSID necesarios para el registro

Hay tres identificadores de clase, o CLSID, asociados a cada filtro. Deberá generar uno o varios de ellos (use uuidgen.exe) para registrar el complemento de filtro.

-   La primera identifica el controlador persistente de todos los filtros, IID IFilter, que es \_ {89BCB740-6119-101A-BCB7-00DD010655AF}. Este CLSID es constante para todos los filtros que implementan IFilter.
-   El segundo (el valor de la clave \_ IFilter de IID) identifica la implementación de IFilter para el tipo de archivo. Esta clave contiene un valor InprocServer32 que especifica el nombre del archivo DLL por ruta de acceso y el modelo de subprocesos. Si el filtro está en la ruta de acceso del sistema, como el directorio system32, un nombre de archivo es suficiente. De lo contrario, este valor debe tener una especificación de ruta de acceso completa.
-   La tercera identifica el tipo de archivo que procesa el filtro y lo devuelve el método GetClassID en la interfaz IPersist.

> [!Note]
>
> En versiones futuras de los sistemas operativos de Microsoft, la instalación de archivos en el directorio system32 puede resultar más difícil, por lo que se recomienda instalarlos en Archivos de programa e incluir una ruta de acceso completa al filtro en el Registro. Por motivos de seguridad, también es prudente especificar una ruta de acceso completa al archivo DLL en el Registro. De lo contrario, se podría cargar una versión de "troyano" del archivo DLL si se encuentra en la ruta de acceso del proceso antes de la versión.

 

### <a name="registration-model"></a>Modelo de registro

Cuando WDS está listo para filtrar un archivo, busca en el Registro en la extensión del archivo para determinar qué filtro cargar. A continuación, sigue una serie de vínculos del Registro para buscar el nombre del archivo DLL de filtro, en este orden:

1.  Desde CLSID ubicados en:

    **HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ Override \\ RSApp**

    **HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

2.  Desde el tipo de contenido del archivo en:

    **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Classes \\ MIME \\ Database \\ Content Type**

3.  Desde la extensión de nombre de archivo (igual que la API LoadIFilter de Win32) en:

    **HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ Override \\ RSApp**

    **HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

    **HKEY \_ CLASSES \_ ROOT \\ extpersistentHandler->CLSID->IID \_ IFilter->CLSID**

4.  De forma predeterminada en:

    **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

### <a name="to-register-a-filter-add-in"></a>Para registrar un complemento de filtro

Debe crear un total de ocho entradas en el Registro para registrar el complemento de filtro, donde:

-   **.ext es** la nueva extensión de nombre de archivo
-   **GUID \_ 1 puede** ser cualquier GUID nuevo generado para esta extensión
-   **89BCB740-6119-101A-BCB7-00DD010655AF** es el GUID de la interfaz IFilter, que es una constante para todas las implementaciones de IFilter.

1.  Registre el controlador persistente para la extensión de nombre de archivo con las siguientes claves y valores:

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  Registre la implementación de IFilter con las siguientes claves y valores:

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  Registre la implementación de IFilter con Windows Desktop Search con la clave y el valor siguientes:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Desarrollo de controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Ifilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 