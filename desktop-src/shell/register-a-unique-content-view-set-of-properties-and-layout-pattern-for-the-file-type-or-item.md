---
description: Puede registrar una lista de propiedades de vista de contenido única y un patrón de diseño para el tipo de archivo o el elemento.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registrar un conjunto de vistas de contenido de propiedades y patrones de diseño para un tipo de archivo o elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104361759"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>Cómo registrar un conjunto de vistas de contenido único de propiedades y patrones de diseño para el tipo de archivo o el elemento

Puede registrar una lista de propiedades de vista de contenido única y un patrón de diseño para el tipo de archivo o el elemento. Si el tipo de archivo o el elemento también están asociados a un tipo, el registro de la vista de contenido específico del tipo de archivo o elemento invalidará el registro del tipo. Esto puede resultar útil si las propiedades más importantes de este elemento son diferentes de otros elementos del mismo tipo. Si no asocia el tipo de archivo o el elemento a un tipo de elemento o registra directamente la vista de contenido, el sistema utiliza la información de la vista de contenido predeterminada (almacenada en una clave del registro a la que hace referencia el último elemento de la matriz de Asociación de todos los elementos, HKEY \_ clases \_ raíz \\ \* )

Antes de registrar una lista de propiedades personalizada para el tipo de archivo, debe comprender el modo de resultados de la búsqueda y el modo de exploración, y los patrones de diseño que están a su disposición.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>Paso 1: Descripción del modo de resultados de la búsqueda y el modo de exploración

La vista de contenido requiere la definición de un modelo de diseño y un conjunto de listas de propiedades para un elemento en un conjunto de resultados de la búsqueda (modo de resultados de búsqueda) y cuando se navega a una ubicación de Shell (modo de exploración). Puede usar los mismos valores para el resultado de la búsqueda y examinar, como `Kind.Music` hace. Como alternativa, puede definir una lista de propiedades y/o un patrón de diseño diferentes `Kind.Document` .

En el caso de `Kind.Document` , los usuarios suelen buscar palabras en el texto del documento. Por lo tanto, incluir más texto de ejemplo en el resultado de la búsqueda podría ser la mejor opción. En el ejemplo siguiente se muestra la vista de contenido de exploración de `Kind.Document` .

![examinar la vista de contenido de kind.document](images/content-view/browsecontentviewkinddocument.png)

Dado que los usuarios no suelen buscar texto determinado al buscar documentos, la mejor opción puede ser optimizar la elección de las propiedades y el diseño para ajustarse a más resultados de búsqueda en la pantalla. En la captura de pantalla siguiente se muestra la vista contenido de la búsqueda de `Kind.Document` .

### <a name="step-2-understanding-layout-patterns"></a>Paso 2: Descripción de los patrones de diseño

Hay cuatro patrones de diseño: alfa, beta, gamma y Delta.

**Diseño alfa**

El patrón de diseño alfa está optimizado para los resultados de búsqueda de documentos que contienen extractos. Tiene las siguientes especificaciones:

-   Filas: 4
-   Propiedades: 7
-   Diseño alfa cuando el elemento tiene 350 píxeles o más de espacio horizontal, tal y como se muestra en la siguiente ilustración.

    ![patrón de diseño alfa](images/content-view/layout1.png)

-   En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño alfa](images/content-view/alphaviewmore.png)

-   En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño alfa en Microsoft Word.](images/content-view/layout2.png)

-   En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![ejemplo de diseño alfa](images/content-view/alphaviewless.png)

**Diseño beta**

El patrón de diseño beta está optimizado para los resultados de búsqueda de documentos de correo electrónico que contienen extractos. Tiene las siguientes especificaciones:

-   Filas: 4
-   Propiedades: 5
-   Diseño beta cuando el elemento tiene 350 píxeles o más de espacio horizontal, tal y como se muestra en la siguiente ilustración.

    ![Diagrama que muestra un ejemplo de diseño beta.](images/content-view/layout3.png)

-   En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño beta para el correo electrónico.](images/content-view/betaviewmore.png)

-   En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño beta con menos de 350 píxeles de espacio horizontal.](images/content-view/layout4.png)

-   En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene menos de 350 píxeles de espacio horizontal:

    ![ejemplo de diseño beta](images/content-view/betaviewless.png)

**Diseño gamma**

El patrón de diseño gamma es similar a alfa, pero usa un diseño de dos líneas en lugar de cuatro. Este diseño es idóneo para los escenarios en los que desea ver un fragmento de código pero desea ajustar más elementos en la pantalla, o para los tipos de archivo que requieren menos espacio para mostrar la información más crítica. El diseño gamma tiene las siguientes especificaciones:

-   Filas: 2
-   Propiedades: 4
-   En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño gamma.](images/content-view/layout5.png)

-   En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño gamma para un elemento de lista de comprobación.](images/content-view/gammaviewmore.png)

-   En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño gamma con menos de 350 píxeles de espacio horizontal.](images/content-view/layout6.png)

-   Ejemplo del diseño gamma cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![ejemplo de diseño gamma](images/content-view/gammaviewless.png)

**Diseño Delta**

El patrón de diseño Delta está optimizado para mostrar muchas propiedades más cortas como la música y las imágenes. Tiene las siguientes especificaciones:

-   Filas: 2
-   Propiedades: 6
-   Diseño Delta cuando el elemento tiene 700 píxeles o más de espacio horizontal, tal y como se muestra en la siguiente ilustración.

    ![Diagrama que muestra un ejemplo de diseño Delta.](images/content-view/layout7.png)

-   Ejemplo del diseño Delta cuando el elemento tiene 700 píxeles o más de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño Delta para un archivo de música.](images/content-view/deltalayoutmore.png)

-   Diseño Delta cuando el elemento tiene entre 350 y 700 píxeles de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño Delta que tiene entre 350 y 700 píxeles de espacio horizontal.](images/content-view/layout8.png)

-   Ejemplo del diseño Delta cuando el elemento tiene entre 350 y 700 píxeles de espacio horizontal.

    ![ejemplo de diseño Delta](images/content-view/deltaviewbetween.png)

-   Diseño Delta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![ejemplo de diseño](images/content-view/layout9.png)

-   Ejemplo del diseño Delta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño Delta para un archivo de música que tiene menos de 350 píxeles de espacio horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>Paso 3: registro de las propiedades personalizadas y el diseño del tipo de archivo

Una vez que comprenda el modo de resultados de la búsqueda, el modo de exploración y los patrones de diseño, puede registrar una lista de propiedades personalizada para el tipo de archivo.

**Para registrar una lista de propiedades personalizadas y un modelo de diseño para el tipo de archivo.**

1.  Elija entre los cuatro patrones de diseño: alfa, beta, gamma o delta.
2.  Tenga en cuenta las siguientes reglas de formato, que se aplican igualmente a los cuatro patrones de diseño:
    -   La propiedad 1 siempre se muestra en un tamaño de fuente mayor. Tamaño de fuente grande que se suele usar para el nombre de elemento, pero también se puede usar para la propiedad de delimitador u otro elemento.
    -   La propiedad 4 está pensada para los extractos de los patrones de diseño alfa, beta y gamma. Esta propiedad tiene más espacio en esos patrones y se muestra en un color de fuente gris, en lugar de negro como el resto de las propiedades, para ayudarlo a resaltar.
    -   Las medidas de píxeles que se muestran a continuación se encuentran en píxeles relativos y el tamaño incluye el icono o la miniatura a la izquierda de las propiedades y el espacio entre el icono o la miniatura y el rectángulo de selección.
    -   La mayoría de las propiedades tienen un tamaño mínimo de presentación. Por lo tanto, no aparecerán si no hay espacio suficiente para ellos en un tamaño de vista determinado. El tamaño mínimo suele ser de 100 píxeles de ancho.
    -   Cada modelo de diseño define el número de filas y el número de propiedades de cada fila.
3.  Decida qué propiedades desea mostrar en el diseño y qué propiedad desea mostrar en cada ubicación. A la hora de decidir qué propiedad Mostrar en cada posición del diseño, tenga en cuenta la longitud típica de la propiedad, su importancia para el usuario y si se debe quitar cuando el tamaño de la ventana sea demasiado pequeño para contener todas las propiedades.
4.  Registre un patrón de diseño y una lista de propiedades para el tipo de archivo o el tipo de elemento agregando las siguientes claves en la clave del registro ProgID para el tipo de archivo o elemento (en este ejemplo, para el tipo de archivo. XYZ).

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  Observe las siguientes directrices de formato para registrar propiedades:

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

    Entre los valores posibles de (ContentViewModeForBrowse) se incluyen los siguientes: prop: ~ System. ItemNameDisplay; System. Author; System. LayoutPattern. PlaceHolder; System. keywords; System. DateModified; ~ System. Size

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Nombres de tipos](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[System. proplist. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[System. proplist. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
