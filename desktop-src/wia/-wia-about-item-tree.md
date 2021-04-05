---
description: Con Windows Vista, el árbol de elementos de adquisición de imágenes de Windows (WIA) ha cambiado significativamente.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Acerca del árbol de elementos IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909874"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Acerca del árbol de elementos IWiaItem2

Con Windows Vista, el árbol de elementos de adquisición de imágenes de Windows (WIA) ha cambiado significativamente. Los elementos [**IWiaItem2**](-wia-iwiaitem2.md) se usan para representar los atributos del dispositivo y los datos del dispositivo. Las aplicaciones de imágenes ven un dispositivo de adquisición de imágenes de Windows (WIA) 2,0 como un árbol jerárquico de elementos, con el elemento raíz que representa el propio dispositivo y los elementos secundarios que representan elementos como orígenes de datos programables, imágenes o carpetas que contienen imágenes.

-   [Elementos de aplicación](#application-items)
-   [Marcas de elemento](#item-flags)
-   [Categorías de elementos](#item-categories)
-   [Elemento raíz](#root-item)
-   [Elemento de datos](#data-item)
-   [Temas relacionados](#related-topics)

## <a name="application-items"></a>Elementos de aplicación

El árbol de elementos de WIA 2,0 que puede ver una aplicación es independiente del árbol creado y mantenido por un minicontrolador de WIA 2,0. Cuando un minicontrolador crea un árbol, el servicio WIA 2,0 usa este árbol de elementos de WIA 2,0 como guía para crear una copia del árbol que las aplicaciones de imágenes pueden ver. Los elementos del árbol copiado se denominan elementos de la *aplicación* . Los elementos del árbol creados por un minicontrolador se denominan elementos de *controlador* .

Un elemento WIA puede representar un origen de datos programable para el alimentador de documentos de un escáner o los datos almacenados en ese dispositivo. Un dispositivo WIA debe dividirse en elementos individuales que describan los diferentes datos generados por ese dispositivo.

Por ejemplo, un escáner WIA que admite el análisis de escáneres y el examen del alimentador de documentos podría dividirse en dos elementos secundarios. Una representa la funcionalidad de digitalización plana y la otra representa la funcionalidad de exploración del alimentador de documentos.

Se pueden colocar varias imágenes en un escáner plano y examinar al mismo tiempo en una carpeta. Con el filtro de segmentación ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), cada imagen o subregión se puede crear como un elemento secundario de la carpeta.

El árbol WIA de un dispositivo de cámara que almacena fotos ("película") puede dividirse en elementos que representan carpetas, subcarpetas y fotos.

## <a name="item-flags"></a>Marcas de elemento

Las marcas de elementos WIA ayudan a clasificar el contenido o el comportamiento compatible de un elemento WIA determinado. Las marcas de elementos WIA se dividen en dos grupos.

1.  Las marcas de estado del elemento notifican el estado actual del elemento WIA, por ejemplo, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, etc.
2.  Los indicadores de uso y representación de datos de elementos notifican los datos que el elemento WIA representa o pueden generar si se transfieren. Por ejemplo, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) es una marca de representación de datos que indica a la aplicación que los datos asociados al elemento WIA actual son datos de imagen y deben tener propiedades de datos de imagen. **WIA \_ \_ \_ Marcas de elemento IPA** es una marca de uso de elementos que indica a la aplicación que el elemento WIA es configurable y sigue un conjunto de reglas de configuración predefinidas basadas en la [**\_ \_ \_ categoría de elemento IPA de WIA**](-wia-wiaitempropcommonitem.md) , y que la configuración puede cambiar el resultado de cada transferencia de datos. (Para obtener más información sobre las definiciones de categoría [, vea categorías de elementos item Categories](#item-categories) ).

En el gráfico siguiente se muestra un ejemplo de un árbol de elementos WIA y las distintas marcas que pueden estar asociadas a cada elemento.

![ejemplos de marcas de elemento para los elementos de un árbol](images/scannertree1.jpg)

## <a name="item-categories"></a>Categorías de elementos

Los elementos de WIA se agrupan en categorías mediante los valores de propiedad de [**\_ \_ \_ categoría de elemento IPA de WIA**](-wia-wiaitempropcommonitem.md) . Estas categorías definen cómo se trata o se utiliza un elemento WIA. Por ejemplo, si el elemento representa un archivo terminado ( \_ el archivo de categoría de WIA \_ finalizada \_ ), una aplicación WIA debe asumir que los datos son estáticos y se encuentran en el dispositivo. Si el elemento representa un alimentador ( \_ alimentador de categoría WIA \_ ), la aplicación debe esperar que contenga las propiedades necesarias del alimentador de documentos y que funcione como un alimentador de documentos.

Las categorías definidas por WIA son:

-   Categoría de WIA \_ \_ auto
-   \_alimentador de categoría WIA \_
-   \_película de categoría WIA \_
-   archivo de categoría de WIA \_ \_ finalizada \_
-   plano de la \_ categoría WIA \_

Por ejemplo, el elemento plano de un escáner puede tener [**las \_ \_ \_ marcas de elemento del IPA de WIA**](-wia-wiaitempropcommonitem.md) establecidas en [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** y **WiaItemTypeProgrammableDataSource**, y la propiedad **\_ \_ \_ categoría de elemento IPA de WIA** establecida en la categoría de WIA \_ \_ plano.

En la tabla siguiente se muestra la agrupación de categorías WIA con marcas de elementos y elementos WIA. En esta tabla no se incluye una lista completa de las marcas de elementos de WIA definidas por WIA.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoría WIA</th>
<th>Marcas de elemento WIA válidas</th>
<th>Conjunto de propiedades de WIA</th>
<th>Elementos WIA</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></li>
</ul></td>
<td>El conjunto de propiedades incluye propiedades del escáner configuradas automáticamente.</td>
<td>Elemento automático WIA que representa la configuración de exploración automática del escáner.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>El conjunto de propiedades incluye propiedades de control de escáner del alimentador (normalmente conjunto de propiedades específicas del documento y imagen).</td>
<td>Elementos del alimentador WIA, incluidos los elementos secundarios que representan las páginas frontal y posterior de un documento.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>El conjunto de propiedades incluye propiedades de control de escáner de película (normalmente, conjunto de propiedades específicas de imagen y documento).</td>
<td>Elementos de película WIA, incluidos los elementos secundarios que representan los fotogramas de digitalización individuales.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
</ul></td>
<td>La propiedad establecida en este elemento depende del tipo de elemento indicado. Por ejemplo, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> debe incluir algunas propiedades de elementos de imagen, como bits por píxel y así sucesivamente.</td>
<td>Elementos de almacenamiento WIA, incluidos los elementos secundarios que representan el contenido del archivo finalizado (archivos de datos como JPEG, HTML, TXT, etc.).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>: puede estar presente si el escáner admite el análisis de varios elementos.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>: puede estar presente si la aplicación genera un elemento WIA durante una sesión de examen de varios elementos.</li>
</ul></td>
<td>El conjunto de propiedades incluye las propiedades de control de escáner plano (normalmente, la imagen y el conjunto de propiedades específicas del documento).</td>
<td>Elementos de escáner WIA, incluidos los elementos secundarios que representan las regiones que se están analizando en la placa de escáner.</td>
</tr>
</tbody>
</table>



 

En el gráfico siguiente se muestra un ejemplo de un árbol de elementos WIA y las distintas categorías que pueden estar asociadas a cada elemento.

![ejemplos de categorías de elementos para los elementos de un árbol](images/scannertree2.jpg)

## <a name="root-item"></a>Elemento raíz

Un elemento raíz de WIA es un elemento de carpeta marcado con marcas [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) y **WiaItemTypeDevice** que representa el propio dispositivo. Contiene atributos de dispositivo como el fabricante, el nombre del dispositivo y los atributos del controlador, como la versión del controlador y el identificador de clase (CLSID) de la interfaz de usuario. Las aplicaciones de creación de imágenes obtienen la raíz del árbol de elementos WIA mediante una llamada al método [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) . La aplicación utiliza el elemento raíz para obtener acceso a los elementos de WIA secundarios individuales enumerando el árbol (vea [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>Data Item

Cualquier elemento que se pueda usar para transferir datos se considera un elemento de datos. Esto incluye los elementos marcados con la marca [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .

Los elementos de carpeta y los elementos que no son de carpeta pueden exponer la capacidad de transferir datos marcando con la marca [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) . Cualquier elemento con esta marca establecida tiene que proporcionar las siguientes propiedades de elemento WIA:

-   [**\_derechos de \_ acceso del IPA de WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_tamaño del \_ elemento \_ IPA de WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_tamaño de \_ búfer de IPA de WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_formato de IPA de WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ formato preferido del IPA de WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_TYMED del IPA de WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_extensión de \_ nombre de archivo de WIA IPA \_**](-wia-wiaitempropcommonitem.md)

Los elementos de origen de datos programables marcados con la marca [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) también deben proporcionar el conjunto de propiedades requerido del elemento de datos.

Los elementos de datos WIA pueden tener propiedades adicionales en función de la configuración de la marca del elemento. Por ejemplo, los elementos de WIA marcados con la marca [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) deben tener propiedades de información específica de la imagen, como la [**\_ \_ profundidad de IPA de WIA**](-wia-wiaitempropcommonitem.md) y el **\_ \_ número \_ de \_ líneas del IPA de WIA**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)
</dt> <dt>

[**IWiaDevMgr2**](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



