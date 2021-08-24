---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Windows Glosario de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efe8bbe07badc7575cc3aba83100814d601bc5c8ebca24961b198950b2e5e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844655"
---
# <a name="windows-search-glossary"></a>Windows Glosario de búsqueda

## <a name=""></a>\#

**Archivo .osd**

OpenSearch Archivo de descriptor.

**Archivo .osdx**

Un OpenSearch xml de descripción que describe las conexiones de servidor disponibles y los formatos de resultado para un origen de datos basado en web específico. Se usa para interactuar con el Windows Shell. Vea también: OpenSearch descriptor.

## <a name="a"></a>A

**Sintaxis de consulta avanzada (AQS)**

La sintaxis de consulta predeterminada usada por Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda. AQS está orientado principalmente al usuario y los usuarios pueden usarlas para crear consultas de AQS, pero también se pueden usar mediante programación. Vea también: Sintaxis de consulta natural (NQS).

**Aqs**

Vea la definición de: Sintaxis de consulta avanzada (AQS).

**Asociación**

Asignación de una extensión de nombre de archivo (por ejemplo, .mp3) o un protocolo (por ejemplo, http) a un identificador de programación (ProgID). Esta asignación se almacena en el Registro como una configuración por usuario con una reserva por equipo. Las aplicaciones que participan en el sistema programas predeterminados establecen la asignación de asociación para la extensión o el protocolo de nombre de archivo para que apunten a las claves ProgID que poseen.

**matriz de asociación**

Lista ordenada de ubicaciones del Registro usadas para almacenar información sobre un tipo de elemento, incluidos controladores, verbos y otros atributos, como el icono y el nombre para mostrar del tipo. Por ejemplo, un archivo .jpg tiene la siguiente matriz de asociación en un sistema Windows predeterminado: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\.jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Esquema XML que se usa para las fuentes web y la distribución de contenido, desarrollado como alternativa a La distribución realmente simple (RSS). El formato de redidición atom se publicó como estándar propuesto por IETF en RFC 4287.

## <a name="b"></a>B

**bind**

Para cargar o asociar código a los datos. Por ejemplo, un controlador puede estar asociado a un origen de datos de Shell.

**Vinculante**

Una solicitud en una consulta de búsqueda para una columna en un conjunto de filas devuelto. El enlace especifica una propiedad que se va a incluir en los resultados de la búsqueda.

**bookmark**

Indicador que identifica de forma única una fila dentro de un conjunto de filas.

## <a name="c"></a>C

**nombre canónico**

Nombre único de un recurso. Canonical significa "según las reglas". Vea también: nombre de verbo canónico.

**nombre del verbo canónico**

Nombre independiente del idioma que se puede usar mediante programación para hacer referencia a un verbo, independientemente de la cadena localizada en la interfaz de usuario. Vea también: nombre canónico, verbo.

**catalog**

Unidad de nivel superior de la organización en Windows Search. Un catálogo representa un conjunto de documentos indexados que se pueden consultar. Un catálogo consta de una tabla de propiedades con el texto o el valor y la ubicación correspondiente almacenada en columnas de la tabla. Cada fila de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada columna de la tabla corresponde a una propiedad . Vea también: index, Windows servicio Search.

**category**

Agrupación jerárquica de filas. Por ejemplo, un resultado de consulta que contiene columnas de autor y título se puede clasificar en función del autor. En este ejemplo, cada grupo de filas que contiene el mismo valor para author constituye una categoría.

**Capítulo**

Colección de filas dentro de un conjunto de filas. Vea también: catálogo, categoría.

**column**

Contenedor para un único tipo de información de una fila. Las columnas se asignan a nombres de propiedad y especifican qué propiedades se usan para los elementos del árbol de comandos de la consulta de búsqueda. Consulte también: categoría.

**árbol de comandos**

Combinación de restricciones, categorías y ordenaciones que se especifican para la consulta de búsqueda. Consulte también: categoría.

**container**

Tipo de elemento de Shell que puede contener otros elementos. Los elementos de un contenedor se exponen al espacio de nombres de Shell mediante un origen de datos de Shell. Entre los ejemplos se incluyen carpetas, unidades, servidores de red y archivos comprimidos con .zip extensión de nombre de archivo. Vea también: Origen de datos de Shell, carpeta, elemento de Shell.

**content**

Texto y propiedades asociadas a un elemento de Shell o a un origen de contenido que se puede indexar.

**origen de contenido**

Elemento al que puede tener acceso el indexador. Los orígenes de contenido son direccionables mediante una dirección URL y un controlador de protocolo proporciona al indexador. Algunos ejemplos son: archivos y carpetas del sistema de archivos, elementos y carpetas de Microsoft Outlook, registros de base de datos y elementos almacenados SharePoint Microsoft. Un origen de contenido se puede exponer como elementos de Shell mediante la implementación de un origen de datos de Shell. Vea también: contenido, elemento de Shell.

**content view (vista de contenido)**

Una vista en Windows Explorer (que se ofrece en Windows 7 y versiones posteriores) que muestra el contenido más relevante para cada elemento de la lista en función de su extensión de nombre de archivo o asociación kind. La vista de contenido usa una lógica de cambiar el tamaño que quita las propiedades cuando el tamaño de la ventana disminuye para asegurarse de que las propiedades más críticas todavía tienen espacio para ser claramente legibles. Vea también: patrón de diseño, kind, kind asociación.

**modo de vista de contenido**

Vea la definición de: vista de contenido.

**menú contextual**

Este término se usa a veces para significar el menú contextual. Vea la definición de: menú contextual.

**controlador de menú contextual**

Este término se usa a veces para significar el controlador del menú contextual. Vea la definición de: controlador de menú contextual.

**rastreo**

Para recorrer en iteración un ámbito de rastreo, identifique los orígenes de contenido que requieren indexación o re indexación.

**ámbito de rastreo**

Colección de almacenes de datos (identificables por dirección URL) que representa el contenido que el indexador rastrea e indexa.

**cursor**

En el contexto del índice local, un cursor es un indicador para trabajar con una fila o un pequeño bloque de filas a la vez en un conjunto de datos devuelto en un conjunto de resultados. Una vez que el cursor se coloca en una fila, se pueden realizar operaciones en esa fila o en un bloque de filas a partir de esa posición.

## <a name="d"></a>D

**Administración de datos, exploración y minería de datos**

Vea la definición de: Extensiones de minería de datos (DMX).

**controlador de objetos de datos**

Controlador que proporciona formatos de Portapapeles adicionales para el objeto de datos (IDataObject) de un elemento. Los objetos de datos se usan en escenarios de arrastrar y colocar y copiar y pegar.

**origen de datos**

Este término se usa a veces para significar el almacén de datos o el origen de datos de Shell. Consulte la definición de: almacén de datos, origen de datos de Shell.

**almacén de datos**

Repositorio de datos. Un almacén de datos se puede exponer al modelo de programación de Shell como un contenedor mediante un origen de datos de Shell. Los elementos de un almacén de datos se pueden indexar mediante el sistema Windows Search mediante un controlador de protocolo.

**Extensiones de minería de datos (DMX)**

Lenguaje de consulta utilizado para crear y manipular la minería de datos. Las plantillas administrativas para Windows 7, Windows Search y Windows Explorer son archivos .admx y se basan en la tecnología DMX. Las plantillas siguientes se pueden personalizar mediante directiva de grupo: Search.admx, Explorer.admx y WindowsExplorer.admx.

**Dmx**

Vea la definición de: Extensiones de minería de datos.

**document**

Elemento de Shell que contiene texto y para el que se podría implementar la interfaz IFilter.

**drop handler**

Controlador que permite que un tipo de elemento determinado admita escenarios de arrastrar y colocar y copiar y pegar.

**drop target**

Objeto de datos que se arrastra y se arrastra a un archivo. Vea también: controlador de datos, controlador de colocación.

**verbo dinámico**

Verbo que depende del estado de un elemento de Shell o del sistema; la apariencia del elemento se basa en el estado y requiere que el código en ejecución determine si debe aparecer el elemento. Vea también: controlador de menú contextual, verbo estático, verbo.

## <a name="e"></a>E

**Comando del explorador**

Objeto que se puede presentar como un botón cerca de la parte superior de la ventana Windows Explorer que proporciona funcionalidad para los elementos y contenedores de esa ventana. Un origen de datos de Shell proporciona los Windows de comandos del Explorador para un elemento de contenedor determinado. Los comandos se usan a veces como verbos.

## <a name="f"></a>F

**búsqueda federada**

Modelo de extensibilidad que permite buscar almacenes de datos y representar los resultados como elementos de Shell en Windows Explorer. Consulte también: proveedor de búsqueda federado, conector de búsqueda, descriptor de OpenSearch, OpenSearch estándar.

**conector de búsqueda federado**

Consulte la definición de: conector de búsqueda.

**proveedor de búsqueda federado**

Un servicio web, implementado por un almacén de datos, que admite los protocolos usados por Windows 7 para que Windows 7 y versiones posteriores puedan buscar en ese almacén de datos de forma remota. Vea también: descriptor OpenSearch, OpenSearch estándar.

**asociación de archivos**

Consulte la definición de: asociación de tipo de archivo.

**formato de archivo**

Formato para los datos almacenados en un archivo que tiene una especificación de formato documentada. Algunos ejemplos son OLE DocFile, OPC, XML, ZIP y otras especificaciones conocidas de formato de archivo. Los creadores de tipos de archivo suelen usar un formato de archivo existente como base de un nuevo tipo de archivo. Un formato de archivo puede ser simplemente una definición a la que no se crea una instancia como un tipo de archivo.

**controlador de formato de archivo**

Este término es un sinónimo del controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**extensión de nombre de archivo**

Consulte la definición de: extensión de nombre de archivo.

**extensión de nombre de archivo**

Indicador principal de un tipo de archivo para los elementos del sistema de archivos, es la parte del nombre de archivo que sigue al punto final. La extensión de nombre de archivo no puede contener espacios ni caracteres no ASCII y solo se aplica a los archivos (no a las carpetas). Las extensiones de nombre de archivo se comparan mediante una función de comparación que no distingue mayúsculas de minúsculas o configuración regional. Consulte también: formato de archivo, tipo de archivo.

**tipo de archivo**

Un valor de extensión de nombre de archivo determinado, como ".htm" o ".jpg", que define una clase de archivos que son del mismo tipo y tienen un conjunto común de asociaciones. Vea también: Tipo, asociación de tipo de archivo.

**asociación de tipo de archivo**

Para una extensión de nombre de archivo determinada, los elementos de la matriz de asociación que definen dónde se pueden registrar los controladores y otros atributos. Vea también: matriz de asociación, tipo de archivo.

**personalización del tipo de archivo**

Asociación que permite a Shell personalizar cómo Shell trata un tipo de archivo. Las personalizaciones de tipo de archivo incluyen: especificar la aplicación que se usa para abrir el archivo al hacer doble clic, agregar comandos al menú contextual para un tipo de archivo, especificar un icono personalizado, especificar un tipo de contenido MIME para asociar con un tipo de archivo, especificar un tipo percibido y especificar una o varias aplicaciones asociadas por tipo de archivo con el cuadro de diálogo Abrir con . Vea también: PerceivedType.

**controlador de tipo de archivo**

Controlador registrado para un tipo de archivo. Vea también: controlador.

**filter**

Implementación de la interfaz IFilter. Abre archivos de un tipo de archivo determinado y filtra propiedades y fragmentos de texto para el indexador. Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLID). Aunque un filtro puede controlar varios tipos de archivo, cada tipo de archivo funciona con un solo filtro.

**Carpeta**

Consulte la definición de: contenedor.

## <a name="h"></a>H

**handler**

Objeto COM que proporciona funcionalidad para un elemento de Shell. La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos. Por ejemplo, la carpeta del sistema de archivos usa el sistema de asociación para buscar los controladores de un tipo de archivo determinado. Vea también: asociación de archivos, tipo de archivo, personalización de tipos de archivo.

## <a name="i"></a>I

**controlador de iconos**

Controlador que proporciona la información necesaria para generar y almacenar en caché un icono de un elemento. El almacén de datos del sistema de archivos admite la carga de un controlador de iconos para un elemento basado en el tipo de archivo, lo que permite que ese controlador proporcione un icono que se usa para todas las instancias de ese tipo de archivo.

**índice**

n. Catálogo que almacena el contenido y las propiedades de los elementos de Shell para habilitar búsquedas rápidas. Vea también: catálogo, indexador, indexación, índice invertido. v. Para acceder a los orígenes de contenido, filtre los orígenes de contenido y propiedades e inserte los valores extraídos en el índice (para texto) y en el almacén de propiedades Windows Search (para propiedades). Vea también: origen de contenido, índice, indexador, índice invertido.

**indexador**

Aplicación que realiza la indexación o coordina la indexación. Vea también: indexación, indexación, índice invertido.

**Controlador de información sobre información**

Controlador que proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre un objeto de interfaz de usuario.

**índice invertido**

Estructura persistente que contiene el contenido que se extraía de los archivos mediante Windows Search. El texto se organiza en un índice que se asigna desde una palabra de una propiedad a una lista de los documentos y ubicaciones dentro de un documento que contiene esa palabra. Por lo tanto, un índice invertido es el inverso del proceso de extraer el texto y las propiedades del documento y colocarlos en el indexador. Vea también: indexación, indexador e indexación.

**item**

Vea la definición de: Elemento de Shell.

**item (clase)**

Consulte la definición de: tipo de archivo.

## <a name="k"></a>K

**Variante**

Propiedad que proporciona un nombre de tipo descriptivo y se puede asociar a una lista de propiedades y un patrón de diseño. Kind se introdujo en Windows Vista para expresar una noción más fácil de usar del tipo de archivo y se definió como una propiedad de cadena de varios valores (valores de cadena canónicos), por lo que puede tener un valor de tipo "audio;video" o "link;document". Algunos nombres de tipo descriptivos ya están asociados a propiedades y patrones de diseño. Por ejemplo, los elementos asociados a Kind.Picture y los elementos asociados a Kind.Document muestran propiedades diferentes incluso cuando están en la misma vista. Cada tipo de elemento se puede asociar a uno de los cuatro patrones de diseño únicos que definen el número de propiedades que se muestran para cada elemento y su diseño. Vea también: Asociación de tipo, vista de contenido, patrón de diseño.

**Asociación de tipo**

Propiedad del sistema de propiedades, denominada System.Kind, que determina qué plantillas de experiencia de usuario se muestran para un archivo. Esta propiedad también proporciona un nombre descriptivo para el tipo del elemento y está vinculada a la extensión de nombre de archivo. Vea también: Tipo.

## <a name="l"></a>L

**patrón de diseño**

Una de las diversas disposiciones para mostrar propiedades. En Windows 7 y versiones posteriores, al registrar un nuevo tipo de archivo, puede usar la vista de contenido para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo. Puede elegir entre cuatro patrones de diseño diferentes: Alpha (para los resultados de búsqueda de documentos que contienen fragmentos de código), Beta (para los resultados de búsqueda de correo electrónico con fragmentos de código), Gamma (similar a Alpha pero con un diseño de dos líneas en lugar de cuatro) y Delta (para mostrar muchas propiedades más cortas, como con música e imágenes). Vea también: vista de contenido, asociación Kind y Kind.

## <a name="m"></a>M

**controlador de metadatos**

Este término se usa a veces para significar controlador de propiedades. Vea la definición de: controlador de propiedades.

## <a name="n"></a>N

**extensión de espacio de nombres**

Consulte la definición de: Origen de datos de Shell.

**namespace walk**

Proceso auxiliar que recorre el espacio de nombres de un contenedor o conjunto de contenedores, detectando cada elemento y posiblemente haciendo algo con cada uno. La interfaz INamespaceWalk se puede usar para recorrer cualquier parte del espacio de nombres de Windows Explorer o para detectar los elementos a los que hace referencia un objeto o vista de datos. Los verbos de contenedor (como "reproducir" en contenedores de Artists) recorrerán el espacio de nombres y detectarán los elementos.

**consulta en lenguaje natural**

Vea la definición de: Sintaxis de consulta natural (NQS).

**Sintaxis de consulta natural (NQS)**

Sintaxis de consulta más relajada que AQS y más similar al lenguaje humano. NQS se puede usar Windows Search para consultar el índice si NQS está seleccionado en lugar del valor predeterminado, AQS. Vea también: Sintaxis de consulta avanzada (AQS).

**palabra irrelevante**

Palabra que se omite por Windows Search cuando está presente en las restricciones especificadas para la consulta de búsqueda, porque tiene poco valor discriminador. Entre los ejemplos se incluyen "and" y "the".

**Nqs**

Vea la definición de: Sintaxis de consulta natural (NQS).

## <a name="o"></a>O

**Object Linking and Embedding Database (OLE DB)**

Conjunto estándar de interfaces que proporciona acceso heterogéneo a diferentes orígenes de información ubicados en cualquier lugar, como sistemas de archivos, carpetas de correo electrónico y bases de datos.

**OLE DB**

Vea la definición de: Object Linking and Embedding Database.

**OpenSearch descriptor**

Un archivo XML que describe las conexiones de servidor disponibles y los formatos de resultado para un origen de datos basado en web específico. Este archivo contiene una o varias plantillas de dirección URL y usa una extensión de nombre de archivo .osdx al interactuar con Windows Shell. Una OpenSearch descripción se conoce a veces como conector de búsqueda, aunque es solo la parte de descripción de un conector. Consulte también: Conector de búsqueda.

**OpenSearch estándar**

Colección de formatos y protocolos simples que se usan para compartir los resultados de búsqueda. Para obtener más información, consulte el sitio OpenSearch web ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Una amplia categoría de tipos de formato de archivo. PerceivedType se introdujo en Windows XP y admite un conjunto limitado de tipos de archivo conocidos (entre los que se incluyen los tipos de archivo Image, Text, Audio y Compressed). Los tipos de archivo, generalmente los tipos de archivo públicos, también pueden tener un tipo percibido. Por ejemplo, los tipos de archivo de imagen .bmp, .png, .jpg y .gif también son del tipo percibido, image. En la capa de programación, PerceivedType se expresa como un entero. Dado que hay código que usa Kind y PerceivedType, los propietarios de formato de archivo deben registrar ambos. Por ejemplo, "reproducir todo" depende de PerceivedType. Consulte también: tipo de archivo.

**controlador de vista previa**

Controlador que genera rápidamente una vista simplificada y de solo lectura del elemento shell que se va a mostrar en el panel de vista previa Windows Explorer.

**Previewer**

Este término se usa a veces para significar controlador de vista previa. Vea la definición de: controlador de vista previa.

**controlador de propiedades**

Controlador que convierte los datos almacenados en un archivo en un esquema estructurado reconocido por y al que pueden acceder Windows Explorer, Windows Search y otras aplicaciones. A continuación, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer propiedades hacia y desde el archivo. Los datos traducidos incluyen la vista de detalles, información sobre información, panel de detalles, páginas de propiedades, etc. Cada controlador de propiedades está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Consulte también: sistema de propiedades.

**controlador de hoja de propiedades**

Controlador que se usa para crear hojas de propiedades personalizadas con imágenes de interfaz de usuario y controles que permiten la interacción personalizada con un tipo de archivo.

**sistema de propiedades**

Un sistema extensible de lectura y escritura de definiciones de datos que usa propiedades implementadas como pares nombre-valor. Vea también: controlador de propiedades, elemento de Shell.

**valor de propiedad**

Valor asociado a un nombre de propiedad para un elemento de Shell. Por ejemplo, "Author", "Size" y "Date Taken" son propiedades. Los valores de propiedad se expresan como una estructura PROPVARIANT.

**controlador de protocolo**

Controlador que tiene acceso a orígenes de contenido y proporciona un objeto IUrlAccessor para un protocolo y una dirección URL especificados. Los controladores de protocolo amplían Windows search y pueden proporcionar notificaciones de cambio a los indexadores. Se requieren controladores de protocolo diferentes para indexar tipos específicos de almacenes de datos. Para proporcionar una experiencia de usuario razonable, también debe proporcionar un origen de datos de Shell para el almacén de datos, además de implementar el controlador de protocolo. El controlador de protocolo expone los elementos del almacén de datos al indexador, mientras que el origen de datos de Shell expone los elementos del almacén de datos al Shell.

## <a name="r"></a>R

**Restricción**

Condición que un archivo debe cumplir para incluirse en los resultados de búsqueda devueltos por Windows Search.

**row**

Columnas que contienen los valores de propiedad que describen un único resultado del conjunto de objetos que coincidieron con las restricciones especificadas en una consulta de búsqueda.

**Filas**

Conjunto de filas devueltas en los resultados de la búsqueda.

## <a name="s"></a>S

**conector de búsqueda**

Un archivo XML que contiene información sobre un almacén de datos. Los conectores de búsqueda se implementan para la búsqueda federada.

**consumidor de búsqueda**

Componente o aplicación que consulta el índice.

**federación de búsqueda**

Consulte la definición de: proveedor de búsqueda federado.

**proveedor de búsqueda**

Componente o aplicación que proporciona datos para Windows Search.

**ámbito de búsqueda**

Este término se usa a veces para significar ámbito de rastreo. Consulte la definición de: ámbito de rastreo.

**Origen de datos de Shell**

Componente que se usa para extender el espacio de nombres de Shell y exponer elementos en un almacén de datos. En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell. Vea también: contenedor, controlador, elemento de Shell.

**Extensión de shell**

Este término se usa a veces para significar controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**Controlador de extensiones de Shell**

Este término se usa a veces para significar controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**Controlador de shell**

Este término se usa a veces para significar controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**Elemento de shell**

Un único fragmento de contenido. Algunos elementos de Shell son orígenes de contenido y otros no. Una carpeta es un origen de contenido, por ejemplo, pero un archivo .jpg no lo es. Los controladores de tipo de archivo exponen elementos de Shell. En algunos contextos, "item" se usa para distinguir contenedores de no contenedores. Vea también: contenedor, origen de contenido, controlador de tipo de archivo.

**Extensión de espacio de nombres de Shell**

Este término se usa a veces para significar el origen de datos de Shell. Consulte la definición de: Origen de datos de Shell.

**menú contextual**

Interfaz de usuario que se usa para presentar una colección de verbos asociados a un elemento de interfaz de usuario, como un archivo o una carpeta.

**Controlador de menú contextual**

Controlador que agrega verbos para un elemento o elementos. Estos verbos se muestran normalmente en un menú contextual. Vea también: menú contextual.

**verbo estático**

Verbo que se aplica a un elemento de Shell sin necesidad de inspeccionar el estado actual de un elemento o sistema. Un verbo estático se basa en un registro estático de los elementos asociados de un elemento y no cambia.

## <a name="t"></a>T

**controlador de miniaturas**

Controlador que proporciona una imagen estática para representar un elemento de Shell.

**proveedor de miniaturas**

Este término se usa a veces para significar el controlador de miniaturas. Vea la definición de: controlador de miniaturas.

## <a name="u"></a>U

**URL template**

Cadena de conexión basada en url que se usa para consultar los resultados de la búsqueda en un servidor web. La plantilla parece una dirección URL, pero contiene varios valores de marcador de posición (como {searchTerms}) que el cliente debe reemplazar por datos sobre los resultados que desea recuperar. La definición de plantillas de dirección URL es clave para implementar la búsqueda federada y OpenSearch estándares.

**nombre de tipo descriptivo**

Vea la definición de: Kind.

## <a name="v"></a>V

**Verbo**

Acción individual a la que puede llamar un elemento de Shell. Algunos ejemplos son abrir e imprimir. Los verbos a veces se conocen como comandos o tareas. Vea también: verbo dinámico, controlador de menú contextual, verbo estático.

**controlador de verbo**

Este término se usa a veces para significar el controlador del menú contextual. Vea definition for: shortcut menu handler (Definición de: controlador de menú contextual).

## <a name="w"></a>W

**Caminar**

Vea definition for: namespace walk (Definición de: espacio de nombres).

**Windows Search**

Vea la definición de: Windows servicio Search.

**Windows Buscar almacén de propiedades**

Caché de valores de propiedad utilizados en la implementación del Windows servicio Search. Estos valores de propiedad se pueden consultar mediante programación mediante el proveedor Windows search OLE DB búsqueda. El Windows de propiedades search recopila y almacena las propiedades emitidas por controladores de filtro o controladores de propiedades cuando se indexa un elemento como un documento de Word. Este almacén se descarta y se recompila cuando se recompila el índice.

**Windows servicio Search**

Hace referencia Windows Search 3.0 y posterior. Este servicio analiza un conjunto de documentos, extrae información útil y, a continuación, organiza la información extraída para que las propiedades de esos documentos se puedan devolver de forma eficaz en respuesta a las consultas. Consulte también: catálogo.
