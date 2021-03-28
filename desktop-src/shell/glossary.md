---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
title: Glosario de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360678"
---
# <a name="shell-glossary"></a>Glosario de Shell

## <a name="a"></a>Un

<dl> <dt>

**Asociación**
</dt> <dd>

Asignación de una extensión de nombre de archivo (por ejemplo,. mp3) o un protocolo (por ejemplo, http) a un identificador de programación (ProgID). Esta asignación se almacena en el registro como una configuración por usuario con una reserva por equipo. Las aplicaciones que participan en el sistema programas predeterminados establecen la asignación de Asociación de la extensión de nombre de archivo o protocolo para que apunten a las claves de ProgID que poseen.

</dd> <dt>

**matriz de asociación**
</dt> <dd>

Lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo. Por ejemplo, un archivo. jpg tiene la siguiente matriz de asociación en un sistema Windows predeterminado: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "HKCR \\ SystemFileAssociations \\ Image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**bind**
</dt> <dd>

Para cargar o asociar código a los datos. Por ejemplo, un controlador puede estar asociado a un origen de datos de Shell.

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**nombre canónico**
</dt> <dd>

Nombre único de un recurso. Canonical significa "según las reglas". Vea también: nombre de verbo canónico.

</dd> <dt>

**nombre canónico de verbo**
</dt> <dd>

Nombre independiente del lenguaje que se puede utilizar mediante programación para hacer referencia a un verbo, independientemente de la cadena localizada en la interfaz de usuario. Vea también: nombre canónico, verbo.

</dd> <dt>

**container**
</dt> <dd>

Un tipo de elemento de Shell que puede contener otros elementos. Los elementos de un contenedor se exponen al espacio de nombres del shell mediante un origen de datos de Shell. Entre los ejemplos se incluyen carpetas, unidades, servidores de red y archivos comprimidos con una extensión de nombre de archivo. zip. Vea también: origen de datos de Shell, carpeta, elemento de Shell.

</dd> <dt>

**content**
</dt> <dd>

Texto y propiedades asociados a un elemento de shell o a un origen de contenido que se puede indizar.

</dd> <dt>

**origen de contenido**
</dt> <dd>

Un elemento al que puede tener acceso el indizador. Los orígenes de contenido son direccionables mediante una dirección URL y se proporcionan al indizador mediante un controlador de protocolo. Algunos ejemplos son: archivos y carpetas del sistema de archivos, elementos y carpetas de Microsoft Outlook, registros de base de datos y elementos almacenados de Microsoft SharePoint. Un origen de contenido se puede exponer como elementos de Shell implementando un origen de datos de Shell. Vea también: contenido, elemento de Shell.

</dd> <dt>

**content view (vista de contenido)**
</dt> <dd>

Una vista en el explorador de Windows (ofrecida en Windows 7 y versiones posteriores) que muestra el contenido más relevante de cada elemento de la lista en función de su extensión de nombre de archivo o asociación de clase. La vista de contenido usa una lógica de cambio de tamaño que quita las propiedades cuando se reduce el tamaño de la ventana para asegurarse de que las propiedades más críticas todavía tienen espacio para ser legibles claramente. Vea también: patrón de diseño, clase, Asociación de clase.

</dd> <dt>

**modo de vista de contenido**
</dt> <dd>

Consulte definición de: vista de contenido.

</dd> <dt>

**menú contextual**
</dt> <dd>

Este término se usa a veces para hacer referencia al menú contextual. Vea la definición de: menú contextual.

</dd> <dt>

**controlador del menú contextual**
</dt> <dd>

Este término se usa a veces para hacer referencia al controlador del menú contextual. Consulte definición de: controlador de menú contextual.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**controlador de objetos de datos**
</dt> <dd>

Un controlador que proporciona formatos adicionales del portapapeles para el objeto de datos (IDataObject) de un elemento. Los objetos de datos se utilizan en escenarios de arrastrar y colocar, y de copiar y pegar.

</dd> <dt>

**origen de datos**
</dt> <dd>

Este término se usa a veces para indicar el almacén de datos o el origen de datos de Shell. Vea la definición de: almacén de datos, origen de datos de Shell.

</dd> <dt>

**almacén de datos**
</dt> <dd>

Un repositorio de datos. Un almacén de datos se puede exponer en el modelo de programación de shell como un contenedor mediante un origen de datos de Shell. El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo.

</dd> <dt>

**composición de escritorio**
</dt> <dd>

Característica de Windows Vista que permite dibujar ventanas individuales en superficies fuera de la pantalla en la memoria de vídeo en lugar de que se dibujen directamente en el dispositivo de pantalla principal.

</dd> <dt>

**document**
</dt> <dd>

Un elemento de Shell que contiene texto y para el que se podría implementar la interfaz de IFilter.

</dd> <dt>

**quitar controlador**
</dt> <dd>

Un controlador que permite que un tipo de elemento determinado admita escenarios de arrastrar y colocar, y copiar y pegar.

</dd> <dt>

**destino de colocación**
</dt> <dd>

Objeto de datos que se arrastra y se coloca en un archivo. Vea también: controlador de datos, quitar controlador.

</dd> <dt>

**verbo dinámico**
</dt> <dd>

Verbo que depende del estado de un elemento de shell o del sistema; la apariencia del elemento se basa en el estado y requiere que el código que se está ejecutando determine si el elemento debe aparecer. Vea también: controlador de menú contextual, verbo estático, verbo.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Explorador (comando)**
</dt> <dd>

Objeto que se puede presentar como un botón cerca de la parte superior de la ventana del explorador de Windows que proporciona funcionalidad para los elementos y contenedores de esa ventana. Un origen de datos de Shell proporciona los objetos de comando del explorador de Windows para un elemento contenedor determinado. Los comandos se utilizan a veces como verbos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**Asociación de archivos**
</dt> <dd>

Vea la definición de: Asociación de tipo de archivo.

</dd> <dt>

**formato de archivo**
</dt> <dd>

Formato de los datos almacenados en un archivo que tiene una especificación de formato documentada. Entre los ejemplos se incluyen OLE archivos de ejemplo, OPC, XML, ZIP y otras especificaciones de formato de archivo bien conocidas. Los creadores de tipos de archivo suelen usar un formato de archivo existente como base de un nuevo tipo de archivo. Un formato de archivo puede ser simplemente una definición de la que no se crean instancias como un tipo de archivo.

</dd> <dt>

**controlador de formato de archivo**
</dt> <dd>

Este término es un sinónimo del controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**extensión de nombre de archivo**
</dt> <dd>

El indicador principal de un tipo de archivo para los elementos del sistema de archivos, es la parte del nombre de archivo que sigue al punto final. La extensión de nombre de archivo no puede contener espacios ni caracteres que no sean ASCII y solo se aplica a archivos (no carpetas). Las extensiones de nombre de archivo se comparan utilizando una función de comparación que no distingue entre mayúsculas y minúsculas o la configuración regional. Vea también: formato de archivo, tipo de archivo.

</dd> <dt>

**tipo de archivo**
</dt> <dd>

Un valor de extensión de nombre de archivo determinado, como ". htm" o ". jpg", que define una clase de archivos que son del mismo tipo y tienen un conjunto común de asociaciones. Vea también: Kind, Asociación de tipo de archivo.

</dd> <dt>

**asociación de tipo de archivo**
</dt> <dd>

Para una extensión de nombre de archivo determinada, los elementos de la matriz de asociaciones que definen dónde se pueden registrar los controladores y otros atributos. Vea también: matriz de asociación, tipo de archivo.

</dd> <dt>

**Personalización de tipos de archivo**
</dt> <dd>

Asociación que permite a Shell personalizar el modo en que Shell trata un tipo de archivo. Las personalizaciones de tipo de archivo incluyen: especificar la aplicación utilizada para abrir el archivo al hacer doble clic, agregar comandos al menú contextual de un tipo de archivo, especificar un icono personalizado, especificar un tipo de contenido MIME para asociarlo a un tipo de archivo, especificar un tipo percibido y especificar una o varias aplicaciones asociadas por tipo de archivo con el cuadro de diálogo Abrir con. Vea también: PerceivedType.

</dd> <dt>

**controlador de tipo de archivo**
</dt> <dd>

Un controlador registrado para un tipo de archivo. Vea también: controlador.

</dd> <dt>

**directorio**
</dt> <dd>

Vea la definición de: container.

</dd> <dt>

**PIDL completo**
</dt> <dd>

PIDL que describe de forma única un objeto relativo a la carpeta del escritorio.

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**controlador**
</dt> <dd>

Objeto COM que proporciona funcionalidad para un elemento de Shell. La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos. Por ejemplo, la carpeta sistema de archivos utiliza el sistema de Asociación para buscar los controladores de un tipo de archivo determinado. Vea también: Asociación de archivos, tipo de archivo, personalización de tipos de archivo.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**controlador de iconos**
</dt> <dd>

Un controlador que proporciona la información necesaria para generar y almacenar en caché un icono para un elemento. El almacén de datos del sistema de archivos admite la carga de un controlador de iconos para un elemento basado en el tipo de archivo, lo que permite a ese controlador proporcionar un icono que se usa para todas las instancias de ese tipo de archivo.

</dd> <dt>

**controlador recuadro informativo**
</dt> <dd>

Un controlador que proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre un objeto de interfaz de usuario.

</dd> <dt>

**item**
</dt> <dd>

Vea la definición de: elemento de Shell.

</dd> <dt>

**clase de elemento**
</dt> <dd>

Vea la definición de: tipo de archivo.

</dd> <dt>

**lista de identificadores de elemento**
</dt> <dd>

Secuencia de una o varias estructuras SHITEMID que define de forma única un objeto relativo a algún objeto raíz.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Variante**
</dt> <dd>

Propiedad que proporciona un nombre de clase fácil de usar y que se puede asociar a una lista de propiedades y un modelo de diseño. La clase se presentó en Windows Vista para expresar una noción más descriptiva para el usuario final del tipo de archivo y se definió como una propiedad de cadena de varios valores (valores de cadena canónico), por lo que puede tener un valor de tipo "audio, vídeo" o "vínculo; documento". Algunos nombres de tipo descriptivos ya están asociados a propiedades y patrones de diseño. Por ejemplo, los elementos asociados a Kind. Picture y los elementos asociados a Kind.Document muestran propiedades diferentes incluso cuando están en la misma vista. Cada tipo de elemento puede asociarse a uno de cuatro patrones de diseño únicos que definen el número de propiedades que se muestran para cada elemento y su diseño. Vea también: Asociación de clase, vista de contenido, patrón de diseño.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**patrón de diseño**
</dt> <dd>

Una de varias formas de mostrar propiedades. En Windows 7 y versiones posteriores, cuando se registra un nuevo tipo de archivo, puede usar la vista de contenido para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo. Puede elegir entre cuatro patrones de diseño diferentes: alfa (para los resultados de búsqueda de documentos que contienen fragmentos de código), beta (para los resultados de búsqueda por correo electrónico con fragmentos de código), gamma (similar a alfa pero con un diseño de dos líneas en lugar de cuatro) y Delta (para mostrar muchas propiedades más cortas, como con música e imágenes). Vea también: vista de contenido, clase, Asociación de clase.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**controlador de metadatos**
</dt> <dd>

Este término se usa a veces para indicar el controlador de propiedad. Vea la definición de: controlador de propiedades.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**extensión de espacio de nombres**
</dt> <dd>

Vea la definición de: origen de datos de Shell.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Vinculación e incrustación de objetos de base de datos (OLE DB)**
</dt> <dd>

Conjunto estándar de interfaces que proporciona acceso heterogéneo a distintos orígenes de información ubicados en cualquier lugar, como sistemas de archivos, carpetas de correo electrónico y bases de datos.

</dd> <dt>

**OLE DB**
</dt> <dd>

Vea la definición de: vinculación de objetos e incrustación de base de datos.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**PerceivedType**
</dt> <dd>

Una amplia categoría de tipos de formato de archivo. PerceivedType se presentó en Windows XP y admite un conjunto limitado de tipos de archivo conocidos (entre los que se incluyen imágenes, texto, audio y tipos de archivos comprimidos). Los tipos de archivo, generalmente los tipos de archivo públicos, también pueden tener un tipo percibido. Por ejemplo, los archivos de imagen Types. bmp,. png,. jpg y. gif también son del tipo percibido, Image. En la capa de programación, PerceivedType se expresa como un entero. Dado que hay código que utiliza Kind y PerceivedType, los propietarios de formato de archivo deben registrar ambos. Por ejemplo, "reproducir todo" depende de PerceivedType. Vea también: tipo de archivo.

</dd> <dt>

**controlador de vista previa**
</dt> <dd>

Un controlador que genera rápidamente una vista simplificada de solo lectura del elemento de Shell que se va a mostrar en el panel de vista previa del explorador de Windows.

</dd> <dt>

**controlador de propiedades**
</dt> <dd>

Un controlador que traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que puede tener acceso el explorador de Windows, Windows Search y otras aplicaciones. Después, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer las propiedades del archivo. Los datos traducidos incluyen vista de detalles, recuadros informativos, panel de detalles, páginas de propiedades, etc. Cada controlador de propiedad está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Vea también: sistema de propiedades.

</dd> <dt>

**controlador de la hoja de propiedades**
</dt> <dd>

Un controlador que se usa para crear hojas de propiedades personalizadas con imágenes de interfaz de usuario y controles que permiten la interacción personalizada con un tipo de archivo.

</dd> <dt>

**sistema de propiedades**
</dt> <dd>

Sistema de lectura y escritura extensible de definiciones de datos que usa propiedades implementadas como pares de nombre y valor. Vea también: controlador de propiedades, elemento de Shell.

</dd> <dt>

**valor de propiedad**
</dt> <dd>

Valor asociado a un nombre de propiedad para un elemento de Shell. Por ejemplo, "autor", "tamaño" y "fecha de toma" son propiedades. Los valores de propiedad se expresan como una estructura PROPVARIANT.

</dd> <dt>

**controlador de protocolo**
</dt> <dd>

Un controlador que tiene acceso a los orígenes de contenido y proporciona un objeto IUrlAccessor para el protocolo y la dirección URL especificados. Los controladores de protocolo amplían la funcionalidad de búsqueda de Windows y pueden proporcionar notificaciones de cambio a los indizadores. Se requieren controladores de protocolo diferentes para indizar tipos específicos de almacenes de datos. Para proporcionar una experiencia de usuario razonable, también debe proporcionar un origen de datos de Shell para el almacén de datos, además de implementar el controlador de protocolo. El controlador de protocolo expone los elementos del almacén de datos al indexador, mientras que el origen de datos del shell expone los elementos del almacén de datos al shell.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**PIDL relativo**
</dt> <dd>

PIDL que es relativo a algún objeto raíz en el espacio de nombres del shell que no sea la carpeta del escritorio. Esta suele ser la carpeta principal del elemento.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Origen de datos de Shell**
</dt> <dd>

Componente que se usa para extender el espacio de nombres del shell y exponer los elementos de un almacén de datos. En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell. Vea también: contenedor, controlador, elemento de Shell.

</dd> <dt>

**Extensión de shell**
</dt> <dd>

Este término se usa a veces para indicar el controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**Controlador de extensión de Shell**
</dt> <dd>

Este término se usa a veces para indicar el controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**Controlador de Shell**
</dt> <dd>

Este término se usa a veces para indicar el controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**Elemento de Shell**
</dt> <dd>

Un único fragmento de contenido. Algunos elementos de Shell son orígenes de contenido y otros no. Una carpeta es un origen de contenido, por ejemplo, pero no un archivo. jpg. Los controladores de tipo de archivo exponen elementos de Shell. En algunos contextos, "Item" se usa para distinguir los contenedores de los no contenedores. Vea también: contenedor, origen de contenido, controlador de tipo de archivo.

</dd> <dt>

**Extensión de espacio de nombres Shell**
</dt> <dd>

Este término se usa a veces para hacer referencia al origen de datos de Shell. Vea la definición de: origen de datos de Shell.

</dd> <dt>

**menú contextual**
</dt> <dd>

Interfaz de usuario que se utiliza para presentar una colección de verbos asociados a un elemento de la interfaz de usuario, como un archivo o una carpeta.

</dd> <dt>

**Controlador del menú contextual**
</dt> <dd>

Un controlador que agrega verbos para un elemento o elementos. Estos verbos se muestran normalmente en un menú contextual. Vea también: menú contextual.

</dd> <dt>

**PIDL simple**
</dt> <dd>

PIDL que se analiza sin comprobación de disco.

</dd> <dt>

**verbo estático**
</dt> <dd>

Un verbo que se aplica a un elemento de Shell sin necesidad de inspeccionar el estado actual de un elemento o sistema. Un verbo estático se basa en un registro estático de los elementos asociados de un elemento y no cambia.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**controlador de miniaturas**
</dt> <dd>

Un controlador que proporciona una imagen estática para representar un elemento de Shell.

</dd> <dt>

**proveedor de miniaturas**
</dt> <dd>

Este término se usa a veces para indicar el controlador de miniaturas. Vea la definición de: controlador de miniaturas.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**nombre descriptivo del tipo de usuario**
</dt> <dd>

Vea la definición de: Kind.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**Verbo**
</dt> <dd>

Una acción individual a la que puede llamar un elemento de Shell. Entre los ejemplos se incluyen abrir e imprimir. Los verbos se conocen a veces como comandos o tareas. Vea también: verbo dinámico, controlador de menú contextual, verbo estático.

</dd> <dt>

**controlador de verbo**
</dt> <dd>

Este término se usa a veces para hacer referencia al controlador del menú contextual. Consulte definición de: controlador de menú contextual.

</dd> </dl>

 

 



