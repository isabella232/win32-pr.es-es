---
description: Una vez que comprenda el modo de resultados de la búsqueda, el modo de exploración y los patrones de diseño, puede registrar una lista de propiedades personalizada para el tipo de archivo. Para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo, siga estos pasos.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Cómo registrar propiedades personalizadas y diseño para el tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997697"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Cómo registrar propiedades personalizadas y diseño para el tipo de archivo

Una vez que comprenda el modo de resultados de la búsqueda, el modo de exploración y los patrones de diseño, puede registrar una lista de propiedades personalizada para el tipo de archivo.

Para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo, siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Elija entre los cuatro patrones de diseño: alfa, beta, gamma o delta.

### <a name="step-2"></a>Paso 2:

Tenga en cuenta las siguientes reglas de formato, que se aplican igualmente a los cuatro patrones de diseño:

-   La propiedad 1 siempre se muestra en un tamaño de fuente mayor. Tamaño de fuente grande que se suele usar para el nombre de elemento, pero también se puede usar para la propiedad de delimitador u otro elemento.
-   La propiedad 4 está pensada para los extractos de los patrones de diseño alfa, beta y gamma. Esta propiedad tiene más espacio en esos patrones y se muestra en un color de fuente gris, en lugar de negro como el resto de las propiedades, para ayudarlo a resaltar.
-   Las medidas de píxeles que se muestran a continuación se encuentran en píxeles relativos y el tamaño incluye el icono o la miniatura a la izquierda de las propiedades y el espacio entre el icono o la miniatura y el rectángulo de selección.
-   La mayoría de las propiedades tienen un tamaño mínimo de presentación. Por lo tanto, no aparecerán si no hay espacio suficiente para ellos en un tamaño de vista determinado. El tamaño mínimo suele ser de 100 píxeles de ancho.
-   Cada modelo de diseño define el número de filas y el número de propiedades de cada fila.

### <a name="step-3"></a>Paso 3:

Decida qué propiedades desea mostrar en el diseño y qué propiedad desea mostrar en cada ubicación. A la hora de decidir qué propiedad Mostrar en cada posición del diseño, tenga en cuenta la longitud típica de la propiedad, su importancia para el usuario y si se debe quitar cuando el tamaño de la ventana sea demasiado pequeño para contener todas las propiedades.

### <a name="step-4"></a>Paso 4:

Registre un patrón de diseño y una lista de propiedades para el tipo de archivo o el tipo de elemento agregando las siguientes claves en la clave del registro ProgID para el tipo de archivo o elemento (en este ejemplo, para el tipo de archivo. XYZ).

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>Paso 5:

Observe las siguientes directrices de formato para registrar propiedades:

-   Cada registro comienza con `prop:`
-   Cada propiedad requiere el nombre completo de la propiedad.
-   Las propiedades se separan con un punto y coma sin espacio.
-   Las propiedades se muestran en el orden definido por el patrón de diseño seleccionado.
-   `~` indica que no se debe mostrar la etiqueta de propiedad.
-   `~System.LayoutPattern.PlaceHolder` debe usarse si se desea dejar en blanco una propiedad que se especifica en el patrón de diseño.

En la clave del registro de ejemplo siguiente se muestran estas instrucciones de formato.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

Entre los valores posibles de (ContentViewModeForBrowse) se incluyen los siguientes: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



