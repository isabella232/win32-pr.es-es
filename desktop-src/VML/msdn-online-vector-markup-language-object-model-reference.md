---
title: Referencia del modelo de objetos VML
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078275"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="cf4be-104">Referencia del modelo de objetos VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-104">VML Object Model Reference</span></span>

<span data-ttu-id="cf4be-105">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cf4be-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cf4be-106">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cf4be-107">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cf4be-108">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="cf4be-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cf4be-109">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cf4be-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cf4be-110">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cf4be-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cf4be-111">En este tema:</span><span class="sxs-lookup"><span data-stu-id="cf4be-111">In this topic:</span></span>

-   [<span data-ttu-id="cf4be-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="cf4be-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="cf4be-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf4be-113">Example</span></span>](#example)
-   [<span data-ttu-id="cf4be-114">Configurar VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="cf4be-115">Referencia de OM de VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="cf4be-116">Elemento de forma</span><span class="sxs-lookup"><span data-stu-id="cf4be-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="cf4be-117">Subelementos del elemento de forma</span><span class="sxs-lookup"><span data-stu-id="cf4be-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="cf4be-118">Background (elemento)</span><span class="sxs-lookup"><span data-stu-id="cf4be-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="cf4be-119">Elemento extrusión</span><span class="sxs-lookup"><span data-stu-id="cf4be-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="cf4be-120">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="cf4be-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="cf4be-121">Group, elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="cf4be-122">Elemento ImageData</span><span class="sxs-lookup"><span data-stu-id="cf4be-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="cf4be-123">Path, elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="cf4be-124">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="cf4be-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="cf4be-125">Sesgar elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="cf4be-126">Elemento stroke</span><span class="sxs-lookup"><span data-stu-id="cf4be-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="cf4be-127">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="cf4be-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="cf4be-128">Tipos de datos utilizados en el modelo de objetos VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="cf4be-129">Introducción</span><span class="sxs-lookup"><span data-stu-id="cf4be-129">Introduction</span></span>

<span data-ttu-id="cf4be-130">[Lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-datetime.html) es un lenguaje basado en texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para extender HTML con el fin de Mostrar información de gráficos vectoriales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="cf4be-131">El Document Object Model VML (DOM) define una interfaz de programación para la manipulación de los elementos de documento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="cf4be-132">Esto permite al usuario crear y modificar dinámicamente gráficos vectoriales a través de una interfaz independiente de la plataforma y del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="cf4be-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="cf4be-133">DOM de VML se ajusta a la especificación [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="cf4be-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="cf4be-134">VML usa el elemento de [forma](#shape-element) como el bloque de creación básico para las imágenes de gráficos vectoriales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="cf4be-135">Una vez creada una forma, puede modificar la forma a través de atributos o de subelementos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="cf4be-136">Por ejemplo, para cambiar el color de una forma, asigne un valor de color al atributo **fillColor** .</span><span class="sxs-lookup"><span data-stu-id="cf4be-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="cf4be-137">Algunos de los atributos de una forma también son [subelementos](/windows) y tienen sus propios atributos, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf4be-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="cf4be-138">Información preliminar</span><span class="sxs-lookup"><span data-stu-id="cf4be-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="cf4be-139">Trusión</span><span class="sxs-lookup"><span data-stu-id="cf4be-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="cf4be-140">Fill</span><span class="sxs-lookup"><span data-stu-id="cf4be-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="cf4be-141">Grupo</span><span class="sxs-lookup"><span data-stu-id="cf4be-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="cf4be-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="cf4be-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="cf4be-143">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="cf4be-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="cf4be-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="cf4be-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="cf4be-145">Sesgar</span><span class="sxs-lookup"><span data-stu-id="cf4be-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="cf4be-146">Stroke</span><span class="sxs-lookup"><span data-stu-id="cf4be-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="cf4be-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="cf4be-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="cf4be-148">El modelo de objetos de VML usa varios [tipos de datos](/windows) para definir parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf4be-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="cf4be-149">Los tipos de objeto que tienen el prefijo "VG" son enumeraciones y los que tienen el prefijo "IVg" son objetos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="cf4be-150">Haga clic aquí para obtener una lista.</span><span class="sxs-lookup"><span data-stu-id="cf4be-150">Click here for a list.</span></span> <span data-ttu-id="cf4be-151">Los tipos de información secundarios se enumeran con parámetros específicos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="cf4be-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf4be-152">Example</span></span>

<span data-ttu-id="cf4be-153">El siguiente código VBScript muestra cómo crear una forma simple:</span><span class="sxs-lookup"><span data-stu-id="cf4be-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="cf4be-154">En el ejemplo anterior, se crea una forma mediante el método Document Object Model **createElement**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="cf4be-155">La forma es una forma Rect predefinida de VML.</span><span class="sxs-lookup"><span data-stu-id="cf4be-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="cf4be-156">Aunque existe el objeto, no puede formar parte del documento hasta que se adjunte al documento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="cf4be-157">Con el método **appendChild** , el Rect se convierte en un elemento secundario de un elemento **div** denominado MyDiv.</span><span class="sxs-lookup"><span data-stu-id="cf4be-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="cf4be-158">Algunos atributos de estilo mínimos (**posición**, **ancho**, **alto**, **superior**, **izquierda**) se establecen para dar a la forma un tamaño específico.</span><span class="sxs-lookup"><span data-stu-id="cf4be-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="cf4be-159">Por último, se asigna un color con el atributo **fillColor** .</span><span class="sxs-lookup"><span data-stu-id="cf4be-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="cf4be-160">Tenga en cuenta que se puede usar cualquier lenguaje de scripting o cualquier lenguaje que pueda trabajar con interfaces Document Object Model.</span><span class="sxs-lookup"><span data-stu-id="cf4be-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="cf4be-161">Configurar VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-161">Setting up VML</span></span>

<span data-ttu-id="cf4be-162">Una implementación de VML se realiza a través de Microsoft Internet Explorer 5,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="cf4be-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="cf4be-163">Para configurar correctamente el objeto de representación en una página web, se deben realizar las siguientes adiciones:</span><span class="sxs-lookup"><span data-stu-id="cf4be-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="cf4be-164">El esquema se debe configurar en la</span><span class="sxs-lookup"><span data-stu-id="cf4be-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="cf4be-165">como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cf4be-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="cf4be-166">El comportamiento de representación debe formar parte del estilo del documento:</span><span class="sxs-lookup"><span data-stu-id="cf4be-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="cf4be-167">A continuación se muestra una página web HTML de ejemplo configurada correctamente para VML que muestra la creación dinámica de una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="cf4be-168">Tenga en cuenta que en las versiones beta, se necesitaba una etiqueta de objeto ActiveX y un estilo de comportamiento diferente.</span><span class="sxs-lookup"><span data-stu-id="cf4be-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="cf4be-169">Referencia de OM de VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-169">VML OM Reference</span></span>

<span data-ttu-id="cf4be-170">Esta referencia define el elemento de [forma](#shape-element) , los [subelementos](/windows)y los [tipos de datos](/windows) que usa el modelo de objetos de VML.</span><span class="sxs-lookup"><span data-stu-id="cf4be-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="cf4be-171">Elemento de forma</span><span class="sxs-lookup"><span data-stu-id="cf4be-171">Shape element</span></span>

<span data-ttu-id="cf4be-172">Las formas son los bloques de creación de las imágenes gráficas definidas por Lenguaje de marcado de vectores (VML).</span><span class="sxs-lookup"><span data-stu-id="cf4be-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="cf4be-173">La forma es el elemento de nivel superior y varios subelementos ayudan a definir la naturaleza de cada forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="cf4be-174">VML proporciona formas predefinidas:</span><span class="sxs-lookup"><span data-stu-id="cf4be-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="cf4be-175">**Atributos de forma**</span><span class="sxs-lookup"><span data-stu-id="cf4be-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="cf4be-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="cf4be-176">**Arc**</span></span>
-   <span data-ttu-id="cf4be-177">**Sensible**</span><span class="sxs-lookup"><span data-stu-id="cf4be-177">**Curve**</span></span>
-   <span data-ttu-id="cf4be-178">**Line**</span><span class="sxs-lookup"><span data-stu-id="cf4be-178">**Line**</span></span>
-   <span data-ttu-id="cf4be-179">**PolyLine**</span><span class="sxs-lookup"><span data-stu-id="cf4be-179">**PolyLine**</span></span>
-   <span data-ttu-id="cf4be-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="cf4be-180">**Rect**</span></span>
-   <span data-ttu-id="cf4be-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="cf4be-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-182">Ajustar</span><span class="sxs-lookup"><span data-stu-id="cf4be-182">Adj</span></span>          | <span data-ttu-id="cf4be-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="cf4be-184">Una lista delimitada por comas de números que son los parámetros de las fórmulas de la guía que definen la ruta de acceso de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="cf4be-185">Se pueden omitir los valores para permitir el uso de los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="cf4be-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="cf4be-186">Puede haber hasta 8 valores de ajuste.</span><span class="sxs-lookup"><span data-stu-id="cf4be-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="cf4be-187">Alt</span><span class="sxs-lookup"><span data-stu-id="cf4be-187">Alt</span></span>          | <span data-ttu-id="cf4be-188">String.</span><span class="sxs-lookup"><span data-stu-id="cf4be-188">String.</span></span> <span data-ttu-id="cf4be-189">Texto alternativo asociado con la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-189">Alternative text associated with shape.</span></span> <span data-ttu-id="cf4be-190">Se usa para la exploración no gráfica.</span><span class="sxs-lookup"><span data-stu-id="cf4be-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cf4be-191">Botón</span><span class="sxs-lookup"><span data-stu-id="cf4be-191">Button</span></span>       | <span data-ttu-id="cf4be-192">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-193">Muestra el comportamiento del botón al hacer clic.</span><span class="sxs-lookup"><span data-stu-id="cf4be-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cf4be-194">BWMode</span><span class="sxs-lookup"><span data-stu-id="cf4be-194">BWMode</span></span>       | <span data-ttu-id="cf4be-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="cf4be-196">Determina cómo se representará la forma en la vista de blanco y negro en las aplicaciones o cuando se imprima en impresoras en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="cf4be-197">Los valores incluyen: **color**, **auto**, **escala de grises**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undrawan**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="cf4be-198">Valor predeterminado: **auto**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="cf4be-199">BWNormal</span><span class="sxs-lookup"><span data-stu-id="cf4be-199">BWNormal</span></span>     | <span data-ttu-id="cf4be-200">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="cf4be-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="cf4be-201">Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en blanco y negro normales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="cf4be-202">Los valores incluyen: **color**, **auto**, **escala de grises**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undrawan**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="cf4be-203">Valor predeterminado: **auto**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="cf4be-204">BWPure</span><span class="sxs-lookup"><span data-stu-id="cf4be-204">BWPure</span></span>       | <span data-ttu-id="cf4be-205">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="cf4be-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="cf4be-206">Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en B/W puro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="cf4be-207">Los valores incluyen: **color**, **auto**, **escala de grises**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undrawan**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="cf4be-208">Valor predeterminado: **auto**.</span><span class="sxs-lookup"><span data-stu-id="cf4be-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="cf4be-209">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="cf4be-209">ChildShapes</span></span>  | <span data-ttu-id="cf4be-210">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="cf4be-210">IVgGroupShapes.</span></span> <span data-ttu-id="cf4be-211">Colección de otras formas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="cf4be-212">Esta colección admite los métodos de longitud y elemento estándar.</span><span class="sxs-lookup"><span data-stu-id="cf4be-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cf4be-213">Chromakey</span><span class="sxs-lookup"><span data-stu-id="cf4be-213">Chromakey</span></span>    | <span data-ttu-id="cf4be-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="cf4be-215">Un valor de color que será transparente y mostrará todo lo que hay detrás de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cf4be-216">Control1</span><span class="sxs-lookup"><span data-stu-id="cf4be-216">Control1</span></span>     | <span data-ttu-id="cf4be-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-218">Punto de control de la curva.</span><span class="sxs-lookup"><span data-stu-id="cf4be-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cf4be-219">Control2</span><span class="sxs-lookup"><span data-stu-id="cf4be-219">Control2</span></span>     | <span data-ttu-id="cf4be-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-221">Punto de control de la curva.</span><span class="sxs-lookup"><span data-stu-id="cf4be-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cf4be-222">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="cf4be-222">CoordOrigin</span></span>  | <span data-ttu-id="cf4be-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordenadas en la esquina superior izquierda del rectángulo del contenedor.</span><span class="sxs-lookup"><span data-stu-id="cf4be-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="cf4be-224">Oscila entre 0 y infinito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="cf4be-225">CoordSize</span><span class="sxs-lookup"><span data-stu-id="cf4be-225">CoordSize</span></span>    | <span data-ttu-id="cf4be-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-227">Ancho y alto del espacio de coordenadas dentro del rectángulo de referencia de esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="cf4be-228">Si no se especifica, es el mismo que el ancho y el alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="cf4be-229">Oscila entre 0 y infinito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-229">Range from 0 to infinity.</span></span> <span data-ttu-id="cf4be-230">Valor predeterminado: "1000, 1000".</span><span class="sxs-lookup"><span data-stu-id="cf4be-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="cf4be-231">Inpendientes</span><span class="sxs-lookup"><span data-stu-id="cf4be-231">EndAngle</span></span>     | <span data-ttu-id="cf4be-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="cf4be-233">Ángulo final de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cf4be-234">Trusión</span><span class="sxs-lookup"><span data-stu-id="cf4be-234">Extrusion</span></span>    | <span data-ttu-id="cf4be-235">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="cf4be-235">IVgExtrusion.</span></span> <span data-ttu-id="cf4be-236">Especifica el valor del objeto de extrusión para esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="cf4be-237">Vea el elemento [extrusión](msdn-online-vml-extrusion-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf4be-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="cf4be-238">Fill</span><span class="sxs-lookup"><span data-stu-id="cf4be-238">Fill</span></span>         | <span data-ttu-id="cf4be-239">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="cf4be-239">VgFillFormat.</span></span> <span data-ttu-id="cf4be-240">Especifica el valor de relleno para esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="cf4be-241">Vea el elemento [Fill](msdn-online-vml-fill-element.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="cf4be-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="cf4be-242">Relleno</span><span class="sxs-lookup"><span data-stu-id="cf4be-242">FillColor</span></span>    | <span data-ttu-id="cf4be-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="cf4be-244">Color principal del pincel que se va a usar para rellenar la ruta de acceso de esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cf4be-245">Has</span><span class="sxs-lookup"><span data-stu-id="cf4be-245">Filled</span></span>       | <span data-ttu-id="cf4be-246">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-247">Si es true, se rellenará la ruta de acceso que define la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="cf4be-248">De forma predeterminada, se rellenará con un color sólido a menos que haya un subelemento Fill que especifique propiedades de relleno más complejas.</span><span class="sxs-lookup"><span data-stu-id="cf4be-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="cf4be-249">Si es false, el relleno es transparente.</span><span class="sxs-lookup"><span data-stu-id="cf4be-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="cf4be-250">Voltear</span><span class="sxs-lookup"><span data-stu-id="cf4be-250">Flip</span></span>         | <span data-ttu-id="cf4be-251">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="cf4be-251">VgFlipOrientation.</span></span> <span data-ttu-id="cf4be-252">Los valores son: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="cf4be-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cf4be-253">ForceDash</span><span class="sxs-lookup"><span data-stu-id="cf4be-253">ForceDash</span></span>    | <span data-ttu-id="cf4be-254">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-255">Indica que se debe representar un contorno discontinuo cuando no haya ninguna línea y sin relleno para una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="cf4be-256">Este comportamiento suele ser útil para hacer que las formas invisibles estén visibles en la edición de aplicaciones para que se puedan seleccionar y gestionar, como en un mapa de imágenes.</span><span class="sxs-lookup"><span data-stu-id="cf4be-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="cf4be-257">Fórmulas</span><span class="sxs-lookup"><span data-stu-id="cf4be-257">Formulas</span></span>     | <span data-ttu-id="cf4be-258">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="cf4be-258">IVgFormulas.</span></span> <span data-ttu-id="cf4be-259">Matriz de fórmulas que define una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cf4be-260">From</span><span class="sxs-lookup"><span data-stu-id="cf4be-260">From</span></span>         | <span data-ttu-id="cf4be-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-262">Punto inicial de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cf4be-263">Referencia</span><span class="sxs-lookup"><span data-stu-id="cf4be-263">HRef</span></span>         | <span data-ttu-id="cf4be-264">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-265">Dirección URL a la que se va a saltar si se hace clic en esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cf4be-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="cf4be-266">ImageData</span></span>    | <span data-ttu-id="cf4be-267">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="cf4be-267">IVgImageData.</span></span> <span data-ttu-id="cf4be-268">Información de imagen si la forma es una imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="cf4be-269">Vea el elemento ImageData para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf4be-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cf4be-270">OnEd</span><span class="sxs-lookup"><span data-stu-id="cf4be-270">OnEd</span></span>         | <span data-ttu-id="cf4be-271">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-272">Oculta todos los identificadores excepto la parte superior izquierda e inferior derecha, como en los controladores de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="cf4be-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="cf4be-273">Opacidad</span><span class="sxs-lookup"><span data-stu-id="cf4be-273">Opacity</span></span>      | <span data-ttu-id="cf4be-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="cf4be-275">Opacidad de la forma completa.</span><span class="sxs-lookup"><span data-stu-id="cf4be-275">The opacity of the entire shape.</span></span> <span data-ttu-id="cf4be-276">Un número entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="cf4be-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cf4be-277">Ruta</span><span class="sxs-lookup"><span data-stu-id="cf4be-277">Path</span></span>         | <span data-ttu-id="cf4be-278">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="cf4be-278">IVgPath.</span></span> <span data-ttu-id="cf4be-279">Cadena que contiene los comandos que definen la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf4be-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cf4be-280">Puntos</span><span class="sxs-lookup"><span data-stu-id="cf4be-280">Points</span></span>       | <span data-ttu-id="cf4be-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="cf4be-282">Colección de puntos que definen una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cf4be-283">Impresión</span><span class="sxs-lookup"><span data-stu-id="cf4be-283">Print</span></span>        | <span data-ttu-id="cf4be-284">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-285">Si es true, esta forma está pensada para imprimirse.</span><span class="sxs-lookup"><span data-stu-id="cf4be-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf4be-286">Rotación</span><span class="sxs-lookup"><span data-stu-id="cf4be-286">Rotation</span></span>     | <span data-ttu-id="cf4be-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="cf4be-288">Establece la rotación de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-288">Sets rotation of shape.</span></span> <span data-ttu-id="cf4be-289">El valor se propaga al estilo de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="cf4be-290">Escala</span><span class="sxs-lookup"><span data-stu-id="cf4be-290">Scale</span></span>        | <span data-ttu-id="cf4be-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-292">Escala de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cf4be-293">Shadow</span><span class="sxs-lookup"><span data-stu-id="cf4be-293">Shadow</span></span>       | <span data-ttu-id="cf4be-294">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="cf4be-294">IVgShadow.</span></span> <span data-ttu-id="cf4be-295">Especifica la sombra para esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="cf4be-296">Vea el elemento [Shadow](msdn-online-vml-shadow-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf4be-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf4be-297">Corta</span><span class="sxs-lookup"><span data-stu-id="cf4be-297">Spt</span></span>          | <span data-ttu-id="cf4be-298">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf4be-299">StartAngle</span><span class="sxs-lookup"><span data-stu-id="cf4be-299">StartAngle</span></span>   | <span data-ttu-id="cf4be-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="cf4be-301">Ángulo inicial de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf4be-302">Carrera</span><span class="sxs-lookup"><span data-stu-id="cf4be-302">Stroke</span></span>       | <span data-ttu-id="cf4be-303">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="cf4be-303">VgStrokeFormat.</span></span> <span data-ttu-id="cf4be-304">Vea Stroke (elemento) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf4be-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cf4be-305">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="cf4be-305">StrokeColor</span></span>  | <span data-ttu-id="cf4be-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="cf4be-307">Color principal del pincel que se va a usar para trazar la ruta de acceso de esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="cf4be-308">Traza</span><span class="sxs-lookup"><span data-stu-id="cf4be-308">Stroked</span></span>      | <span data-ttu-id="cf4be-309">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-310">Si es true, se trazará la ruta de acceso que define la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cf4be-311">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="cf4be-311">StrokeWeight</span></span> | <span data-ttu-id="cf4be-312">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="cf4be-313">Ancho del pincel que se va a usar para trazar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf4be-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="cf4be-314">Oscila entre 0 y 1584.</span><span class="sxs-lookup"><span data-stu-id="cf4be-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cf4be-315">TextPath</span><span class="sxs-lookup"><span data-stu-id="cf4be-315">TextPath</span></span>     | <span data-ttu-id="cf4be-316">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="cf4be-316">IVgTextPath.</span></span> <span data-ttu-id="cf4be-317">Especifica el objeto TextPath de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="cf4be-318">Vea el elemento [TextPath](msdn-online-vml-textpath-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf4be-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="cf4be-319">En</span><span class="sxs-lookup"><span data-stu-id="cf4be-319">To</span></span>           | <span data-ttu-id="cf4be-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-321">Punto final de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf4be-322">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-322">Type</span></span>         | <span data-ttu-id="cf4be-323">String.</span><span class="sxs-lookup"><span data-stu-id="cf4be-323">String.</span></span> <span data-ttu-id="cf4be-324">Tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="cf4be-325">Subelementos del elemento de forma</span><span class="sxs-lookup"><span data-stu-id="cf4be-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="cf4be-326">Los siguientes subelementos forman parte del modelo de objetos de VML.</span><span class="sxs-lookup"><span data-stu-id="cf4be-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="cf4be-327">Información preliminar</span><span class="sxs-lookup"><span data-stu-id="cf4be-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="cf4be-328">Trusión</span><span class="sxs-lookup"><span data-stu-id="cf4be-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="cf4be-329">Fill</span><span class="sxs-lookup"><span data-stu-id="cf4be-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="cf4be-330">Grupo</span><span class="sxs-lookup"><span data-stu-id="cf4be-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="cf4be-331">Imagedata</span><span class="sxs-lookup"><span data-stu-id="cf4be-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="cf4be-332">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="cf4be-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="cf4be-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="cf4be-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="cf4be-334">Sesgar</span><span class="sxs-lookup"><span data-stu-id="cf4be-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="cf4be-335">Stroke</span><span class="sxs-lookup"><span data-stu-id="cf4be-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="cf4be-336">TextPath</span><span class="sxs-lookup"><span data-stu-id="cf4be-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="cf4be-337">Background (elemento)</span><span class="sxs-lookup"><span data-stu-id="cf4be-337">Background element</span></span>

<span data-ttu-id="cf4be-338">Describe el relleno del fondo de una página mediante los rellenos de VML.</span><span class="sxs-lookup"><span data-stu-id="cf4be-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="cf4be-339">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-340">BWMode</span><span class="sxs-lookup"><span data-stu-id="cf4be-340">BWMode</span></span>    | <span data-ttu-id="cf4be-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="cf4be-342">Determina cómo se representará la forma en la vista de blanco y negro en las aplicaciones o cuando se imprima.</span><span class="sxs-lookup"><span data-stu-id="cf4be-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="cf4be-343">BWNormal</span><span class="sxs-lookup"><span data-stu-id="cf4be-343">BWNormal</span></span>  | <span data-ttu-id="cf4be-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="cf4be-345">Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en blanco y negro normales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="cf4be-346">BWPure</span><span class="sxs-lookup"><span data-stu-id="cf4be-346">BWPure</span></span>    | <span data-ttu-id="cf4be-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="cf4be-348">Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en blanco y negro puros.</span><span class="sxs-lookup"><span data-stu-id="cf4be-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="cf4be-349">Fill</span><span class="sxs-lookup"><span data-stu-id="cf4be-349">Fill</span></span>      | <span data-ttu-id="cf4be-350">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="cf4be-350">VgFillFormat.</span></span> <span data-ttu-id="cf4be-351">Especifica el relleno para esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="cf4be-352">Vea [Fill](msdn-online-vml-fill-element.md) (elemento) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf4be-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="cf4be-353">Relleno</span><span class="sxs-lookup"><span data-stu-id="cf4be-353">FillColor</span></span> | <span data-ttu-id="cf4be-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="cf4be-355">Color principal del pincel que se va a usar para rellenar la ruta de acceso de esta forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="cf4be-356">Duplicado del valor de color en el elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="cf4be-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="cf4be-357">El valor predeterminado es blanco.</span><span class="sxs-lookup"><span data-stu-id="cf4be-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="cf4be-358">Elemento extrusión</span><span class="sxs-lookup"><span data-stu-id="cf4be-358">Extrusion element</span></span>

<span data-ttu-id="cf4be-359">Describe una extrusión 3D de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="cf4be-360">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-361">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="cf4be-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="cf4be-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-363">Si es true, el centro de rotación del grupo de objetos 3D (de hecho, solo hay un objeto en el grupo) se determina automáticamente como el centro del grupo; de lo contrario, viene determinado por los parámetros RotationCenter, que son una fracción de la forma con 0, 0, 0, que es el centro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-364">Nivel de detalle</span><span class="sxs-lookup"><span data-stu-id="cf4be-364">BackDepth</span></span></td>
<td><span data-ttu-id="cf4be-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="cf4be-366">Cantidad de extrusión hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="cf4be-366">Amount of backward extrusion.</span></span> <span data-ttu-id="cf4be-367">Oscila entre 0 y 32767.</span><span class="sxs-lookup"><span data-stu-id="cf4be-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-368">Luminosidad</span><span class="sxs-lookup"><span data-stu-id="cf4be-368">Brightness</span></span></td>
<td><span data-ttu-id="cf4be-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="cf4be-370">Brillo general de la escena.</span><span class="sxs-lookup"><span data-stu-id="cf4be-370">Overall brightness of the scene.</span></span> <span data-ttu-id="cf4be-371">El valor predeterminado es &quot; 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-372">Color</span><span class="sxs-lookup"><span data-stu-id="cf4be-372">Color</span></span></td>
<td><span data-ttu-id="cf4be-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="cf4be-374">Color de la extrusión.</span><span class="sxs-lookup"><span data-stu-id="cf4be-374">The color of the extrusion.</span></span> <span data-ttu-id="cf4be-375">Solo se usa si ColorMode es personalizado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="cf4be-376">De lo contrario, establece automáticamente el color del efecto de extrusión en el mismo que el FillColor.</span><span class="sxs-lookup"><span data-stu-id="cf4be-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-377">Property</span><span class="sxs-lookup"><span data-stu-id="cf4be-377">ColorMode</span></span></td>
<td><span data-ttu-id="cf4be-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="cf4be-378">Vg3DColorMode.</span></span> <span data-ttu-id="cf4be-379">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-380">Auto (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-380">Auto (default)</span></span></li>
<li><span data-ttu-id="cf4be-381">Personalizados</span><span class="sxs-lookup"><span data-stu-id="cf4be-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-382">Difusión</span><span class="sxs-lookup"><span data-stu-id="cf4be-382">Diffusity</span></span></td>
<td><span data-ttu-id="cf4be-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="cf4be-384">La relación entre el incidente y el reflejo difuso.</span><span class="sxs-lookup"><span data-stu-id="cf4be-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="cf4be-385">Los valores inferiores a 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="cf4be-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-386">Edge</span><span class="sxs-lookup"><span data-stu-id="cf4be-386">Edge</span></span></td>
<td><span data-ttu-id="cf4be-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="cf4be-388">Establece el tamaño de un borde biselado redondeado simulado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="cf4be-389">Oscila entre 0 y 32767 en el punto flotante pts.</span><span class="sxs-lookup"><span data-stu-id="cf4be-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="cf4be-390">El valor predeterminado es &quot; 1PT. &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-391">Faceta</span><span class="sxs-lookup"><span data-stu-id="cf4be-391">Facet</span></span></td>
<td><span data-ttu-id="cf4be-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="cf4be-393">Establece la faceta de la escena.</span><span class="sxs-lookup"><span data-stu-id="cf4be-393">Sets the facet of the scene.</span></span> <span data-ttu-id="cf4be-394">El valor predeterminado es &quot; 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-395">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="cf4be-395">ForeDepth</span></span></td>
<td><span data-ttu-id="cf4be-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="cf4be-397">Cantidad de extrusión hacia delante.</span><span class="sxs-lookup"><span data-stu-id="cf4be-397">Amount of forward extrusion.</span></span> <span data-ttu-id="cf4be-398">Oscila entre 0 y 32767.</span><span class="sxs-lookup"><span data-stu-id="cf4be-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-399">LightFace</span><span class="sxs-lookup"><span data-stu-id="cf4be-399">LightFace</span></span></td>
<td><span data-ttu-id="cf4be-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-401">Determimes si la cara frontal del objeto responderá a los cambios en la iluminación 3D, por ejemplo, cuando un objeto se rote.</span><span class="sxs-lookup"><span data-stu-id="cf4be-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-402">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="cf4be-402">LightHarsh</span></span></td>
<td><span data-ttu-id="cf4be-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-404">Iluminación severa para la fuente de luz principal.</span><span class="sxs-lookup"><span data-stu-id="cf4be-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="cf4be-405">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="cf4be-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="cf4be-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="cf4be-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-408">Iluminación severa para la fuente de luz secundaria.</span><span class="sxs-lookup"><span data-stu-id="cf4be-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="cf4be-409">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="cf4be-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-410">LightLevel</span><span class="sxs-lookup"><span data-stu-id="cf4be-410">LightLevel</span></span></td>
<td><span data-ttu-id="cf4be-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="cf4be-412">Intensidad de la fuente de luz principal.</span><span class="sxs-lookup"><span data-stu-id="cf4be-412">Intensity of the primary light source.</span></span> <span data-ttu-id="cf4be-413">El valor predeterminado es &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="cf4be-414">LightLevel2</span></span></td>
<td><span data-ttu-id="cf4be-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="cf4be-416">Intensidad de la fuente de luz secundaria.</span><span class="sxs-lookup"><span data-stu-id="cf4be-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="cf4be-417">El valor predeterminado es &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-418">LightPosition</span><span class="sxs-lookup"><span data-stu-id="cf4be-418">LightPosition</span></span></td>
<td><span data-ttu-id="cf4be-419">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="cf4be-419">Vector3D.</span></span> <span data-ttu-id="cf4be-420">Posición de la fuente de luz primaria.</span><span class="sxs-lookup"><span data-stu-id="cf4be-420">Position of the primary light source.</span></span> <span data-ttu-id="cf4be-421">El valor predeterminado es &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="cf4be-422">LightPosition2</span></span></td>
<td><span data-ttu-id="cf4be-423">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="cf4be-423">Vector3D.</span></span> <span data-ttu-id="cf4be-424">Posición de la fuente de luz secundaria.</span><span class="sxs-lookup"><span data-stu-id="cf4be-424">Position of the secondary light source.</span></span> <span data-ttu-id="cf4be-425">El valor predeterminado es &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-426">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="cf4be-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="cf4be-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-428">&quot;Lockrotationcenter &quot; significa que el giro del grupo se define para que sea por el ángulo de rotación [1] grados sobre el eje y en la Página seguido de un ángulo de rotación [0] grados sobre el eje x.</span><span class="sxs-lookup"><span data-stu-id="cf4be-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="cf4be-429">Cuando LockRotationCenter es false, el giro se define como por grados de ángulo de orientación sobre el vector definido por orientación.</span><span class="sxs-lookup"><span data-stu-id="cf4be-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="cf4be-430">Por lo tanto, por ejemplo, lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) es equivalente a lockrotationcenter = true RotationAngle = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="cf4be-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-431">Metal</span><span class="sxs-lookup"><span data-stu-id="cf4be-431">Metal</span></span></td>
<td><span data-ttu-id="cf4be-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-433">Hace que la luz reflejada especular sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más metálico.</span><span class="sxs-lookup"><span data-stu-id="cf4be-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-434">Activado</span><span class="sxs-lookup"><span data-stu-id="cf4be-434">On</span></span></td>
<td><span data-ttu-id="cf4be-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-436">Activa y desactiva la presentación del efecto de extrusión.</span><span class="sxs-lookup"><span data-stu-id="cf4be-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-437">Orientación</span><span class="sxs-lookup"><span data-stu-id="cf4be-437">Orientation</span></span></td>
<td><span data-ttu-id="cf4be-438">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="cf4be-438">Vector3D.</span></span> <span data-ttu-id="cf4be-439">Orientación de la cámara.</span><span class="sxs-lookup"><span data-stu-id="cf4be-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-440">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="cf4be-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="cf4be-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="cf4be-442">Ángulo entre la orientación de la cámara y el plano XY.</span><span class="sxs-lookup"><span data-stu-id="cf4be-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-443">Plano</span><span class="sxs-lookup"><span data-stu-id="cf4be-443">Plane</span></span></td>
<td><span data-ttu-id="cf4be-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="cf4be-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="cf4be-445">Permite la extrusión de los planos ortogonales al plano de pantalla.</span><span class="sxs-lookup"><span data-stu-id="cf4be-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="cf4be-446">Requiere que se especifiquen ForeDepth y postdepth en las unidades de dibujo en lugar de en emus.</span><span class="sxs-lookup"><span data-stu-id="cf4be-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="cf4be-447">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-448">XY</span><span class="sxs-lookup"><span data-stu-id="cf4be-448">XY</span></span></li>
<li><span data-ttu-id="cf4be-449">ZX</span><span class="sxs-lookup"><span data-stu-id="cf4be-449">ZX</span></span></li>
<li><span data-ttu-id="cf4be-450">YZ</span><span class="sxs-lookup"><span data-stu-id="cf4be-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-451">Representación</span><span class="sxs-lookup"><span data-stu-id="cf4be-451">Render</span></span></td>
<td><span data-ttu-id="cf4be-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="cf4be-452">Vg3DRenderMode.</span></span> <span data-ttu-id="cf4be-453">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-454">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-454">Solid (default)</span></span></li>
<li><span data-ttu-id="cf4be-455">Estructura</span><span class="sxs-lookup"><span data-stu-id="cf4be-455">WireFrame</span></span></li>
<li><span data-ttu-id="cf4be-456">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="cf4be-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-457">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="cf4be-457">RotationAngle</span></span></td>
<td><span data-ttu-id="cf4be-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-459">AngleX, AngleY o AngleZ se controla mediante el atributo ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="cf4be-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-460">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="cf4be-460">RotationCenter</span></span></td>
<td><span data-ttu-id="cf4be-461">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="cf4be-461">Vector3D.</span></span> <span data-ttu-id="cf4be-462">Centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="cf4be-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-463">Brillo</span><span class="sxs-lookup"><span data-stu-id="cf4be-463">Shininess</span></span></td>
<td><span data-ttu-id="cf4be-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="cf4be-465">Determina cómo se concentra o propaga la reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="cf4be-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="cf4be-466">Un valor alto sería de 8 a 10 y se aproximaría a un reflejo, y un valor bajo sería de 2 a 3 y se aproximaría la ropa de sequined.</span><span class="sxs-lookup"><span data-stu-id="cf4be-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="cf4be-467">Se recomiendan los valores 3 a 7.</span><span class="sxs-lookup"><span data-stu-id="cf4be-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="cf4be-468">Los valores altos reflejarán los orígenes de luz del Pinpoint.</span><span class="sxs-lookup"><span data-stu-id="cf4be-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-469">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="cf4be-469">SkewAmt</span></span></td>
<td><span data-ttu-id="cf4be-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="cf4be-471">Si el tipo es Parallel, el atributo determina la cantidad de sesgo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="cf4be-472">Oscila entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="cf4be-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-473">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="cf4be-473">SkewAngle</span></span></td>
<td><span data-ttu-id="cf4be-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="cf4be-475">Si el tipo es Parallel, el atributo determina el grado de sesgo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="cf4be-476">El valor predeterminado es &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-477">Especulación</span><span class="sxs-lookup"><span data-stu-id="cf4be-477">Specularity</span></span></td>
<td><span data-ttu-id="cf4be-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="cf4be-479">La relación del incidente con la luz reflejada especular.</span><span class="sxs-lookup"><span data-stu-id="cf4be-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="cf4be-480">Los valores inferiores a 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="cf4be-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-481">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-481">Type</span></span></td>
<td><span data-ttu-id="cf4be-482">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="cf4be-482">VgExtrusionType.</span></span> <span data-ttu-id="cf4be-483">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-484">Parallel (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="cf4be-485">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="cf4be-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-486">Cuánto</span><span class="sxs-lookup"><span data-stu-id="cf4be-486">Viewpoint</span></span></td>
<td><span data-ttu-id="cf4be-487">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="cf4be-487">Vector3D.</span></span> <span data-ttu-id="cf4be-488">El punto desde el que se está viendo la escena.</span><span class="sxs-lookup"><span data-stu-id="cf4be-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-489">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="cf4be-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="cf4be-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-491">Puede tener valores de 0,5 a-0,5 para colocar el origen del punto de vista en el cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="cf4be-492">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="cf4be-492">Fill element</span></span>

<span data-ttu-id="cf4be-493">Describe cómo se debe rellenar una ruta de acceso para los rellenos más complejos que un color sólido.</span><span class="sxs-lookup"><span data-stu-id="cf4be-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="cf4be-494">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-495">AlignShape</span><span class="sxs-lookup"><span data-stu-id="cf4be-495">AlignShape</span></span></td>
<td><span data-ttu-id="cf4be-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-497">Alinee la imagen con la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-497">Align the image with the shape.</span></span> <span data-ttu-id="cf4be-498">Si es false, alinea la imagen con la ventana.</span><span class="sxs-lookup"><span data-stu-id="cf4be-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-499">Ángulo</span><span class="sxs-lookup"><span data-stu-id="cf4be-499">Angle</span></span></td>
<td><span data-ttu-id="cf4be-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="cf4be-501">El ángulo a lo largo del que se dirige el degradado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="cf4be-502">0 grados está a lo largo del eje horizontal de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="cf4be-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-503">Aspecto</span><span class="sxs-lookup"><span data-stu-id="cf4be-503">Aspect</span></span></td>
<td><span data-ttu-id="cf4be-504"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="cf4be-505">El atributo ImageSize se ajustará para conservar el aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="cf4be-506">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="cf4be-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-507">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-507">Value</span></span></th>
<th><span data-ttu-id="cf4be-508">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-509">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cf4be-509">Ignore</span></span></td>
<td><span data-ttu-id="cf4be-510">Omitir problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-511">Al menos</span><span class="sxs-lookup"><span data-stu-id="cf4be-511">AtLeast</span></span></td>
<td><span data-ttu-id="cf4be-512">La imagen es al menos tan grande como el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-513">AtMos</span><span class="sxs-lookup"><span data-stu-id="cf4be-513">AtMost</span></span></td>
<td><span data-ttu-id="cf4be-514">La imagen no es mayor que el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-515">Color</span><span class="sxs-lookup"><span data-stu-id="cf4be-515">Color</span></span></td>
<td><span data-ttu-id="cf4be-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Color de relleno principal.</span><span class="sxs-lookup"><span data-stu-id="cf4be-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="cf4be-517">Igual que el atributo FillColor de Shape.</span><span class="sxs-lookup"><span data-stu-id="cf4be-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-518">Color2</span><span class="sxs-lookup"><span data-stu-id="cf4be-518">Color2</span></span></td>
<td><span data-ttu-id="cf4be-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="cf4be-520">Color secundario de un relleno cuando el tipo de imagen es el patrón o un relleno de degradado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-521">Colores</span><span class="sxs-lookup"><span data-stu-id="cf4be-521">Colors</span></span></td>
<td><span data-ttu-id="cf4be-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="cf4be-523">Colores intermedios del degradado y sus posiciones relativas a lo largo del degradado; por ejemplo, &quot; 30% rojo, 70% azul, 90% verde &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="cf4be-524">El color principal (atributo de color de la forma) es 0% y el color secundario (atributo color2) es 100%.</span><span class="sxs-lookup"><span data-stu-id="cf4be-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-525">Foco</span><span class="sxs-lookup"><span data-stu-id="cf4be-525">Focus</span></span></td>
<td><span data-ttu-id="cf4be-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="cf4be-527">Punto focal del relleno de degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="cf4be-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="cf4be-528">Los valores van de-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="cf4be-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-529">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="cf4be-529">FocusPosition</span></span></td>
<td><span data-ttu-id="cf4be-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-531">Posición del rectángulo más interior de los degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="cf4be-532">El vector es una fracción (0,0-1,0) del ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-533">FocusSize</span><span class="sxs-lookup"><span data-stu-id="cf4be-533">FocusSize</span></span></td>
<td><span data-ttu-id="cf4be-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamaño del rectángulo más interno de los degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="cf4be-535">El vector es una fracción (de 0,0 a 1,0) del ancho y el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-536">Método</span><span class="sxs-lookup"><span data-stu-id="cf4be-536">Method</span></span></td>
<td><span data-ttu-id="cf4be-537">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="cf4be-537">VgSigmaType.</span></span> <span data-ttu-id="cf4be-538">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="cf4be-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="cf4be-539">None</span><span class="sxs-lookup"><span data-stu-id="cf4be-539">None</span></span></li>
<li><span data-ttu-id="cf4be-540">Lineal</span><span class="sxs-lookup"><span data-stu-id="cf4be-540">Linear</span></span></li>
<li><span data-ttu-id="cf4be-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="cf4be-541">Sigma</span></span></li>
<li><span data-ttu-id="cf4be-542">Any</span><span class="sxs-lookup"><span data-stu-id="cf4be-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="cf4be-543">El valor predeterminado es Sigma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-544">Activado</span><span class="sxs-lookup"><span data-stu-id="cf4be-544">On</span></span></td>
<td><span data-ttu-id="cf4be-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-546">Activa la presentación de relleno.</span><span class="sxs-lookup"><span data-stu-id="cf4be-546">Turns fill display on.</span></span> <span data-ttu-id="cf4be-547">Igual que el atributo Fill de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-548">Opacidad</span><span class="sxs-lookup"><span data-stu-id="cf4be-548">Opacity</span></span></td>
<td><span data-ttu-id="cf4be-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="cf4be-550">Opacidad del relleno.</span><span class="sxs-lookup"><span data-stu-id="cf4be-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="cf4be-551">Opacity2</span></span></td>
<td><span data-ttu-id="cf4be-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="cf4be-553">La opacidad secundaria de los degradados.</span><span class="sxs-lookup"><span data-stu-id="cf4be-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-554">Origen</span><span class="sxs-lookup"><span data-stu-id="cf4be-554">Origin</span></span></td>
<td><span data-ttu-id="cf4be-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-556">Punto relativo a la esquina superior izquierda de la imagen que se trata como el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="cf4be-557">El valor predeterminado es el centro de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-557">Default is the center of the image.</span></span> <span data-ttu-id="cf4be-558">El vector es una fracción (de 0,0 a 1,0) del ancho y el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-559">Posición</span><span class="sxs-lookup"><span data-stu-id="cf4be-559">Position</span></span></td>
<td><span data-ttu-id="cf4be-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-561">Señale el rectángulo de referencia de la forma para colocar el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="cf4be-562">El valor predeterminado es el centro del rectángulo del contenedor.</span><span class="sxs-lookup"><span data-stu-id="cf4be-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="cf4be-563">El vector es una fracción (0,0-1,0) del ancho y el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-564">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cf4be-564">Size</span></span></td>
<td><span data-ttu-id="cf4be-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-566">Tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-566">The size of the image.</span></span> <span data-ttu-id="cf4be-567">El valor predeterminado es el tamaño en píxeles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-567">Default is pixel size of the image.</span></span> <span data-ttu-id="cf4be-568">Se puede especificar en coordenadas absolutas o en porcentaje.</span><span class="sxs-lookup"><span data-stu-id="cf4be-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-569">Origen</span><span class="sxs-lookup"><span data-stu-id="cf4be-569">Src</span></span></td>
<td><span data-ttu-id="cf4be-570"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="cf4be-571">Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón.</span><span class="sxs-lookup"><span data-stu-id="cf4be-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="cf4be-572">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-573">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-573">Type</span></span></td>
<td><span data-ttu-id="cf4be-574">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="cf4be-574">VgFillType.</span></span> <span data-ttu-id="cf4be-575">Puede ser uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="cf4be-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="cf4be-576">Información previa</span><span class="sxs-lookup"><span data-stu-id="cf4be-576">Background</span></span></li>
<li><span data-ttu-id="cf4be-577">Fotograma</span><span class="sxs-lookup"><span data-stu-id="cf4be-577">Frame</span></span></li>
<li><span data-ttu-id="cf4be-578">Degradado</span><span class="sxs-lookup"><span data-stu-id="cf4be-578">Gradient</span></span></li>
<li><span data-ttu-id="cf4be-579">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="cf4be-579">GradientCenter</span></span></li>
<li><span data-ttu-id="cf4be-580">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="cf4be-580">GradientRadial</span></span></li>
<li><span data-ttu-id="cf4be-581">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="cf4be-581">GradientTitle</span></span></li>
<li><span data-ttu-id="cf4be-582">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="cf4be-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="cf4be-583">Patrón</span><span class="sxs-lookup"><span data-stu-id="cf4be-583">Pattern</span></span></li>
<li><span data-ttu-id="cf4be-584">Sólido</span><span class="sxs-lookup"><span data-stu-id="cf4be-584">Solid</span></span></li>
<li><span data-ttu-id="cf4be-585">Tile</span><span class="sxs-lookup"><span data-stu-id="cf4be-585">Tile</span></span></li>
</ul>
<span data-ttu-id="cf4be-586">Mosaico, patrón y marco requieren que se proporcionen los atributos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="cf4be-587">Gradiente y GradientRadial requieren que se proporcionen los atributos de degradado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="cf4be-588">Group, elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-588">Group element</span></span>

<span data-ttu-id="cf4be-589">Un grupo es una colección de formas individuales que se pueden colocar y transformar como una unidad.</span><span class="sxs-lookup"><span data-stu-id="cf4be-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-590">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-590">Item</span></span>   | <span data-ttu-id="cf4be-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-592">Elemento especificado en la matriz de formas.</span><span class="sxs-lookup"><span data-stu-id="cf4be-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="cf4be-593">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-593">Length</span></span> | <span data-ttu-id="cf4be-594">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-595">Número de formas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="cf4be-596">Elemento ImageData</span><span class="sxs-lookup"><span data-stu-id="cf4be-596">Imagedata element</span></span>

<span data-ttu-id="cf4be-597">Describe una imagen que se va a representar en la parte superior de una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-598">Suavizado</span><span class="sxs-lookup"><span data-stu-id="cf4be-598">BiLevel</span></span>     | <span data-ttu-id="cf4be-599">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-600">Mostrar imagen en solo dos colores (normalmente blanco y negro).</span><span class="sxs-lookup"><span data-stu-id="cf4be-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cf4be-601">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="cf4be-601">BlackLevel</span></span>  | <span data-ttu-id="cf4be-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="cf4be-603">Permite ajustar para establecer el nivel de modo que los negros aparezcan como verdaderos negros, y todos los demás colores estén visibles como sombras por encima del negro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="cf4be-604">Chromakey</span><span class="sxs-lookup"><span data-stu-id="cf4be-604">Chromakey</span></span>   | <span data-ttu-id="cf4be-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="cf4be-606">Color transparente de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cf4be-607">CropBottom</span><span class="sxs-lookup"><span data-stu-id="cf4be-607">CropBottom</span></span>  | <span data-ttu-id="cf4be-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-609">Recortar la distancia desde la parte inferior de la imagen expresada como un porcentaje del tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="cf4be-610">CropLeft</span><span class="sxs-lookup"><span data-stu-id="cf4be-610">CropLeft</span></span>    | <span data-ttu-id="cf4be-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-612">Recortar la distancia desde el borde izquierdo de la imagen expresado como una fracción del tamaño de la imagen (de 0,0 a 1,0).</span><span class="sxs-lookup"><span data-stu-id="cf4be-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="cf4be-613">Sin embargo, se admite "out-recortar" y, por tanto, se admiten los valores menores que 0 y mayores que 1; por ejemplo,-5, 20 recortarían los límites 25X el tamaño de la imagen con 4/5 en un lado de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="cf4be-614">CropRight</span><span class="sxs-lookup"><span data-stu-id="cf4be-614">CropRight</span></span>   | <span data-ttu-id="cf4be-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-616">Recortar la distancia a la derecha de la imagen expresada como un porcentaje del tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="cf4be-617">CropTop</span><span class="sxs-lookup"><span data-stu-id="cf4be-617">CropTop</span></span>     | <span data-ttu-id="cf4be-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-619">Recortar la distancia desde la parte superior de la imagen expresada como un porcentaje del tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="cf4be-620">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="cf4be-620">EmbossColor</span></span> | <span data-ttu-id="cf4be-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="cf4be-622">Se establece en un porcentaje del color de la sombra para crear un efecto de imagen en relieve.</span><span class="sxs-lookup"><span data-stu-id="cf4be-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="cf4be-623">Beneficios</span><span class="sxs-lookup"><span data-stu-id="cf4be-623">Gain</span></span>        | <span data-ttu-id="cf4be-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-625">Ajusta la intensidad de todos los colores.</span><span class="sxs-lookup"><span data-stu-id="cf4be-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="cf4be-626">En esencia, establece cómo será el blanco brillante.</span><span class="sxs-lookup"><span data-stu-id="cf4be-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="cf4be-627">Oscila entre 0 y 32767.</span><span class="sxs-lookup"><span data-stu-id="cf4be-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="cf4be-628">Gamma</span><span class="sxs-lookup"><span data-stu-id="cf4be-628">Gamma</span></span>       | <span data-ttu-id="cf4be-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="cf4be-630">Corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-630">Gamma correction.</span></span> <span data-ttu-id="cf4be-631">Al aumentarlo, se obtiene una imagen más contrastada.</span><span class="sxs-lookup"><span data-stu-id="cf4be-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="cf4be-632">GrayScale</span><span class="sxs-lookup"><span data-stu-id="cf4be-632">GrayScale</span></span>   | <span data-ttu-id="cf4be-633">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-634">Mostrar imagen en colores de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="cf4be-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cf4be-635">Origen</span><span class="sxs-lookup"><span data-stu-id="cf4be-635">Src</span></span>         | <span data-ttu-id="cf4be-636">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-637">Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón.</span><span class="sxs-lookup"><span data-stu-id="cf4be-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="cf4be-638">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="cf4be-639">Path, elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-639">Path element</span></span>

<span data-ttu-id="cf4be-640">Define la ruta de acceso que conforma la forma usando una cadena que contiene un conjunto completo de comandos de "movimiento del lápiz".</span><span class="sxs-lookup"><span data-stu-id="cf4be-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-641">Limo</span><span class="sxs-lookup"><span data-stu-id="cf4be-641">Limo</span></span></td>
<td><span data-ttu-id="cf4be-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="cf4be-643">Define el punto en el que se estira la forma; por ejemplo, en el caso de una forma Giraffe, el punto limo sería el cuello, por lo que cuando se cambia el tamaño de la forma, el cuello se estira y el resto de la forma mantendrá sus dimensiones.</span><span class="sxs-lookup"><span data-stu-id="cf4be-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-644">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="cf4be-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="cf4be-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="cf4be-646">Matriz que contiene los rectángulos que definen dónde debe ir el texto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-647">V</span><span class="sxs-lookup"><span data-stu-id="cf4be-647">V</span></span></td>
<td><span data-ttu-id="cf4be-648"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="cf4be-649">Coincide con el atributo v de la etiqueta path.</span><span class="sxs-lookup"><span data-stu-id="cf4be-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="cf4be-650">Tenga en cuenta que la ruta de acceso puede corresponder al atributo o elemento de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf4be-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-651">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-651">Value</span></span></td>
<td><span data-ttu-id="cf4be-652"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="cf4be-653">Representación de texto de los comandos que definen la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf4be-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="cf4be-654">Los valores de la coordenada X o y pueden ser una referencia a una fórmula en el formulario &quot; @# &quot; donde # es el número ordinal de la fórmula, por ejemplo, &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="cf4be-655">Esta cadena de atributo se compone de un amplio conjunto de comandos, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf4be-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-656">Get-Help</span><span class="sxs-lookup"><span data-stu-id="cf4be-656">Command</span></span></th>
<th><span data-ttu-id="cf4be-657">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-658">AE (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="cf4be-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="cf4be-659"><strong>Center</strong>(x, y) <strong>tamaño</strong>(w, h) <strong>ángulo inicial</strong>, <strong>ángulo final</strong></span><span class="sxs-lookup"><span data-stu-id="cf4be-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="cf4be-660">Dibuja un segmento de una elipse.</span><span class="sxs-lookup"><span data-stu-id="cf4be-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="cf4be-661">Una línea recta se dibuja desde el punto actual hasta el punto inicial del segmento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-662">al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="cf4be-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="cf4be-663">Igual que AE, salvo que hay una m implícita al punto inicial del segmento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-664">ar (arco)</span><span class="sxs-lookup"><span data-stu-id="cf4be-664">ar (arc)</span></span></td>
<td><span data-ttu-id="cf4be-665">Igual que en.</span><span class="sxs-lookup"><span data-stu-id="cf4be-665">Same as at.</span></span> <span data-ttu-id="cf4be-666">Sin embargo, un nuevo subtrazado lo inicia un m implícito en el punto inicial del arco.</span><span class="sxs-lookup"><span data-stu-id="cf4be-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-667">a las (ArcTo)</span><span class="sxs-lookup"><span data-stu-id="cf4be-667">at (arcto)</span></span></td>
<td><span data-ttu-id="cf4be-668"><strong>izquierda</strong>, <strong>superior</strong>, <strong>derecha</strong>, <strong>inferior</strong>, <strong>Inicio</strong>(x, y) <strong>final</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="cf4be-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="cf4be-669">Los primeros cuatro valores definen el rectángulo de selección de una elipse.</span><span class="sxs-lookup"><span data-stu-id="cf4be-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="cf4be-670">Los cuatro últimos definen dos vectores radiales.</span><span class="sxs-lookup"><span data-stu-id="cf4be-670">The last four define two radial vectors.</span></span> <span data-ttu-id="cf4be-671">Se dibuja un segmento de la elipse que comienza en el ángulo definido por el vector de radio de inicio y termina en el ángulo definido por el vector final.</span><span class="sxs-lookup"><span data-stu-id="cf4be-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="cf4be-672">Una línea recta se dibuja desde el punto actual hasta el principio del arco. El arco siempre se dibuja en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="cf4be-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-673">c (curvato)</span><span class="sxs-lookup"><span data-stu-id="cf4be-673">c (curveto)</span></span></td>
<td><span data-ttu-id="cf4be-674"><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>a</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="cf4be-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="cf4be-675">Dibuja una curva Bézier cúbica desde el punto actual a la coordenada proporcionada por los dos parámetros finales, los puntos de control especificados por los cuatro primeros parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf4be-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="cf4be-676">El punto actual se convierte en el extremo de la curva.</span><span class="sxs-lookup"><span data-stu-id="cf4be-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-677">e (fin)</span><span class="sxs-lookup"><span data-stu-id="cf4be-677">e (end)</span></span></td>
<td><span data-ttu-id="cf4be-678">Finaliza el conjunto actual de subtrazados.</span><span class="sxs-lookup"><span data-stu-id="cf4be-678">End the current set of subpaths.</span></span> <span data-ttu-id="cf4be-679">Un conjunto determinado de subrutas (como delimitado por end) se rellenan con eofill.</span><span class="sxs-lookup"><span data-stu-id="cf4be-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="cf4be-680">Los conjuntos posteriores de subtrazados se rellenan de forma independiente y se superponen a los existentes.</span><span class="sxs-lookup"><span data-stu-id="cf4be-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-681">l (lineTo)</span><span class="sxs-lookup"><span data-stu-id="cf4be-681">l (lineto)</span></span></td>
<td><span data-ttu-id="cf4be-682">x, y</span><span class="sxs-lookup"><span data-stu-id="cf4be-682">x,y</span></span><br/> <span data-ttu-id="cf4be-683">Dibuja una línea del punto actual a la coordenada x, y determinada, que se convierte en el nuevo punto actual.</span><span class="sxs-lookup"><span data-stu-id="cf4be-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="cf4be-684">Se pueden especificar pares de coordenadas adicionales para formar una polilínea, por ejemplo, &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-685">m (moveTo)</span><span class="sxs-lookup"><span data-stu-id="cf4be-685">m (moveto)</span></span></td>
<td><span data-ttu-id="cf4be-686">x, y</span><span class="sxs-lookup"><span data-stu-id="cf4be-686">x,y</span></span><br/> <span data-ttu-id="cf4be-687">Inicia un nuevo subtrazado en la coordenada x, y dada.</span><span class="sxs-lookup"><span data-stu-id="cf4be-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-688">NF (noFill)</span><span class="sxs-lookup"><span data-stu-id="cf4be-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="cf4be-689">El conjunto actual de subtrazados (delimitados por end) no se rellenará.</span><span class="sxs-lookup"><span data-stu-id="cf4be-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-690">NS (noStroke)</span><span class="sxs-lookup"><span data-stu-id="cf4be-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="cf4be-691">No se trazará el conjunto actual de subtrazados (delimitados por end).</span><span class="sxs-lookup"><span data-stu-id="cf4be-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-692">QB (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="cf4be-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="cf4be-693">(<strong>ControlPoint</strong>(x, y)) \*,<strong>End</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="cf4be-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="cf4be-694">Define una o varias curvas Bézier cuadráticas por medio de puntos de control y un punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="cf4be-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="cf4be-695">Los puntos intermedios (en curva) se obtienen mediante la interpolación entre los puntos de control sucesivos similares a las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="cf4be-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="cf4be-696">No es necesario que el subtrazado sea un inicio, en cuyo caso el subtrazado está cerrado y el último punto define el punto inicial.</span><span class="sxs-lookup"><span data-stu-id="cf4be-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-697">QX (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="cf4be-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="cf4be-698"><strong>End</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="cf4be-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="cf4be-699">Una elipse de cuarto se dibuja desde el punto actual hasta el punto de conexión dado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="cf4be-700">Inicialmente, el segmento elíptico es tangencial a una línea paralela al eje x; es decir, el segmento comienza horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="cf4be-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-701">qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="cf4be-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="cf4be-702"><strong>End</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="cf4be-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="cf4be-703">Igual que QX, salvo que el segmento elíptico es inicialmente tangencial a una línea paralela al eje y; es decir, el segmento comienza verticalmente.</span><span class="sxs-lookup"><span data-stu-id="cf4be-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-704">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="cf4be-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="cf4be-705">x, y</span><span class="sxs-lookup"><span data-stu-id="cf4be-705">x,y</span></span> <br/> <span data-ttu-id="cf4be-706">Dibuja una línea del punto actual a la coordenada relativa (CPX + x, CPY + y).</span><span class="sxs-lookup"><span data-stu-id="cf4be-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="cf4be-707">Si se proporcionan pares de coordenadas adicionales, cada punto nuevo se calcula en relación con el último.</span><span class="sxs-lookup"><span data-stu-id="cf4be-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-708">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="cf4be-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="cf4be-709">x, y</span><span class="sxs-lookup"><span data-stu-id="cf4be-709">x,y</span></span><br/> <span data-ttu-id="cf4be-710">Inicia un nuevo subtrazado en las coordenadas relativas (CPX + x, CPY + y) donde CPX, CPY es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="cf4be-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-711">v (curvato)</span><span class="sxs-lookup"><span data-stu-id="cf4be-711">v (curveto)</span></span></td>
<td><span data-ttu-id="cf4be-712"><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>a</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="cf4be-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="cf4be-713">Curva Bézier cúbica que usa las coordenadas especificadas en relación con el punto actual.</span><span class="sxs-lookup"><span data-stu-id="cf4be-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="cf4be-714">Todos los puntos se calculan en relación con el mismo punto inicial.</span><span class="sxs-lookup"><span data-stu-id="cf4be-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-715">WA (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="cf4be-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="cf4be-716">Igual que en, pero el arco se dibuja en sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="cf4be-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-717">WR (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="cf4be-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="cf4be-718">Igual que ar pero se dibuja en sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="cf4be-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-719">x (cerrar)</span><span class="sxs-lookup"><span data-stu-id="cf4be-719">x (close)</span></span></td>
<td><span data-ttu-id="cf4be-720">Cerrar el subtrazado actual dibujando una línea recta desde el punto actual hasta el punto de movimiento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="cf4be-721">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="cf4be-721">Shadow element</span></span>

<span data-ttu-id="cf4be-722">Describe un efecto de sombra en una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-723">Color</span><span class="sxs-lookup"><span data-stu-id="cf4be-723">Color</span></span></td>
<td><span data-ttu-id="cf4be-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="cf4be-725">Color de la sombra principal.</span><span class="sxs-lookup"><span data-stu-id="cf4be-725">Color of the primary shadow.</span></span> <span data-ttu-id="cf4be-726">El valor predeterminado es RGB (128128128)</span><span class="sxs-lookup"><span data-stu-id="cf4be-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-727">Color2</span><span class="sxs-lookup"><span data-stu-id="cf4be-727">Color2</span></span></td>
<td><span data-ttu-id="cf4be-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="cf4be-729">Color de la segunda sombra o resaltado en una sombra en relieve o grabado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="cf4be-730">El valor predeterminado es RGB (203203203).</span><span class="sxs-lookup"><span data-stu-id="cf4be-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-731">Matrix</span><span class="sxs-lookup"><span data-stu-id="cf4be-731">Matrix</span></span></td>
<td><span data-ttu-id="cf4be-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="cf4be-733">Una matriz de transformación de perspectiva con el formato, &quot; SXX, SXY, SYX, SYY, PX, py &quot; [s = Scale, p = Perspective].</span><span class="sxs-lookup"><span data-stu-id="cf4be-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="cf4be-734">Los elementos s especifican cómo se debe escalar la sombra con respecto a la forma y los elementos p especifican cómo debe sesgar la sombra con respecto a la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="cf4be-735">Por ejemplo, la siguiente matriz cambia el tamaño de la forma por un factor de 2 y lo sesga por un factor de 4 en todas las direcciones:</span><span class="sxs-lookup"><span data-stu-id="cf4be-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="cf4be-736">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="cf4be-737">Esta matriz solo se utiliza si el tipo de la sombra se establece en Perspective.</span><span class="sxs-lookup"><span data-stu-id="cf4be-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-738">Oculta</span><span class="sxs-lookup"><span data-stu-id="cf4be-738">Obscured</span></span></td>
<td><span data-ttu-id="cf4be-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-740">La sombra puede verse a través de si no hay ningún relleno en la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="cf4be-741">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="cf4be-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-742">Offset</span><span class="sxs-lookup"><span data-stu-id="cf4be-742">Offset</span></span></td>
<td><span data-ttu-id="cf4be-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="cf4be-744">Cantidad de desplazamiento x, y de la ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="cf4be-745">El valor predeterminado es &quot; 2PT, 2PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="cf4be-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="cf4be-746">Offset2</span></span></td>
<td><span data-ttu-id="cf4be-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-748">Cantidad de desplazamiento x, y segundo de la ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="cf4be-749">Los valores son una medida absoluta o un valor fraccionario de forma (de-0,5 a + 0,5).</span><span class="sxs-lookup"><span data-stu-id="cf4be-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-750">Activado</span><span class="sxs-lookup"><span data-stu-id="cf4be-750">On</span></span></td>
<td><span data-ttu-id="cf4be-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-752">Activa y desactiva la presentación de la sombra.</span><span class="sxs-lookup"><span data-stu-id="cf4be-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-753">Opacidad</span><span class="sxs-lookup"><span data-stu-id="cf4be-753">Opacity</span></span></td>
<td><span data-ttu-id="cf4be-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="cf4be-755">Opacidad del efecto de sombra.</span><span class="sxs-lookup"><span data-stu-id="cf4be-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-756">Origen</span><span class="sxs-lookup"><span data-stu-id="cf4be-756">Origin</span></span></td>
<td><span data-ttu-id="cf4be-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Un par de valores fraccionarios de la forma de-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="cf4be-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-758">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-758">Type</span></span></td>
<td><span data-ttu-id="cf4be-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="cf4be-760">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-761">Single (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-761">Single (default)</span></span></li>
<li><span data-ttu-id="cf4be-762">Doble</span><span class="sxs-lookup"><span data-stu-id="cf4be-762">Double</span></span></li>
<li><span data-ttu-id="cf4be-763">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="cf4be-763">Perspective</span></span></li>
<li><span data-ttu-id="cf4be-764">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="cf4be-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="cf4be-765">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="cf4be-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="cf4be-766">Emboss</span><span class="sxs-lookup"><span data-stu-id="cf4be-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="cf4be-767">Sesgar elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-767">Skew element</span></span>

<span data-ttu-id="cf4be-768">Describe un efecto de sesgo de perspectiva en una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="cf4be-769">El sesgo se aplica a los datos de gráficos vectoriales, no a los datos de imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-770">Matrix</span><span class="sxs-lookup"><span data-stu-id="cf4be-770">Matrix</span></span> | <span data-ttu-id="cf4be-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-772">Una matriz de transformación de perspectiva con el formato "SXX, SXY, SYX, SYY, PX, py" \[ s = Scale, p = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="cf4be-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="cf4be-773">Si el desplazamiento está en unidades absolutas, PX, py se encuentran en las unidades de la UEM ^-1. en caso contrario, son una fracción inversa del tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="cf4be-774">Offset</span><span class="sxs-lookup"><span data-stu-id="cf4be-774">Offset</span></span> | <span data-ttu-id="cf4be-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-776">Cantidad de desplazamiento x, y de la ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="cf4be-777">El valor predeterminado es "2PT, 2PT".</span><span class="sxs-lookup"><span data-stu-id="cf4be-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="cf4be-778">Activado</span><span class="sxs-lookup"><span data-stu-id="cf4be-778">On</span></span>     | <span data-ttu-id="cf4be-779">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-780">Activa o desactiva la presentación del sesgo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="cf4be-781">Origen</span><span class="sxs-lookup"><span data-stu-id="cf4be-781">Origin</span></span> | <span data-ttu-id="cf4be-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-783">Un par de valores fraccionarios de la forma de-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="cf4be-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="cf4be-784">Elemento stroke</span><span class="sxs-lookup"><span data-stu-id="cf4be-784">Stroke element</span></span>

<span data-ttu-id="cf4be-785">Describe cómo dibujar la ruta de acceso si se desea algo más allá de una línea sólida con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="cf4be-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-786">Color</span><span class="sxs-lookup"><span data-stu-id="cf4be-786">Color</span></span></td>
<td><span data-ttu-id="cf4be-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-788">Color de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-788">The color of the line.</span></span> <span data-ttu-id="cf4be-789">Igual que el atributo StrokeColor de la forma, pero lo reemplaza.</span><span class="sxs-lookup"><span data-stu-id="cf4be-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-790">Color2</span><span class="sxs-lookup"><span data-stu-id="cf4be-790">Color2</span></span></td>
<td><span data-ttu-id="cf4be-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="cf4be-792">Color secundario.</span><span class="sxs-lookup"><span data-stu-id="cf4be-792">Secondary color.</span></span> <span data-ttu-id="cf4be-793">Se usa cuando FillType es pattern.</span><span class="sxs-lookup"><span data-stu-id="cf4be-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="cf4be-794">DashStyle</span></span></td>
<td><span data-ttu-id="cf4be-795"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="cf4be-796">Formato de estilo de guión.</span><span class="sxs-lookup"><span data-stu-id="cf4be-796">Dash style format.</span></span> <span data-ttu-id="cf4be-797">Puede ser un valor específico o una secuencia de números con un patrón de guiones definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cf4be-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="cf4be-798">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-799">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-799">Solid (default)</span></span></li>
<li><span data-ttu-id="cf4be-800">ShortDash</span><span class="sxs-lookup"><span data-stu-id="cf4be-800">ShortDash</span></span></li>
<li><span data-ttu-id="cf4be-801">ShortDot</span><span class="sxs-lookup"><span data-stu-id="cf4be-801">ShortDot</span></span></li>
<li><span data-ttu-id="cf4be-802">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="cf4be-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="cf4be-803">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="cf4be-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="cf4be-804">Punto</span><span class="sxs-lookup"><span data-stu-id="cf4be-804">Dot</span></span></li>
<li><span data-ttu-id="cf4be-805">Guión</span><span class="sxs-lookup"><span data-stu-id="cf4be-805">Dash</span></span></li>
<li><span data-ttu-id="cf4be-806">DashDot</span><span class="sxs-lookup"><span data-stu-id="cf4be-806">DashDot</span></span></li>
<li><span data-ttu-id="cf4be-807">LongDash</span><span class="sxs-lookup"><span data-stu-id="cf4be-807">LongDash</span></span></li>
<li><span data-ttu-id="cf4be-808">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="cf4be-808">LongDashDot</span></span></li>
<li><span data-ttu-id="cf4be-809">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="cf4be-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-810">EndArrow</span><span class="sxs-lookup"><span data-stu-id="cf4be-810">EndArrow</span></span></td>
<td><span data-ttu-id="cf4be-811"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="cf4be-812">Punta de flecha del final de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="cf4be-813">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-814">Ninguna (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-814">None (default)</span></span></li>
<li><span data-ttu-id="cf4be-815">Bloquear</span><span class="sxs-lookup"><span data-stu-id="cf4be-815">Block</span></span></li>
<li><span data-ttu-id="cf4be-816">Clásico</span><span class="sxs-lookup"><span data-stu-id="cf4be-816">Classic</span></span></li>
<li><span data-ttu-id="cf4be-817">Diamond</span><span class="sxs-lookup"><span data-stu-id="cf4be-817">Diamond</span></span></li>
<li><span data-ttu-id="cf4be-818">Elipse</span><span class="sxs-lookup"><span data-stu-id="cf4be-818">Oval</span></span></li>
<li><span data-ttu-id="cf4be-819">Abrir</span><span class="sxs-lookup"><span data-stu-id="cf4be-819">Open</span></span></li>
<li><span data-ttu-id="cf4be-820">Comillas angulares</span><span class="sxs-lookup"><span data-stu-id="cf4be-820">Chevron</span></span></li>
<li><span data-ttu-id="cf4be-821">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="cf4be-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-822">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="cf4be-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="cf4be-823"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="cf4be-824">Longitud de la punta de flecha para el final de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="cf4be-825">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-826">Short</span><span class="sxs-lookup"><span data-stu-id="cf4be-826">Short</span></span></li>
<li><span data-ttu-id="cf4be-827">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-827">Medium (default)</span></span></li>
<li><span data-ttu-id="cf4be-828">long</span><span class="sxs-lookup"><span data-stu-id="cf4be-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-829">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="cf4be-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="cf4be-830"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="cf4be-831">Ancho de la punta de flecha para el final de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="cf4be-832">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-833">Restrictiv</span><span class="sxs-lookup"><span data-stu-id="cf4be-833">Narrow</span></span></li>
<li><span data-ttu-id="cf4be-834">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-834">Medium (default)</span></span></li>
<li><span data-ttu-id="cf4be-835">Ancho</span><span class="sxs-lookup"><span data-stu-id="cf4be-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-836">EndCap</span><span class="sxs-lookup"><span data-stu-id="cf4be-836">EndCap</span></span></td>
<td><span data-ttu-id="cf4be-837"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="cf4be-838">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-839">Plano</span><span class="sxs-lookup"><span data-stu-id="cf4be-839">Flat</span></span></li>
<li><span data-ttu-id="cf4be-840">Square</span><span class="sxs-lookup"><span data-stu-id="cf4be-840">Square</span></span></li>
<li><span data-ttu-id="cf4be-841">Round</span><span class="sxs-lookup"><span data-stu-id="cf4be-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-842">FillType</span><span class="sxs-lookup"><span data-stu-id="cf4be-842">FillType</span></span></td>
<td><span data-ttu-id="cf4be-843"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="cf4be-844">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-845">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-845">Solid (default)</span></span></li>
<li><span data-ttu-id="cf4be-846">Tile</span><span class="sxs-lookup"><span data-stu-id="cf4be-846">Tile</span></span></li>
<li><span data-ttu-id="cf4be-847">Patrón</span><span class="sxs-lookup"><span data-stu-id="cf4be-847">Pattern</span></span></li>
<li><span data-ttu-id="cf4be-848">Fotograma</span><span class="sxs-lookup"><span data-stu-id="cf4be-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-849">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="cf4be-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="cf4be-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-851">Alinee la imagen con la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-851">Align the image with the shape.</span></span> <span data-ttu-id="cf4be-852">Si es false, alinea la imagen con la ventana.</span><span class="sxs-lookup"><span data-stu-id="cf4be-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-853">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="cf4be-853">ImageAspect</span></span></td>
<td><span data-ttu-id="cf4be-854"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="cf4be-855">El atributo ImageSize se ajustará para conservar el aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="cf4be-856">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="cf4be-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-857">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-857">Value</span></span></th>
<th><span data-ttu-id="cf4be-858">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-859">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cf4be-859">Ignore</span></span></td>
<td><span data-ttu-id="cf4be-860">Omitir problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-861">Al menos</span><span class="sxs-lookup"><span data-stu-id="cf4be-861">AtLeast</span></span></td>
<td><span data-ttu-id="cf4be-862">La imagen es al menos tan grande como el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-863">AtMos</span><span class="sxs-lookup"><span data-stu-id="cf4be-863">AtMost</span></span></td>
<td><span data-ttu-id="cf4be-864">La imagen no es mayor que el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="cf4be-865">ImageSize</span></span></td>
<td><span data-ttu-id="cf4be-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="cf4be-867">Tamaño de la imagen con la que se va a formar el pincel.</span><span class="sxs-lookup"><span data-stu-id="cf4be-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="cf4be-868">El valor predeterminado es el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-869">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="cf4be-869">JoinStyle</span></span></td>
<td><span data-ttu-id="cf4be-870"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="cf4be-871">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-872">Round (Unión redondeada)</span><span class="sxs-lookup"><span data-stu-id="cf4be-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="cf4be-873">Bisel (unión biselada)</span><span class="sxs-lookup"><span data-stu-id="cf4be-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="cf4be-874">Angular (unión angular)</span><span class="sxs-lookup"><span data-stu-id="cf4be-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-875">Estilo de línea</span><span class="sxs-lookup"><span data-stu-id="cf4be-875">LineStyle</span></span></td>
<td><span data-ttu-id="cf4be-876"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="cf4be-877">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-878">Single</span><span class="sxs-lookup"><span data-stu-id="cf4be-878">Single</span></span></li>
<li><span data-ttu-id="cf4be-879">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="cf4be-880">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="cf4be-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="cf4be-881">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="cf4be-882">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-883">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="cf4be-883">MiterLimit</span></span></td>
<td><span data-ttu-id="cf4be-884"><a href="msdn-online-vml-vglength.md">Longitud</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="cf4be-885">Distancia máxima entre el punto interno y el punto exterior de una Unión.</span><span class="sxs-lookup"><span data-stu-id="cf4be-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="cf4be-886">Este número es un múltiplo del grosor de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="cf4be-887">Oscila entre 0 y 32.767.</span><span class="sxs-lookup"><span data-stu-id="cf4be-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-888">Activado</span><span class="sxs-lookup"><span data-stu-id="cf4be-888">On</span></span></td>
<td><span data-ttu-id="cf4be-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="cf4be-890">Activa y desactiva la presentación de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="cf4be-891">Igual que el atributo stroke de la forma, pero lo reemplaza.</span><span class="sxs-lookup"><span data-stu-id="cf4be-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-892">Opacidad</span><span class="sxs-lookup"><span data-stu-id="cf4be-892">Opacity</span></span></td>
<td><span data-ttu-id="cf4be-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="cf4be-894">Opacidad del trazo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-895">Origen</span><span class="sxs-lookup"><span data-stu-id="cf4be-895">Src</span></span></td>
<td><span data-ttu-id="cf4be-896">String.</span><span class="sxs-lookup"><span data-stu-id="cf4be-896">String.</span></span> <span data-ttu-id="cf4be-897">Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón.</span><span class="sxs-lookup"><span data-stu-id="cf4be-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="cf4be-898">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="cf4be-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-899">StartArrow</span><span class="sxs-lookup"><span data-stu-id="cf4be-899">StartArrow</span></span></td>
<td><span data-ttu-id="cf4be-900"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="cf4be-901">Punta de flecha del inicio de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="cf4be-902">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-903">Ninguna (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-903">None (default)</span></span></li>
<li><span data-ttu-id="cf4be-904">Bloquear</span><span class="sxs-lookup"><span data-stu-id="cf4be-904">Block</span></span></li>
<li><span data-ttu-id="cf4be-905">Clásico</span><span class="sxs-lookup"><span data-stu-id="cf4be-905">Classic</span></span></li>
<li><span data-ttu-id="cf4be-906">Diamond</span><span class="sxs-lookup"><span data-stu-id="cf4be-906">Diamond</span></span></li>
<li><span data-ttu-id="cf4be-907">Elipse</span><span class="sxs-lookup"><span data-stu-id="cf4be-907">Oval</span></span></li>
<li><span data-ttu-id="cf4be-908">Abrir</span><span class="sxs-lookup"><span data-stu-id="cf4be-908">Open</span></span></li>
<li><span data-ttu-id="cf4be-909">Comillas angulares</span><span class="sxs-lookup"><span data-stu-id="cf4be-909">Chevron</span></span></li>
<li><span data-ttu-id="cf4be-910">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="cf4be-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-911">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="cf4be-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="cf4be-912">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="cf4be-912">VgArrowHeadLength.</span></span> <span data-ttu-id="cf4be-913">Longitud de la punta de flecha para el inicio de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="cf4be-914">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-915">Short</span><span class="sxs-lookup"><span data-stu-id="cf4be-915">Short</span></span></li>
<li><span data-ttu-id="cf4be-916">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-916">Medium (default)</span></span></li>
<li><span data-ttu-id="cf4be-917">long</span><span class="sxs-lookup"><span data-stu-id="cf4be-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-918">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="cf4be-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="cf4be-919">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="cf4be-919">VgArrowheadWidth.</span></span> <span data-ttu-id="cf4be-920">Ancho de la punta de flecha para el inicio de la línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="cf4be-921">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-922">Ancho medio estrecho (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="cf4be-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-923">Peso</span><span class="sxs-lookup"><span data-stu-id="cf4be-923">Weight</span></span></td>
<td><span data-ttu-id="cf4be-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="cf4be-925">Ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-925">Width of line.</span></span> <span data-ttu-id="cf4be-926">Oscila entre 0 y 1584.</span><span class="sxs-lookup"><span data-stu-id="cf4be-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf4be-927">El atributo DashStyle permite al usuario especificar un patrón de guiones definido de forma personalizada.</span><span class="sxs-lookup"><span data-stu-id="cf4be-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="cf4be-928">Esto se hace mediante una serie de números.</span><span class="sxs-lookup"><span data-stu-id="cf4be-928">This is done using a series of numbers.</span></span> <span data-ttu-id="cf4be-929">Los estilos de guión se definen en términos de la longitud del guión (la parte dibujada del trazo) y la longitud del espacio entre los guiones.</span><span class="sxs-lookup"><span data-stu-id="cf4be-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="cf4be-930">Las longitudes son relativas al ancho de línea; una longitud de &quot; 1 &quot; es igual al ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="cf4be-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="cf4be-931">El estilo EndCap se aplica a cada guión; los estilos de flecha no lo son.</span><span class="sxs-lookup"><span data-stu-id="cf4be-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="cf4be-932">La cadena define primero la longitud del guión y, a continuación, la longitud del espacio.</span><span class="sxs-lookup"><span data-stu-id="cf4be-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="cf4be-933">Esto puede repetirse para formar estilos de guiones complejos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="cf4be-934">La cadena siempre debe contener un par de números; Si contiene un número impar de números, es posible que se descarte la última.</span><span class="sxs-lookup"><span data-stu-id="cf4be-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="cf4be-935">En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="cf4be-936">&quot;0 &quot; implica un punto que debe ser fourfold simétrico (con Endcaps redondeada debe ser un círculo).</span><span class="sxs-lookup"><span data-stu-id="cf4be-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="cf4be-937">Si el Endcap de línea es plano, un visor debe elegir un guion del sistema operativo integrado siempre que sea posible (es decir, algo que sea rápido de dibujar).</span><span class="sxs-lookup"><span data-stu-id="cf4be-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="cf4be-938">A continuación se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-940">guiones cortos (cada guion y el espacio entre dos es el doble del ancho de la línea)</span><span class="sxs-lookup"><span data-stu-id="cf4be-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-942">punto (cada guión es el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea)</span><span class="sxs-lookup"><span data-stu-id="cf4be-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-944">Dash (cada guion es cuatro veces el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea)</span><span class="sxs-lookup"><span data-stu-id="cf4be-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-946">Guion largo</span><span class="sxs-lookup"><span data-stu-id="cf4be-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-948">guión punto</span><span class="sxs-lookup"><span data-stu-id="cf4be-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-950">guión largo (punto)</span><span class="sxs-lookup"><span data-stu-id="cf4be-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="cf4be-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="cf4be-952">guión largo (punto)</span><span class="sxs-lookup"><span data-stu-id="cf4be-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="cf4be-953">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="cf4be-953">TextPath element</span></span>

<span data-ttu-id="cf4be-954">Describe una ruta de acceso vectorial basada en los datos de texto, la fuente y los estilos proporcionados.</span><span class="sxs-lookup"><span data-stu-id="cf4be-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="cf4be-955">La ruta de acceso de texto se distorsiona para ajustarse a un elemento de **ruta de acceso** si se proporciona.</span><span class="sxs-lookup"><span data-stu-id="cf4be-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-956">FitPath</span><span class="sxs-lookup"><span data-stu-id="cf4be-956">FitPath</span></span>  | <span data-ttu-id="cf4be-957">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-958">Ajusta el tamaño del texto para rellenar la ruta en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="cf4be-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="cf4be-959">FitShape</span><span class="sxs-lookup"><span data-stu-id="cf4be-959">FitShape</span></span> | <span data-ttu-id="cf4be-960">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-961">Estira la ruta de acceso del texto hasta los bordes del cuadro de forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="cf4be-962">Activado</span><span class="sxs-lookup"><span data-stu-id="cf4be-962">On</span></span>       | <span data-ttu-id="cf4be-963">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-964">Determina si las rutas de acceso de caracteres se muestran o no.</span><span class="sxs-lookup"><span data-stu-id="cf4be-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="cf4be-965">String</span><span class="sxs-lookup"><span data-stu-id="cf4be-965">String</span></span>   | <span data-ttu-id="cf4be-966">String.</span><span class="sxs-lookup"><span data-stu-id="cf4be-966">String.</span></span> <span data-ttu-id="cf4be-967">Texto que se va a representar como una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="cf4be-968">Trim</span><span class="sxs-lookup"><span data-stu-id="cf4be-968">Trim</span></span>     | <span data-ttu-id="cf4be-969">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-970">Quita cualquier espacio adicional reservado para ascendentes y descendentes si no se usa.</span><span class="sxs-lookup"><span data-stu-id="cf4be-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="cf4be-971">XScale</span><span class="sxs-lookup"><span data-stu-id="cf4be-971">XScale</span></span>   | <span data-ttu-id="cf4be-972">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-973">Use la medida x recta en lugar de medir a lo largo del trazado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="cf4be-974">Tipos de datos utilizados en el modelo de objetos VML</span><span class="sxs-lookup"><span data-stu-id="cf4be-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="cf4be-975">El modelo de objetos VML usa los siguientes tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="cf4be-976">Double</span><span class="sxs-lookup"><span data-stu-id="cf4be-976">Double</span></span>](/windows)
-   [<span data-ttu-id="cf4be-977">Fijo</span><span class="sxs-lookup"><span data-stu-id="cf4be-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="cf4be-978">Entero</span><span class="sxs-lookup"><span data-stu-id="cf4be-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="cf4be-979">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="cf4be-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="cf4be-980">IVgColor</span><span class="sxs-lookup"><span data-stu-id="cf4be-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="cf4be-981">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="cf4be-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="cf4be-982">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="cf4be-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="cf4be-983">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="cf4be-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="cf4be-984">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="cf4be-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="cf4be-985">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="cf4be-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="cf4be-986">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="cf4be-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="cf4be-987">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="cf4be-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="cf4be-988">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="cf4be-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="cf4be-989">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="cf4be-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="cf4be-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="cf4be-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="cf4be-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="cf4be-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="cf4be-992">Duración</span><span class="sxs-lookup"><span data-stu-id="cf4be-992">Length</span></span>](/windows)
-   <span data-ttu-id="cf4be-993">[Measure](/windows) (Medida)</span><span class="sxs-lookup"><span data-stu-id="cf4be-993">[Measure](/windows)</span></span>
-   [<span data-ttu-id="cf4be-994">String</span><span class="sxs-lookup"><span data-stu-id="cf4be-994">String</span></span>](/windows)
-   [<span data-ttu-id="cf4be-995">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="cf4be-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="cf4be-996">VgFraction</span><span class="sxs-lookup"><span data-stu-id="cf4be-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="cf4be-997">VgTriState</span><span class="sxs-lookup"><span data-stu-id="cf4be-997">VgTriState</span></span>](/windows)

<span data-ttu-id="cf4be-998">**Double (tipo de datos)**</span><span class="sxs-lookup"><span data-stu-id="cf4be-998">**Double data type**</span></span>

<span data-ttu-id="cf4be-999">Un entero de precisión doble con un intervalo de-infinito a infinito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="cf4be-1000">**Tipo de datos Fixed**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1000">**Fixed data type**</span></span>

<span data-ttu-id="cf4be-1001">Número de punto flotante con un intervalo comprendido entre-32.766,0 y 32.766,0.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="cf4be-1002">**Tipo de datos Integer**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1002">**Integer data type**</span></span>

<span data-ttu-id="cf4be-1003">Entero con un intervalo de-infinito a infinito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="cf4be-1004">**IVgAdjustments, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="cf4be-1005">Colección de ajustes de una forma que se puede utilizar para cambiar las dimensiones de una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="cf4be-1006">Los ajustes se pueden usar como marcadores de posición temporales o, por cualquier motivo, se usarían variables.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="cf4be-1007">Solo hay 8 ajustes en la colección.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="cf4be-1008">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1008">Attributes</span></span> | <span data-ttu-id="cf4be-1009">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="cf4be-1010">Exists</span></span>     | <span data-ttu-id="cf4be-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="cf4be-1012">Determina si existe un ajuste especificado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="cf4be-1013">Tenga en cuenta que se debe usar un índice; es decir, exists (Item) se debe usar para recuperar la existencia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="cf4be-1014">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-1014">Item</span></span>       | <span data-ttu-id="cf4be-1015">[Largo](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1016">Matriz de ajustes indizada de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="cf4be-1017">Tenga en cuenta que los ajustes pueden especificarse de SPARC. es decir, es posible que no siempre se rellenen los valores de matriz intermedios.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="cf4be-1018">Por ejemplo, los elementos 1, 3 y 5 podrían tener valores para una longitud de 3, con el elemento (0), el elemento (2) y el elemento (4) especificado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="cf4be-1019">Para ver si existe un elemento, utilice el atributo EXISTS.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="cf4be-1020">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1020">Length</span></span>     | <span data-ttu-id="cf4be-1021">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1022">Número de ajustes.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1022">Number of adjustments.</span></span> <span data-ttu-id="cf4be-1023">No puede ser mayor que 8.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cf4be-1024">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1024">Value</span></span>      | <span data-ttu-id="cf4be-1025">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1026">Representación de texto de valores numéricos, con comas entre cada número.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="cf4be-1027">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1027">**IVgColor**</span></span>

<span data-ttu-id="cf4be-1028">Especifica un color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-1029">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1029">Attributes</span></span></th>
<th><span data-ttu-id="cf4be-1030">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="cf4be-1031">RGB</span></span></td>
<td><span data-ttu-id="cf4be-1032"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="cf4be-1033">Valor RGB (Long) del color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="cf4be-1034">Solo es válido si el tipo es RGB.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1035">R</span><span class="sxs-lookup"><span data-stu-id="cf4be-1035">R</span></span></td>
<td><span data-ttu-id="cf4be-1036"><a href="#data-types-used-in-the-vml-object-model">Entero</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="cf4be-1037">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1037">Red component of the color.</span></span> <span data-ttu-id="cf4be-1038">Puede oscilar entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1039">G</span><span class="sxs-lookup"><span data-stu-id="cf4be-1039">G</span></span></td>
<td><span data-ttu-id="cf4be-1040"><a href="#data-types-used-in-the-vml-object-model">Entero</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="cf4be-1041">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1041">Green component of the color.</span></span> <span data-ttu-id="cf4be-1042">Puede oscilar entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1043">B</span><span class="sxs-lookup"><span data-stu-id="cf4be-1043">B</span></span></td>
<td><span data-ttu-id="cf4be-1044"><a href="#data-types-used-in-the-vml-object-model">Entero</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="cf4be-1045">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1045">Blue component of the color.</span></span> <span data-ttu-id="cf4be-1046">Puede oscilar entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1047">String</span><span class="sxs-lookup"><span data-stu-id="cf4be-1047">String</span></span></td>
<td><span data-ttu-id="cf4be-1048"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="cf4be-1049">Representación de texto del color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1049">Text representation of the color.</span></span> <span data-ttu-id="cf4be-1050">Se admiten los siguientes tipos de colores con nombre:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="cf4be-1051">Negro (#000000)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="cf4be-1052">Silver (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="cf4be-1053">Gris (#808080)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="cf4be-1054">Blanco (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="cf4be-1055">Granate (#800000)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="cf4be-1056">Rojo (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="cf4be-1057">Púrpura (#800080)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="cf4be-1058">Fuchsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="cf4be-1059">Verde (#008000)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="cf4be-1060">Lima (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="cf4be-1061">Oliva (#808000)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="cf4be-1062">Amarillo (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="cf4be-1063">Navy (#000080)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="cf4be-1064">Blue (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="cf4be-1065">Verde azulado (#008080)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="cf4be-1066">Aguamarina (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1067">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-1067">Type</span></span></td>
<td><span data-ttu-id="cf4be-1068"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="cf4be-1069">Tipo de color.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1069">Type of color.</span></span> <span data-ttu-id="cf4be-1070">Uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="cf4be-1071">Mixto</span><span class="sxs-lookup"><span data-stu-id="cf4be-1071">Mixed</span></span></li>
<li><span data-ttu-id="cf4be-1072">con nombre</span><span class="sxs-lookup"><span data-stu-id="cf4be-1072">Named</span></span></li>
<li><span data-ttu-id="cf4be-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="cf4be-1073">RGB</span></span></li>
<li><span data-ttu-id="cf4be-1074">Scheme</span><span class="sxs-lookup"><span data-stu-id="cf4be-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf4be-1075">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1075">**IVgEquation**</span></span>

<span data-ttu-id="cf4be-1076">Ecuaciones utilizadas para las fórmulas.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1077">Operación</span><span class="sxs-lookup"><span data-stu-id="cf4be-1077">Operation</span></span></td>
<td><span data-ttu-id="cf4be-1078"><strong>VgEquationOperationType</strong> Nombre de la operación que se va a realizar en los parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="cf4be-1079">En una ecuación se pueden usar las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-1080">Operación</span><span class="sxs-lookup"><span data-stu-id="cf4be-1080">Operation</span></span></th>
<th><span data-ttu-id="cf4be-1081">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="cf4be-1082">Abs</span></span></td>
<td><span data-ttu-id="cf4be-1083">Valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1083">Absolute value.</span></span> <br/> <span data-ttu-id="cf4be-1084"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1085">Atan2</span></span></td>
<td><span data-ttu-id="cf4be-1086">Aritmética polar: resultados en unidades FD (grados multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="cf4be-1087"><strong>ATAN2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1088">Cos</span></span></td>
<td><span data-ttu-id="cf4be-1089">Coseno, argumento en unidades FD (grados multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="cf4be-1090">v \* <strong>cos</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="cf4be-1092">Conserva la precisión completa en el cálculo intermedio.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="cf4be-1093">v \* <strong>cos (ATAN2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="cf4be-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1094">Elipse</span><span class="sxs-lookup"><span data-stu-id="cf4be-1094">Ellipse</span></span></td>
<td><span data-ttu-id="cf4be-1095">Elipse</span><span class="sxs-lookup"><span data-stu-id="cf4be-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1096">Si</span><span class="sxs-lookup"><span data-stu-id="cf4be-1096">If</span></span></td>
<td><span data-ttu-id="cf4be-1097">Condición if test.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1097">If Condition test.</span></span> <span data-ttu-id="cf4be-1098">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="cf4be-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="cf4be-1099">P1: P2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1100">Máx.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1100">Max</span></span></td>
<td><span data-ttu-id="cf4be-1101">El mayor de dos valores.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="cf4be-1102"><strong>máx</strong>. (v, P1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1103">Mid</span><span class="sxs-lookup"><span data-stu-id="cf4be-1103">Mid</span></span></td>
<td><span data-ttu-id="cf4be-1104">Promedio (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1105">Min</span><span class="sxs-lookup"><span data-stu-id="cf4be-1105">Min</span></span></td>
<td><span data-ttu-id="cf4be-1106">El menor de dos valores.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1106">The lesser of two values.</span></span> <span data-ttu-id="cf4be-1107"><strong>mín</strong>. (v, P1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="cf4be-1108">Mod</span></span></td>
<td><span data-ttu-id="cf4be-1109">Valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1110">Producto</span><span class="sxs-lookup"><span data-stu-id="cf4be-1110">Product</span></span></td>
<td><span data-ttu-id="cf4be-1111">Se utiliza para la multiplicación y la división.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1111">Used for multiplication and division.</span></span> <span data-ttu-id="cf4be-1112">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="cf4be-1113">Sin</span></span></td>
<td><span data-ttu-id="cf4be-1114">Seno, argumento en unidades FD (grados multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="cf4be-1115">v \* <strong>sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="cf4be-1117">Conserva la precisión completa en el cálculo intermedio.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="cf4be-1118">v \* <strong>sin</strong>(<strong>ATAN2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="cf4be-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="cf4be-1119">Sqrt</span></span></td>
<td><span data-ttu-id="cf4be-1120">El resultado es positivo y se redondea hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="cf4be-1121"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1122">Sum</span><span class="sxs-lookup"><span data-stu-id="cf4be-1122">Sum</span></span></td>
<td><span data-ttu-id="cf4be-1123">Se utiliza para sumar y restar.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="cf4be-1124">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1125">Sumangle</span><span class="sxs-lookup"><span data-stu-id="cf4be-1125">Sumangle</span></span></td>
<td><span data-ttu-id="cf4be-1126">Ángulo existente (escalado por 65536), donde P1 y P2 están en grados.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="cf4be-1127">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="cf4be-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="cf4be-1128">Tan</span></span></td>
<td><span data-ttu-id="cf4be-1129">Tangente, el argumento está en unidades FD (grados multiplicado por 65536).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="cf4be-1130">v \* tan (P1)</span><span class="sxs-lookup"><span data-stu-id="cf4be-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1131">Val</span><span class="sxs-lookup"><span data-stu-id="cf4be-1131">Val</span></span></td>
<td><span data-ttu-id="cf4be-1132">Define un valor de guía de otro valor.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1133">Parámetro1</span><span class="sxs-lookup"><span data-stu-id="cf4be-1133">Param1</span></span></td>
<td><span data-ttu-id="cf4be-1134"><strong>Entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="cf4be-1135">El primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="cf4be-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="cf4be-1137"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="cf4be-1138">Tipo del primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1138">The type of the first parameter.</span></span> <span data-ttu-id="cf4be-1139">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-1140">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-1140">Type</span></span></th>
<th><span data-ttu-id="cf4be-1141">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1142">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1142">Value</span></span></td>
<td><span data-ttu-id="cf4be-1143">El parámetro es un valor simple.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1144">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="cf4be-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="cf4be-1145">Parámetro es una referencia a un ajuste.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="cf4be-1146">Por ejemplo, si el primer parámetro es 1, se utilizará el valor del primer ajuste.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1147">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="cf4be-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="cf4be-1148">Es el resultado de una referencia al resultado de una fórmula anterior.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="cf4be-1149">Por ejemplo, si el primer parámetro es 2, se usará el resultado de la fórmula 2.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1150">Param2</span></span></td>
<td><span data-ttu-id="cf4be-1151"><strong>Entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="cf4be-1152">El segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="cf4be-1154"><strong>VgFormulaParamType</strong> Tipo del parámetro 2.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1155">Val</span><span class="sxs-lookup"><span data-stu-id="cf4be-1155">Val</span></span></td>
<td><span data-ttu-id="cf4be-1156"><strong>Entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="cf4be-1157">Resultado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="cf4be-1158">Valtype2</span></span></td>
<td><span data-ttu-id="cf4be-1159"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="cf4be-1160">Tipo del resultado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf4be-1161">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="cf4be-1162">Especifica un rectángulo fijo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="cf4be-1163">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1163">Attributes</span></span> | <span data-ttu-id="cf4be-1164">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1165">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1165">Value</span></span>      | <span data-ttu-id="cf4be-1166">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1167">Valor de texto que especifica la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="cf4be-1168">Left</span><span class="sxs-lookup"><span data-stu-id="cf4be-1168">Left</span></span>       | <span data-ttu-id="cf4be-1169">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1170">Coordenada izquierda del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="cf4be-1171">Superior</span><span class="sxs-lookup"><span data-stu-id="cf4be-1171">Top</span></span>        | <span data-ttu-id="cf4be-1172">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1173">Coordenada superior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="cf4be-1174">Right</span><span class="sxs-lookup"><span data-stu-id="cf4be-1174">Right</span></span>      | <span data-ttu-id="cf4be-1175">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1176">Coordenada derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="cf4be-1177">Bottom</span><span class="sxs-lookup"><span data-stu-id="cf4be-1177">Bottom</span></span>     | <span data-ttu-id="cf4be-1178">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1179">Coordenada inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="cf4be-1180">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="cf4be-1181">Matriz de rectángulos fijos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="cf4be-1182">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1182">Attributes</span></span> | <span data-ttu-id="cf4be-1183">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1184">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1184">Value</span></span>      | <span data-ttu-id="cf4be-1185">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1186">Representación de texto de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="cf4be-1187">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1187">Length</span></span>     | <span data-ttu-id="cf4be-1188">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1189">Número de rectángulos en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="cf4be-1190">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-1190">Item</span></span>       | <span data-ttu-id="cf4be-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1192">Objeto de rectángulo en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="cf4be-1193">**IVgFormula** , tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="cf4be-1194">Definiciones de fórmulas que pueden variar la ruta de acceso de una forma o que se pueden usar para otros fines de cálculo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="cf4be-1195">Las fórmulas se pueden basar en el atributo **ADJ** de una forma, que puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="cf4be-1196">Las fórmulas también pueden hacer referencia a otras fórmulas.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="cf4be-1197">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1197">Attributes</span></span> | <span data-ttu-id="cf4be-1198">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1199">Eqn</span><span class="sxs-lookup"><span data-stu-id="cf4be-1199">Eqn</span></span>        | <span data-ttu-id="cf4be-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1201">Cada fórmula define un valor único como el resultado de la evaluación de la expresión.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="cf4be-1202">Este atributo define la expresión y tiene la forma general de una operación seguida de hasta tres argumentos, que pueden ser valores de ajuste (por ejemplo, \# 2), los resultados de las fórmulas anteriores (por ejemplo, @2 ), números fijos o valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="cf4be-1203">**IVgFormulas, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="cf4be-1204">Colección de objetos de fórmula.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="cf4be-1205">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1205">Attributes</span></span> | <span data-ttu-id="cf4be-1206">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1207">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1207">Length</span></span>     | <span data-ttu-id="cf4be-1208">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1209">Número de objetos de fórmula en la colección.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="cf4be-1210">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-1210">Item</span></span>       | <span data-ttu-id="cf4be-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1212">Una fórmula específica.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1212">A specific formula.</span></span> <span data-ttu-id="cf4be-1213">Tenga en cuenta que la matriz de fórmulas puede ser heredada pantalla el tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="cf4be-1214">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="cf4be-1215">Matriz de colores que definen un degradado (rango de colores mezclado).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="cf4be-1216">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1216">Attributes</span></span> | <span data-ttu-id="cf4be-1217">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1218">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1218">Value</span></span>      | <span data-ttu-id="cf4be-1219">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1220">Especifica la matriz de colores; por ejemplo, "red. 2; verde. 4; negro. 7 "</span><span class="sxs-lookup"><span data-stu-id="cf4be-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="cf4be-1221">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1221">Length</span></span>     | <span data-ttu-id="cf4be-1222">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1223">Número de colores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="cf4be-1224">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1224">Methods</span></span>     | <span data-ttu-id="cf4be-1225">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1226">AddColor</span><span class="sxs-lookup"><span data-stu-id="cf4be-1226">AddColor</span></span>    | <span data-ttu-id="cf4be-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="cf4be-1228">Agrega un nuevo color en el extremo especificado por fracción.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="cf4be-1229">El nuevo color es blanco de forma predeterminada y es el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="cf4be-1230">Después, se puede cambiar el color por referencia.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="cf4be-1231">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="cf4be-1231">RemoveColor</span></span> | <span data-ttu-id="cf4be-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="cf4be-1233">Quita un color en el extremo especificado por fracción.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="cf4be-1234">Nota: Si 0,0 o 1,0 no existe, es implícito y se usa el color blanco en ese punto.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="cf4be-1235">**Tipo de IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="cf4be-1236">Matriz de puntos que definen una forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="cf4be-1237">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1237">Attributes</span></span> | <span data-ttu-id="cf4be-1238">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4be-1239">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1239">Value</span></span>      | <span data-ttu-id="cf4be-1240">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1241">Representación de texto de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="cf4be-1242">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1242">Length</span></span>     | <span data-ttu-id="cf4be-1243">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="cf4be-1244">Número de puntos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="cf4be-1245">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf4be-1245">Item</span></span>       | <span data-ttu-id="cf4be-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="cf4be-1247">Punto en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="cf4be-1248">**Tipo de IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="cf4be-1249">Matriz que se usa para sesgar formas, una matriz de transformación de perspectiva con el formato "*SXX, SXY, SYX, SYY, PX, py* " \[ *s* = Scale, *p* = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="cf4be-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="cf4be-1250">Si el desplazamiento está en unidades absolutas, *PX, py* se encuentran en unidades de la UEM ^-1. en caso contrario, son una fracción inversa del tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="cf4be-1251">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1251">Attributes</span></span>   | <span data-ttu-id="cf4be-1252">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="cf4be-1253">XtoX</span><span class="sxs-lookup"><span data-stu-id="cf4be-1253">XtoX</span></span>         | <span data-ttu-id="cf4be-1254">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="cf4be-1255">YtoX</span><span class="sxs-lookup"><span data-stu-id="cf4be-1255">YtoX</span></span>         | <span data-ttu-id="cf4be-1256">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="cf4be-1257">XtoY</span><span class="sxs-lookup"><span data-stu-id="cf4be-1257">XtoY</span></span>         | <span data-ttu-id="cf4be-1258">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="cf4be-1259">YtoY</span><span class="sxs-lookup"><span data-stu-id="cf4be-1259">YtoY</span></span>         | <span data-ttu-id="cf4be-1260">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="cf4be-1261">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="cf4be-1261">PerspectiveX</span></span> | <span data-ttu-id="cf4be-1262">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="cf4be-1263">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="cf4be-1263">PerspectiveY</span></span> | <span data-ttu-id="cf4be-1264">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="cf4be-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="cf4be-1265">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="cf4be-1266">Especifica el desplazamiento del sesgo.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-1267">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1267">Attributes</span></span></th>
<th><span data-ttu-id="cf4be-1268">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1269">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1269">Value</span></span></td>
<td><span data-ttu-id="cf4be-1270"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="cf4be-1271">Representación de texto de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1272">X</span><span class="sxs-lookup"><span data-stu-id="cf4be-1272">X</span></span></td>
<td><span data-ttu-id="cf4be-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1274">Componente X.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1274">X component.</span></span> <span data-ttu-id="cf4be-1275">Porcentaje o medida.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1275">Percentage or measure.</span></span> <span data-ttu-id="cf4be-1276">Si no hay unidades, el tipo ShapeRelative es implícito; de lo contrario, el tipo absoluto es implícito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1277">Y</span><span class="sxs-lookup"><span data-stu-id="cf4be-1277">Y</span></span></td>
<td><span data-ttu-id="cf4be-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1279">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1280">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-1280">Type</span></span></td>
<td><span data-ttu-id="cf4be-1281"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="cf4be-1282">Especifica el tipo de transformación.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="cf4be-1283">Los valores válidos son los puntos enteros comprendidos entre-Infinity y Infinity.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-1284">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-1284">Type</span></span></th>
<th><span data-ttu-id="cf4be-1285">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1286">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="cf4be-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="cf4be-1287">Los valores de desplazamiento son porcentajes (proporciones) del tamaño de la forma original; por ejemplo, un valor de 0,5 significa una desfase de la mitad del tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1288">Absoluto</span><span class="sxs-lookup"><span data-stu-id="cf4be-1288">Absolute</span></span></td>
<td><span data-ttu-id="cf4be-1289">Los valores son unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf4be-1290">**IVgVector2D, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="cf4be-1291">Especifica un vector bidimensional que consta de dos números **Double** .</span><span class="sxs-lookup"><span data-stu-id="cf4be-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf4be-1292">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4be-1292">Attributes</span></span></th>
<th><span data-ttu-id="cf4be-1293">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4be-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1294">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1294">Value</span></span></td>
<td><span data-ttu-id="cf4be-1295"><strong>Cadena</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1295"><strong>String</strong>.</span></span> <span data-ttu-id="cf4be-1296">Representación de texto de ambos números vectoriales separados por un espacio.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1297">X</span><span class="sxs-lookup"><span data-stu-id="cf4be-1297">X</span></span></td>
<td><span data-ttu-id="cf4be-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1299">Componente X de este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1300">Y</span><span class="sxs-lookup"><span data-stu-id="cf4be-1300">Y</span></span></td>
<td><span data-ttu-id="cf4be-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1302">Componente Y de este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1303">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-1303">Type</span></span></td>
<td><span data-ttu-id="cf4be-1304"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="cf4be-1305">Unidades previstas para este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1305">Expected units for this vector.</span></span> <span data-ttu-id="cf4be-1306">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-1307">Medida</span><span class="sxs-lookup"><span data-stu-id="cf4be-1307">Measure</span></span></li>
<li><span data-ttu-id="cf4be-1308">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1308">Length</span></span></li>
<li><span data-ttu-id="cf4be-1309">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="cf4be-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="cf4be-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="cf4be-1310">Fraction</span></span></li>
<li><span data-ttu-id="cf4be-1311">Número entero de porcentaje</span><span class="sxs-lookup"><span data-stu-id="cf4be-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf4be-1312">**IVgVector3D, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="cf4be-1313">Especifica un vector tridimensional que consta de tres números **dobles** .</span><span class="sxs-lookup"><span data-stu-id="cf4be-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf4be-1314">Value</span><span class="sxs-lookup"><span data-stu-id="cf4be-1314">Value</span></span></td>
<td><span data-ttu-id="cf4be-1315"><strong>Cadena</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1315"><strong>String</strong>.</span></span> <span data-ttu-id="cf4be-1316">Representación de texto de tres números vectoriales separados por un espacio.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1317">X</span><span class="sxs-lookup"><span data-stu-id="cf4be-1317">X</span></span></td>
<td><span data-ttu-id="cf4be-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1319">Componente X de este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1320">Y</span><span class="sxs-lookup"><span data-stu-id="cf4be-1320">Y</span></span></td>
<td><span data-ttu-id="cf4be-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1322">Componente Y de este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf4be-1323">Z</span><span class="sxs-lookup"><span data-stu-id="cf4be-1323">Z</span></span></td>
<td><span data-ttu-id="cf4be-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="cf4be-1325">Componente Z de este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf4be-1326">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4be-1326">Type</span></span></td>
<td><span data-ttu-id="cf4be-1327"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="cf4be-1328">Unidades previstas para este vector.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1328">Expected units for this vector.</span></span> <span data-ttu-id="cf4be-1329">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="cf4be-1330">Medida</span><span class="sxs-lookup"><span data-stu-id="cf4be-1330">Measure</span></span></li>
<li><span data-ttu-id="cf4be-1331">Length</span><span class="sxs-lookup"><span data-stu-id="cf4be-1331">Length</span></span></li>
<li><span data-ttu-id="cf4be-1332">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="cf4be-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="cf4be-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="cf4be-1333">Fraction</span></span></li>
<li><span data-ttu-id="cf4be-1334">Número</span><span class="sxs-lookup"><span data-stu-id="cf4be-1334">Number</span></span></li>
<li><span data-ttu-id="cf4be-1335">Porcentaje</span><span class="sxs-lookup"><span data-stu-id="cf4be-1335">Percentage</span></span></li>
<li><span data-ttu-id="cf4be-1336">Entero</span><span class="sxs-lookup"><span data-stu-id="cf4be-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf4be-1337">**Tipo de datos de longitud**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1337">**Length data type**</span></span>

<span data-ttu-id="cf4be-1338">Número de punto flotante con un intervalo comprendido entre 0 y infinito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="cf4be-1339">**Tipo de datos Measure**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1339">**Measure data type**</span></span>

<span data-ttu-id="cf4be-1340">Un número de punto flotante desde-Infinity hasta el infinito.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="cf4be-1341">**String (tipo de datos)**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1341">**String data type**</span></span>

<span data-ttu-id="cf4be-1342">Datos de caracteres de cualquier longitud.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1342">Character data of any length.</span></span>

<span data-ttu-id="cf4be-1343">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="cf4be-1344">Modo de representación de blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="cf4be-1345">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1345">Possible values are:</span></span>

-   <span data-ttu-id="cf4be-1346">**Color**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1346">**Color**</span></span>
-   <span data-ttu-id="cf4be-1347">**Automático**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1347">**Auto**</span></span>
-   <span data-ttu-id="cf4be-1348">**Aclarar**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1348">**GrayScale**</span></span>
-   <span data-ttu-id="cf4be-1349">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="cf4be-1350">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1350">**InverseGray**</span></span>
-   <span data-ttu-id="cf4be-1351">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="cf4be-1352">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="cf4be-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1353">**HighContrast**</span></span>
-   <span data-ttu-id="cf4be-1354">**Negro**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1354">**Black**</span></span>
-   <span data-ttu-id="cf4be-1355">**Blanco**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1355">**White**</span></span>
-   <span data-ttu-id="cf4be-1356">**No dibujado**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1356">**Undrawn**</span></span>

<span data-ttu-id="cf4be-1357">**VgFraction, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1357">**VgFraction data type**</span></span>

<span data-ttu-id="cf4be-1358">Número de punto flotante con un intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="cf4be-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="cf4be-1359">Las fracciones también se pueden especificar como un porcentaje; por ejemplo, "50%".</span><span class="sxs-lookup"><span data-stu-id="cf4be-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="cf4be-1360">**Tipo de VgTriState**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="cf4be-1361">Enumeración utilizada para los valores que pueden ser de uno de estos tres Estados:</span><span class="sxs-lookup"><span data-stu-id="cf4be-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="cf4be-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1362">**TRUE**</span></span>
-   <span data-ttu-id="cf4be-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1363">**FALSE**</span></span>
-   <span data-ttu-id="cf4be-1364">**COMBINACIÓN**</span><span class="sxs-lookup"><span data-stu-id="cf4be-1364">**MIXED**</span></span>