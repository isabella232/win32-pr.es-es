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
ms.openlocfilehash: 9ef488a715532372592606f31dcfe1925a93dc29de78a54c869db83c21433c08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049868"
---
# <a name="shell-glossary"></a>Glosario de Shell

## <a name="a"></a>A

<dl> <dt>

**Asociación**
</dt> <dd>

Asignación de una extensión de nombre de archivo (por ejemplo, .mp3) o protocolo (por ejemplo, http) a un identificador de programación (ProgID). Esta asignación se almacena en el Registro como una configuración por usuario con una reserva por equipo. Las aplicaciones que participan en el sistema programas predeterminados establecen la asignación de asociación para que la extensión o el protocolo de nombre de archivo apunten a las claves progID que poseen.

</dd> <dt>

**matriz de asociación**
</dt> <dd>

Lista ordenada de ubicaciones del Registro usadas para almacenar información sobre un tipo de elemento, incluidos controladores, verbos y otros atributos, como el icono y el nombre para mostrar del tipo. Por ejemplo, un archivo .jpg tiene la siguiente matriz de asociación en un sistema Windows predeterminado: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\.jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**bind**
</dt> <dd>

Para cargar o asociar código a datos. Por ejemplo, un controlador puede estar asociado a un origen de datos de Shell.

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**nombre canónico**
</dt> <dd>

Nombre único de un recurso. Canonical significa "según las reglas". Vea también: nombre de verbo canónico.

</dd> <dt>

**nombre del verbo canónico**
</dt> <dd>

Nombre independiente del idioma que se puede usar mediante programación para hacer referencia a un verbo, independientemente de la cadena localizada en la interfaz de usuario. Vea también: nombre canónico, verbo.

</dd> <dt>

**container**
</dt> <dd>

Tipo de elemento de Shell que puede contener otros elementos. Los elementos de un contenedor se exponen al espacio de nombres de Shell mediante un origen de datos de Shell. Algunos ejemplos son carpetas, unidades, servidores de red y archivos comprimidos con una .zip de nombre de archivo. Consulte también: Origen de datos de Shell, carpeta, elemento de Shell.

</dd> <dt>

**content**
</dt> <dd>

Texto y propiedades asociadas a un elemento de Shell o un origen de contenido que se puede indexar.

</dd> <dt>

**origen de contenido**
</dt> <dd>

Elemento al que puede tener acceso el indexador. Los orígenes de contenido son direccionables mediante una dirección URL y un controlador de protocolo proporciona al indexador. Algunos ejemplos son: archivos y carpetas del sistema de archivos, Outlook y carpetas de Microsoft, registros de base de datos y elementos almacenados SharePoint Microsoft. Un origen de contenido se puede exponer como elementos de Shell implementando un origen de datos de Shell. Vea también: contenido, elemento de Shell.

</dd> <dt>

**content view (vista de contenido)**
</dt> <dd>

Vista en Windows Explorer (que se ofrece en Windows 7 y versiones posteriores) que muestra el contenido más relevante para cada elemento de la lista en función de su extensión de nombre de archivo o asociación kind. La vista de contenido usa una lógica de cambiar el tamaño que quita las propiedades cuando el tamaño de la ventana disminuye para asegurarse de que las propiedades más críticas todavía tienen espacio para ser claramente legibles. Vea también: patrón de diseño, tipo, asociación de tipo.

</dd> <dt>

**modo de vista de contenido**
</dt> <dd>

Vea la definición de: vista de contenido.

</dd> <dt>

**menú contextual**
</dt> <dd>

Este término se usa a veces para significar menú contextual. Vea la definición de: menú contextual.

</dd> <dt>

**controlador de menú contextual**
</dt> <dd>

Este término se usa a veces para significar controlador de menú contextual. Vea definición de: controlador de menú contextual.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**controlador de objetos de datos**
</dt> <dd>

Controlador que proporciona formatos de Portapapeles adicionales para el objeto de datos (IDataObject) de un elemento. Los objetos de datos se usan en escenarios de arrastrar y colocar y copiar y pegar.

</dd> <dt>

**origen de datos**
</dt> <dd>

Este término se usa a veces para significar el almacén de datos o el origen de datos de Shell. Consulte la definición de: almacén de datos, origen de datos de Shell.

</dd> <dt>

**almacén de datos**
</dt> <dd>

Un repositorio de datos. Un almacén de datos se puede exponer al modelo de programación de Shell como un contenedor mediante un origen de datos de Shell. Los elementos de un almacén de datos se pueden indexar mediante el Windows Search mediante un controlador de protocolo.

</dd> <dt>

**composición de escritorio**
</dt> <dd>

Una Windows Vista que permite dibujar ventanas individuales en superficies fuera de la pantalla en la memoria de vídeo en lugar de dibujarse directamente en el dispositivo de pantalla principal.

</dd> <dt>

**document**
</dt> <dd>

Elemento de Shell que contiene texto y para el que se podría implementar la interfaz IFilter.

</dd> <dt>

**controlador drop**
</dt> <dd>

Controlador que permite que un tipo de elemento determinado admita escenarios de arrastrar y colocar y copiar y pegar.

</dd> <dt>

**destino de colocación**
</dt> <dd>

Objeto de datos que se arrastra y se descarta en un archivo. Vea también: controlador de datos, controlador de colocación.

</dd> <dt>

**verbo dinámico**
</dt> <dd>

Verbo que depende del estado de un elemento de Shell o del sistema; la apariencia del elemento se basa en el estado y requiere que el código en ejecución determine si el elemento debe aparecer. Vea también: controlador de menú contextual, verbo estático, verbo.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Comando del explorador**
</dt> <dd>

Objeto que se puede presentar como un botón cerca de la parte superior de la ventana explorador de Windows que proporciona funcionalidad para los elementos y contenedores de esa ventana. Un origen de datos de Shell proporciona los objetos Windows explorer para un elemento de contenedor determinado. Los comandos se usan a veces como verbos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**asociación de archivos**
</dt> <dd>

Vea la definición de: asociación de tipo de archivo.

</dd> <dt>

**formato de archivo**
</dt> <dd>

Formato de los datos almacenados en un archivo que tiene una especificación de formato documentada. Algunos ejemplos son OLE DocFile, OPC, XML, ZIP y otras especificaciones conocidas de formato de archivo. Los creadores de tipos de archivo suelen usar un formato de archivo existente como base de un nuevo tipo de archivo. Un formato de archivo puede ser simplemente una definición a la que no se crea una instancia como un tipo de archivo.

</dd> <dt>

**controlador de formato de archivo**
</dt> <dd>

Este término es un sinónimo del controlador de tipos de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**extensión de nombre de archivo**
</dt> <dd>

El indicador principal de un tipo de archivo para los elementos del sistema de archivos es la parte del nombre de archivo que sigue al punto final. La extensión de nombre de archivo no puede contener espacios ni caracteres no ASCII y solo se aplica a archivos (no carpetas). Las extensiones de nombre de archivo se comparan mediante una función de comparación que no distingue mayúsculas de minúsculas ni configuración regional. Vea también: formato de archivo, tipo de archivo.

</dd> <dt>

**tipo de archivo**
</dt> <dd>

Un valor de extensión de nombre de archivo determinado, como ".htm" o ".jpg", que define una clase de archivos que son del mismo tipo y tienen un conjunto común de asociaciones. Vea también: Tipo, asociación de tipo de archivo.

</dd> <dt>

**asociación de tipo de archivo**
</dt> <dd>

Para una extensión de nombre de archivo determinada, los elementos de la matriz de asociación que definen dónde se pueden registrar los controladores y otros atributos. Vea también: matriz de asociación, tipo de archivo.

</dd> <dt>

**personalización del tipo de archivo**
</dt> <dd>

Asociación que permite a Shell personalizar cómo Shell trata un tipo de archivo. Las personalizaciones de tipo de archivo incluyen: especificar la aplicación que se usa para abrir el archivo cuando se hace doble clic, agregar comandos al menú contextual para un tipo de archivo, especificar un icono personalizado, especificar un tipo de contenido MIME para asociar con un tipo de archivo, especificar un tipo percibido y especificar una o varias aplicaciones asociadas por tipo de archivo con el cuadro de diálogo Abrir con . Vea también: PerceivedType.

</dd> <dt>

**controlador de tipo de archivo**
</dt> <dd>

Controlador registrado para un tipo de archivo. Vea también: controlador.

</dd> <dt>

**Carpeta**
</dt> <dd>

Consulte la definición de: contenedor.

</dd> <dt>

**PIDL completo**
</dt> <dd>

PIDL que describe de forma única un objeto relativo a la carpeta de escritorio.

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**handler**
</dt> <dd>

Objeto COM que proporciona funcionalidad para un elemento de Shell. La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos. Por ejemplo, la carpeta del sistema de archivos usa el sistema de asociación para buscar los controladores de un tipo de archivo determinado. Vea también: asociación de archivos, tipo de archivo, personalización de tipo de archivo.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**controlador de iconos**
</dt> <dd>

Controlador que proporciona la información necesaria para generar y almacenar en caché un icono de un elemento. El almacén de datos del sistema de archivos admite la carga de un controlador de iconos para un elemento basado en el tipo de archivo, lo que permite a ese controlador proporcionar un icono que se usa para todas las instancias de ese tipo de archivo.

</dd> <dt>

**Controlador de información**
</dt> <dd>

Controlador que proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre un objeto de interfaz de usuario.

</dd> <dt>

**item**
</dt> <dd>

Vea la definición de: Elemento de shell.

</dd> <dt>

**clase item**
</dt> <dd>

Consulte la definición de: tipo de archivo.

</dd> <dt>

**lista de identificadores de elemento**
</dt> <dd>

Secuencia de una o varias estructuras DESASEYD que definen de forma única un objeto relativo a algún objeto raíz.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Variante**
</dt> <dd>

Propiedad que proporciona un nombre de tipo descriptivo y se puede asociar a una lista de propiedades y un patrón de diseño. Kind se introdujo en Windows Vista para expresar una noción más fácil de usar del tipo de archivo y se definió como una propiedad de cadena de varios valores (valores de cadena canónicos), por lo que puede tener un valor kind "audio;video" o "link;document". Algunos nombres de tipo descriptivos ya están asociados a propiedades y patrones de diseño. Por ejemplo, los elementos asociados a Kind.Picture y los elementos asociados a Kind.Document muestran propiedades diferentes incluso cuando están en la misma vista. Cada tipo de elemento se puede asociar a uno de los cuatro patrones de diseño únicos que definen el número de propiedades mostradas para cada elemento y su diseño. Vea también: Asociación de tipo, vista de contenido, patrón de diseño.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**patrón de diseño**
</dt> <dd>

Una de las distintas disposiciones para mostrar propiedades. En Windows 7 y versiones posteriores, al registrar un nuevo tipo de archivo, puede usar la vista de contenido para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo. Puede elegir entre cuatro patrones de diseño diferentes: Alfa (para los resultados de búsqueda de documentos que contienen fragmentos de código), Beta (para resultados de búsqueda de correo electrónico con fragmentos de código), Gamma (similar a Alpha pero con un diseño de dos líneas en lugar de cuatro) y Delta (para mostrar muchas propiedades más cortas, como con música e imágenes). Vea también: vista de contenido, kind, kind association.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**controlador de metadatos**
</dt> <dd>

Este término se usa a veces para significar controlador de propiedades. Vea la definición de: controlador de propiedades.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**extensión de espacio de nombres**
</dt> <dd>

Consulte la definición de: Origen de datos del shell.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Object Linking and Embedding Database (OLE DB)**
</dt> <dd>

Un conjunto estándar de interfaces que proporciona acceso heterogéneo a orígenes dispares de información ubicados en cualquier lugar, como sistemas de archivos, carpetas de correo electrónico y bases de datos.

</dd> <dt>

**OLE DB**
</dt> <dd>

Consulte la definición de: Object Linking and Embedding Database.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**PerceivedType**
</dt> <dd>

Una amplia categoría de tipos de formato de archivo. PerceivedType se introdujo en Windows XP y admite un conjunto limitado de tipos de archivo conocidos (por ejemplo, los tipos de archivo Image, Text, Audio y Compressed). Los tipos de archivo, generalmente los tipos de archivo públicos, también pueden tener un tipo percibido. Por ejemplo, los tipos de archivo de imagen .bmp, .png, .jpg y .gif también son del tipo percibido, image. En la capa de programación, PerceivedType se expresa como un entero. Dado que hay código que usa Kind y PerceivedType, los propietarios de formato de archivo deben registrar ambos. Por ejemplo, "reproducir todo" depende de PerceivedType. Vea también: Tipo de archivo.

</dd> <dt>

**controlador de vista previa**
</dt> <dd>

Controlador que genera rápidamente una vista simplificada y de solo lectura del elemento shell que se mostrará en el panel de vista previa Windows Explorer.

</dd> <dt>

**controlador de propiedades**
</dt> <dd>

Controlador que traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que pueden acceder Windows Explorer, Windows Search y otras aplicaciones. Estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer propiedades en y desde el archivo. Los datos traducidos incluyen la vista de detalles, información sobre información, el panel de detalles, las páginas de propiedades, etc. Cada controlador de propiedades está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Consulte también: sistema de propiedades.

</dd> <dt>

**controlador de hoja de propiedades**
</dt> <dd>

Controlador que se usa para crear hojas de propiedades personalizadas con imágenes de interfaz de usuario y controles que permiten la interacción personalizada con un tipo de archivo.

</dd> <dt>

**sistema de propiedades**
</dt> <dd>

Un sistema extensible de lectura y escritura de definiciones de datos que usa propiedades implementadas como pares nombre-valor. Vea también: controlador de propiedades, elemento de Shell.

</dd> <dt>

**valor de propiedad**
</dt> <dd>

Valor asociado a un nombre de propiedad para un elemento de Shell. Por ejemplo, "Author", "Size" y "Date Taken" son propiedades. Los valores de propiedad se expresan como una estructura PROPVARIANT.

</dd> <dt>

**controlador de protocolo**
</dt> <dd>

Controlador que tiene acceso a orígenes de contenido y proporciona un objeto IUrlAccessor para un protocolo y una dirección URL especificados. Los controladores de protocolo amplían Windows search y pueden proporcionar notificaciones de cambio a los indexadores. Se requieren distintos controladores de protocolo para indexar tipos específicos de almacenes de datos. Para proporcionar una experiencia de usuario razonable, también debe proporcionar un origen de datos de Shell para el almacén de datos, además de implementar el controlador de protocolo. El controlador de protocolo expone los elementos del almacén de datos al indexador, mientras que el origen de datos de Shell expone los elementos del almacén de datos al shell.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**PIDL relativa**
</dt> <dd>

PIDL relativa a algún objeto raíz en el espacio de nombres del shell que no sea la carpeta de escritorio. Esta es normalmente la carpeta primaria del elemento.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Origen de datos de shell**
</dt> <dd>

Componente que se usa para ampliar el espacio de nombres de Shell y exponer elementos en un almacén de datos. En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell. Vea también: contenedor, controlador, elemento de Shell.

</dd> <dt>

**Extensión de shell**
</dt> <dd>

Este término se usa a veces para significar controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**Controlador de extensión de shell**
</dt> <dd>

Este término se usa a veces para significar controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**Controlador de shell**
</dt> <dd>

Este término se usa a veces para significar controlador de tipo de archivo. Vea la definición de: controlador de tipo de archivo.

</dd> <dt>

**Elemento de shell**
</dt> <dd>

Un único fragmento de contenido. Algunos elementos de Shell son orígenes de contenido y otros no. Una carpeta es un origen de contenido, por ejemplo, pero un .jpg no lo es. Los controladores de tipo de archivo exponen elementos de Shell. En algunos contextos, se usa "item" para distinguir contenedores de no contenedores. Vea también: contenedor, origen de contenido, controlador de tipo de archivo.

</dd> <dt>

**Extensión de espacio de nombres de Shell**
</dt> <dd>

Este término se usa a veces para significar origen de datos de Shell. Consulte la definición de: Origen de datos del shell.

</dd> <dt>

**menú contextual**
</dt> <dd>

Interfaz de usuario que se usa para presentar una colección de verbos asociados a un elemento de interfaz de usuario, como un archivo o una carpeta.

</dd> <dt>

**Controlador de menú contextual**
</dt> <dd>

Controlador que agrega verbos para un elemento o elementos. Estos verbos se muestran normalmente en un menú contextual. Vea también: menú contextual.

</dd> <dt>

**PIDL simple**
</dt> <dd>

PIDL que se analiza sin comprobación de disco.

</dd> <dt>

**verbo estático**
</dt> <dd>

Verbo que se aplica a un elemento de Shell sin necesidad de inspeccionar el estado actual de un elemento o sistema. Un verbo estático se basa en un registro estático de los elementos asociados de un elemento y no cambia.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**controlador de miniaturas**
</dt> <dd>

Controlador que proporciona una imagen estática para representar un elemento de Shell.

</dd> <dt>

**proveedor de miniaturas**
</dt> <dd>

Este término se usa a veces para significar controlador de miniaturas. Vea la definición de: controlador de miniaturas.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**nombre de tipo descriptivo**
</dt> <dd>

Vea la definición de: Kind.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**Verbo**
</dt> <dd>

Acción individual a la que puede llamar un elemento de Shell. Entre los ejemplos se incluyen open e print. Los verbos a veces se conocen como comandos o tareas. Vea también: verbo dinámico, controlador de menú contextual, verbo estático.

</dd> <dt>

**controlador de verbo**
</dt> <dd>

Este término se usa a veces para significar controlador de menú contextual. Vea definición de: controlador de menú contextual.

</dd> </dl>

 

 



