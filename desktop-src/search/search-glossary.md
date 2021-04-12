---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Glosario de búsqueda de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac0620f4c85c43aac6d41300e16e3e5a8dd037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153937"
---
# <a name="windows-search-glossary"></a>Glosario de búsqueda de Windows

## <a name=""></a>\#

**archivo. OSD**

Archivo de descriptor de OpenSearch.

**archivo. osdx**

Un archivo XML de descripción de OpenSearch que describe las conexiones de servidor disponibles y los formatos de resultado para un origen de datos específico basado en Web. Se usa para interactuar con el shell de Windows. Vea también: descriptor de OpenSearch.

## <a name="a"></a>A

**Sintaxis de consulta avanzada (AQS)**

La sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda. AQS es principalmente orientada al usuario y puede ser utilizada por los usuarios para compilar consultas AQS, pero también se puede usar mediante programación. Vea también: sintaxis de consulta natural (NQS).

**AQS**

Consulte la definición de: sintaxis de consulta avanzada (AQS).

**Asociación**

Asignación de una extensión de nombre de archivo (por ejemplo,. mp3) o un protocolo (por ejemplo, http) a un identificador de programación (ProgID). Esta asignación se almacena en el registro como una configuración por usuario con una reserva por equipo. Las aplicaciones que participan en el sistema programas predeterminados establecen la asignación de Asociación de la extensión de nombre de archivo o protocolo para que apunten a las claves de ProgID que poseen.

**matriz de asociación**

Lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo. Por ejemplo, un archivo. jpg tiene la siguiente matriz de asociación en un sistema Windows predeterminado: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "HKCR \\ SystemFileAssociations \\ Image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Un esquema XML que se usa para las fuentes web y la distribución de contenido, desarrollado como alternativa a la distribución realmente simple (RSS). El formato de redifusión de Atom se publicó como un estándar propuesto por IETF en RFC 4287.

## <a name="b"></a>B

**bind**

Para cargar o asociar código a los datos. Por ejemplo, un controlador puede estar asociado a un origen de datos de Shell.

**enlace**

Una solicitud en una consulta de búsqueda para una columna en un conjunto de filas devuelto. El enlace especifica una propiedad que se va a incluir en los resultados de la búsqueda.

**bookmark**

Indicador que identifica de forma única una fila dentro de un conjunto de filas.

## <a name="c"></a>C

**nombre canónico**

Nombre único de un recurso. Canonical significa "según las reglas". Vea también: nombre de verbo canónico.

**nombre canónico de verbo**

Nombre independiente del lenguaje que se puede utilizar mediante programación para hacer referencia a un verbo, independientemente de la cadena localizada en la interfaz de usuario. Vea también: nombre canónico, verbo.

**catalog**

La unidad de mayor nivel de organización en Windows Search. Un catálogo representa un conjunto de documentos indizados que se pueden consultar. Un catálogo se compone de una tabla de propiedades con el texto o el valor y la ubicación correspondiente almacenada en las columnas de la tabla. Cada fila de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada columna de la tabla corresponde a una propiedad. Vea también: índice, servicio búsqueda de Windows.

**category**

Agrupación jerárquica de filas. Por ejemplo, el resultado de una consulta que contiene columnas de autor y título se puede clasificar en función del autor. En este ejemplo, cada grupo de filas que contiene el mismo valor para Author constituye una categoría.

**Capítulo**

Colección de filas dentro de un conjunto de filas. Vea también: Catálogo, categoría.

**column**

Contenedor de un solo tipo de información de una fila. Las columnas se asignan a los nombres de propiedad y especifican las propiedades que se usan para los elementos de árbol de comandos de la consulta de búsqueda. Vea también: categoría.

**árbol de comandos**

Combinación de restricciones, categorías y criterios de ordenación que se especifican para la consulta de búsqueda. Vea también: categoría.

**container**

Un tipo de elemento de Shell que puede contener otros elementos. Los elementos de un contenedor se exponen al espacio de nombres del shell mediante un origen de datos de Shell. Entre los ejemplos se incluyen carpetas, unidades, servidores de red y archivos comprimidos con una extensión de nombre de archivo. zip. Vea también: origen de datos de Shell, carpeta, elemento de Shell.

**content**

Texto y propiedades asociados a un elemento de shell o a un origen de contenido que se puede indizar.

**origen de contenido**

Un elemento al que puede tener acceso el indizador. Los orígenes de contenido son direccionables mediante una dirección URL y se proporcionan al indizador mediante un controlador de protocolo. Algunos ejemplos son: archivos y carpetas del sistema de archivos, elementos y carpetas de Microsoft Outlook, registros de base de datos y elementos almacenados de Microsoft SharePoint. Un origen de contenido se puede exponer como elementos de Shell implementando un origen de datos de Shell. Vea también: contenido, elemento de Shell.

**content view (vista de contenido)**

Una vista en el explorador de Windows (ofrecida en Windows 7 y versiones posteriores) que muestra el contenido más relevante de cada elemento de la lista en función de su extensión de nombre de archivo o asociación de clase. La vista de contenido usa una lógica de cambio de tamaño que quita las propiedades cuando se reduce el tamaño de la ventana para asegurarse de que las propiedades más críticas todavía tienen espacio para ser legibles claramente. Vea también: patrón de diseño, clase, Asociación de clase.

**modo de vista de contenido**

Consulte definición de: vista de contenido.

**menú contextual**

Este término se usa a veces para hacer referencia al menú contextual. Vea la definición de: menú contextual.

**controlador del menú contextual**

Este término se usa a veces para hacer referencia al controlador del menú contextual. Consulte definición de: controlador de menú contextual.

**rastreo**

Para recorrer en iteración un ámbito de rastreo, identifique los orígenes de contenido que requieran indización o reindización.

**ámbito de rastreo**

Colección de almacenes de datos (identificables por dirección URL) que representa el contenido que el indexador rastrea e indexa.

**cursor**

En el contexto del índice local, un cursor es un indicador para trabajar con una fila o un pequeño bloque de filas a la vez en un conjunto de datos devueltos en un conjunto de resultados. Una vez que el cursor se coloca en una fila, se pueden realizar operaciones en esa fila o en un bloque de filas a partir de esa posición.

## <a name="d"></a>D

**Administración de datos, exploración y minería de datos**

Vea la definición de: extensiones de minería de datos (DMX).

**controlador de objetos de datos**

Un controlador que proporciona formatos adicionales del portapapeles para el objeto de datos (IDataObject) de un elemento. Los objetos de datos se utilizan en escenarios de arrastrar y colocar, y de copiar y pegar.

**origen de datos**

Este término se usa a veces para indicar el almacén de datos o el origen de datos de Shell. Vea la definición de: almacén de datos, origen de datos de Shell.

**almacén de datos**

Un repositorio de datos. Un almacén de datos se puede exponer en el modelo de programación de shell como un contenedor mediante un origen de datos de Shell. El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo.

**Extensiones de minería de datos (DMX)**

Lenguaje de consulta que se utiliza para crear y manipular la minería de datos. Las plantillas administrativas para Windows 7, Windows Search y el explorador de Windows son archivos. ADMX y se basan en la tecnología DMX. Las siguientes plantillas se pueden personalizar a través de directiva de grupo: Search. ADMX, Explorer. ADMX y WindowsExplorer. ADMX.

**DMX**

Vea la definición de: extensiones de minería de datos.

**document**

Un elemento de Shell que contiene texto y para el que se podría implementar la interfaz de IFilter.

**quitar controlador**

Un controlador que permite que un tipo de elemento determinado admita escenarios de arrastrar y colocar, y copiar y pegar.

**destino de colocación**

Objeto de datos que se arrastra y se coloca en un archivo. Vea también: controlador de datos, quitar controlador.

**verbo dinámico**

Verbo que depende del estado de un elemento de shell o del sistema; la apariencia del elemento se basa en el estado y requiere que el código que se está ejecutando determine si el elemento debe aparecer. Vea también: controlador de menú contextual, verbo estático, verbo.

## <a name="e"></a>E

**Explorador (comando)**

Objeto que se puede presentar como un botón cerca de la parte superior de la ventana del explorador de Windows que proporciona funcionalidad para los elementos y contenedores de esa ventana. Un origen de datos de Shell proporciona los objetos de comando del explorador de Windows para un elemento contenedor determinado. Los comandos se utilizan a veces como verbos.

## <a name="f"></a>F

**búsqueda federada**

Modelo de extensibilidad que permite buscar almacenes de datos y representar los resultados como elementos de Shell en el explorador de Windows. Vea también: proveedor de búsquedas federadas, conector de búsqueda, descriptor de OpenSearch, estándar de OpenSearch.

**conector de búsqueda federado**

Consulte la definición de: conector de búsqueda.

**proveedor de búsquedas federado**

Un servicio Web, implementado por un almacén de datos, que admite los protocolos usados por Windows 7 para que Windows 7 y versiones posteriores puedan buscar ese almacén de datos de forma remota. Vea también: descriptor de OpenSearch, estándar de OpenSearch.

**Asociación de archivos**

Vea la definición de: Asociación de tipo de archivo.

**formato de archivo**

Formato de los datos almacenados en un archivo que tiene una especificación de formato documentada. Entre los ejemplos se incluyen OLE archivos de ejemplo, OPC, XML, ZIP y otras especificaciones de formato de archivo bien conocidas. Los creadores de tipos de archivo suelen usar un formato de archivo existente como base de un nuevo tipo de archivo. Un formato de archivo puede ser simplemente una definición de la que no se crean instancias como un tipo de archivo.

**controlador de formato de archivo**

Este término es un sinónimo del controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**extensión de nombre de archivo**

Vea la definición de: extensión de nombre de archivo.

**extensión de nombre de archivo**

El indicador principal de un tipo de archivo para los elementos del sistema de archivos, es la parte del nombre de archivo que sigue al punto final. La extensión de nombre de archivo no puede contener espacios ni caracteres que no sean ASCII y solo se aplica a archivos (no carpetas). Las extensiones de nombre de archivo se comparan utilizando una función de comparación que no distingue entre mayúsculas y minúsculas o la configuración regional. Vea también: formato de archivo, tipo de archivo.

**tipo de archivo**

Un valor de extensión de nombre de archivo determinado, como ". htm" o ". jpg", que define una clase de archivos que son del mismo tipo y tienen un conjunto común de asociaciones. Vea también: Kind, Asociación de tipo de archivo.

**asociación de tipo de archivo**

Para una extensión de nombre de archivo determinada, los elementos de la matriz de asociaciones que definen dónde se pueden registrar los controladores y otros atributos. Vea también: matriz de asociación, tipo de archivo.

**Personalización de tipos de archivo**

Asociación que permite a Shell personalizar el modo en que Shell trata un tipo de archivo. Las personalizaciones de tipo de archivo incluyen: especificar la aplicación utilizada para abrir el archivo al hacer doble clic, agregar comandos al menú contextual de un tipo de archivo, especificar un icono personalizado, especificar un tipo de contenido MIME para asociarlo a un tipo de archivo, especificar un tipo percibido y especificar una o varias aplicaciones asociadas por tipo de archivo con el cuadro de diálogo Abrir con. Vea también: PerceivedType.

**controlador de tipo de archivo**

Un controlador registrado para un tipo de archivo. Vea también: controlador.

**filter**

Implementación de la interfaz IFilter. Abre los archivos de un tipo de archivo determinado y filtra las propiedades y fragmentos de texto del indexador. Los filtros se asocian a los tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLSID). Aunque un filtro puede controlar varios tipos de archivo, cada tipo de archivo funciona con un solo filtro.

**directorio**

Vea la definición de: container.

## <a name="h"></a>H

**controlador**

Objeto COM que proporciona funcionalidad para un elemento de Shell. La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos. Por ejemplo, la carpeta sistema de archivos utiliza el sistema de Asociación para buscar los controladores de un tipo de archivo determinado. Vea también: Asociación de archivos, tipo de archivo, personalización de tipos de archivo.

## <a name="i"></a>I

**controlador de iconos**

Un controlador que proporciona la información necesaria para generar y almacenar en caché un icono para un elemento. El almacén de datos del sistema de archivos admite la carga de un controlador de iconos para un elemento basado en el tipo de archivo, lo que permite a ese controlador proporcionar un icono que se usa para todas las instancias de ese tipo de archivo.

**índice**

n. Catálogo que almacena el contenido y las propiedades de los elementos de Shell para habilitar las búsquedas rápidas. Vea también: Catálogo, indexador, indexación, índice invertido. v. Para obtener acceso a los orígenes de contenido, filtre los orígenes de contenido y propiedades e inserte los valores extraídos en el índice (para texto) y el almacén de propiedades de búsqueda de Windows (para propiedades). Vea también: origen de contenido, índice, indexador e índice invertido.

**indexador**

Aplicación que realiza la indización o la indización de coordenadas. Vea también: índice, indexación, índice invertido.

**controlador recuadro informativo**

Un controlador que proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre un objeto de interfaz de usuario.

**Índice invertido**

Estructura persistente que contiene el contenido extraído de los archivos por la búsqueda de Windows. El texto se organiza en un índice que se asigna desde una palabra de una propiedad a una lista de documentos y ubicaciones dentro de un documento que contiene esa palabra. Por lo tanto, un índice invertido es el inverso del proceso de extracción del texto y las propiedades del documento y los coloca en el indizador. Vea también: índice, indexador e indexación.

**item**

Vea la definición de: elemento de Shell.

**clase de elemento**

Vea la definición de: tipo de archivo.

## <a name="k"></a>K

**Variante**

Propiedad que proporciona un nombre de clase fácil de usar y que se puede asociar a una lista de propiedades y un modelo de diseño. La clase se presentó en Windows Vista para expresar una noción más descriptiva para el usuario final del tipo de archivo y se definió como una propiedad de cadena de varios valores (valores de cadena canónico), por lo que puede tener un valor de tipo "audio, vídeo" o "vínculo; documento". Algunos nombres de tipo descriptivos ya están asociados a propiedades y patrones de diseño. Por ejemplo, los elementos asociados a Kind. Picture y los elementos asociados a Kind.Document muestran propiedades diferentes incluso cuando están en la misma vista. Cada tipo de elemento puede asociarse a uno de cuatro patrones de diseño únicos que definen el número de propiedades que se muestran para cada elemento y su diseño. Vea también: Asociación de clase, vista de contenido, patrón de diseño.

**Asociación de clase**

Propiedad del sistema de propiedades, denominada System. Kind, que determina qué plantillas de experiencia de usuario se muestran para un archivo. Esta propiedad también proporciona un nombre descriptivo para el tipo del elemento y se vincula a la extensión de nombre de archivo. Vea también: Kind.

## <a name="l"></a>L

**patrón de diseño**

Una de varias formas de mostrar propiedades. En Windows 7 y versiones posteriores, cuando se registra un nuevo tipo de archivo, puede usar la vista de contenido para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo. Puede elegir entre cuatro patrones de diseño diferentes: alfa (para los resultados de búsqueda de documentos que contienen fragmentos de código), beta (para los resultados de búsqueda por correo electrónico con fragmentos de código), gamma (similar a alfa pero con un diseño de dos líneas en lugar de cuatro) y Delta (para mostrar muchas propiedades más cortas, como con música e imágenes). Vea también: vista de contenido, clase, Asociación de clase.

## <a name="m"></a>M

**controlador de metadatos**

Este término se usa a veces para indicar el controlador de propiedad. Vea la definición de: controlador de propiedades.

## <a name="n"></a>N

**extensión de espacio de nombres**

Vea la definición de: origen de datos de Shell.

**recorrido del espacio de nombres**

Proceso auxiliar que atraviesa el espacio de nombres de un contenedor o un conjunto de contenedores, detectando cada elemento y, posiblemente, haciendo algo con cada uno. La interfaz INamespaceWalk se puede usar para recorrer cualquier parte del espacio de nombres del explorador de Windows o para detectar los elementos a los que hace referencia un objeto de datos o una vista. Los verbos de contenedor (por ejemplo, "Play" en los contenedores de artistas) recorren el espacio de nombres y detectan los elementos.

**consulta en lenguaje natural**

Vea la definición de: sintaxis de consulta natural (NQS).

**Sintaxis de consulta natural (NQS)**

Una sintaxis de consulta que es más relajada que AQS y es más similar a la lengua humana. La búsqueda de Windows puede usar NQS para consultar el índice si se selecciona NQS en lugar del valor predeterminado, AQS. Vea también: sintaxis de consulta avanzada (AQS).

**palabra irrelevante**

Una palabra omitida por búsqueda de Windows cuando está presente en las restricciones especificadas para la consulta de búsqueda, porque tiene un pequeño valor discriminado. Entre los ejemplos se incluyen "and" y "The".

**NQS**

Vea la definición de: sintaxis de consulta natural (NQS).

## <a name="o"></a>O

**Vinculación e incrustación de objetos de base de datos (OLE DB)**

Conjunto estándar de interfaces que proporciona acceso heterogéneo a distintos orígenes de información ubicados en cualquier lugar, como sistemas de archivos, carpetas de correo electrónico y bases de datos.

**OLE DB**

Vea la definición de: vinculación de objetos e incrustación de base de datos.

**Descriptor de OpenSearch**

Archivo XML que describe las conexiones de servidor disponibles y los formatos de resultado para un origen de datos específico basado en Web. Este archivo contiene una o varias plantillas de URL y usa una extensión de nombre de archivo. osdx al interactuar con el shell de Windows. Una descripción de OpenSearch a veces se conoce como conector de búsqueda, aunque solo es la parte de la descripción de un conector. Vea también: conector de búsqueda.

**Estándar de OpenSearch**

Colección de formatos y protocolos simples usados para compartir los resultados de la búsqueda. Para obtener más información, vea el sitio web de OpenSearch ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Una amplia categoría de tipos de formato de archivo. PerceivedType se presentó en Windows XP y admite un conjunto limitado de tipos de archivo conocidos (entre los que se incluyen imágenes, texto, audio y tipos de archivos comprimidos). Los tipos de archivo, generalmente los tipos de archivo públicos, también pueden tener un tipo percibido. Por ejemplo, los archivos de imagen Types. bmp,. png,. jpg y. gif también son del tipo percibido, Image. En la capa de programación, PerceivedType se expresa como un entero. Dado que hay código que utiliza Kind y PerceivedType, los propietarios de formato de archivo deben registrar ambos. Por ejemplo, "reproducir todo" depende de PerceivedType. Vea también: tipo de archivo.

**controlador de vista previa**

Un controlador que genera rápidamente una vista simplificada de solo lectura del elemento de Shell que se va a mostrar en el panel de vista previa del explorador de Windows.

**vista previa**

Este término se usa a veces para indicar el controlador de vista previa. Vea la definición de: controlador de vista previa.

**controlador de propiedades**

Un controlador que traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que puede tener acceso el explorador de Windows, Windows Search y otras aplicaciones. Después, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer las propiedades del archivo. Los datos traducidos incluyen vista de detalles, recuadros informativos, panel de detalles, páginas de propiedades, etc. Cada controlador de propiedad está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Vea también: sistema de propiedades.

**controlador de la hoja de propiedades**

Un controlador que se usa para crear hojas de propiedades personalizadas con imágenes de interfaz de usuario y controles que permiten la interacción personalizada con un tipo de archivo.

**sistema de propiedades**

Sistema de lectura y escritura extensible de definiciones de datos que usa propiedades implementadas como pares de nombre y valor. Vea también: controlador de propiedades, elemento de Shell.

**valor de propiedad**

Valor asociado a un nombre de propiedad para un elemento de Shell. Por ejemplo, "autor", "tamaño" y "fecha de toma" son propiedades. Los valores de propiedad se expresan como una estructura PROPVARIANT.

**controlador de protocolo**

Un controlador que tiene acceso a los orígenes de contenido y proporciona un objeto IUrlAccessor para el protocolo y la dirección URL especificados. Los controladores de protocolo amplían la funcionalidad de búsqueda de Windows y pueden proporcionar notificaciones de cambio a los indizadores. Se requieren controladores de protocolo diferentes para indizar tipos específicos de almacenes de datos. Para proporcionar una experiencia de usuario razonable, también debe proporcionar un origen de datos de Shell para el almacén de datos, además de implementar el controlador de protocolo. El controlador de protocolo expone los elementos del almacén de datos al indexador, mientras que el origen de datos del shell expone los elementos del almacén de datos al shell.

## <a name="r"></a>R

**prohibición**

Condición que un archivo debe cumplir para que se incluya en los resultados de búsqueda devueltos por Windows Search.

**row**

Columnas que contienen los valores de propiedad que describen un solo resultado del conjunto de objetos que coincidían con las restricciones especificadas en una consulta de búsqueda.

**MultiRow**

Conjunto de filas devueltas en los resultados de la búsqueda.

## <a name="s"></a>S

**conector de búsqueda**

Archivo XML que contiene información acerca de un almacén de datos. Los conectores de búsqueda se implementan para la búsqueda federada.

**buscar consumidor**

Componente o aplicación que consulta el índice.

**buscar Federación**

Vea la definición de: proveedor de búsquedas federado.

**proveedor de búsquedas**

Componente o aplicación que proporciona datos a la búsqueda de Windows.

**ámbito de búsqueda**

Este término se usa a veces para indicar el ámbito de rastreo. Vea la definición de: ámbito de rastreo.

**Origen de datos de Shell**

Componente que se usa para extender el espacio de nombres del shell y exponer los elementos de un almacén de datos. En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell. Vea también: contenedor, controlador, elemento de Shell.

**Extensión de shell**

Este término se usa a veces para indicar el controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**Controlador de extensión de Shell**

Este término se usa a veces para indicar el controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**Controlador de Shell**

Este término se usa a veces para indicar el controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

**Elemento de Shell**

Un único fragmento de contenido. Algunos elementos de Shell son orígenes de contenido y otros no. Una carpeta es un origen de contenido, por ejemplo, pero no un archivo. jpg. Los controladores de tipo de archivo exponen elementos de Shell. En algunos contextos, "Item" se usa para distinguir los contenedores de los no contenedores. Vea también: contenedor, origen de contenido, controlador de tipo de archivo.

**Extensión de espacio de nombres Shell**

Este término se usa a veces para hacer referencia al origen de datos de Shell. Vea la definición de: origen de datos de Shell.

**menú contextual**

Interfaz de usuario que se utiliza para presentar una colección de verbos asociados a un elemento de la interfaz de usuario, como un archivo o una carpeta.

**Controlador del menú contextual**

Un controlador que agrega verbos para un elemento o elementos. Estos verbos se muestran normalmente en un menú contextual. Vea también: menú contextual.

**verbo estático**

Un verbo que se aplica a un elemento de Shell sin necesidad de inspeccionar el estado actual de un elemento o sistema. Un verbo estático se basa en un registro estático de los elementos asociados de un elemento y no cambia.

## <a name="t"></a>T

**controlador de miniaturas**

Un controlador que proporciona una imagen estática para representar un elemento de Shell.

**proveedor de miniaturas**

Este término se usa a veces para indicar el controlador de miniaturas. Vea la definición de: controlador de miniaturas.

## <a name="u"></a>U

**URL template**

Cadena de conexión basada en la dirección URL que se utiliza para consultar los resultados de una búsqueda en un servidor Web. La plantilla es similar a una dirección URL, pero contiene varios valores de marcador de posición (como {searchTerms}) que el cliente debe reemplazar por datos sobre los resultados que desea recuperar. La definición de las plantillas de dirección URL es clave para implementar la búsqueda federada y los estándares de OpenSearch.

**nombre descriptivo del tipo de usuario**

Vea la definición de: Kind.

## <a name="v"></a>V

**Verbo**

Una acción individual a la que puede llamar un elemento de Shell. Entre los ejemplos se incluyen abrir e imprimir. Los verbos se conocen a veces como comandos o tareas. Vea también: verbo dinámico, controlador de menú contextual, verbo estático.

**controlador de verbo**

Este término se usa a veces para hacer referencia al controlador del menú contextual. Consulte definición de: controlador de menú contextual.

## <a name="w"></a>W

**analice**

Vea la definición de: recorrido del espacio de nombres.

**Windows Search**

Consulte la definición de: servicio Windows Search.

**Almacén de propiedades de Windows Search**

La memoria caché de los valores de propiedad utilizados en la implementación del servicio Windows Search. Estos valores de propiedad se pueden consultar mediante programación con el proveedor de OLE DB de Windows Search. El almacén de propiedades de búsqueda de Windows recopila y almacena propiedades emitidas por controladores de filtro o controladores de propiedades cuando se indiza un elemento como un documento de Word. Este almacén se descarta y se vuelve a generar cuando se vuelve a generar el índice.

**Servicio búsqueda de Windows**

Hace referencia a Windows Search 3,0 y versiones posteriores. Este servicio analiza un conjunto de documentos, extrae información útil y, a continuación, organiza la información extraída para que las propiedades de esos documentos puedan devolverse de forma eficaz en respuesta a las consultas. Vea también: Catálogo.
