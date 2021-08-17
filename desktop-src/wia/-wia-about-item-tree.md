---
description: Con Windows Vista, el Windows de elementos de adquisición de imágenes (WIA) ha cambiado significativamente.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Acerca del árbol de elementos IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae342f5a85e61b6384604dae703881c6888e3e1cf8e61cc8a39a32ac77ad436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264438"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Acerca del árbol de elementos IWiaItem2

Con Windows Vista, el Windows de elementos de adquisición de imágenes (WIA) ha cambiado significativamente. [**Los elementos IWiaItem2**](-wia-iwiaitem2.md) se usan para representar los atributos de dispositivo y los datos del dispositivo. Las aplicaciones de creación de imágenes ven un dispositivo de adquisición de imágenes de Windows (WIA) 2.0 como un árbol jerárquico de elementos, con el elemento raíz que representa el propio dispositivo y los elementos secundarios que representan elementos como orígenes de datos programables, imágenes o carpetas que contienen imágenes.

-   [Elementos de aplicación](#application-items)
-   [Marcas de elemento](#item-flags)
-   [Categorías de elementos](#item-categories)
-   [Elemento raíz](#root-item)
-   [Elemento de datos](#data-item)
-   [Temas relacionados](#related-topics)

## <a name="application-items"></a>Elementos de aplicación

El árbol de elementos de WIA 2.0 que puede ver una aplicación es independiente del árbol creado y mantenido por un minidriver de WIA 2.0. Cuando un minidriver crea un árbol, el servicio WIA 2.0 usa este árbol de elementos de WIA 2.0 como guía para crear una copia del árbol que pueden ver las aplicaciones de creación de imágenes. Los elementos del árbol copiado se denominan *elementos de* aplicación. Los elementos del árbol creado por un minidriver se denominan *elementos de* controlador.

Un elemento de WIA puede representar un origen de datos programable para el fuente de documentos de un analizador o los datos almacenados en ese dispositivo. Un dispositivo WIA debe dividirse en elementos individuales que describan los distintos datos generados por ese dispositivo.

Por ejemplo, un analizador de WIA que admita el examen plano y el de fuente de documentos podría dividirse en dos elementos secundarios. Una representa la funcionalidad de análisis de planos y la otra representa la funcionalidad de examen del feeder de documentos.

Varias imágenes colocadas en un escáner plano y examinadas al mismo tiempo se pueden colocar en una carpeta. Con el filtro de segmentación ([**IWiaSegmentationFilter),**](-wia-iwiasegmentationfilter.md)cada imagen o subregión se puede crear como un elemento secundario de la carpeta.

El árbol WIA de un dispositivo de cámara que almacena fotos ("Película") se puede dividir en elementos que representan carpetas, subcarpetas y fotos.

## <a name="item-flags"></a>Marcas de elemento

Las marcas de elementos de WIA ayudan a clasificar el contenido o el comportamiento admitido de un elemento de WIA determinado. Las marcas de elementos de WIA se agrupan en dos grupos.

1.  Las marcas de estado del elemento informan del estado actual del elemento de WIA, por ejemplo, [**WiaItemTypeDisconnected,**](-wia-wia-item-type-flags.md) **WiaItemTypeDeleted,** etc.
2.  Las marcas de uso o representación de datos de elementos informan de los datos que el elemento de WIA representa o pueden generar si se transfieren. Por ejemplo, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) es una marca de representación de datos que indica a la aplicación que los datos asociados al elemento wia actual son datos de imagen y deben tener propiedades de datos de imagen. **WIA \_ IPA \_ ITEM \_ FLAGS** es una marca de uso de elementos que indica a la aplicación que el elemento de WIA es configurable y sigue un conjunto de reglas de configuración predefinidas basadas en LA CATEGORÍA DE ELEMENTO [**\_ IPA \_ \_**](-wia-wiaitempropcommonitem.md) de WIA y que la configuración puede cambiar el resultado de cada transferencia de datos. (Para obtener más información sobre las definiciones de categoría, vea [Categorías de elementos](#item-categories) categorías de elementos).

En el gráfico siguiente se muestra un ejemplo de un árbol de elementos de WIA y las distintas marcas que podrían estar asociadas a cada elemento.

![ejemplos de marcas de elementos para elementos de un árbol](images/scannertree1.jpg)

## <a name="item-categories"></a>Categorías de elementos

Los elementos de WIA se agrupan en categorías mediante los valores [**de propiedad ITEM CATEGORY de WIA \_ IPA. \_ \_**](-wia-wiaitempropcommonitem.md) Estas categorías definen cómo se va a tratar o usar un elemento de WIA. Por ejemplo, si el elemento representa un archivo terminado (WIA CATEGORY FINISHED FILE), una aplicación WIA debe suponer que los datos son estáticos y se encuentran \_ \_ en el \_ dispositivo. Si el elemento representa un feeder (WIA CATEGORY FEEDER), la aplicación debe esperar que contenga las propiedades de fuente de documentos necesarias y funcione como un \_ \_ feeder de documentos.

Las categorías definidas por WIA son:

-   WIA \_ CATEGORY \_ AUTO
-   FUENTE DE \_ CATEGORÍA \_ WIA
-   WIA \_ CATEGORY \_ PELÍCULAS
-   ARCHIVO FINALIZADO \_ DE CATEGORÍA \_ \_ WIA
-   CATEGORÍA WIA \_ \_ PLANA

Por ejemplo, el elemento plano de un analizador puede tener [**WIA \_ IPA \_ ITEM \_ FLAGS**](-wia-wiaitempropcommonitem.md) establecido en [**WiaItemTypeImage,**](-wia-wia-item-type-flags.md) **WiaItemTypeTransfer** y **WiaItemTypeProgrammableDataSource,** y la propiedad **WIA \_ IPA \_ ITEM \_ CATEGORY** establecida en WIA \_ CATEGORY \_ FLATBED.

En la tabla siguiente se muestra la agrupación de categorías de WIA con marcas de elementos y elementos de WIA. Esta tabla no incluye una lista completa de las marcas de elementos de WIA definidas por WIA.



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
<th>Marcas de elementos de WIA válidas</th>
<th>Conjunto de propiedades de WIA</th>
<th>Elementos de WIA</th>
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
<td>El conjunto de propiedades incluye propiedades del analizador configuradas automáticamente.</td>
<td>Elemento automático de WIA que representa la configuración de examen configurada automáticamente del analizador.</td>
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
<td>El conjunto de propiedades incluye propiedades de control del analizador de fuentes (normalmente, conjunto de propiedades específicas de imagen y documento).</td>
<td>Elementos del feeder de WIA, incluidos los elementos secundarios que representan las páginas frontal y posterior de un documento.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>El conjunto de propiedades incluye propiedades de control del escáner de películas (normalmente, conjunto de propiedades específicos de imagen y documento).</td>
<td>Elementos de WIA Película, incluidos los elementos secundarios que representan los fotogramas de examen individuales.</td>
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
<td>La propiedad establecida en este elemento depende del tipo de elemento notificado. Por ejemplo, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> debe incluir algunas propiedades de elemento de imagen, como bits por píxel, etc.</td>
<td>Elementos de almacenamiento WIA, incluidos los elementos secundarios que representan el contenido del archivo finalizado (archivos de datos como JPEG, HTML, TXT, etc.).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder:</strong></a>puede estar presente si el analizador admite el examen de varios elementos.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated:</strong></a>puede estar presente si la aplicación genera un elemento de WIA durante una sesión de examen de varios elementos.</li>
</ul></td>
<td>El conjunto de propiedades incluye propiedades de control de escáner planas (normalmente imagen y conjunto de propiedades específico del documento).</td>
<td>Elementos planas WIA, incluidos los elementos secundarios que representan las regiones que se examinan en la placa plana del analizador.</td>
</tr>
</tbody>
</table>



 

En el gráfico siguiente se muestra un ejemplo de un árbol de elementos de WIA y las distintas categorías que podrían asociarse a cada elemento.

![ejemplos de categorías de elementos para elementos de un árbol](images/scannertree2.jpg)

## <a name="root-item"></a>Elemento raíz

Un elemento raíz de WIA es un elemento de carpeta marcado con marcas [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) y **WiaItemTypeDevice** que representa el propio dispositivo. Contiene atributos de dispositivo como fabricante, nombre de dispositivo y atributos de controlador, como la versión del controlador y el identificador de clase de interfaz de usuario (CLSID). Las aplicaciones de creación de imágenes obtienen la raíz del árbol de elementos de WIA mediante una llamada al método [**IWiaDevMgr2::CreateDevice.**](-wia-iwiadevmgr2-createdevice.md) La aplicación usa el elemento raíz para obtener acceso a los elementos de WIA secundarios individuales enumerando el árbol (vea [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>Data Item

Cualquier elemento que se pueda usar para transferir datos se considera un elemento de datos. Esto incluye elementos marcados con la [**marca WiaItemTypeProgrammableDataSource.**](-wia-wia-item-type-flags.md)

Los elementos de carpeta y los elementos que no son de carpeta pueden exponer la capacidad de transferir datos si se marcan con la [**marca WiaItemTypeTransfer.**](-wia-wia-item-type-flags.md) Cualquier elemento con este conjunto de marcas debe proporcionar las siguientes propiedades de elemento de WIA:

-   [**DERECHOS DE \_ ACCESO DE IPA \_ DE WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**TAMAÑO DEL \_ ELEMENTO IPA \_ DE WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**TAMAÑO DE BÚFER \_ DE IPA \_ DE WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**FORMATO \_ IPA DE WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**FORMATO \_ PREFERIDO DE IPA \_ DE WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ TYMED**](-wia-wiaitempropcommonitem.md)
-   [**EXTENSIÓN DE NOMBRE \_ DE ARCHIVO DE IPA \_ DE WIA \_**](-wia-wiaitempropcommonitem.md)

Los elementos de origen de datos programables marcados [**con la marca WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) también deben proporcionar el conjunto de propiedades necesaria del elemento de datos.

Los elementos de datos de WIA pueden tener propiedades adicionales en función de la configuración de marca del elemento. Por ejemplo, los elementos de WIA marcados con la marca [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) deben tener propiedades de información específicas de la imagen, como [**WIA \_ IPA \_ DEPTH**](-wia-wiaitempropcommonitem.md) y **WIA \_ IPA \_ NUMBER OF \_ \_ LINES**.

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

 

 



