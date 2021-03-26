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
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="ea2da-103">Cómo registrar un conjunto de vistas de contenido único de propiedades y patrones de diseño para el tipo de archivo o el elemento</span><span class="sxs-lookup"><span data-stu-id="ea2da-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="ea2da-104">Puede registrar una lista de propiedades de vista de contenido única y un patrón de diseño para el tipo de archivo o el elemento.</span><span class="sxs-lookup"><span data-stu-id="ea2da-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="ea2da-105">Si el tipo de archivo o el elemento también están asociados a un tipo, el registro de la vista de contenido específico del tipo de archivo o elemento invalidará el registro del tipo.</span><span class="sxs-lookup"><span data-stu-id="ea2da-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="ea2da-106">Esto puede resultar útil si las propiedades más importantes de este elemento son diferentes de otros elementos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="ea2da-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="ea2da-107">Si no asocia el tipo de archivo o el elemento a un tipo de elemento o registra directamente la vista de contenido, el sistema utiliza la información de la vista de contenido predeterminada (almacenada en una clave del registro a la que hace referencia el último elemento de la matriz de Asociación de todos los elementos, HKEY \_ clases \_ raíz \\ \* )</span><span class="sxs-lookup"><span data-stu-id="ea2da-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="ea2da-108">Antes de registrar una lista de propiedades personalizada para el tipo de archivo, debe comprender el modo de resultados de la búsqueda y el modo de exploración, y los patrones de diseño que están a su disposición.</span><span class="sxs-lookup"><span data-stu-id="ea2da-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="ea2da-109">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ea2da-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="ea2da-110">Paso 1: Descripción del modo de resultados de la búsqueda y el modo de exploración</span><span class="sxs-lookup"><span data-stu-id="ea2da-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="ea2da-111">La vista de contenido requiere la definición de un modelo de diseño y un conjunto de listas de propiedades para un elemento en un conjunto de resultados de la búsqueda (modo de resultados de búsqueda) y cuando se navega a una ubicación de Shell (modo de exploración).</span><span class="sxs-lookup"><span data-stu-id="ea2da-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="ea2da-112">Puede usar los mismos valores para el resultado de la búsqueda y examinar, como `Kind.Music` hace.</span><span class="sxs-lookup"><span data-stu-id="ea2da-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="ea2da-113">Como alternativa, puede definir una lista de propiedades y/o un patrón de diseño diferentes `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="ea2da-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="ea2da-114">En el caso de `Kind.Document` , los usuarios suelen buscar palabras en el texto del documento.</span><span class="sxs-lookup"><span data-stu-id="ea2da-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="ea2da-115">Por lo tanto, incluir más texto de ejemplo en el resultado de la búsqueda podría ser la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="ea2da-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="ea2da-116">En el ejemplo siguiente se muestra la vista de contenido de exploración de `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="ea2da-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![examinar la vista de contenido de kind.document](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="ea2da-118">Dado que los usuarios no suelen buscar texto determinado al buscar documentos, la mejor opción puede ser optimizar la elección de las propiedades y el diseño para ajustarse a más resultados de búsqueda en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ea2da-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="ea2da-119">En la captura de pantalla siguiente se muestra la vista contenido de la búsqueda de `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="ea2da-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="ea2da-120">Paso 2: Descripción de los patrones de diseño</span><span class="sxs-lookup"><span data-stu-id="ea2da-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="ea2da-121">Hay cuatro patrones de diseño: alfa, beta, gamma y Delta.</span><span class="sxs-lookup"><span data-stu-id="ea2da-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="ea2da-122">**Diseño alfa**</span><span class="sxs-lookup"><span data-stu-id="ea2da-122">**Alpha layout**</span></span>

<span data-ttu-id="ea2da-123">El patrón de diseño alfa está optimizado para los resultados de búsqueda de documentos que contienen extractos.</span><span class="sxs-lookup"><span data-stu-id="ea2da-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="ea2da-124">Tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="ea2da-124">It has the following specifications:</span></span>

-   <span data-ttu-id="ea2da-125">Filas: 4</span><span class="sxs-lookup"><span data-stu-id="ea2da-125">Rows: 4</span></span>
-   <span data-ttu-id="ea2da-126">Propiedades: 7</span><span class="sxs-lookup"><span data-stu-id="ea2da-126">Properties: 7</span></span>
-   <span data-ttu-id="ea2da-127">Diseño alfa cuando el elemento tiene 350 píxeles o más de espacio horizontal, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ea2da-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![patrón de diseño alfa](images/content-view/layout1.png)

-   <span data-ttu-id="ea2da-129">En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene 350 píxeles o más de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagrama que muestra un ejemplo de diseño alfa](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="ea2da-131">En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Captura de pantalla que muestra un ejemplo de diseño alfa en Microsoft Word.](images/content-view/layout2.png)

-   <span data-ttu-id="ea2da-133">En la ilustración siguiente se muestra el diseño alfa cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![ejemplo de diseño alfa](images/content-view/alphaviewless.png)

<span data-ttu-id="ea2da-135">**Diseño beta**</span><span class="sxs-lookup"><span data-stu-id="ea2da-135">**Beta Layout**</span></span>

<span data-ttu-id="ea2da-136">El patrón de diseño beta está optimizado para los resultados de búsqueda de documentos de correo electrónico que contienen extractos.</span><span class="sxs-lookup"><span data-stu-id="ea2da-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="ea2da-137">Tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="ea2da-137">It has the following specifications:</span></span>

-   <span data-ttu-id="ea2da-138">Filas: 4</span><span class="sxs-lookup"><span data-stu-id="ea2da-138">Rows: 4</span></span>
-   <span data-ttu-id="ea2da-139">Propiedades: 5</span><span class="sxs-lookup"><span data-stu-id="ea2da-139">Properties: 5</span></span>
-   <span data-ttu-id="ea2da-140">Diseño beta cuando el elemento tiene 350 píxeles o más de espacio horizontal, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ea2da-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagrama que muestra un ejemplo de diseño beta.](images/content-view/layout3.png)

-   <span data-ttu-id="ea2da-142">En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene 350 píxeles o más de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Captura de pantalla que muestra un ejemplo de diseño beta para el correo electrónico.](images/content-view/betaviewmore.png)

-   <span data-ttu-id="ea2da-144">En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagrama que muestra un ejemplo de diseño beta con menos de 350 píxeles de espacio horizontal.](images/content-view/layout4.png)

-   <span data-ttu-id="ea2da-146">En la ilustración siguiente se muestra el diseño beta cuando el elemento tiene menos de 350 píxeles de espacio horizontal:</span><span class="sxs-lookup"><span data-stu-id="ea2da-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![ejemplo de diseño beta](images/content-view/betaviewless.png)

<span data-ttu-id="ea2da-148">**Diseño gamma**</span><span class="sxs-lookup"><span data-stu-id="ea2da-148">**Gamma Layout**</span></span>

<span data-ttu-id="ea2da-149">El patrón de diseño gamma es similar a alfa, pero usa un diseño de dos líneas en lugar de cuatro.</span><span class="sxs-lookup"><span data-stu-id="ea2da-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="ea2da-150">Este diseño es idóneo para los escenarios en los que desea ver un fragmento de código pero desea ajustar más elementos en la pantalla, o para los tipos de archivo que requieren menos espacio para mostrar la información más crítica.</span><span class="sxs-lookup"><span data-stu-id="ea2da-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="ea2da-151">El diseño gamma tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="ea2da-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="ea2da-152">Filas: 2</span><span class="sxs-lookup"><span data-stu-id="ea2da-152">Rows: 2</span></span>
-   <span data-ttu-id="ea2da-153">Propiedades: 4</span><span class="sxs-lookup"><span data-stu-id="ea2da-153">Properties: 4</span></span>
-   <span data-ttu-id="ea2da-154">En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene 350 píxeles o más de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagrama que muestra un ejemplo de diseño gamma.](images/content-view/layout5.png)

-   <span data-ttu-id="ea2da-156">En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene 350 píxeles o más de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Captura de pantalla que muestra un ejemplo de diseño gamma para un elemento de lista de comprobación.](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="ea2da-158">En la ilustración siguiente se muestra el diseño gamma cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagrama que muestra un ejemplo de diseño gamma con menos de 350 píxeles de espacio horizontal.](images/content-view/layout6.png)

-   <span data-ttu-id="ea2da-160">Ejemplo del diseño gamma cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![ejemplo de diseño gamma](images/content-view/gammaviewless.png)

<span data-ttu-id="ea2da-162">**Diseño Delta**</span><span class="sxs-lookup"><span data-stu-id="ea2da-162">**Delta Layout**</span></span>

<span data-ttu-id="ea2da-163">El patrón de diseño Delta está optimizado para mostrar muchas propiedades más cortas como la música y las imágenes.</span><span class="sxs-lookup"><span data-stu-id="ea2da-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="ea2da-164">Tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="ea2da-164">It has the following specifications:</span></span>

-   <span data-ttu-id="ea2da-165">Filas: 2</span><span class="sxs-lookup"><span data-stu-id="ea2da-165">Rows: 2</span></span>
-   <span data-ttu-id="ea2da-166">Propiedades: 6</span><span class="sxs-lookup"><span data-stu-id="ea2da-166">Properties: 6</span></span>
-   <span data-ttu-id="ea2da-167">Diseño Delta cuando el elemento tiene 700 píxeles o más de espacio horizontal, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ea2da-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagrama que muestra un ejemplo de diseño Delta.](images/content-view/layout7.png)

-   <span data-ttu-id="ea2da-169">Ejemplo del diseño Delta cuando el elemento tiene 700 píxeles o más de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![Captura de pantalla que muestra un ejemplo de diseño Delta para un archivo de música.](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="ea2da-171">Diseño Delta cuando el elemento tiene entre 350 y 700 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Diagrama que muestra un ejemplo de diseño Delta que tiene entre 350 y 700 píxeles de espacio horizontal.](images/content-view/layout8.png)

-   <span data-ttu-id="ea2da-173">Ejemplo del diseño Delta cuando el elemento tiene entre 350 y 700 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![ejemplo de diseño Delta](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="ea2da-175">Diseño Delta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![ejemplo de diseño](images/content-view/layout9.png)

-   <span data-ttu-id="ea2da-177">Ejemplo del diseño Delta cuando el elemento tiene menos de 350 píxeles de espacio horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea2da-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Captura de pantalla que muestra un ejemplo de diseño Delta para un archivo de música que tiene menos de 350 píxeles de espacio horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="ea2da-179">Paso 3: registro de las propiedades personalizadas y el diseño del tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="ea2da-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="ea2da-180">Una vez que comprenda el modo de resultados de la búsqueda, el modo de exploración y los patrones de diseño, puede registrar una lista de propiedades personalizada para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="ea2da-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="ea2da-181">**Para registrar una lista de propiedades personalizadas y un modelo de diseño para el tipo de archivo.**</span><span class="sxs-lookup"><span data-stu-id="ea2da-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="ea2da-182">Elija entre los cuatro patrones de diseño: alfa, beta, gamma o delta.</span><span class="sxs-lookup"><span data-stu-id="ea2da-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="ea2da-183">Tenga en cuenta las siguientes reglas de formato, que se aplican igualmente a los cuatro patrones de diseño:</span><span class="sxs-lookup"><span data-stu-id="ea2da-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="ea2da-184">La propiedad 1 siempre se muestra en un tamaño de fuente mayor.</span><span class="sxs-lookup"><span data-stu-id="ea2da-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="ea2da-185">Tamaño de fuente grande que se suele usar para el nombre de elemento, pero también se puede usar para la propiedad de delimitador u otro elemento.</span><span class="sxs-lookup"><span data-stu-id="ea2da-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="ea2da-186">La propiedad 4 está pensada para los extractos de los patrones de diseño alfa, beta y gamma.</span><span class="sxs-lookup"><span data-stu-id="ea2da-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="ea2da-187">Esta propiedad tiene más espacio en esos patrones y se muestra en un color de fuente gris, en lugar de negro como el resto de las propiedades, para ayudarlo a resaltar.</span><span class="sxs-lookup"><span data-stu-id="ea2da-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="ea2da-188">Las medidas de píxeles que se muestran a continuación se encuentran en píxeles relativos y el tamaño incluye el icono o la miniatura a la izquierda de las propiedades y el espacio entre el icono o la miniatura y el rectángulo de selección.</span><span class="sxs-lookup"><span data-stu-id="ea2da-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="ea2da-189">La mayoría de las propiedades tienen un tamaño mínimo de presentación.</span><span class="sxs-lookup"><span data-stu-id="ea2da-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="ea2da-190">Por lo tanto, no aparecerán si no hay espacio suficiente para ellos en un tamaño de vista determinado.</span><span class="sxs-lookup"><span data-stu-id="ea2da-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="ea2da-191">El tamaño mínimo suele ser de 100 píxeles de ancho.</span><span class="sxs-lookup"><span data-stu-id="ea2da-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="ea2da-192">Cada modelo de diseño define el número de filas y el número de propiedades de cada fila.</span><span class="sxs-lookup"><span data-stu-id="ea2da-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="ea2da-193">Decida qué propiedades desea mostrar en el diseño y qué propiedad desea mostrar en cada ubicación.</span><span class="sxs-lookup"><span data-stu-id="ea2da-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="ea2da-194">A la hora de decidir qué propiedad Mostrar en cada posición del diseño, tenga en cuenta la longitud típica de la propiedad, su importancia para el usuario y si se debe quitar cuando el tamaño de la ventana sea demasiado pequeño para contener todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea2da-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="ea2da-195">Registre un patrón de diseño y una lista de propiedades para el tipo de archivo o el tipo de elemento agregando las siguientes claves en la clave del registro ProgID para el tipo de archivo o elemento (en este ejemplo, para el tipo de archivo. XYZ).</span><span class="sxs-lookup"><span data-stu-id="ea2da-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="ea2da-196">Observe las siguientes directrices de formato para registrar propiedades:</span><span class="sxs-lookup"><span data-stu-id="ea2da-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="ea2da-197">Cada registro comienza con `prop:`</span><span class="sxs-lookup"><span data-stu-id="ea2da-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="ea2da-198">Cada propiedad requiere el nombre completo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="ea2da-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="ea2da-199">Las propiedades se separan con un punto y coma sin espacio.</span><span class="sxs-lookup"><span data-stu-id="ea2da-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="ea2da-200">Las propiedades se muestran en el orden definido por el patrón de diseño seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ea2da-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="ea2da-201">`~` indica que no se debe mostrar la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ea2da-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="ea2da-202">`~System.LayoutPattern.PlaceHolder` debe usarse si se desea dejar en blanco una propiedad que se especifica en el patrón de diseño.</span><span class="sxs-lookup"><span data-stu-id="ea2da-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="ea2da-203">En la clave del registro de ejemplo siguiente se muestran estas instrucciones de formato.</span><span class="sxs-lookup"><span data-stu-id="ea2da-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="ea2da-204">Entre los valores posibles de (ContentViewModeForBrowse) se incluyen los siguientes: prop: ~ System. ItemNameDisplay; System. Author; System. LayoutPattern. PlaceHolder; System. keywords; System. DateModified; ~ System. Size</span><span class="sxs-lookup"><span data-stu-id="ea2da-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="ea2da-205">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea2da-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea2da-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea2da-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea2da-207">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="ea2da-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="ea2da-208">Nombres de tipos</span><span class="sxs-lookup"><span data-stu-id="ea2da-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="ea2da-209">System. proplist. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="ea2da-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="ea2da-210">System. proplist. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="ea2da-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
