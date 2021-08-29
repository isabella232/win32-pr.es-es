---
description: Puede registrar una lista de propiedades de vista de contenido única y un patrón de diseño para el tipo de archivo o elemento.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registrar un conjunto de propiedades de vista de contenido y un patrón de diseño para un tipo de archivo o elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a3df2b65f0c977b5898e2fa35a28091052dde508c0d381379303119068ab3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820505"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>Cómo registrar un conjunto de propiedades y un patrón de diseño de vista de contenido único para el tipo de archivo o elemento

Puede registrar una lista de propiedades de vista de contenido única y un patrón de diseño para el tipo de archivo o elemento. Si el tipo de archivo o elemento también está asociado a un tipo, el registro de vista contenido específico del tipo de archivo o elemento invalidará el registro kind. Esto puede ser útil si las propiedades más importantes de este elemento son diferentes de otros elementos del mismo tipo. Si no asocia el tipo de archivo o el elemento a un elemento Kind o registra directamente la vista Content, el sistema usa la información de vista de contenido predeterminada (almacenada en una clave del Registro a la que hace referencia el último elemento de la matriz de asociación de todos los elementos, HKEY \_ CLASSES \_ ROOT \\ \* ).

Antes de registrar una lista de propiedades personalizadas para el tipo de archivo, debe comprender el modo resultado de la búsqueda y el modo examinar, así como los patrones de diseño que están disponibles.

## <a name="instructions"></a>Instructions

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>Paso 1: Descripción del modo de resultados de búsqueda y el modo de exploración

La vista de contenido requiere definir un patrón de diseño y un conjunto de listas de propiedades para un elemento en un conjunto de resultados de búsqueda (modo de resultados de búsqueda) y al navegar a una ubicación de Shell (modo examinar). Puede usar los mismos valores para Resultado de búsqueda y Examinar, como `Kind.Music` hace. Como alternativa, puede definir una lista de propiedades o un patrón de diseño diferentes como `Kind.Document` lo hace.

En el caso de `Kind.Document` , los usuarios suelen buscar palabras en el texto del documento. Por lo tanto, incluir más texto de ejemplo en el resultado de la búsqueda podría ser la mejor opción. En el ejemplo siguiente se muestra la vista Examinar contenido de `Kind.Document` .

![examinar vista de contenido de kind.document](images/content-view/browsecontentviewkinddocument.png)

Dado que los usuarios rara vez buscan texto determinado al buscar documentos, la mejor opción es optimizar la elección de propiedades y diseño para ajustarse a más resultados de búsqueda en la pantalla. En la siguiente captura de pantalla se muestra la vista Contenido de búsqueda de `Kind.Document` .

### <a name="step-2-understanding-layout-patterns"></a>Paso 2: Descripción de los patrones de diseño

Hay cuatro patrones de diseño: Alfa, Beta, Gamma y Delta.

**Diseño alfa**

El patrón de diseño Alfa está optimizado para los resultados de búsqueda de documentos que contienen extractos. Tiene las siguientes especificaciones:

-   Filas: 4
-   Propiedades: 7
-   Diseño alfa cuando el elemento tiene 350 píxeles o más de espacio horizontal, como se muestra en la ilustración siguiente.

    ![patrón de diseño alfa](images/content-view/layout1.png)

-   En la ilustración siguiente se muestra el diseño Alfa cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño alfa](images/content-view/alphaviewmore.png)

-   En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño alfa en Microsoft Word.](images/content-view/layout2.png)

-   En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![ejemplo de diseño alfa](images/content-view/alphaviewless.png)

**Diseño beta**

El patrón de diseño beta está optimizado para los resultados de búsqueda de documentos de correo electrónico que contienen extractos. Tiene las siguientes especificaciones:

-   Filas: 4
-   Propiedades: 5
-   Diseño beta cuando el elemento tiene 350 píxeles o más de espacio horizontal, como se muestra en la ilustración siguiente.

    ![Diagrama que muestra un ejemplo de diseño beta.](images/content-view/layout3.png)

-   En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño beta para correo electrónico.](images/content-view/betaviewmore.png)

-   En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño beta con menos de 350 píxeles de espacio horizontal.](images/content-view/layout4.png)

-   En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene menos de 350 píxeles de espacio horizontal:

    ![Ejemplo de diseño beta](images/content-view/betaviewless.png)

**Diseño gamma**

El patrón de diseño Gamma es similar a Alfa, pero usa un diseño de dos líneas en lugar de cuatro. Este diseño es ideal para escenarios en los que desea ver un fragmento de código pero desea ajustar más elementos en la pantalla, o para los tipos de archivo que requieren menos espacio para mostrar la información más crítica. El diseño Gamma tiene las siguientes especificaciones:

-   Filas: 2
-   Propiedades: 4
-   En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño gamma.](images/content-view/layout5.png)

-   En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene 350 píxeles o más de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño gamma para un elemento de lista de comprobación.](images/content-view/gammaviewmore.png)

-   En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño gamma con menos de 350 píxeles de espacio horizontal.](images/content-view/layout6.png)

-   Ejemplo del diseño gamma cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Ejemplo de diseño gamma](images/content-view/gammaviewless.png)

**Diseño delta**

El patrón de diseño Delta está optimizado para mostrar muchas propiedades más cortas, como música e imágenes. Tiene las siguientes especificaciones:

-   Filas: 2
-   Propiedades: 6
-   Diseño diferencial cuando el elemento tiene 700 píxeles o más de espacio horizontal, como se muestra en la ilustración siguiente.

    ![Diagrama que muestra un ejemplo de diseño delta.](images/content-view/layout7.png)

-   Ejemplo del diseño delta cuando el elemento tiene 700 píxeles o más de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño delta para un archivo de música.](images/content-view/deltalayoutmore.png)

-   Diseño diferencial cuando el elemento tiene entre 350 y 700 píxeles de espacio horizontal.

    ![Diagrama que muestra un ejemplo de diseño delta que tiene entre 350 y 700 píxeles de espacio horizontal.](images/content-view/layout8.png)

-   Ejemplo del diseño delta cuando el elemento tiene entre 350 y 700 píxeles de espacio horizontal.

    ![ejemplo de diseño delta](images/content-view/deltaviewbetween.png)

-   Diseño diferencial cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![ejemplo de diseño](images/content-view/layout9.png)

-   Ejemplo del diseño delta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.

    ![Captura de pantalla que muestra un ejemplo de diseño delta para un archivo de música con menos de 350 píxeles de espacio horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>Paso 3: Registrar propiedades personalizadas y diseño para el tipo de archivo

Una vez que comprenda el modo resultado de la búsqueda, el modo Examinar y los patrones de diseño, puede registrar una lista de propiedades personalizadas para el tipo de archivo.

**Para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo.**

1.  Elija entre los cuatro patrones de diseño: Alfa, Beta, Gamma o Delta.
2.  Tenga en cuenta las siguientes reglas de formato, que se aplican igualmente a los cuatro patrones de diseño:
    -   La propiedad 1 siempre se muestra en un tamaño de fuente mayor. El tamaño de fuente grande normalmente se usa para el nombre del elemento, pero también se puede usar para el delimitador u otra propiedad de elemento.
    -   La propiedad 4 está pensada para extractos de los patrones de diseño Alfa, Beta y Gamma. Esta propiedad se asigna más espacio en esos patrones y se muestra en un color de fuente gris, en lugar del negro como las otras propiedades, para ayudar a destacar.
    -   Las medidas de píxel siguientes están en píxeles relativos y el tamaño incluye el icono o miniatura a la izquierda de las propiedades y el espacio entre el icono o miniatura y el rectángulo de selección.
    -   La mayoría de las propiedades tienen un tamaño de presentación mínimo. Por lo tanto, no aparecerán si no hay suficiente espacio para ellos en un tamaño de vista determinado. El tamaño mínimo suele ser de 100 píxeles de ancho.
    -   Cada patrón de diseño define el número de filas y el número de propiedades de cada fila.
3.  Decida qué propiedades desea mostrar en el diseño y qué propiedad desea mostrar en cada ubicación. Al decidir qué propiedad se va a mostrar en cada posición del diseño, tenga en cuenta la longitud típica de la propiedad, su importancia para el usuario y si se debe descartar cuando el tamaño de la ventana sea demasiado pequeño para contener todas las propiedades.
4.  Registre un patrón de diseño y una lista de propiedades para el tipo de archivo o el tipo de elemento agregando las siguientes claves en la clave del Registro ProgID para el tipo de archivo o elemento (en este ejemplo, para el tipo de archivo .xyz).

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  Observe las siguientes directrices de formato para registrar propiedades:

    -   Cada registro comienza por `prop:`
    -   Cada propiedad requiere el nombre completo de la propiedad.
    -   Las propiedades están separadas por un punto y coma sin espacio.
    -   Las propiedades se muestran en el orden definido por el patrón de diseño seleccionado.
    -   `~` indica que no se debe mostrar la etiqueta de propiedad.
    -   `~System.LayoutPattern.PlaceHolder` debe usarse si desea dejar en blanco una propiedad especificada en el patrón de diseño.

    La siguiente clave del Registro de ejemplo ilustra estas directrices de formato.

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    Entre los valores posibles de (ContentViewModeForBrowse) se incluyen los siguientes: prop:~System.ItemNameDisplay; System.Author; System.LayoutPattern.Placeholder; System.Keywords; System.DateModified; ~System.Size

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Nombres de tipo](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
