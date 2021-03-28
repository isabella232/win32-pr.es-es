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
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="23031-103">Cómo registrar propiedades personalizadas y diseño para el tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="23031-103">How to Register Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="23031-104">Una vez que comprenda el modo de resultados de la búsqueda, el modo de exploración y los patrones de diseño, puede registrar una lista de propiedades personalizada para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="23031-104">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="23031-105">Para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="23031-105">To register a custom property list and layout pattern for your file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="23031-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="23031-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="23031-107">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="23031-107">Step 1:</span></span>

<span data-ttu-id="23031-108">Elija entre los cuatro patrones de diseño: alfa, beta, gamma o delta.</span><span class="sxs-lookup"><span data-stu-id="23031-108">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>

### <a name="step-2"></a><span data-ttu-id="23031-109">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="23031-109">Step 2:</span></span>

<span data-ttu-id="23031-110">Tenga en cuenta las siguientes reglas de formato, que se aplican igualmente a los cuatro patrones de diseño:</span><span class="sxs-lookup"><span data-stu-id="23031-110">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>

-   <span data-ttu-id="23031-111">La propiedad 1 siempre se muestra en un tamaño de fuente mayor.</span><span class="sxs-lookup"><span data-stu-id="23031-111">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="23031-112">Tamaño de fuente grande que se suele usar para el nombre de elemento, pero también se puede usar para la propiedad de delimitador u otro elemento.</span><span class="sxs-lookup"><span data-stu-id="23031-112">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
-   <span data-ttu-id="23031-113">La propiedad 4 está pensada para los extractos de los patrones de diseño alfa, beta y gamma.</span><span class="sxs-lookup"><span data-stu-id="23031-113">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="23031-114">Esta propiedad tiene más espacio en esos patrones y se muestra en un color de fuente gris, en lugar de negro como el resto de las propiedades, para ayudarlo a resaltar.</span><span class="sxs-lookup"><span data-stu-id="23031-114">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
-   <span data-ttu-id="23031-115">Las medidas de píxeles que se muestran a continuación se encuentran en píxeles relativos y el tamaño incluye el icono o la miniatura a la izquierda de las propiedades y el espacio entre el icono o la miniatura y el rectángulo de selección.</span><span class="sxs-lookup"><span data-stu-id="23031-115">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
-   <span data-ttu-id="23031-116">La mayoría de las propiedades tienen un tamaño mínimo de presentación.</span><span class="sxs-lookup"><span data-stu-id="23031-116">Most properties have a minimum display size.</span></span> <span data-ttu-id="23031-117">Por lo tanto, no aparecerán si no hay espacio suficiente para ellos en un tamaño de vista determinado.</span><span class="sxs-lookup"><span data-stu-id="23031-117">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="23031-118">El tamaño mínimo suele ser de 100 píxeles de ancho.</span><span class="sxs-lookup"><span data-stu-id="23031-118">The minimum size is usually 100 pixels wide.</span></span>
-   <span data-ttu-id="23031-119">Cada modelo de diseño define el número de filas y el número de propiedades de cada fila.</span><span class="sxs-lookup"><span data-stu-id="23031-119">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>

### <a name="step-3"></a><span data-ttu-id="23031-120">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="23031-120">Step 3:</span></span>

<span data-ttu-id="23031-121">Decida qué propiedades desea mostrar en el diseño y qué propiedad desea mostrar en cada ubicación.</span><span class="sxs-lookup"><span data-stu-id="23031-121">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="23031-122">A la hora de decidir qué propiedad Mostrar en cada posición del diseño, tenga en cuenta la longitud típica de la propiedad, su importancia para el usuario y si se debe quitar cuando el tamaño de la ventana sea demasiado pequeño para contener todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="23031-122">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>

### <a name="step-4"></a><span data-ttu-id="23031-123">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="23031-123">Step 4:</span></span>

<span data-ttu-id="23031-124">Registre un patrón de diseño y una lista de propiedades para el tipo de archivo o el tipo de elemento agregando las siguientes claves en la clave del registro ProgID para el tipo de archivo o elemento (en este ejemplo, para el tipo de archivo. XYZ).</span><span class="sxs-lookup"><span data-stu-id="23031-124">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a><span data-ttu-id="23031-125">Paso 5:</span><span class="sxs-lookup"><span data-stu-id="23031-125">Step 5:</span></span>

<span data-ttu-id="23031-126">Observe las siguientes directrices de formato para registrar propiedades:</span><span class="sxs-lookup"><span data-stu-id="23031-126">Observe the following formatting guidelines for registering properties:</span></span>

-   <span data-ttu-id="23031-127">Cada registro comienza con `prop:`</span><span class="sxs-lookup"><span data-stu-id="23031-127">Each registration starts with `prop:`</span></span>
-   <span data-ttu-id="23031-128">Cada propiedad requiere el nombre completo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="23031-128">Each property requires the full property name.</span></span>
-   <span data-ttu-id="23031-129">Las propiedades se separan con un punto y coma sin espacio.</span><span class="sxs-lookup"><span data-stu-id="23031-129">Properties are separated by a semicolon with no space.</span></span>
-   <span data-ttu-id="23031-130">Las propiedades se muestran en el orden definido por el patrón de diseño seleccionado.</span><span class="sxs-lookup"><span data-stu-id="23031-130">Properties are displayed in the order defined by the selected layout pattern.</span></span>
-   <span data-ttu-id="23031-131">`~` indica que no se debe mostrar la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="23031-131">`~` indicates that the property label should not be displayed.</span></span>
-   <span data-ttu-id="23031-132">`~System.LayoutPattern.PlaceHolder` debe usarse si se desea dejar en blanco una propiedad que se especifica en el patrón de diseño.</span><span class="sxs-lookup"><span data-stu-id="23031-132">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

<span data-ttu-id="23031-133">En la clave del registro de ejemplo siguiente se muestran estas instrucciones de formato.</span><span class="sxs-lookup"><span data-stu-id="23031-133">The following sample registry key illustrates these formatting guidelines.</span></span>

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

<span data-ttu-id="23031-134">Entre los valores posibles de (ContentViewModeForBrowse) se incluyen los siguientes: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span><span class="sxs-lookup"><span data-stu-id="23031-134">Possible values for (ContentViewModeForBrowse) include the following: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span></span>

 

 



