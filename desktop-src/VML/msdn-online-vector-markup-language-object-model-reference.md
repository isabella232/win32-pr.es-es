---
title: Referencia del modelo de objetos VML
description: En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444826"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="c4552-104">Referencia del modelo de objetos VML</span><span class="sxs-lookup"><span data-stu-id="c4552-104">VML Object Model Reference</span></span>

<span data-ttu-id="c4552-105">En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c4552-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c4552-106">Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="c4552-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c4552-107">A partir de diciembre de 2011, este tema se archivó.</span><span class="sxs-lookup"><span data-stu-id="c4552-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c4552-108">Como resultado, ya no se mantiene activamente.</span><span class="sxs-lookup"><span data-stu-id="c4552-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c4552-109">Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="c4552-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c4552-110">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c4552-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c4552-111">En este tema:</span><span class="sxs-lookup"><span data-stu-id="c4552-111">In this topic:</span></span>

-   [<span data-ttu-id="c4552-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="c4552-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="c4552-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4552-113">Example</span></span>](#example)
-   [<span data-ttu-id="c4552-114">Configuración de VML</span><span class="sxs-lookup"><span data-stu-id="c4552-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="c4552-115">Referencia de VML OM</span><span class="sxs-lookup"><span data-stu-id="c4552-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="c4552-116">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="c4552-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="c4552-117">Subelementos del elemento Shape</span><span class="sxs-lookup"><span data-stu-id="c4552-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="c4552-118">Elemento Background</span><span class="sxs-lookup"><span data-stu-id="c4552-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="c4552-119">Elemento de extrusión</span><span class="sxs-lookup"><span data-stu-id="c4552-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="c4552-120">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="c4552-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="c4552-121">Group, elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="c4552-122">Elemento Imagedata</span><span class="sxs-lookup"><span data-stu-id="c4552-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="c4552-123">Path, elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="c4552-124">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="c4552-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="c4552-125">Elemento Skew</span><span class="sxs-lookup"><span data-stu-id="c4552-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="c4552-126">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="c4552-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="c4552-127">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="c4552-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="c4552-128">Tipos de datos usados en el modelo de objetos VML</span><span class="sxs-lookup"><span data-stu-id="c4552-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="c4552-129">Introducción</span><span class="sxs-lookup"><span data-stu-id="c4552-129">Introduction</span></span>

<span data-ttu-id="c4552-130">[Lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-datetime.html) es un lenguaje basado en texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para ampliar HTML con el fin de mostrar información gráfica vectorial.</span><span class="sxs-lookup"><span data-stu-id="c4552-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="c4552-131">El comando VML Document Object Model (DOM) define una interfaz de programación para la manipulación de los elementos del documento.</span><span class="sxs-lookup"><span data-stu-id="c4552-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="c4552-132">Esto permite al usuario crear y modificar dinámicamente gráficos vectoriales a través de una interfaz neutra de la plataforma y del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="c4552-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="c4552-133">EL DOM de VML se ajusta a la [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) especificación.</span><span class="sxs-lookup"><span data-stu-id="c4552-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="c4552-134">VML usa el [elemento Shape](#shape-element) como bloque de creación básico para imágenes gráficas vectoriales.</span><span class="sxs-lookup"><span data-stu-id="c4552-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="c4552-135">Una vez creada una forma, puede modificarla a través de atributos o mediante subelementos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c4552-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="c4552-136">Por ejemplo, para cambiar el color de una forma, asigne un valor de color al **atributo FillColor.**</span><span class="sxs-lookup"><span data-stu-id="c4552-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="c4552-137">Algunos de los atributos de una forma también son [subelementos](/windows) y tienen sus propios atributos, incluidos los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4552-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="c4552-138">Información preliminar</span><span class="sxs-lookup"><span data-stu-id="c4552-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="c4552-139">Extrusión</span><span class="sxs-lookup"><span data-stu-id="c4552-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="c4552-140">Fill</span><span class="sxs-lookup"><span data-stu-id="c4552-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="c4552-141">Grupo</span><span class="sxs-lookup"><span data-stu-id="c4552-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="c4552-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="c4552-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="c4552-143">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="c4552-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="c4552-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="c4552-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="c4552-145">Sesgar</span><span class="sxs-lookup"><span data-stu-id="c4552-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="c4552-146">Golpe</span><span class="sxs-lookup"><span data-stu-id="c4552-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="c4552-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="c4552-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="c4552-148">VmL OM usa varios tipos [de datos para](/windows) definir parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4552-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="c4552-149">Los tipos de datos con el prefijo "Dvón" son enumeraciones y los que tienen como prefijo "IVg" son objetos .</span><span class="sxs-lookup"><span data-stu-id="c4552-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="c4552-150">Haga clic aquí para obtener una lista.</span><span class="sxs-lookup"><span data-stu-id="c4552-150">Click here for a list.</span></span> <span data-ttu-id="c4552-151">Los tipos de datos menores se enumeran con parámetros específicos.</span><span class="sxs-lookup"><span data-stu-id="c4552-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="c4552-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4552-152">Example</span></span>

<span data-ttu-id="c4552-153">El siguiente código VBScript muestra cómo crear una forma simple:</span><span class="sxs-lookup"><span data-stu-id="c4552-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="c4552-154">En el ejemplo anterior, se crea una forma mediante el Document Object Model **método CreateElement**.</span><span class="sxs-lookup"><span data-stu-id="c4552-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="c4552-155">La forma es una forma rect predefinida de VML.</span><span class="sxs-lookup"><span data-stu-id="c4552-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="c4552-156">Aunque el objeto existe, no puede formar parte del documento hasta que se adjunta al documento.</span><span class="sxs-lookup"><span data-stu-id="c4552-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="c4552-157">Con el **método AppendChild,** rect se hace un elemento secundario de **un elemento DIV** denominado MyDiv.</span><span class="sxs-lookup"><span data-stu-id="c4552-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="c4552-158">Algunos atributos de estilo mínimos **(Posición,** **Ancho,** **Alto,** **Superior,** **Izquierda)** se establecen para dar a la forma un tamaño específico.</span><span class="sxs-lookup"><span data-stu-id="c4552-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="c4552-159">Por último, se asigna un color con el **atributo FillColor.**</span><span class="sxs-lookup"><span data-stu-id="c4552-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="c4552-160">Tenga en cuenta que se puede usar cualquier lenguaje de scripting o cualquier lenguaje que pueda trabajar con Document Object Model interfaces.</span><span class="sxs-lookup"><span data-stu-id="c4552-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="c4552-161">Configuración de VML</span><span class="sxs-lookup"><span data-stu-id="c4552-161">Setting up VML</span></span>

<span data-ttu-id="c4552-162">Una implementación de VML se realiza a través de Microsoft Internet Explorer 5.0 o superior.</span><span class="sxs-lookup"><span data-stu-id="c4552-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="c4552-163">Para configurar el objeto de representación correctamente en una página web, se deben realizar las siguientes adiciones:</span><span class="sxs-lookup"><span data-stu-id="c4552-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="c4552-164">El esquema debe configurarse en la versión inicial.</span><span class="sxs-lookup"><span data-stu-id="c4552-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="c4552-165">etiqueta de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c4552-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="c4552-166">El comportamiento de representación debe formar parte del estilo del documento:</span><span class="sxs-lookup"><span data-stu-id="c4552-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="c4552-167">A continuación se muestra una página web HTML de ejemplo configurada correctamente para VML que muestra la creación dinámica de una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="c4552-168">Tenga en cuenta que en las versiones beta, se requería una etiqueta de objeto ActiveX y un estilo de comportamiento diferente.</span><span class="sxs-lookup"><span data-stu-id="c4552-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="c4552-169">Referencia de VML OM</span><span class="sxs-lookup"><span data-stu-id="c4552-169">VML OM Reference</span></span>

<span data-ttu-id="c4552-170">Esta referencia define el [elemento Shape,](#shape-element) [los subelementos](/windows)y [los](/windows) tipos de datos que usa el modelo de objetos de VML.</span><span class="sxs-lookup"><span data-stu-id="c4552-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="c4552-171">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="c4552-171">Shape element</span></span>

<span data-ttu-id="c4552-172">Las formas son los bloques de creación de imágenes gráficas definidas por Lenguaje de marcado de vectores (VML).</span><span class="sxs-lookup"><span data-stu-id="c4552-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="c4552-173">La forma es el elemento de nivel superior y varios subelementos ayudan a definir la naturaleza de cada forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="c4552-174">VML proporciona formas predefinidas:</span><span class="sxs-lookup"><span data-stu-id="c4552-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="c4552-175">**Atributos de forma**</span><span class="sxs-lookup"><span data-stu-id="c4552-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="c4552-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="c4552-176">**Arc**</span></span>
-   <span data-ttu-id="c4552-177">**Curva**</span><span class="sxs-lookup"><span data-stu-id="c4552-177">**Curve**</span></span>
-   <span data-ttu-id="c4552-178">**Line**</span><span class="sxs-lookup"><span data-stu-id="c4552-178">**Line**</span></span>
-   <span data-ttu-id="c4552-179">**Polilínea**</span><span class="sxs-lookup"><span data-stu-id="c4552-179">**PolyLine**</span></span>
-   <span data-ttu-id="c4552-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="c4552-180">**Rect**</span></span>
-   <span data-ttu-id="c4552-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="c4552-181">**RoundRect**</span></span>



|   <span data-ttu-id="c4552-182">Subelemento</span><span class="sxs-lookup"><span data-stu-id="c4552-182">Subelement</span></span>           |    <span data-ttu-id="c4552-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-184">Adj</span><span class="sxs-lookup"><span data-stu-id="c4552-184">Adj</span></span>          | <span data-ttu-id="c4552-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="c4552-186">Lista delimitada por comas de números que son los parámetros de las fórmulas de guía que definen el trazado de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="c4552-187">Los valores se pueden omitir para permitir el uso de valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c4552-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="c4552-188">Puede haber hasta 8 valores de ajuste.</span><span class="sxs-lookup"><span data-stu-id="c4552-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="c4552-189">Alt</span><span class="sxs-lookup"><span data-stu-id="c4552-189">Alt</span></span>          | <span data-ttu-id="c4552-190">String.</span><span class="sxs-lookup"><span data-stu-id="c4552-190">String.</span></span> <span data-ttu-id="c4552-191">Texto alternativo asociado a la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-191">Alternative text associated with shape.</span></span> <span data-ttu-id="c4552-192">Se usa para la exploración no gráfica.</span><span class="sxs-lookup"><span data-stu-id="c4552-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c4552-193">Botón</span><span class="sxs-lookup"><span data-stu-id="c4552-193">Button</span></span>       | <span data-ttu-id="c4552-194">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-195">Muestra el comportamiento del botón al hacer clic.</span><span class="sxs-lookup"><span data-stu-id="c4552-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c4552-196">BWMode</span><span class="sxs-lookup"><span data-stu-id="c4552-196">BWMode</span></span>       | <span data-ttu-id="c4552-197">[DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="c4552-198">Determina cómo se representará la forma en la vista en blanco y negro en las aplicaciones o cuando se imprime en impresoras en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="c4552-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="c4552-199">Los valores incluyen: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="c4552-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="c4552-200">Valor predeterminado: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="c4552-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="c4552-201">BWNormal</span><span class="sxs-lookup"><span data-stu-id="c4552-201">BWNormal</span></span>     | <span data-ttu-id="c4552-202">DvBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="c4552-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="c4552-203">Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en blanco y negro normal.</span><span class="sxs-lookup"><span data-stu-id="c4552-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="c4552-204">Los valores incluyen: **Color,** **Auto,** **GrayScale,** **LightGrayScale,** **InverseGray,** **GrayOutline,** **BlackTextAndLines,** **HighContrast,** **Black,** **White** y **Undrawn.**</span><span class="sxs-lookup"><span data-stu-id="c4552-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="c4552-205">Valor predeterminado: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="c4552-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="c4552-206">BWPure</span><span class="sxs-lookup"><span data-stu-id="c4552-206">BWPure</span></span>       | <span data-ttu-id="c4552-207">DvBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="c4552-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="c4552-208">Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en B/W puro.</span><span class="sxs-lookup"><span data-stu-id="c4552-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="c4552-209">Los valores incluyen: **Color,** **Auto,** **GrayScale,** **LightGrayScale,** **InverseGray,** **GrayOutline,** **BlackTextAndLines,** **HighContrast,** **Black,** **White** y **Undrawn.**</span><span class="sxs-lookup"><span data-stu-id="c4552-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="c4552-210">Valor predeterminado: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="c4552-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="c4552-211">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="c4552-211">ChildShapes</span></span>  | <span data-ttu-id="c4552-212">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="c4552-212">IVgGroupShapes.</span></span> <span data-ttu-id="c4552-213">Colección de otras formas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="c4552-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="c4552-214">Esta colección admite los métodos Length y Item estándar.</span><span class="sxs-lookup"><span data-stu-id="c4552-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c4552-215">Chromakey</span><span class="sxs-lookup"><span data-stu-id="c4552-215">Chromakey</span></span>    | <span data-ttu-id="c4552-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="c4552-217">Valor de color que será transparente y mostrará todo lo que hay detrás de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c4552-218">Control1</span><span class="sxs-lookup"><span data-stu-id="c4552-218">Control1</span></span>     | <span data-ttu-id="c4552-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-220">Punto de control para curva.</span><span class="sxs-lookup"><span data-stu-id="c4552-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4552-221">Control2</span><span class="sxs-lookup"><span data-stu-id="c4552-221">Control2</span></span>     | <span data-ttu-id="c4552-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-223">Punto de control para curva.</span><span class="sxs-lookup"><span data-stu-id="c4552-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4552-224">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="c4552-224">CoordOrigin</span></span>  | <span data-ttu-id="c4552-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordenadas en la esquina superior izquierda del rectángulo del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c4552-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="c4552-226">Va de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="c4552-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="c4552-227">CoordSize</span><span class="sxs-lookup"><span data-stu-id="c4552-227">CoordSize</span></span>    | <span data-ttu-id="c4552-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-229">Ancho y alto del espacio de coordenadas dentro del rectángulo de referencia de esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="c4552-230">Si no se especifica, es igual que el ancho y alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c4552-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="c4552-231">Va de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="c4552-231">Range from 0 to infinity.</span></span> <span data-ttu-id="c4552-232">Valor predeterminado: "1000 1000".</span><span class="sxs-lookup"><span data-stu-id="c4552-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="c4552-233">EndAngle</span><span class="sxs-lookup"><span data-stu-id="c4552-233">EndAngle</span></span>     | <span data-ttu-id="c4552-234">[DvangleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="c4552-235">Ángulo final de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c4552-236">Extrusión</span><span class="sxs-lookup"><span data-stu-id="c4552-236">Extrusion</span></span>    | <span data-ttu-id="c4552-237">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="c4552-237">IVgExtrusion.</span></span> <span data-ttu-id="c4552-238">Especifica el valor del objeto de extrusión para esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="c4552-239">Consulte el [elemento Extrusión](msdn-online-vml-extrusion-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4552-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="c4552-240">Rellenar</span><span class="sxs-lookup"><span data-stu-id="c4552-240">Fill</span></span>         | <span data-ttu-id="c4552-241">FillFormat.</span><span class="sxs-lookup"><span data-stu-id="c4552-241">VgFillFormat.</span></span> <span data-ttu-id="c4552-242">Especifica el valor de relleno para esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="c4552-243">Consulte el [elemento Fill](msdn-online-vml-fill-element.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="c4552-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="c4552-244">FillColor</span><span class="sxs-lookup"><span data-stu-id="c4552-244">FillColor</span></span>    | <span data-ttu-id="c4552-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="c4552-246">Color principal del pincel que se va a usar para rellenar el trazado de esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4552-247">Lleno</span><span class="sxs-lookup"><span data-stu-id="c4552-247">Filled</span></span>       | <span data-ttu-id="c4552-248">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-249">Si es True, se rellenará la ruta de acceso que define la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="c4552-250">De forma predeterminada, se rellenará con un color sólido a menos que haya un subelemento Fill que especifique propiedades de relleno más complejas.</span><span class="sxs-lookup"><span data-stu-id="c4552-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="c4552-251">Si es False, el relleno es transparente.</span><span class="sxs-lookup"><span data-stu-id="c4552-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="c4552-252">Voltear</span><span class="sxs-lookup"><span data-stu-id="c4552-252">Flip</span></span>         | <span data-ttu-id="c4552-253">DvFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="c4552-253">VgFlipOrientation.</span></span> <span data-ttu-id="c4552-254">Los valores son: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="c4552-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c4552-255">ForceDash</span><span class="sxs-lookup"><span data-stu-id="c4552-255">ForceDash</span></span>    | <span data-ttu-id="c4552-256">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-257">Indicación de que se debe representar un contorno discontinuo cuando no hay ninguna línea ni relleno para una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="c4552-258">Este comportamiento suele ser útil para hacer que las formas invisibles sean visibles en las aplicaciones de edición para que se puedan seleccionar y operar, como en un mapa de imágenes.</span><span class="sxs-lookup"><span data-stu-id="c4552-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="c4552-259">Fórmulas</span><span class="sxs-lookup"><span data-stu-id="c4552-259">Formulas</span></span>     | <span data-ttu-id="c4552-260">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="c4552-260">IVgFormulas.</span></span> <span data-ttu-id="c4552-261">Matriz de fórmulas que define una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c4552-262">From</span><span class="sxs-lookup"><span data-stu-id="c4552-262">From</span></span>         | <span data-ttu-id="c4552-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-264">Punto inicial de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c4552-265">Href</span><span class="sxs-lookup"><span data-stu-id="c4552-265">HRef</span></span>         | <span data-ttu-id="c4552-266">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-267">Dirección URL a la que saltar si se hace clic en esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c4552-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="c4552-268">ImageData</span></span>    | <span data-ttu-id="c4552-269">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="c4552-269">IVgImageData.</span></span> <span data-ttu-id="c4552-270">Información de la imagen si la forma es una imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="c4552-271">Vea el elemento ImageData para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4552-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c4552-272">OnEd</span><span class="sxs-lookup"><span data-stu-id="c4552-272">OnEd</span></span>         | <span data-ttu-id="c4552-273">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-274">Oculta todos los identificadores excepto la parte superior izquierda e inferior derecha, como en los identificadores de un segmento de línea recta.</span><span class="sxs-lookup"><span data-stu-id="c4552-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="c4552-275">Opacidad</span><span class="sxs-lookup"><span data-stu-id="c4552-275">Opacity</span></span>      | <span data-ttu-id="c4552-276">[DvIon.](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="c4552-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="c4552-277">Opacidad de toda la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-277">The opacity of the entire shape.</span></span> <span data-ttu-id="c4552-278">Número entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="c4552-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c4552-279">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="c4552-279">Path</span></span>         | <span data-ttu-id="c4552-280">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="c4552-280">IVgPath.</span></span> <span data-ttu-id="c4552-281">Cadena que contiene los comandos que definen la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4552-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4552-282">Puntos</span><span class="sxs-lookup"><span data-stu-id="c4552-282">Points</span></span>       | <span data-ttu-id="c4552-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="c4552-284">Colección de puntos que definen una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c4552-285">Impresión</span><span class="sxs-lookup"><span data-stu-id="c4552-285">Print</span></span>        | <span data-ttu-id="c4552-286">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-287">Si es True, esta forma está pensada para imprimirse.</span><span class="sxs-lookup"><span data-stu-id="c4552-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c4552-288">Rotación</span><span class="sxs-lookup"><span data-stu-id="c4552-288">Rotation</span></span>     | <span data-ttu-id="c4552-289">[DvangleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="c4552-290">Establece la rotación de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-290">Sets rotation of shape.</span></span> <span data-ttu-id="c4552-291">El valor se propaga al estilo de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="c4552-292">Escala</span><span class="sxs-lookup"><span data-stu-id="c4552-292">Scale</span></span>        | <span data-ttu-id="c4552-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-294">Escala de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c4552-295">Shadow</span><span class="sxs-lookup"><span data-stu-id="c4552-295">Shadow</span></span>       | <span data-ttu-id="c4552-296">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="c4552-296">IVgShadow.</span></span> <span data-ttu-id="c4552-297">Especifica la sombra de esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="c4552-298">Consulte el [elemento Shadow](msdn-online-vml-shadow-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4552-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c4552-299">Spt</span><span class="sxs-lookup"><span data-stu-id="c4552-299">Spt</span></span>          | <span data-ttu-id="c4552-300">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c4552-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c4552-301">StartAngle</span><span class="sxs-lookup"><span data-stu-id="c4552-301">StartAngle</span></span>   | <span data-ttu-id="c4552-302">[DvangleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="c4552-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="c4552-303">Ángulo de inicio de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c4552-304">Carrera</span><span class="sxs-lookup"><span data-stu-id="c4552-304">Stroke</span></span>       | <span data-ttu-id="c4552-305">DvstrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="c4552-305">VgStrokeFormat.</span></span> <span data-ttu-id="c4552-306">Vea Elemento Stroke para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4552-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4552-307">Strokecolor</span><span class="sxs-lookup"><span data-stu-id="c4552-307">StrokeColor</span></span>  | <span data-ttu-id="c4552-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="c4552-309">Color principal del pincel que se va a usar para acariciar el trazado de esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c4552-310">Acarició</span><span class="sxs-lookup"><span data-stu-id="c4552-310">Stroked</span></span>      | <span data-ttu-id="c4552-311">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-312">Si es True, se trazo el trazado que define la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c4552-313">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="c4552-313">StrokeWeight</span></span> | <span data-ttu-id="c4552-314">[SILENGTH](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="c4552-315">Ancho del pincel que se usará para acariciar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4552-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="c4552-316">Intervalos entre 0 y 1584.</span><span class="sxs-lookup"><span data-stu-id="c4552-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c4552-317">TextPath</span><span class="sxs-lookup"><span data-stu-id="c4552-317">TextPath</span></span>     | <span data-ttu-id="c4552-318">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="c4552-318">IVgTextPath.</span></span> <span data-ttu-id="c4552-319">Especifica el objeto TextPath de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="c4552-320">Consulte el [elemento TextPath](msdn-online-vml-textpath-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4552-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4552-321">En</span><span class="sxs-lookup"><span data-stu-id="c4552-321">To</span></span>           | <span data-ttu-id="c4552-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-323">Punto final de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c4552-324">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-324">Type</span></span>         | <span data-ttu-id="c4552-325">String.</span><span class="sxs-lookup"><span data-stu-id="c4552-325">String.</span></span> <span data-ttu-id="c4552-326">Tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="c4552-327">Subelementos del elemento Shape</span><span class="sxs-lookup"><span data-stu-id="c4552-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="c4552-328">Los siguientes subelementos forman parte del modelo de objetos VML.</span><span class="sxs-lookup"><span data-stu-id="c4552-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="c4552-329">Información preliminar</span><span class="sxs-lookup"><span data-stu-id="c4552-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="c4552-330">Extrusión</span><span class="sxs-lookup"><span data-stu-id="c4552-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="c4552-331">Fill</span><span class="sxs-lookup"><span data-stu-id="c4552-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="c4552-332">Grupo</span><span class="sxs-lookup"><span data-stu-id="c4552-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="c4552-333">Imagedata</span><span class="sxs-lookup"><span data-stu-id="c4552-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="c4552-334">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="c4552-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="c4552-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="c4552-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="c4552-336">Sesgar</span><span class="sxs-lookup"><span data-stu-id="c4552-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="c4552-337">Golpe</span><span class="sxs-lookup"><span data-stu-id="c4552-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="c4552-338">TextPath</span><span class="sxs-lookup"><span data-stu-id="c4552-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="c4552-339">Elemento Background</span><span class="sxs-lookup"><span data-stu-id="c4552-339">Background element</span></span>

<span data-ttu-id="c4552-340">Describe el relleno del fondo de una página mediante rellenos de VML.</span><span class="sxs-lookup"><span data-stu-id="c4552-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="c4552-341">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-341">Attribute</span></span>        |   <span data-ttu-id="c4552-342">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-343">BWMode</span><span class="sxs-lookup"><span data-stu-id="c4552-343">BWMode</span></span>    | <span data-ttu-id="c4552-344">[DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="c4552-345">Determina cómo se representará la forma en la vista en blanco y negro en las aplicaciones o cuando se imprima.</span><span class="sxs-lookup"><span data-stu-id="c4552-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="c4552-346">BWNormal</span><span class="sxs-lookup"><span data-stu-id="c4552-346">BWNormal</span></span>  | <span data-ttu-id="c4552-347">[DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="c4552-348">Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en blanco y negro normales.</span><span class="sxs-lookup"><span data-stu-id="c4552-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="c4552-349">BWPure</span><span class="sxs-lookup"><span data-stu-id="c4552-349">BWPure</span></span>    | <span data-ttu-id="c4552-350">[DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="c4552-351">Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en blanco y negro puro.</span><span class="sxs-lookup"><span data-stu-id="c4552-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="c4552-352">Rellenar</span><span class="sxs-lookup"><span data-stu-id="c4552-352">Fill</span></span>      | <span data-ttu-id="c4552-353">FillFillFormat.</span><span class="sxs-lookup"><span data-stu-id="c4552-353">VgFillFormat.</span></span> <span data-ttu-id="c4552-354">Especifica el relleno de esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="c4552-355">Vea [Elemento Fill](msdn-online-vml-fill-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4552-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="c4552-356">FillColor</span><span class="sxs-lookup"><span data-stu-id="c4552-356">FillColor</span></span> | <span data-ttu-id="c4552-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="c4552-358">Color principal del pincel que se va a usar para rellenar el trazado de esta forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="c4552-359">Duplicado del valor Color en el elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="c4552-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="c4552-360">El valor predeterminado es blanco.</span><span class="sxs-lookup"><span data-stu-id="c4552-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="c4552-361">Elemento Desatrusión</span><span class="sxs-lookup"><span data-stu-id="c4552-361">Extrusion element</span></span>

<span data-ttu-id="c4552-362">Describe una extrusión 3D de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="c4552-363">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="c4552-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-364">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="c4552-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="c4552-365"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-366">Si es True, el centro de rotación del grupo de objetos 3D (de hecho, solo hay un objeto en el grupo) se determina automáticamente como el centro del grupo; De lo contrario, viene determinado por los parámetros RotationCenter, que son una fracción de la forma con 0,0,0 como centro.</span><span class="sxs-lookup"><span data-stu-id="c4552-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-367">BackDepth</span><span class="sxs-lookup"><span data-stu-id="c4552-367">BackDepth</span></span></td>
<td><span data-ttu-id="c4552-368"><a href="msdn-online-vml-vglength.md"><strong>DvLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="c4552-369">Cantidad de extrusión hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="c4552-369">Amount of backward extrusion.</span></span> <span data-ttu-id="c4552-370">Oscila entre 0 y 32767.</span><span class="sxs-lookup"><span data-stu-id="c4552-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-371">Luminosidad</span><span class="sxs-lookup"><span data-stu-id="c4552-371">Brightness</span></span></td>
<td><span data-ttu-id="c4552-372"><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="c4552-373">Brillo general de la escena.</span><span class="sxs-lookup"><span data-stu-id="c4552-373">Overall brightness of the scene.</span></span> <span data-ttu-id="c4552-374">El valor &quot; predeterminado es 20 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-375">Color</span><span class="sxs-lookup"><span data-stu-id="c4552-375">Color</span></span></td>
<td><span data-ttu-id="c4552-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="c4552-377">Color de la extrusión.</span><span class="sxs-lookup"><span data-stu-id="c4552-377">The color of the extrusion.</span></span> <span data-ttu-id="c4552-378">Solo se usa si ColorMode es Personalizado.</span><span class="sxs-lookup"><span data-stu-id="c4552-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="c4552-379">De lo contrario, Auto establece el color del efecto de extrusión en el mismo que FillColor.</span><span class="sxs-lookup"><span data-stu-id="c4552-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-380">ColorMode</span><span class="sxs-lookup"><span data-stu-id="c4552-380">ColorMode</span></span></td>
<td><span data-ttu-id="c4552-381">Dv3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="c4552-381">Vg3DColorMode.</span></span> <span data-ttu-id="c4552-382">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-383">Auto (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-383">Auto (default)</span></span></li>
<li><span data-ttu-id="c4552-384">Personalizado</span><span class="sxs-lookup"><span data-stu-id="c4552-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-385">Diffusity</span><span class="sxs-lookup"><span data-stu-id="c4552-385">Diffusity</span></span></td>
<td><span data-ttu-id="c4552-386"><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="c4552-387">Proporción de incidente con luz reflejada difusamente.</span><span class="sxs-lookup"><span data-stu-id="c4552-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="c4552-388">Los valores menores que 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="c4552-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-389">Edge</span><span class="sxs-lookup"><span data-stu-id="c4552-389">Edge</span></span></td>
<td><span data-ttu-id="c4552-390"><a href="msdn-online-vml-vglength.md">DvLength</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="c4552-391">Establece el tamaño de un borde biselado redondeado simulado.</span><span class="sxs-lookup"><span data-stu-id="c4552-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="c4552-392">Oscila entre 0 y 32767 en puntos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="c4552-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="c4552-393">El valor predeterminado &quot; es 1pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-394">Faceta</span><span class="sxs-lookup"><span data-stu-id="c4552-394">Facet</span></span></td>
<td><span data-ttu-id="c4552-395"><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="c4552-396">Establece la faceta de la escena.</span><span class="sxs-lookup"><span data-stu-id="c4552-396">Sets the facet of the scene.</span></span> <span data-ttu-id="c4552-397">El valor &quot; predeterminado es 30 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-398">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="c4552-398">ForeDepth</span></span></td>
<td><span data-ttu-id="c4552-399"><a href="msdn-online-vml-vglength.md">DvLength</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="c4552-400">Cantidad de extrusión hacia delante.</span><span class="sxs-lookup"><span data-stu-id="c4552-400">Amount of forward extrusion.</span></span> <span data-ttu-id="c4552-401">Oscila entre 0 y 32767.</span><span class="sxs-lookup"><span data-stu-id="c4552-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-402">LightFace</span><span class="sxs-lookup"><span data-stu-id="c4552-402">LightFace</span></span></td>
<td><span data-ttu-id="c4552-403"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-404">Determina si la cara frontal del objeto responderá a los cambios en la iluminación 3D, por ejemplo, cuando un objeto gira.</span><span class="sxs-lookup"><span data-stu-id="c4552-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-405">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="c4552-405">LightHarsh</span></span></td>
<td><span data-ttu-id="c4552-406"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-407">Iluminación desalumbrada para la fuente de luz principal.</span><span class="sxs-lookup"><span data-stu-id="c4552-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="c4552-408">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="c4552-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="c4552-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="c4552-410"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-411">Iluminación desalumbrada para la fuente de luz secundaria.</span><span class="sxs-lookup"><span data-stu-id="c4552-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="c4552-412">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="c4552-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-413">LightLevel</span><span class="sxs-lookup"><span data-stu-id="c4552-413">LightLevel</span></span></td>
<td><span data-ttu-id="c4552-414"><a href="#data-types-used-in-the-vml-object-model">NumberNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="c4552-415">Intensidad de la fuente de luz principal.</span><span class="sxs-lookup"><span data-stu-id="c4552-415">Intensity of the primary light source.</span></span> <span data-ttu-id="c4552-416">El valor &quot; predeterminado es 38000. &quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="c4552-417">LightLevel2</span></span></td>
<td><span data-ttu-id="c4552-418"><a href="#data-types-used-in-the-vml-object-model">NumberNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="c4552-419">Intensidad de la fuente de luz secundaria.</span><span class="sxs-lookup"><span data-stu-id="c4552-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="c4552-420">El valor &quot; predeterminado es 38000. &quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-421">LightPosition</span><span class="sxs-lookup"><span data-stu-id="c4552-421">LightPosition</span></span></td>
<td><span data-ttu-id="c4552-422">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="c4552-422">Vector3D.</span></span> <span data-ttu-id="c4552-423">Posición de la fuente de luz principal.</span><span class="sxs-lookup"><span data-stu-id="c4552-423">Position of the primary light source.</span></span> <span data-ttu-id="c4552-424">El valor &quot; predeterminado es 50000,0,10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="c4552-425">LightPosition2</span></span></td>
<td><span data-ttu-id="c4552-426">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="c4552-426">Vector3D.</span></span> <span data-ttu-id="c4552-427">Posición de la fuente de luz secundaria.</span><span class="sxs-lookup"><span data-stu-id="c4552-427">Position of the secondary light source.</span></span> <span data-ttu-id="c4552-428">El valor &quot; predeterminado es -50000,0,10000. &quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-429">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="c4552-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="c4552-430"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-431">&quot;Lockrotationcenter significa que la rotación del grupo se define para que sea mediante ángulo de rotación[1] grados sobre el eje Y de la página seguido de ángulo de rotación[0] grados sobre el eje &quot; X.</span><span class="sxs-lookup"><span data-stu-id="c4552-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="c4552-432">Cuando LockRotationCenter es False, la rotación se define para que sea por grados de ángulo de orientación sobre el vector definido por la orientación.</span><span class="sxs-lookup"><span data-stu-id="c4552-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="c4552-433">Por ejemplo, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) equivale a lockrotationcenter=true rotationangle=(0,45).</span><span class="sxs-lookup"><span data-stu-id="c4552-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-434">Metal</span><span class="sxs-lookup"><span data-stu-id="c4552-434">Metal</span></span></td>
<td><span data-ttu-id="c4552-435"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-436">Hace que la luz reflejada especularmente sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más ligero.</span><span class="sxs-lookup"><span data-stu-id="c4552-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-437">Activado</span><span class="sxs-lookup"><span data-stu-id="c4552-437">On</span></span></td>
<td><span data-ttu-id="c4552-438"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-439">Activa y desactiva la presentación del efecto de extrusión.</span><span class="sxs-lookup"><span data-stu-id="c4552-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-440">Orientación</span><span class="sxs-lookup"><span data-stu-id="c4552-440">Orientation</span></span></td>
<td><span data-ttu-id="c4552-441">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="c4552-441">Vector3D.</span></span> <span data-ttu-id="c4552-442">Orientación de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c4552-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-443">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="c4552-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="c4552-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">DvangleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="c4552-445">Ángulo entre la orientación de la cámara y el plano xy.</span><span class="sxs-lookup"><span data-stu-id="c4552-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-446">Avión</span><span class="sxs-lookup"><span data-stu-id="c4552-446">Plane</span></span></td>
<td><span data-ttu-id="c4552-447">Dv3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="c4552-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="c4552-448">Permite la extrusión desde planos ortogonales al plano de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c4552-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="c4552-449">Requiere que ForeDepth y BackDepth se especifiquen en unidades de dibujo en lugar de emus.</span><span class="sxs-lookup"><span data-stu-id="c4552-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="c4552-450">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-451">Xy</span><span class="sxs-lookup"><span data-stu-id="c4552-451">XY</span></span></li>
<li><span data-ttu-id="c4552-452">Zx</span><span class="sxs-lookup"><span data-stu-id="c4552-452">ZX</span></span></li>
<li><span data-ttu-id="c4552-453">Yz</span><span class="sxs-lookup"><span data-stu-id="c4552-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-454">Representación</span><span class="sxs-lookup"><span data-stu-id="c4552-454">Render</span></span></td>
<td><span data-ttu-id="c4552-455">Dv3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="c4552-455">Vg3DRenderMode.</span></span> <span data-ttu-id="c4552-456">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-457">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-457">Solid (default)</span></span></li>
<li><span data-ttu-id="c4552-458">Alambre</span><span class="sxs-lookup"><span data-stu-id="c4552-458">WireFrame</span></span></li>
<li><span data-ttu-id="c4552-459">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="c4552-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-460">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="c4552-460">RotationAngle</span></span></td>
<td><span data-ttu-id="c4552-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-462">AngleX, AngleY o AngleZ se controla mediante el atributo ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="c4552-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-463">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="c4552-463">RotationCenter</span></span></td>
<td><span data-ttu-id="c4552-464">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="c4552-464">Vector3D.</span></span> <span data-ttu-id="c4552-465">Centro de rotación.</span><span class="sxs-lookup"><span data-stu-id="c4552-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-466">Brillo</span><span class="sxs-lookup"><span data-stu-id="c4552-466">Shininess</span></span></td>
<td><span data-ttu-id="c4552-467"><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="c4552-468">Determina lo que es la reflexión especular entrelazados o es una reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="c4552-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="c4552-469">Un valor alto sería de 8 a 10 y se aproximaría a un reflejo, y un valor bajo sería de 2 a 3 y se aproximaría a la ropa entrelazada.</span><span class="sxs-lookup"><span data-stu-id="c4552-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="c4552-470">Se recomiendan valores de 3 a 7.</span><span class="sxs-lookup"><span data-stu-id="c4552-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="c4552-471">Los valores altos reflejarán las fuentes de luz precisas.</span><span class="sxs-lookup"><span data-stu-id="c4552-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-472">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="c4552-472">SkewAmt</span></span></td>
<td><span data-ttu-id="c4552-473"><a href="#data-types-used-in-the-vml-object-model">DvPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="c4552-474">Si Type es Parallel, el atributo determina la cantidad de asimetría.</span><span class="sxs-lookup"><span data-stu-id="c4552-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="c4552-475">Oscila entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="c4552-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-476">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="c4552-476">SkewAngle</span></span></td>
<td><span data-ttu-id="c4552-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">DvangleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="c4552-478">Si Type es Parallel, el atributo determina el grado de asimetría.</span><span class="sxs-lookup"><span data-stu-id="c4552-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="c4552-479">El valor &quot; predeterminado es -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-480">Especularidad</span><span class="sxs-lookup"><span data-stu-id="c4552-480">Specularity</span></span></td>
<td><span data-ttu-id="c4552-481"><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="c4552-482">Proporción del incidente con la luz reflejada especularmente.</span><span class="sxs-lookup"><span data-stu-id="c4552-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="c4552-483">Los valores inferiores a 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="c4552-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-484">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-484">Type</span></span></td>
<td><span data-ttu-id="c4552-485">DvExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="c4552-485">VgExtrusionType.</span></span> <span data-ttu-id="c4552-486">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-487">Parallel (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="c4552-488">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="c4552-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-489">Mirador</span><span class="sxs-lookup"><span data-stu-id="c4552-489">Viewpoint</span></span></td>
<td><span data-ttu-id="c4552-490">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="c4552-490">Vector3D.</span></span> <span data-ttu-id="c4552-491">Punto desde el que se está visualizando la escena.</span><span class="sxs-lookup"><span data-stu-id="c4552-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-492">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="c4552-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="c4552-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-494">Puede tener valores de 0,5 a -0,5 para colocar el origen del punto de vista en el cuadro de límite de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="c4552-495">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="c4552-495">Fill element</span></span>

<span data-ttu-id="c4552-496">Describe cómo se debe rellenar un trazado para rellenos más complejos que un color sólido.</span><span class="sxs-lookup"><span data-stu-id="c4552-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="c4552-497">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="c4552-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-498">AlignShape</span><span class="sxs-lookup"><span data-stu-id="c4552-498">AlignShape</span></span></td>
<td><span data-ttu-id="c4552-499"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-500">Alinee la imagen con la forma .</span><span class="sxs-lookup"><span data-stu-id="c4552-500">Align the image with the shape.</span></span> <span data-ttu-id="c4552-501">Si es False, alinee la imagen con la ventana.</span><span class="sxs-lookup"><span data-stu-id="c4552-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-502">Ángulo</span><span class="sxs-lookup"><span data-stu-id="c4552-502">Angle</span></span></td>
<td><span data-ttu-id="c4552-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">DvangleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="c4552-504">Ángulo a lo largo del cual va el degradado.</span><span class="sxs-lookup"><span data-stu-id="c4552-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="c4552-505">0 grados a lo largo del eje horizontal de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="c4552-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-506">Aspecto</span><span class="sxs-lookup"><span data-stu-id="c4552-506">Aspect</span></span></td>
<td><span data-ttu-id="c4552-507"><strong>DvAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="c4552-508">El atributo ImageSize se ajustará para conservar el aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="c4552-509">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="c4552-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-510">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-510">Value</span></span></th>
<th><span data-ttu-id="c4552-511">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-512">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c4552-512">Ignore</span></span></td>
<td><span data-ttu-id="c4552-513">Omitir problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="c4552-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-514">Atleast</span><span class="sxs-lookup"><span data-stu-id="c4552-514">AtLeast</span></span></td>
<td><span data-ttu-id="c4552-515">La imagen es al menos tan grande como el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-516">Atmost</span><span class="sxs-lookup"><span data-stu-id="c4552-516">AtMost</span></span></td>
<td><span data-ttu-id="c4552-517">La imagen no es mayor que el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-518">Color</span><span class="sxs-lookup"><span data-stu-id="c4552-518">Color</span></span></td>
<td><span data-ttu-id="c4552-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Color de relleno principal.</span><span class="sxs-lookup"><span data-stu-id="c4552-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="c4552-520">Igual que el atributo FillColor en forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-521">Color2</span><span class="sxs-lookup"><span data-stu-id="c4552-521">Color2</span></span></td>
<td><span data-ttu-id="c4552-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="c4552-523">Color secundario de un relleno cuando el tipo de imagen es Pattern o un relleno de degradado.</span><span class="sxs-lookup"><span data-stu-id="c4552-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-524">Colores</span><span class="sxs-lookup"><span data-stu-id="c4552-524">Colors</span></span></td>
<td><span data-ttu-id="c4552-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="c4552-526">Colores intermedios en el degradado y sus posiciones relativas a lo largo del degradado, por ejemplo, &quot; 30 % rojo, 70 % azul, 90 % verde &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="c4552-527">El color principal (atributo color en forma) es 0 % y el color secundario (atributo Color2) es 100 %.</span><span class="sxs-lookup"><span data-stu-id="c4552-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-528">Foco</span><span class="sxs-lookup"><span data-stu-id="c4552-528">Focus</span></span></td>
<td><span data-ttu-id="c4552-529"><a href="#data-types-used-in-the-vml-object-model">DvSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="c4552-530">Punto focal para relleno de degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="c4552-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="c4552-531">Los valores van de -100 a +100.</span><span class="sxs-lookup"><span data-stu-id="c4552-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-532">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="c4552-532">FocusPosition</span></span></td>
<td><span data-ttu-id="c4552-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-534">Posición del rectángulo más interno para degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="c4552-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="c4552-535">El vector es una fracción (0,0 - 1,0) del ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-536">FocusSize</span><span class="sxs-lookup"><span data-stu-id="c4552-536">FocusSize</span></span></td>
<td><span data-ttu-id="c4552-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamaño del rectángulo más interno para degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="c4552-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="c4552-538">El vector es una fracción (de 0,0 a 1,0) del ancho y alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-539">Método</span><span class="sxs-lookup"><span data-stu-id="c4552-539">Method</span></span></td>
<td><span data-ttu-id="c4552-540">DvsigmaType.</span><span class="sxs-lookup"><span data-stu-id="c4552-540">VgSigmaType.</span></span> <span data-ttu-id="c4552-541">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="c4552-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="c4552-542">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c4552-542">None</span></span></li>
<li><span data-ttu-id="c4552-543">Lineal</span><span class="sxs-lookup"><span data-stu-id="c4552-543">Linear</span></span></li>
<li><span data-ttu-id="c4552-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="c4552-544">Sigma</span></span></li>
<li><span data-ttu-id="c4552-545">Any</span><span class="sxs-lookup"><span data-stu-id="c4552-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="c4552-546">El valor predeterminado es Sigma.</span><span class="sxs-lookup"><span data-stu-id="c4552-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-547">Activado</span><span class="sxs-lookup"><span data-stu-id="c4552-547">On</span></span></td>
<td><span data-ttu-id="c4552-548"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-549">Activa la presentación de relleno.</span><span class="sxs-lookup"><span data-stu-id="c4552-549">Turns fill display on.</span></span> <span data-ttu-id="c4552-550">Igual que el atributo Fill en forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-551">Opacidad</span><span class="sxs-lookup"><span data-stu-id="c4552-551">Opacity</span></span></td>
<td><span data-ttu-id="c4552-552"><a href="msdn-online-vml-vgfraction-data-type.md">Accionario.</a></span><span class="sxs-lookup"><span data-stu-id="c4552-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="c4552-553">Opacidad del relleno.</span><span class="sxs-lookup"><span data-stu-id="c4552-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-554">Opacidad2</span><span class="sxs-lookup"><span data-stu-id="c4552-554">Opacity2</span></span></td>
<td><span data-ttu-id="c4552-555"><a href="msdn-online-vml-vgfraction-data-type.md">Accionario.</a></span><span class="sxs-lookup"><span data-stu-id="c4552-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="c4552-556">Opacidad secundaria de los degradados.</span><span class="sxs-lookup"><span data-stu-id="c4552-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-557">Origen</span><span class="sxs-lookup"><span data-stu-id="c4552-557">Origin</span></span></td>
<td><span data-ttu-id="c4552-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-559">Punto relativo a la esquina superior izquierda de la imagen que se trata como el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="c4552-560">El valor predeterminado es el centro de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-560">Default is the center of the image.</span></span> <span data-ttu-id="c4552-561">El vector es una fracción (de 0,0 a 1,0) del ancho y alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-562">Posición</span><span class="sxs-lookup"><span data-stu-id="c4552-562">Position</span></span></td>
<td><span data-ttu-id="c4552-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-564">Apunte en el rectángulo de referencia de la forma para colocar el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="c4552-565">El valor predeterminado es el centro del rectángulo del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c4552-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="c4552-566">El vector es una fracción (0,0 - 1,0) del ancho y alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-567">Size</span><span class="sxs-lookup"><span data-stu-id="c4552-567">Size</span></span></td>
<td><span data-ttu-id="c4552-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-569">Tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-569">The size of the image.</span></span> <span data-ttu-id="c4552-570">El valor predeterminado es el tamaño de píxel de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-570">Default is pixel size of the image.</span></span> <span data-ttu-id="c4552-571">Se puede especificar en coordenadas absolutas o porcentaje.</span><span class="sxs-lookup"><span data-stu-id="c4552-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-572">Origen</span><span class="sxs-lookup"><span data-stu-id="c4552-572">Src</span></span></td>
<td><span data-ttu-id="c4552-573"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="c4552-574">Dirección URL de una imagen que se cargará para los rellenos de imagen y patrón.</span><span class="sxs-lookup"><span data-stu-id="c4552-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="c4552-575">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-576">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-576">Type</span></span></td>
<td><span data-ttu-id="c4552-577">TipoDeFillFill.</span><span class="sxs-lookup"><span data-stu-id="c4552-577">VgFillType.</span></span> <span data-ttu-id="c4552-578">Puede ser uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="c4552-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="c4552-579">Información previa</span><span class="sxs-lookup"><span data-stu-id="c4552-579">Background</span></span></li>
<li><span data-ttu-id="c4552-580">Fotograma</span><span class="sxs-lookup"><span data-stu-id="c4552-580">Frame</span></span></li>
<li><span data-ttu-id="c4552-581">Degradado</span><span class="sxs-lookup"><span data-stu-id="c4552-581">Gradient</span></span></li>
<li><span data-ttu-id="c4552-582">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="c4552-582">GradientCenter</span></span></li>
<li><span data-ttu-id="c4552-583">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="c4552-583">GradientRadial</span></span></li>
<li><span data-ttu-id="c4552-584">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="c4552-584">GradientTitle</span></span></li>
<li><span data-ttu-id="c4552-585">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="c4552-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="c4552-586">Patrón</span><span class="sxs-lookup"><span data-stu-id="c4552-586">Pattern</span></span></li>
<li><span data-ttu-id="c4552-587">Sólido</span><span class="sxs-lookup"><span data-stu-id="c4552-587">Solid</span></span></li>
<li><span data-ttu-id="c4552-588">Tile</span><span class="sxs-lookup"><span data-stu-id="c4552-588">Tile</span></span></li>
</ul>
<span data-ttu-id="c4552-589">Tile, Pattern y Frame requieren que se proporcionan los atributos de imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="c4552-590">Gradient y GradientRadial requieren que se suministre los atributos de degradado.</span><span class="sxs-lookup"><span data-stu-id="c4552-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="c4552-591">Group, elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-591">Group element</span></span>

<span data-ttu-id="c4552-592">Un grupo es una colección de formas individuales que se pueden colocar y transformar como una unidad.</span><span class="sxs-lookup"><span data-stu-id="c4552-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="c4552-593">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-593">Attribute</span></span>        |   <span data-ttu-id="c4552-594">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-595">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-595">Item</span></span>   | <span data-ttu-id="c4552-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-597">Elemento especificado en la matriz de formas.</span><span class="sxs-lookup"><span data-stu-id="c4552-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="c4552-598">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-598">Length</span></span> | <span data-ttu-id="c4552-599">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-600">Número de formas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="c4552-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="c4552-601">Elemento Imagedata</span><span class="sxs-lookup"><span data-stu-id="c4552-601">Imagedata element</span></span>

<span data-ttu-id="c4552-602">Describe una imagen que se va a representar sobre una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="c4552-603">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-603">Attribute</span></span>        |   <span data-ttu-id="c4552-604">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-605">Binivel</span><span class="sxs-lookup"><span data-stu-id="c4552-605">BiLevel</span></span>     | <span data-ttu-id="c4552-606">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-607">Mostrar la imagen en solo dos colores (normalmente, blanco y negro).</span><span class="sxs-lookup"><span data-stu-id="c4552-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c4552-608">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="c4552-608">BlackLevel</span></span>  | <span data-ttu-id="c4552-609">[DvIon.](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="c4552-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="c4552-610">Permite el ajuste para establecer el nivel de modo que los negros aparezcan como verdaderos negros y todos los demás colores sean visibles como tonalidades por encima del negro.</span><span class="sxs-lookup"><span data-stu-id="c4552-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c4552-611">Chromakey</span><span class="sxs-lookup"><span data-stu-id="c4552-611">Chromakey</span></span>   | <span data-ttu-id="c4552-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="c4552-613">Color transparente de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c4552-614">CropBottom</span><span class="sxs-lookup"><span data-stu-id="c4552-614">CropBottom</span></span>  | <span data-ttu-id="c4552-615">[NumberNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-616">Recortar la distancia desde la parte inferior de la imagen expresada como un porcentaje del tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="c4552-617">CropLeft</span><span class="sxs-lookup"><span data-stu-id="c4552-617">CropLeft</span></span>    | <span data-ttu-id="c4552-618">[NumberNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-619">Recortar distancia desde el borde izquierdo de la imagen expresado como una fracción del tamaño de la imagen (de 0,0 a 1,0).</span><span class="sxs-lookup"><span data-stu-id="c4552-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="c4552-620">Sin embargo, se admite el "recorte fuera de recorte" y, por tanto, se admiten valores menores que 0 y mayores que 1. Por ejemplo, -5, 20 recortaría los límites 25 veces el tamaño de la imagen con 4/5 en un lado de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="c4552-621">CropRight</span><span class="sxs-lookup"><span data-stu-id="c4552-621">CropRight</span></span>   | <span data-ttu-id="c4552-622">[NumberNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-623">Recortar la distancia desde la derecha de la imagen expresada como un porcentaje del tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="c4552-624">CropTop</span><span class="sxs-lookup"><span data-stu-id="c4552-624">CropTop</span></span>     | <span data-ttu-id="c4552-625">[NumberNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-626">Recortar distancia desde la parte superior de la imagen expresada como un porcentaje del tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="c4552-627">RelieveColor</span><span class="sxs-lookup"><span data-stu-id="c4552-627">EmbossColor</span></span> | <span data-ttu-id="c4552-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="c4552-629">Se establece en un porcentaje del color de sombra para crear un efecto de imagen en relieve.</span><span class="sxs-lookup"><span data-stu-id="c4552-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="c4552-630">Ganar</span><span class="sxs-lookup"><span data-stu-id="c4552-630">Gain</span></span>        | <span data-ttu-id="c4552-631">[DvPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-632">Ajusta la intensidad de todos los colores.</span><span class="sxs-lookup"><span data-stu-id="c4552-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="c4552-633">Básicamente establece lo claro que será el blanco.</span><span class="sxs-lookup"><span data-stu-id="c4552-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="c4552-634">Oscila entre 0 y 32767.</span><span class="sxs-lookup"><span data-stu-id="c4552-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="c4552-635">Gamma</span><span class="sxs-lookup"><span data-stu-id="c4552-635">Gamma</span></span>       | <span data-ttu-id="c4552-636">[DvIon.](msdn-online-vml-vgfraction-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="c4552-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="c4552-637">Corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="c4552-637">Gamma correction.</span></span> <span data-ttu-id="c4552-638">Aumentarla proporciona más contraste a una imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="c4552-639">GrayScale</span><span class="sxs-lookup"><span data-stu-id="c4552-639">GrayScale</span></span>   | <span data-ttu-id="c4552-640">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-641">Mostrar imagen en colores de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="c4552-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c4552-642">Origen</span><span class="sxs-lookup"><span data-stu-id="c4552-642">Src</span></span>         | <span data-ttu-id="c4552-643">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-644">Dirección URL de una imagen que se cargará para rellenos de imagen y patrón.</span><span class="sxs-lookup"><span data-stu-id="c4552-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="c4552-645">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="c4552-646">Path, elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-646">Path element</span></span>

<span data-ttu-id="c4552-647">Define la ruta de acceso que forma la forma, utilizando una cadena que contiene un amplio conjunto de comandos de "movimiento de lápiz".</span><span class="sxs-lookup"><span data-stu-id="c4552-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-648">Limusina</span><span class="sxs-lookup"><span data-stu-id="c4552-648">Limo</span></span></td>
<td><span data-ttu-id="c4552-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="c4552-650">Define el punto en el que se extiende la forma; Por ejemplo, para una forma de jirafa, el punto de limusina estaría en el cuello, por lo que cuando se cambie el tamaño de la forma, el cuello se ajustará y el resto de la forma mantendrá sus dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c4552-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-651">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="c4552-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="c4552-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="c4552-653">Matriz que contiene los rectángulos que definen dónde debe ir el texto.</span><span class="sxs-lookup"><span data-stu-id="c4552-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-654">V</span><span class="sxs-lookup"><span data-stu-id="c4552-654">V</span></span></td>
<td><span data-ttu-id="c4552-655"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="c4552-656">Coincide con el atributo v de la etiqueta Path.</span><span class="sxs-lookup"><span data-stu-id="c4552-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="c4552-657">Tenga en cuenta que path puede corresponder al atributo o elemento Path.</span><span class="sxs-lookup"><span data-stu-id="c4552-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-658">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-658">Value</span></span></td>
<td><span data-ttu-id="c4552-659"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="c4552-660">Representación de texto de los comandos que definen la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4552-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="c4552-661">Los valores de coordenadas X o y pueden ser una referencia a una fórmula con el formato # es el número ordinal de la fórmula, por &quot; @# &quot; ejemplo, &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="c4552-662">Esta cadena de atributo se conste de un amplio conjunto de comandos, incluidos los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4552-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-663">Comando</span><span class="sxs-lookup"><span data-stu-id="c4552-663">Command</span></span></th>
<th><span data-ttu-id="c4552-664">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-665">ae (anglepsipseto)</span><span class="sxs-lookup"><span data-stu-id="c4552-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="c4552-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span><span class="sxs-lookup"><span data-stu-id="c4552-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="c4552-667">Dibuje un segmento de una elipse.</span><span class="sxs-lookup"><span data-stu-id="c4552-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="c4552-668">Se dibuja una línea recta desde el punto actual hasta el punto inicial del segmento.</span><span class="sxs-lookup"><span data-stu-id="c4552-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-669">al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="c4552-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="c4552-670">Igual que ae, salvo que hay un valor m implícito en el punto inicial del segmento.</span><span class="sxs-lookup"><span data-stu-id="c4552-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-671">ar (arc)</span><span class="sxs-lookup"><span data-stu-id="c4552-671">ar (arc)</span></span></td>
<td><span data-ttu-id="c4552-672">Igual que at.</span><span class="sxs-lookup"><span data-stu-id="c4552-672">Same as at.</span></span> <span data-ttu-id="c4552-673">Sin embargo, una nueva sub ruta de acceso se inicia mediante un m implícito hasta el punto inicial del arco.</span><span class="sxs-lookup"><span data-stu-id="c4552-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-674">at (arcto)</span><span class="sxs-lookup"><span data-stu-id="c4552-674">at (arcto)</span></span></td>
<td><span data-ttu-id="c4552-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom,</strong> <strong>start</strong>(x,y) end (x,y) <strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="c4552-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="c4552-676">Los cuatro primeros valores definen el rectángulo delimitador de una elipse.</span><span class="sxs-lookup"><span data-stu-id="c4552-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="c4552-677">Los cuatro últimos definen dos vectores radiales.</span><span class="sxs-lookup"><span data-stu-id="c4552-677">The last four define two radial vectors.</span></span> <span data-ttu-id="c4552-678">Se dibuja un segmento de la elipse que comienza en el ángulo definido por el vector de radio inicial y termina en el ángulo definido por el vector final.</span><span class="sxs-lookup"><span data-stu-id="c4552-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="c4552-679">Se dibuja una línea recta desde el punto actual hasta el inicio del arco. El arco siempre se dibuja en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="c4552-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-680">c (curveto)</span><span class="sxs-lookup"><span data-stu-id="c4552-680">c (curveto)</span></span></td>
<td><span data-ttu-id="c4552-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>a</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="c4552-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="c4552-682">Dibuje una curva bézier cúbica desde el punto actual hasta la coordenada dada por los dos parámetros finales, los puntos de control que dan los cuatro primeros parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4552-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="c4552-683">El punto actual se convierte en el punto de conexión del bézier.</span><span class="sxs-lookup"><span data-stu-id="c4552-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-684">e (final)</span><span class="sxs-lookup"><span data-stu-id="c4552-684">e (end)</span></span></td>
<td><span data-ttu-id="c4552-685">Finalice el conjunto actual de subpaths.</span><span class="sxs-lookup"><span data-stu-id="c4552-685">End the current set of subpaths.</span></span> <span data-ttu-id="c4552-686">Un conjunto determinado de subpaths (delimitado por el final) se rellena mediante eofill.</span><span class="sxs-lookup"><span data-stu-id="c4552-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="c4552-687">Los conjuntos posteriores de subpaths se rellenan de forma independiente y se superponen en los existentes.</span><span class="sxs-lookup"><span data-stu-id="c4552-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-688">l (lineto)</span><span class="sxs-lookup"><span data-stu-id="c4552-688">l (lineto)</span></span></td>
<td><span data-ttu-id="c4552-689">x,y</span><span class="sxs-lookup"><span data-stu-id="c4552-689">x,y</span></span><br/> <span data-ttu-id="c4552-690">Dibuje una línea desde el punto actual hasta la coordenada x,y dada, que se convierte en el nuevo punto actual.</span><span class="sxs-lookup"><span data-stu-id="c4552-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="c4552-691">Se pueden especificar pares de coordenadas adicionales para formar una polilínea, por ejemplo, &quot; l 10,13,45,27,89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-692">m (moveto)</span><span class="sxs-lookup"><span data-stu-id="c4552-692">m (moveto)</span></span></td>
<td><span data-ttu-id="c4552-693">x,y</span><span class="sxs-lookup"><span data-stu-id="c4552-693">x,y</span></span><br/> <span data-ttu-id="c4552-694">Inicie una nueva subpath en la coordenada x,y dada.</span><span class="sxs-lookup"><span data-stu-id="c4552-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-695">nf (nofill)</span><span class="sxs-lookup"><span data-stu-id="c4552-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="c4552-696">El conjunto actual de subpaths (delimitado por el final) no se rellenará.</span><span class="sxs-lookup"><span data-stu-id="c4552-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-697">ns (nostroke)</span><span class="sxs-lookup"><span data-stu-id="c4552-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="c4552-698">El conjunto actual de subpaths (delimitado por el final) no se acariciará.</span><span class="sxs-lookup"><span data-stu-id="c4552-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-699">qb (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="c4552-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="c4552-700">(<strong>punto de</strong>control (x, y))\*,<strong>end</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="c4552-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="c4552-701">Define una o varias curvas bézier cuadráticas mediante puntos de control y un punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="c4552-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="c4552-702">Los puntos intermedios (en curva) se obtienen mediante la interpolación entre puntos de control sucesivos similares a las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="c4552-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="c4552-703">La subpath no necesita ser un inicio, en cuyo caso se cierra la subpath y el último punto define el punto inicial.</span><span class="sxs-lookup"><span data-stu-id="c4552-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-704">qx (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="c4552-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="c4552-705"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="c4552-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="c4552-706">Se dibuja un botón de puntos suspensivos desde el punto actual hasta el punto de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="c4552-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="c4552-707">El segmento elíptico es inicialmente tangencial a una línea paralela al eje X; Es decir, el segmento se inicia horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c4552-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-708">qy (elipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="c4552-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="c4552-709"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="c4552-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="c4552-710">Igual que qx, salvo que el segmento elíptico es inicialmente tangencial a una línea paralela al eje Y; Es decir, el segmento se inicia verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c4552-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-711">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="c4552-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="c4552-712">x,y</span><span class="sxs-lookup"><span data-stu-id="c4552-712">x,y</span></span> <br/> <span data-ttu-id="c4552-713">Dibuje una línea desde el punto actual hasta la coordenada relativa (cpx + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="c4552-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="c4552-714">Si se dan pares de coordenadas adicionales, cada nuevo punto se calcula con respecto al último.</span><span class="sxs-lookup"><span data-stu-id="c4552-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-715">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="c4552-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="c4552-716">x,y</span><span class="sxs-lookup"><span data-stu-id="c4552-716">x,y</span></span><br/> <span data-ttu-id="c4552-717">Inicie una nueva subpath en las coordenadas relativas (cpx + x, cpy + y) donde cpx, cpy es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="c4552-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-718">v (curveto)</span><span class="sxs-lookup"><span data-stu-id="c4552-718">v (curveto)</span></span></td>
<td><span data-ttu-id="c4552-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>a</strong> (x,y)</span><span class="sxs-lookup"><span data-stu-id="c4552-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="c4552-720">Curva bézier cúbica con las coordenadas dadas en relación con el punto actual.</span><span class="sxs-lookup"><span data-stu-id="c4552-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="c4552-721">Todos los puntos se calculan con respecto al mismo punto inicial.</span><span class="sxs-lookup"><span data-stu-id="c4552-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-722">wa (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="c4552-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="c4552-723">Igual que en , pero el arco se dibuja en dirección en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="c4552-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-724">wr (en el sentido de las agujas del reloj)</span><span class="sxs-lookup"><span data-stu-id="c4552-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="c4552-725">Igual que ar, pero se dibuja en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="c4552-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-726">x (cerrar)</span><span class="sxs-lookup"><span data-stu-id="c4552-726">x (close)</span></span></td>
<td><span data-ttu-id="c4552-727">Cierre el subpath actual dibujando una línea recta desde el punto actual hasta el punto de traslado original.</span><span class="sxs-lookup"><span data-stu-id="c4552-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="c4552-728">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="c4552-728">Shadow element</span></span>

<span data-ttu-id="c4552-729">Describe un efecto de sombra en una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-730">Color</span><span class="sxs-lookup"><span data-stu-id="c4552-730">Color</span></span></td>
<td><span data-ttu-id="c4552-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="c4552-732">Color de la sombra principal.</span><span class="sxs-lookup"><span data-stu-id="c4552-732">Color of the primary shadow.</span></span> <span data-ttu-id="c4552-733">El valor predeterminado es RGB(128,128,128)</span><span class="sxs-lookup"><span data-stu-id="c4552-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-734">Color2</span><span class="sxs-lookup"><span data-stu-id="c4552-734">Color2</span></span></td>
<td><span data-ttu-id="c4552-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="c4552-736">Color de la segunda sombra, o resalte en una sombra con relieve o con relieve.</span><span class="sxs-lookup"><span data-stu-id="c4552-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="c4552-737">El valor predeterminado es RGB(203,203,203).</span><span class="sxs-lookup"><span data-stu-id="c4552-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-738">Matriz</span><span class="sxs-lookup"><span data-stu-id="c4552-738">Matrix</span></span></td>
<td><span data-ttu-id="c4552-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="c4552-740">Matriz de transformación de perspectiva con el formato &quot; sxx,sxy,syx,syy,px,py &quot; [s=scale, p=perspective].</span><span class="sxs-lookup"><span data-stu-id="c4552-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="c4552-741">Los elementos s especifican cómo se debe escalar la sombra con respecto a la forma y los elementos p especifican cómo se debe sesgar la sombra con respecto a la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="c4552-742">Por ejemplo, la siguiente matriz cambia el tamaño de la forma por un factor de 2 y la sesga por un factor de 4 en todas las direcciones:</span><span class="sxs-lookup"><span data-stu-id="c4552-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="c4552-743">&quot;2,2,2,2,4,4&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="c4552-744">Esta matriz solo se usa si el tipo de la sombra se establece en perspective.</span><span class="sxs-lookup"><span data-stu-id="c4552-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-745">Oscurecido</span><span class="sxs-lookup"><span data-stu-id="c4552-745">Obscured</span></span></td>
<td><span data-ttu-id="c4552-746"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-747">La sombra se puede ver si no hay ningún relleno en la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="c4552-748">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="c4552-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-749">Offset</span><span class="sxs-lookup"><span data-stu-id="c4552-749">Offset</span></span></td>
<td><span data-ttu-id="c4552-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="c4552-751">Cantidad de desplazamiento x,y desde la ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="c4552-752">El valor &quot; predeterminado es 2pt,2pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="c4552-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="c4552-753">Offset2</span></span></td>
<td><span data-ttu-id="c4552-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-755">Cantidad de desplazamiento x,y segundo desde la ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="c4552-756">Los valores son una medida absoluta o un valor fraccional de forma (de -0,5 a +0,5).</span><span class="sxs-lookup"><span data-stu-id="c4552-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-757">Activado</span><span class="sxs-lookup"><span data-stu-id="c4552-757">On</span></span></td>
<td><span data-ttu-id="c4552-758"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-759">Activa y desactiva la presentación de la sombra.</span><span class="sxs-lookup"><span data-stu-id="c4552-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-760">Opacidad</span><span class="sxs-lookup"><span data-stu-id="c4552-760">Opacity</span></span></td>
<td><span data-ttu-id="c4552-761"><a href="msdn-online-vml-vgfraction-data-type.md">Accionario</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="c4552-762">Opacidad del efecto de sombra.</span><span class="sxs-lookup"><span data-stu-id="c4552-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-763">Origen</span><span class="sxs-lookup"><span data-stu-id="c4552-763">Origin</span></span></td>
<td><span data-ttu-id="c4552-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Par de valores fraccionales de forma de -0,5 a +0,5.</span><span class="sxs-lookup"><span data-stu-id="c4552-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-765">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-765">Type</span></span></td>
<td><span data-ttu-id="c4552-766"><a href="#data-types-used-in-the-vml-object-model">DvshadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="c4552-767">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-768">Single (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-768">Single (default)</span></span></li>
<li><span data-ttu-id="c4552-769">Double</span><span class="sxs-lookup"><span data-stu-id="c4552-769">Double</span></span></li>
<li><span data-ttu-id="c4552-770">Perspectiva</span><span class="sxs-lookup"><span data-stu-id="c4552-770">Perspective</span></span></li>
<li><span data-ttu-id="c4552-771">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="c4552-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="c4552-772">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="c4552-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="c4552-773">Emboss</span><span class="sxs-lookup"><span data-stu-id="c4552-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="c4552-774">Elemento Skew</span><span class="sxs-lookup"><span data-stu-id="c4552-774">Skew element</span></span>

<span data-ttu-id="c4552-775">Describe un efecto de sesgo de perspectiva en una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="c4552-776">El sesgo se aplica a los datos gráficos vectoriales, no a los datos de imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="c4552-777">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-777">Attribute</span></span>        |   <span data-ttu-id="c4552-778">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-779">Matriz</span><span class="sxs-lookup"><span data-stu-id="c4552-779">Matrix</span></span> | <span data-ttu-id="c4552-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-781">Matriz de transformación de perspectiva con el formato "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective \] .</span><span class="sxs-lookup"><span data-stu-id="c4552-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="c4552-782">Si offset está en unidades absolutas, px,py están en emu ^ -1 unidades; de lo contrario, son una fracción inversa del tamaño de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="c4552-783">Offset</span><span class="sxs-lookup"><span data-stu-id="c4552-783">Offset</span></span> | <span data-ttu-id="c4552-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-785">Cantidad de desplazamiento x,y desde la ubicación de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="c4552-786">El valor predeterminado es "2pt,2pt".</span><span class="sxs-lookup"><span data-stu-id="c4552-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="c4552-787">Activado</span><span class="sxs-lookup"><span data-stu-id="c4552-787">On</span></span>     | <span data-ttu-id="c4552-788">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-789">Activa o desactiva la presentación del sesgo.</span><span class="sxs-lookup"><span data-stu-id="c4552-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="c4552-790">Origen</span><span class="sxs-lookup"><span data-stu-id="c4552-790">Origin</span></span> | <span data-ttu-id="c4552-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-792">Par de valores fraccionales de forma de -0,5 a +0,5.</span><span class="sxs-lookup"><span data-stu-id="c4552-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="c4552-793">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="c4552-793">Stroke element</span></span>

<span data-ttu-id="c4552-794">Describe cómo dibujar el trazado si se desea algo más allá de una línea sólida con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="c4552-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-795">Color</span><span class="sxs-lookup"><span data-stu-id="c4552-795">Color</span></span></td>
<td><span data-ttu-id="c4552-796"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-797">Color de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-797">The color of the line.</span></span> <span data-ttu-id="c4552-798">Igual que el atributo StrokeColor en Shape, pero lo invalida.</span><span class="sxs-lookup"><span data-stu-id="c4552-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-799">Color2</span><span class="sxs-lookup"><span data-stu-id="c4552-799">Color2</span></span></td>
<td><span data-ttu-id="c4552-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="c4552-801">Color secundario.</span><span class="sxs-lookup"><span data-stu-id="c4552-801">Secondary color.</span></span> <span data-ttu-id="c4552-802">Se usa cuando FillType es Pattern.</span><span class="sxs-lookup"><span data-stu-id="c4552-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-803">DashStyle</span><span class="sxs-lookup"><span data-stu-id="c4552-803">DashStyle</span></span></td>
<td><span data-ttu-id="c4552-804"><strong>BvLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="c4552-805">Formato de estilo de guión.</span><span class="sxs-lookup"><span data-stu-id="c4552-805">Dash style format.</span></span> <span data-ttu-id="c4552-806">Puede ser un valor específico o una secuencia de números con un patrón de guion definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c4552-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="c4552-807">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-808">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-808">Solid (default)</span></span></li>
<li><span data-ttu-id="c4552-809">ShortDash</span><span class="sxs-lookup"><span data-stu-id="c4552-809">ShortDash</span></span></li>
<li><span data-ttu-id="c4552-810">ShortDot</span><span class="sxs-lookup"><span data-stu-id="c4552-810">ShortDot</span></span></li>
<li><span data-ttu-id="c4552-811">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="c4552-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="c4552-812">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="c4552-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="c4552-813">Punto</span><span class="sxs-lookup"><span data-stu-id="c4552-813">Dot</span></span></li>
<li><span data-ttu-id="c4552-814">Guión</span><span class="sxs-lookup"><span data-stu-id="c4552-814">Dash</span></span></li>
<li><span data-ttu-id="c4552-815">DashDot</span><span class="sxs-lookup"><span data-stu-id="c4552-815">DashDot</span></span></li>
<li><span data-ttu-id="c4552-816">LongDash</span><span class="sxs-lookup"><span data-stu-id="c4552-816">LongDash</span></span></li>
<li><span data-ttu-id="c4552-817">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="c4552-817">LongDashDot</span></span></li>
<li><span data-ttu-id="c4552-818">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="c4552-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-819">EndArrow</span><span class="sxs-lookup"><span data-stu-id="c4552-819">EndArrow</span></span></td>
<td><span data-ttu-id="c4552-820"><strong>DomainArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="c4552-821">Punta de flecha para el final de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="c4552-822">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-823">Ninguna (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-823">None (default)</span></span></li>
<li><span data-ttu-id="c4552-824">Bloquear</span><span class="sxs-lookup"><span data-stu-id="c4552-824">Block</span></span></li>
<li><span data-ttu-id="c4552-825">Clásico</span><span class="sxs-lookup"><span data-stu-id="c4552-825">Classic</span></span></li>
<li><span data-ttu-id="c4552-826">Diamond</span><span class="sxs-lookup"><span data-stu-id="c4552-826">Diamond</span></span></li>
<li><span data-ttu-id="c4552-827">Elipse</span><span class="sxs-lookup"><span data-stu-id="c4552-827">Oval</span></span></li>
<li><span data-ttu-id="c4552-828">Abrir</span><span class="sxs-lookup"><span data-stu-id="c4552-828">Open</span></span></li>
<li><span data-ttu-id="c4552-829">Comillas angulares</span><span class="sxs-lookup"><span data-stu-id="c4552-829">Chevron</span></span></li>
<li><span data-ttu-id="c4552-830">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="c4552-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-831">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="c4552-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="c4552-832"><strong>DvArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="c4552-833">Longitud de la punta de flecha para el final de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="c4552-834">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-835">Short</span><span class="sxs-lookup"><span data-stu-id="c4552-835">Short</span></span></li>
<li><span data-ttu-id="c4552-836">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-836">Medium (default)</span></span></li>
<li><span data-ttu-id="c4552-837">long</span><span class="sxs-lookup"><span data-stu-id="c4552-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-838">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="c4552-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="c4552-839"><strong>DvArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="c4552-840">Ancho de flecha para el final de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="c4552-841">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-842">Estrecho</span><span class="sxs-lookup"><span data-stu-id="c4552-842">Narrow</span></span></li>
<li><span data-ttu-id="c4552-843">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-843">Medium (default)</span></span></li>
<li><span data-ttu-id="c4552-844">Ancho</span><span class="sxs-lookup"><span data-stu-id="c4552-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-845">Endcap</span><span class="sxs-lookup"><span data-stu-id="c4552-845">EndCap</span></span></td>
<td><span data-ttu-id="c4552-846"><strong>DvLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="c4552-847">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-848">Plano</span><span class="sxs-lookup"><span data-stu-id="c4552-848">Flat</span></span></li>
<li><span data-ttu-id="c4552-849">Square</span><span class="sxs-lookup"><span data-stu-id="c4552-849">Square</span></span></li>
<li><span data-ttu-id="c4552-850">Round</span><span class="sxs-lookup"><span data-stu-id="c4552-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-851">FillType</span><span class="sxs-lookup"><span data-stu-id="c4552-851">FillType</span></span></td>
<td><span data-ttu-id="c4552-852"><strong>DvLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="c4552-853">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-854">Solid (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-854">Solid (default)</span></span></li>
<li><span data-ttu-id="c4552-855">Tile</span><span class="sxs-lookup"><span data-stu-id="c4552-855">Tile</span></span></li>
<li><span data-ttu-id="c4552-856">Patrón</span><span class="sxs-lookup"><span data-stu-id="c4552-856">Pattern</span></span></li>
<li><span data-ttu-id="c4552-857">Fotograma</span><span class="sxs-lookup"><span data-stu-id="c4552-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-858">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="c4552-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="c4552-859"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-860">Alinee la imagen con la forma .</span><span class="sxs-lookup"><span data-stu-id="c4552-860">Align the image with the shape.</span></span> <span data-ttu-id="c4552-861">Si es False, alinee la imagen con la ventana.</span><span class="sxs-lookup"><span data-stu-id="c4552-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-862">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="c4552-862">ImageAspect</span></span></td>
<td><span data-ttu-id="c4552-863"><strong>DvAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="c4552-864">El atributo ImageSize se ajustará para conservar el aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="c4552-865">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="c4552-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-866">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-866">Value</span></span></th>
<th><span data-ttu-id="c4552-867">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-868">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c4552-868">Ignore</span></span></td>
<td><span data-ttu-id="c4552-869">Omitir problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="c4552-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-870">Atleast</span><span class="sxs-lookup"><span data-stu-id="c4552-870">AtLeast</span></span></td>
<td><span data-ttu-id="c4552-871">La imagen es al menos tan grande como el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-872">Atmost</span><span class="sxs-lookup"><span data-stu-id="c4552-872">AtMost</span></span></td>
<td><span data-ttu-id="c4552-873">La imagen no es mayor que el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-874">ImageSize</span><span class="sxs-lookup"><span data-stu-id="c4552-874">ImageSize</span></span></td>
<td><span data-ttu-id="c4552-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="c4552-876">Tamaño de la imagen con la que se formará el pincel.</span><span class="sxs-lookup"><span data-stu-id="c4552-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="c4552-877">El valor predeterminado es el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-878">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="c4552-878">JoinStyle</span></span></td>
<td><span data-ttu-id="c4552-879"><strong>BvLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="c4552-880">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-881">Redondeada (unión redondeada)</span><span class="sxs-lookup"><span data-stu-id="c4552-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="c4552-882">Bisel (unión biselada)</span><span class="sxs-lookup"><span data-stu-id="c4552-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="c4552-883">Miter (miter joint)</span><span class="sxs-lookup"><span data-stu-id="c4552-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-884">Estilo de línea</span><span class="sxs-lookup"><span data-stu-id="c4552-884">LineStyle</span></span></td>
<td><span data-ttu-id="c4552-885"><strong>StyleLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="c4552-886">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-887">Single</span><span class="sxs-lookup"><span data-stu-id="c4552-887">Single</span></span></li>
<li><span data-ttu-id="c4552-888">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="c4552-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="c4552-889">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="c4552-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="c4552-890">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="c4552-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="c4552-891">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="c4552-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-892">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="c4552-892">MiterLimit</span></span></td>
<td><span data-ttu-id="c4552-893"><a href="msdn-online-vml-vglength.md">Longitud</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="c4552-894">Distancia máxima entre el punto interno y el punto exterior de una unión.</span><span class="sxs-lookup"><span data-stu-id="c4552-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="c4552-895">Este número es un múltiplo del grosor de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="c4552-896">Oscila entre 0 y 32 767.</span><span class="sxs-lookup"><span data-stu-id="c4552-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-897">Activado</span><span class="sxs-lookup"><span data-stu-id="c4552-897">On</span></span></td>
<td><span data-ttu-id="c4552-898"><a href="msdn-online-vml-vgtristate.md">DvTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="c4552-899">Activa y desactiva la presentación de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="c4552-900">Igual que el atributo Stroke en Shape, pero lo invalida.</span><span class="sxs-lookup"><span data-stu-id="c4552-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-901">Opacidad</span><span class="sxs-lookup"><span data-stu-id="c4552-901">Opacity</span></span></td>
<td><span data-ttu-id="c4552-902"><a href="msdn-online-vml-vgfraction-data-type.md">Accionario</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="c4552-903">Opacidad del trazo.</span><span class="sxs-lookup"><span data-stu-id="c4552-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-904">Origen</span><span class="sxs-lookup"><span data-stu-id="c4552-904">Src</span></span></td>
<td><span data-ttu-id="c4552-905">String.</span><span class="sxs-lookup"><span data-stu-id="c4552-905">String.</span></span> <span data-ttu-id="c4552-906">Dirección URL a una imagen que se cargará para los rellenos de imagen y patrón.</span><span class="sxs-lookup"><span data-stu-id="c4552-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="c4552-907">Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</span><span class="sxs-lookup"><span data-stu-id="c4552-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-908">StartArrow</span><span class="sxs-lookup"><span data-stu-id="c4552-908">StartArrow</span></span></td>
<td><span data-ttu-id="c4552-909"><strong>DvArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="c4552-910">Punta de flecha para el inicio de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="c4552-911">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-912">Ninguna (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-912">None (default)</span></span></li>
<li><span data-ttu-id="c4552-913">Bloquear</span><span class="sxs-lookup"><span data-stu-id="c4552-913">Block</span></span></li>
<li><span data-ttu-id="c4552-914">Clásico</span><span class="sxs-lookup"><span data-stu-id="c4552-914">Classic</span></span></li>
<li><span data-ttu-id="c4552-915">Diamond</span><span class="sxs-lookup"><span data-stu-id="c4552-915">Diamond</span></span></li>
<li><span data-ttu-id="c4552-916">Elipse</span><span class="sxs-lookup"><span data-stu-id="c4552-916">Oval</span></span></li>
<li><span data-ttu-id="c4552-917">Abrir</span><span class="sxs-lookup"><span data-stu-id="c4552-917">Open</span></span></li>
<li><span data-ttu-id="c4552-918">Comillas angulares</span><span class="sxs-lookup"><span data-stu-id="c4552-918">Chevron</span></span></li>
<li><span data-ttu-id="c4552-919">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="c4552-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-920">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="c4552-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="c4552-921">BvArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="c4552-921">VgArrowHeadLength.</span></span> <span data-ttu-id="c4552-922">Longitud de la punta de flecha para el inicio de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="c4552-923">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-924">Short</span><span class="sxs-lookup"><span data-stu-id="c4552-924">Short</span></span></li>
<li><span data-ttu-id="c4552-925">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-925">Medium (default)</span></span></li>
<li><span data-ttu-id="c4552-926">long</span><span class="sxs-lookup"><span data-stu-id="c4552-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-927">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="c4552-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="c4552-928">BvArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="c4552-928">VgArrowheadWidth.</span></span> <span data-ttu-id="c4552-929">Ancho de punta de flecha para el inicio de la línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="c4552-930">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-931">Ancho medio estrecho (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="c4552-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-932">Peso</span><span class="sxs-lookup"><span data-stu-id="c4552-932">Weight</span></span></td>
<td><span data-ttu-id="c4552-933"><a href="msdn-online-vml-vglength.md">DvLength</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="c4552-934">Ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-934">Width of line.</span></span> <span data-ttu-id="c4552-935">Oscila entre 0 y 1584.</span><span class="sxs-lookup"><span data-stu-id="c4552-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="c4552-936">El atributo DashStyle permite al usuario especificar un patrón de guiones definido de forma personalizada.</span><span class="sxs-lookup"><span data-stu-id="c4552-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="c4552-937">Esto se hace mediante una serie de números.</span><span class="sxs-lookup"><span data-stu-id="c4552-937">This is done using a series of numbers.</span></span> <span data-ttu-id="c4552-938">Los estilos de guion se definen en términos de la longitud del guion (la parte dibujada del trazo) y la longitud del espacio entre los guiones.</span><span class="sxs-lookup"><span data-stu-id="c4552-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="c4552-939">Las longitudes son relativas al ancho de línea; una longitud de &quot; 1 &quot; es igual al ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="c4552-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="c4552-940">El estilo EndCap se aplica a cada guión, los estilos de flecha no lo son.</span><span class="sxs-lookup"><span data-stu-id="c4552-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="c4552-941">La cadena define primero la longitud del guion y, a continuación, la longitud del espacio.</span><span class="sxs-lookup"><span data-stu-id="c4552-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="c4552-942">Esto se puede repetir para formar estilos de guion complejos.</span><span class="sxs-lookup"><span data-stu-id="c4552-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="c4552-943">La cadena siempre debe contener un par de números; si contiene un número impar de números, se puede pasar por alto el último.</span><span class="sxs-lookup"><span data-stu-id="c4552-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="c4552-944">En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="c4552-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="c4552-945">&quot;0 implica un punto que debe ser cuatro veces simétrico (con las puntas de &quot; finalización redondeados debe ser un círculo).</span><span class="sxs-lookup"><span data-stu-id="c4552-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="c4552-946">Si el final de línea es Plano, un visor debe elegir un guión del sistema operativo integrado siempre que sea posible (es decir, algo que sea rápido de dibujar).</span><span class="sxs-lookup"><span data-stu-id="c4552-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="c4552-947">A continuación se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c4552-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-949">guiones cortos (cada guión y el espacio entre ellos tiene el doble de ancho que la línea)</span><span class="sxs-lookup"><span data-stu-id="c4552-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-951">punto (cada guión es el ancho de la línea, mientras que cada espacio es el doble del ancho de la línea)</span><span class="sxs-lookup"><span data-stu-id="c4552-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-953">dash (cada guión es cuatro veces el ancho de la línea, mientras que cada espacio es el doble del ancho de la línea)</span><span class="sxs-lookup"><span data-stu-id="c4552-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-955">long-dash</span><span class="sxs-lookup"><span data-stu-id="c4552-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-957">punto de guion</span><span class="sxs-lookup"><span data-stu-id="c4552-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-959">punto de guion largo</span><span class="sxs-lookup"><span data-stu-id="c4552-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="c4552-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="c4552-961">punto de guion largo</span><span class="sxs-lookup"><span data-stu-id="c4552-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="c4552-962">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="c4552-962">TextPath element</span></span>

<span data-ttu-id="c4552-963">Describe una ruta de acceso vectorial basada en los datos de texto, la fuente y los estilos proporcionados.</span><span class="sxs-lookup"><span data-stu-id="c4552-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="c4552-964">La ruta de acceso de texto se deforma para ajustarse a un **elemento Path** si se proporciona.</span><span class="sxs-lookup"><span data-stu-id="c4552-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="c4552-965">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-965">Attribute</span></span>        |   <span data-ttu-id="c4552-966">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-967">FitPath</span><span class="sxs-lookup"><span data-stu-id="c4552-967">FitPath</span></span>  | <span data-ttu-id="c4552-968">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-969">Tamaños del texto en el que se va a rellenar la ruta de acceso en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="c4552-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="c4552-970">FitShape</span><span class="sxs-lookup"><span data-stu-id="c4552-970">FitShape</span></span> | <span data-ttu-id="c4552-971">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-972">Extiende la ruta de texto hasta los bordes del cuadro de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="c4552-973">Activado</span><span class="sxs-lookup"><span data-stu-id="c4552-973">On</span></span>       | <span data-ttu-id="c4552-974">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-975">Determina si se muestran o no las rutas de acceso de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c4552-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="c4552-976">String</span><span class="sxs-lookup"><span data-stu-id="c4552-976">String</span></span>   | <span data-ttu-id="c4552-977">String.</span><span class="sxs-lookup"><span data-stu-id="c4552-977">String.</span></span> <span data-ttu-id="c4552-978">Texto que se representará como una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="c4552-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="c4552-979">Trim</span><span class="sxs-lookup"><span data-stu-id="c4552-979">Trim</span></span>     | <span data-ttu-id="c4552-980">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-981">Quita cualquier espacio adicional reservado para ascendentes y descendientes si no se usa.</span><span class="sxs-lookup"><span data-stu-id="c4552-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="c4552-982">Xscale</span><span class="sxs-lookup"><span data-stu-id="c4552-982">XScale</span></span>   | <span data-ttu-id="c4552-983">[DvTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-984">Use la medida x recta en lugar de medir a lo largo de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4552-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="c4552-985">Tipos de datos usados en el modelo de objetos VML</span><span class="sxs-lookup"><span data-stu-id="c4552-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="c4552-986">El modelo de objetos VML usa los siguientes tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="c4552-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="c4552-987">Double</span><span class="sxs-lookup"><span data-stu-id="c4552-987">Double</span></span>](/windows)
-   [<span data-ttu-id="c4552-988">Fijo</span><span class="sxs-lookup"><span data-stu-id="c4552-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="c4552-989">Entero</span><span class="sxs-lookup"><span data-stu-id="c4552-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="c4552-990">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="c4552-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="c4552-991">IVgColor</span><span class="sxs-lookup"><span data-stu-id="c4552-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="c4552-992">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="c4552-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="c4552-993">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="c4552-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="c4552-994">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="c4552-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="c4552-995">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="c4552-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="c4552-996">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="c4552-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="c4552-997">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="c4552-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="c4552-998">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="c4552-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="c4552-999">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="c4552-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="c4552-1000">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="c4552-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="c4552-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="c4552-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="c4552-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="c4552-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="c4552-1003">Duración</span><span class="sxs-lookup"><span data-stu-id="c4552-1003">Length</span></span>](/windows)
-   <span data-ttu-id="c4552-1004">[Measure](/windows) (Medida)</span><span class="sxs-lookup"><span data-stu-id="c4552-1004">[Measure](/windows)</span></span>
-   [<span data-ttu-id="c4552-1005">String</span><span class="sxs-lookup"><span data-stu-id="c4552-1005">String</span></span>](/windows)
-   [<span data-ttu-id="c4552-1006">DvBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="c4552-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="c4552-1007">Accionario</span><span class="sxs-lookup"><span data-stu-id="c4552-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="c4552-1008">DvTriState</span><span class="sxs-lookup"><span data-stu-id="c4552-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="c4552-1009">**Tipo de datos double**</span><span class="sxs-lookup"><span data-stu-id="c4552-1009">**Double data type**</span></span>

<span data-ttu-id="c4552-1010">Entero de precisión doble con intervalo de -infinity a infinito.</span><span class="sxs-lookup"><span data-stu-id="c4552-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="c4552-1011">**Tipo de datos fijo**</span><span class="sxs-lookup"><span data-stu-id="c4552-1011">**Fixed data type**</span></span>

<span data-ttu-id="c4552-1012">Número de punto flotante con un intervalo de -32.766.0 a 32.766,0.</span><span class="sxs-lookup"><span data-stu-id="c4552-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="c4552-1013">**Tipo de datos entero**</span><span class="sxs-lookup"><span data-stu-id="c4552-1013">**Integer data type**</span></span>

<span data-ttu-id="c4552-1014">Entero con un intervalo de -infinity a infinity.</span><span class="sxs-lookup"><span data-stu-id="c4552-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="c4552-1015">**Tipo de datos IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="c4552-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="c4552-1016">Colección de ajustes en una forma que se puede usar para cambiar las dimensiones de una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="c4552-1017">Los ajustes se pueden usar como marcadores de posición temporales o por cualquier motivo usaría variables.</span><span class="sxs-lookup"><span data-stu-id="c4552-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="c4552-1018">Solo hay 8 ajustes en la colección.</span><span class="sxs-lookup"><span data-stu-id="c4552-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="c4552-1019">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1019">Attribute</span></span> | <span data-ttu-id="c4552-1020">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="c4552-1021">Exists</span></span>     | <span data-ttu-id="c4552-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="c4552-1023">Determina si existe un ajuste especificado.</span><span class="sxs-lookup"><span data-stu-id="c4552-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="c4552-1024">Tenga en cuenta que se debe usar un índice; es decir, exists( item ) debe usarse para recuperar la existencia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c4552-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="c4552-1025">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-1025">Item</span></span>       | <span data-ttu-id="c4552-1026">[Largo.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="c4552-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1027">Matriz de ajustes indizados de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="c4552-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="c4552-1028">Tenga en cuenta que los ajustes se pueden especificar de forma sparcely; Es decir, es posible que los valores intermedios de la matriz no siempre se llenen.</span><span class="sxs-lookup"><span data-stu-id="c4552-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="c4552-1029">Por ejemplo, los elementos 1, 3 y 5 podrían tener valores para una longitud de 3, con item(0), item(2) y item(4) especificados.</span><span class="sxs-lookup"><span data-stu-id="c4552-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="c4552-1030">Para ver si existe un elemento, use el atributo Exists.</span><span class="sxs-lookup"><span data-stu-id="c4552-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="c4552-1031">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1031">Length</span></span>     | <span data-ttu-id="c4552-1032">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1033">Número de ajustes.</span><span class="sxs-lookup"><span data-stu-id="c4552-1033">Number of adjustments.</span></span> <span data-ttu-id="c4552-1034">No puede ser mayor que 8.</span><span class="sxs-lookup"><span data-stu-id="c4552-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c4552-1035">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1035">Value</span></span>      | <span data-ttu-id="c4552-1036">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1037">Representación de texto de valores numéricos, con comas entre cada número.</span><span class="sxs-lookup"><span data-stu-id="c4552-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="c4552-1038">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="c4552-1038">**IVgColor**</span></span>

<span data-ttu-id="c4552-1039">Especifica un color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-1040">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4552-1040">Attributes</span></span></th>
<th><span data-ttu-id="c4552-1041">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="c4552-1042">RGB</span></span></td>
<td><span data-ttu-id="c4552-1043"><strong>DverGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="c4552-1044">Valor RGB (Long) del color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="c4552-1045">Solo es válido si Type es RGB.</span><span class="sxs-lookup"><span data-stu-id="c4552-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1046">R</span><span class="sxs-lookup"><span data-stu-id="c4552-1046">R</span></span></td>
<td><span data-ttu-id="c4552-1047"><a href="#data-types-used-in-the-vml-object-model">Entero</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="c4552-1048">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1048">Red component of the color.</span></span> <span data-ttu-id="c4552-1049">Puede oscilar entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="c4552-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1050">G</span><span class="sxs-lookup"><span data-stu-id="c4552-1050">G</span></span></td>
<td><span data-ttu-id="c4552-1051"><a href="#data-types-used-in-the-vml-object-model">Entero</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="c4552-1052">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1052">Green component of the color.</span></span> <span data-ttu-id="c4552-1053">Puede oscilar entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="c4552-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1054">B</span><span class="sxs-lookup"><span data-stu-id="c4552-1054">B</span></span></td>
<td><span data-ttu-id="c4552-1055"><a href="#data-types-used-in-the-vml-object-model">Entero</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="c4552-1056">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1056">Blue component of the color.</span></span> <span data-ttu-id="c4552-1057">Puede oscilar entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="c4552-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1058">String</span><span class="sxs-lookup"><span data-stu-id="c4552-1058">String</span></span></td>
<td><span data-ttu-id="c4552-1059"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="c4552-1060">Representación de texto del color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1060">Text representation of the color.</span></span> <span data-ttu-id="c4552-1061">Se admiten los siguientes tipos de colores con nombre:</span><span class="sxs-lookup"><span data-stu-id="c4552-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="c4552-1062">Negro (#000000)</span><span class="sxs-lookup"><span data-stu-id="c4552-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="c4552-1063">Silver (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="c4552-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="c4552-1064">Gris (#808080)</span><span class="sxs-lookup"><span data-stu-id="c4552-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="c4552-1065">Blanco (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="c4552-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="c4552-1066">Maroon (#800000)</span><span class="sxs-lookup"><span data-stu-id="c4552-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="c4552-1067">Rojo (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="c4552-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="c4552-1068">Púrpura (#800080)</span><span class="sxs-lookup"><span data-stu-id="c4552-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="c4552-1069">Ría (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="c4552-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="c4552-1070">Verde (#008000)</span><span class="sxs-lookup"><span data-stu-id="c4552-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="c4552-1071">Lime (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="c4552-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="c4552-1072">Negra (#808000)</span><span class="sxs-lookup"><span data-stu-id="c4552-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="c4552-1073">Amarillo (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="c4552-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="c4552-1074">India (#000080)</span><span class="sxs-lookup"><span data-stu-id="c4552-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="c4552-1075">Azul (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="c4552-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="c4552-1076">Teal (#008080)</span><span class="sxs-lookup"><span data-stu-id="c4552-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="c4552-1077">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="c4552-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1078">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-1078">Type</span></span></td>
<td><span data-ttu-id="c4552-1079"><strong>DvcolorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="c4552-1080">Tipo de color.</span><span class="sxs-lookup"><span data-stu-id="c4552-1080">Type of color.</span></span> <span data-ttu-id="c4552-1081">Uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4552-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="c4552-1082">Mixto</span><span class="sxs-lookup"><span data-stu-id="c4552-1082">Mixed</span></span></li>
<li><span data-ttu-id="c4552-1083">con nombre</span><span class="sxs-lookup"><span data-stu-id="c4552-1083">Named</span></span></li>
<li><span data-ttu-id="c4552-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="c4552-1084">RGB</span></span></li>
<li><span data-ttu-id="c4552-1085">Scheme</span><span class="sxs-lookup"><span data-stu-id="c4552-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4552-1086">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="c4552-1086">**IVgEquation**</span></span>

<span data-ttu-id="c4552-1087">Ecuaciones usadas para fórmulas.</span><span class="sxs-lookup"><span data-stu-id="c4552-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1088">Operación</span><span class="sxs-lookup"><span data-stu-id="c4552-1088">Operation</span></span></td>
<td><span data-ttu-id="c4552-1089"><strong>BvEquationOperationType</strong> Nombre de la operación que se realizará en los parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4552-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="c4552-1090">Las siguientes operaciones se pueden usar en una ecuación:</span><span class="sxs-lookup"><span data-stu-id="c4552-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-1091">Operación</span><span class="sxs-lookup"><span data-stu-id="c4552-1091">Operation</span></span></th>
<th><span data-ttu-id="c4552-1092">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="c4552-1093">Abs</span></span></td>
<td><span data-ttu-id="c4552-1094">Valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="c4552-1094">Absolute value.</span></span> <br/> <span data-ttu-id="c4552-1095"><strong>abs</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="c4552-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="c4552-1096">Atan2</span></span></td>
<td><span data-ttu-id="c4552-1097">Aritmética polar: da como resultado unidades fd (grados multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="c4552-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="c4552-1098"><strong>atan2</strong>(p1,v)</span><span class="sxs-lookup"><span data-stu-id="c4552-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="c4552-1099">Cos</span></span></td>
<td><span data-ttu-id="c4552-1100">Coseno, argumento en unidades fd (grados multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="c4552-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="c4552-1101">v \* <strong>cos</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="c4552-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="c4552-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="c4552-1103">Conserva la precisión completa en el cálculo intermedio.</span><span class="sxs-lookup"><span data-stu-id="c4552-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="c4552-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="c4552-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1105">Elipse</span><span class="sxs-lookup"><span data-stu-id="c4552-1105">Ellipse</span></span></td>
<td><span data-ttu-id="c4552-1106">Elipse</span><span class="sxs-lookup"><span data-stu-id="c4552-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1107">Si</span><span class="sxs-lookup"><span data-stu-id="c4552-1107">If</span></span></td>
<td><span data-ttu-id="c4552-1108">Prueba de condición if.</span><span class="sxs-lookup"><span data-stu-id="c4552-1108">If Condition test.</span></span> <span data-ttu-id="c4552-1109">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="c4552-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="c4552-1110">p1: p2</span><span class="sxs-lookup"><span data-stu-id="c4552-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1111">Max</span><span class="sxs-lookup"><span data-stu-id="c4552-1111">Max</span></span></td>
<td><span data-ttu-id="c4552-1112">Mayor de dos valores.</span><span class="sxs-lookup"><span data-stu-id="c4552-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="c4552-1113"><strong>max</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="c4552-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1114">Mid</span><span class="sxs-lookup"><span data-stu-id="c4552-1114">Mid</span></span></td>
<td><span data-ttu-id="c4552-1115">Average ( v + p1)/2</span><span class="sxs-lookup"><span data-stu-id="c4552-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1116">Min</span><span class="sxs-lookup"><span data-stu-id="c4552-1116">Min</span></span></td>
<td><span data-ttu-id="c4552-1117">Menor de dos valores.</span><span class="sxs-lookup"><span data-stu-id="c4552-1117">The lesser of two values.</span></span> <span data-ttu-id="c4552-1118"><strong>min</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="c4552-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="c4552-1119">Mod</span></span></td>
<td><span data-ttu-id="c4552-1120">Valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="c4552-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1121">Producto</span><span class="sxs-lookup"><span data-stu-id="c4552-1121">Product</span></span></td>
<td><span data-ttu-id="c4552-1122">Se usa para la multiplicación y la división.</span><span class="sxs-lookup"><span data-stu-id="c4552-1122">Used for multiplication and division.</span></span> <span data-ttu-id="c4552-1123">v \* p1 / p2</span><span class="sxs-lookup"><span data-stu-id="c4552-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1124">Seno</span><span class="sxs-lookup"><span data-stu-id="c4552-1124">Sin</span></span></td>
<td><span data-ttu-id="c4552-1125">Seno, argumento en unidades fd (grados multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="c4552-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="c4552-1126">v \* <strong>sin</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="c4552-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="c4552-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="c4552-1128">Conserva la precisión completa en el cálculo intermedio.</span><span class="sxs-lookup"><span data-stu-id="c4552-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="c4552-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span><span class="sxs-lookup"><span data-stu-id="c4552-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="c4552-1130">Sqrt</span></span></td>
<td><span data-ttu-id="c4552-1131">El resultado es positivo y se redondea hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="c4552-1132"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="c4552-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1133">Sum</span><span class="sxs-lookup"><span data-stu-id="c4552-1133">Sum</span></span></td>
<td><span data-ttu-id="c4552-1134">Se usa para sumar y restar.</span><span class="sxs-lookup"><span data-stu-id="c4552-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="c4552-1135">v + p1 p2</span><span class="sxs-lookup"><span data-stu-id="c4552-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1136">Sumangle</span><span class="sxs-lookup"><span data-stu-id="c4552-1136">Sumangle</span></span></td>
<td><span data-ttu-id="c4552-1137">Ángulo existente (escalado en 65536), donde p1 y p2 están en grados.</span><span class="sxs-lookup"><span data-stu-id="c4552-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="c4552-1138">v + p1 \* 65536 + p2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="c4552-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="c4552-1139">Tan</span></span></td>
<td><span data-ttu-id="c4552-1140">Tangente, el argumento está en unidades fd (grados multiplicados por 65536).</span><span class="sxs-lookup"><span data-stu-id="c4552-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="c4552-1141">v \* tan( p1 )</span><span class="sxs-lookup"><span data-stu-id="c4552-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1142">Val</span><span class="sxs-lookup"><span data-stu-id="c4552-1142">Val</span></span></td>
<td><span data-ttu-id="c4552-1143">Define un valor de guía de otro valor.</span><span class="sxs-lookup"><span data-stu-id="c4552-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1144">Param1</span><span class="sxs-lookup"><span data-stu-id="c4552-1144">Param1</span></span></td>
<td><span data-ttu-id="c4552-1145"><strong>Entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="c4552-1146">El primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4552-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="c4552-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="c4552-1148"><strong>DvFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="c4552-1149">Tipo del primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4552-1149">The type of the first parameter.</span></span> <span data-ttu-id="c4552-1150">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4552-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-1151">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-1151">Type</span></span></th>
<th><span data-ttu-id="c4552-1152">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1153">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1153">Value</span></span></td>
<td><span data-ttu-id="c4552-1154">El parámetro es un valor simple.</span><span class="sxs-lookup"><span data-stu-id="c4552-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1155">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="c4552-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="c4552-1156">El parámetro es una referencia a un ajuste.</span><span class="sxs-lookup"><span data-stu-id="c4552-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="c4552-1157">Por ejemplo, si el primer parámetro es 1, se usará el valor del primer ajuste.</span><span class="sxs-lookup"><span data-stu-id="c4552-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1158">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="c4552-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="c4552-1159">El parámetro es el resultado de una referencia al resultado de una fórmula anterior.</span><span class="sxs-lookup"><span data-stu-id="c4552-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="c4552-1160">Por ejemplo, si el primer parámetro es 2, se usará el resultado de la fórmula 2.</span><span class="sxs-lookup"><span data-stu-id="c4552-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="c4552-1161">Param2</span></span></td>
<td><span data-ttu-id="c4552-1162"><strong>Entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="c4552-1163">El segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4552-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="c4552-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="c4552-1165"><strong>DvFormulaParamType</strong> Tipo del parámetro 2.</span><span class="sxs-lookup"><span data-stu-id="c4552-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1166">Val</span><span class="sxs-lookup"><span data-stu-id="c4552-1166">Val</span></span></td>
<td><span data-ttu-id="c4552-1167"><strong>Entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="c4552-1168">Resultado.</span><span class="sxs-lookup"><span data-stu-id="c4552-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="c4552-1169">Valtype2</span></span></td>
<td><span data-ttu-id="c4552-1170"><strong>DvFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="c4552-1171">Tipo del resultado.</span><span class="sxs-lookup"><span data-stu-id="c4552-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4552-1172">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4552-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="c4552-1173">Especifica un rectángulo fijo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="c4552-1174">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1174">Attribute</span></span> | <span data-ttu-id="c4552-1175">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1176">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1176">Value</span></span>      | <span data-ttu-id="c4552-1177">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1178">Valor de texto que especifica la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4552-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="c4552-1179">Left</span><span class="sxs-lookup"><span data-stu-id="c4552-1179">Left</span></span>       | <span data-ttu-id="c4552-1180">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1181">Coordenada situada más a la izquierda del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="c4552-1182">Superior</span><span class="sxs-lookup"><span data-stu-id="c4552-1182">Top</span></span>        | <span data-ttu-id="c4552-1183">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1184">Coordenada superior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="c4552-1185">Right</span><span class="sxs-lookup"><span data-stu-id="c4552-1185">Right</span></span>      | <span data-ttu-id="c4552-1186">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1187">Coordenada situada más a la derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="c4552-1188">Inferior</span><span class="sxs-lookup"><span data-stu-id="c4552-1188">Bottom</span></span>     | <span data-ttu-id="c4552-1189">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1190">Coordenada inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="c4552-1191">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="c4552-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="c4552-1192">Matriz de rectángulos fijos.</span><span class="sxs-lookup"><span data-stu-id="c4552-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="c4552-1193">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1193">Attribute</span></span> | <span data-ttu-id="c4552-1194">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1195">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1195">Value</span></span>      | <span data-ttu-id="c4552-1196">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1197">Representación de texto de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c4552-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="c4552-1198">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1198">Length</span></span>     | <span data-ttu-id="c4552-1199">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1200">Número de rectángulos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="c4552-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="c4552-1201">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-1201">Item</span></span>       | <span data-ttu-id="c4552-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1203">Objeto de rectángulo en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c4552-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="c4552-1204">**Tipo de datos IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="c4552-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="c4552-1205">Definiciones de fórmulas que pueden variar el trazado de una forma o usarse para otros fines de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="c4552-1206">Las fórmulas se pueden basar en el **atributo Adj** de una forma, que puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="c4552-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="c4552-1207">Las fórmulas también pueden hacer referencia a otras fórmulas.</span><span class="sxs-lookup"><span data-stu-id="c4552-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="c4552-1208">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1208">Attribute</span></span>| <span data-ttu-id="c4552-1209">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1210">Eqn</span><span class="sxs-lookup"><span data-stu-id="c4552-1210">Eqn</span></span>        | <span data-ttu-id="c4552-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1212">Cada fórmula define un valor único como resultado de la evaluación de la expresión.</span><span class="sxs-lookup"><span data-stu-id="c4552-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="c4552-1213">La expresión se define mediante este atributo y tiene la forma general de una operación seguida de hasta tres argumentos, que pueden ser valores de ajuste (por ejemplo, 2), los resultados de fórmulas anteriores (por ejemplo, ), números fijos o valores \# @2 predefinidos.</span><span class="sxs-lookup"><span data-stu-id="c4552-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="c4552-1214">**Tipo de datos IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="c4552-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="c4552-1215">Colección de objetos de fórmula.</span><span class="sxs-lookup"><span data-stu-id="c4552-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="c4552-1216">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1216">Attribute</span></span> | <span data-ttu-id="c4552-1217">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1218">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1218">Length</span></span>     | <span data-ttu-id="c4552-1219">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1220">Número de objetos de fórmula de la colección.</span><span class="sxs-lookup"><span data-stu-id="c4552-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="c4552-1221">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-1221">Item</span></span>       | <span data-ttu-id="c4552-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1223">Una fórmula específica.</span><span class="sxs-lookup"><span data-stu-id="c4552-1223">A specific formula.</span></span> <span data-ttu-id="c4552-1224">Tenga en cuenta que la matriz de fórmulas se puede heredar en el tipo de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="c4552-1225">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="c4552-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="c4552-1226">Matriz de colores que definen un degradado (intervalo combinado de colores).</span><span class="sxs-lookup"><span data-stu-id="c4552-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="c4552-1227">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1227">Attribute</span></span> | <span data-ttu-id="c4552-1228">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1229">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1229">Value</span></span>      | <span data-ttu-id="c4552-1230">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1231">Especifica la matriz de colores; por ejemplo, "red .2; verde .4; black .7"</span><span class="sxs-lookup"><span data-stu-id="c4552-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="c4552-1232">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1232">Length</span></span>     | <span data-ttu-id="c4552-1233">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1234">Número de colores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c4552-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="c4552-1235">Método</span><span class="sxs-lookup"><span data-stu-id="c4552-1235">Method</span></span>     | <span data-ttu-id="c4552-1236">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1237">AddColor</span><span class="sxs-lookup"><span data-stu-id="c4552-1237">AddColor</span></span>    | <span data-ttu-id="c4552-1238">[Accionario](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="c4552-1239">Agrega un nuevo color en el punto de conexión especificado por fracción.</span><span class="sxs-lookup"><span data-stu-id="c4552-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="c4552-1240">El nuevo color es blanco de forma predeterminada y es el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c4552-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="c4552-1241">A continuación, el color se puede cambiar por referencia.</span><span class="sxs-lookup"><span data-stu-id="c4552-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="c4552-1242">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="c4552-1242">RemoveColor</span></span> | <span data-ttu-id="c4552-1243">[Accionario](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="c4552-1244">Quita un color en el punto de conexión especificado por fracción.</span><span class="sxs-lookup"><span data-stu-id="c4552-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="c4552-1245">Nota: Si 0,0 o 1,0 no existe, está implícito y el color blanco se usa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="c4552-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="c4552-1246">**Tipo de datos IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="c4552-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="c4552-1247">Matriz de puntos que definen una forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="c4552-1248">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1248">Attribute</span></span> | <span data-ttu-id="c4552-1249">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4552-1250">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1250">Value</span></span>      | <span data-ttu-id="c4552-1251">[Cadena](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1252">Representación de texto de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c4552-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="c4552-1253">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1253">Length</span></span>     | <span data-ttu-id="c4552-1254">[Entero](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="c4552-1255">Número de puntos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="c4552-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="c4552-1256">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4552-1256">Item</span></span>       | <span data-ttu-id="c4552-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4552-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="c4552-1258">Punto en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c4552-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="c4552-1259">**Tipo de datos IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="c4552-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="c4552-1260">Matriz usada para sesgar formas, una matriz de transformación de perspectiva con el formato "*sxx,sxy,syx,syy,px,py* " \[ *s* =scale, *p* =perspective \] .</span><span class="sxs-lookup"><span data-stu-id="c4552-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="c4552-1261">Si offset está en unidades absolutas, *px,py* están en unidades emu ^-1; de lo contrario, son una fracción inversa del tamaño de forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="c4552-1262">Atributo</span><span class="sxs-lookup"><span data-stu-id="c4552-1262">Attribute</span></span>   | <span data-ttu-id="c4552-1263">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="c4552-1264">XtoX</span><span class="sxs-lookup"><span data-stu-id="c4552-1264">XtoX</span></span>         | <span data-ttu-id="c4552-1265">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="c4552-1266">YtoX</span><span class="sxs-lookup"><span data-stu-id="c4552-1266">YtoX</span></span>         | <span data-ttu-id="c4552-1267">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="c4552-1268">XtoY</span><span class="sxs-lookup"><span data-stu-id="c4552-1268">XtoY</span></span>         | <span data-ttu-id="c4552-1269">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="c4552-1270">YtoY</span><span class="sxs-lookup"><span data-stu-id="c4552-1270">YtoY</span></span>         | <span data-ttu-id="c4552-1271">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="c4552-1272">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="c4552-1272">PerspectiveX</span></span> | <span data-ttu-id="c4552-1273">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="c4552-1274">PerspectiveY</span><span class="sxs-lookup"><span data-stu-id="c4552-1274">PerspectiveY</span></span> | <span data-ttu-id="c4552-1275">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="c4552-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="c4552-1276">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="c4552-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="c4552-1277">Especifica el desplazamiento del sesgo.</span><span class="sxs-lookup"><span data-stu-id="c4552-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-1278">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4552-1278">Attributes</span></span></th>
<th><span data-ttu-id="c4552-1279">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1280">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1280">Value</span></span></td>
<td><span data-ttu-id="c4552-1281"><a href="#data-types-used-in-the-vml-object-model">Cadena</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="c4552-1282">Representación de texto de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c4552-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1283">X</span><span class="sxs-lookup"><span data-stu-id="c4552-1283">X</span></span></td>
<td><span data-ttu-id="c4552-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1285">Componente X.</span><span class="sxs-lookup"><span data-stu-id="c4552-1285">X component.</span></span> <span data-ttu-id="c4552-1286">Porcentaje o medida.</span><span class="sxs-lookup"><span data-stu-id="c4552-1286">Percentage or measure.</span></span> <span data-ttu-id="c4552-1287">Si no hay unidades, el tipo ShapeRelative está implícito; De lo contrario, el tipo absoluto está implícito.</span><span class="sxs-lookup"><span data-stu-id="c4552-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1288">esté</span><span class="sxs-lookup"><span data-stu-id="c4552-1288">Y</span></span></td>
<td><span data-ttu-id="c4552-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1290">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="c4552-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1291">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-1291">Type</span></span></td>
<td><span data-ttu-id="c4552-1292"><strong>DvTransformwTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="c4552-1293">Especifica el tipo de transformación.</span><span class="sxs-lookup"><span data-stu-id="c4552-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="c4552-1294">Los valores válidos son puntos enteros comprendidos entre -infinity e infinity.</span><span class="sxs-lookup"><span data-stu-id="c4552-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-1295">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-1295">Type</span></span></th>
<th><span data-ttu-id="c4552-1296">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1297">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="c4552-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="c4552-1298">Los valores del desplazamiento son porcentajes (relaciones) del tamaño de la forma original; Por ejemplo, un valor de 0,5 significa un desplazamiento a la mitad del tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4552-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1299">Absoluto</span><span class="sxs-lookup"><span data-stu-id="c4552-1299">Absolute</span></span></td>
<td><span data-ttu-id="c4552-1300">Los valores son unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="c4552-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4552-1301">**Tipo de datos IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="c4552-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="c4552-1302">Especifica un vector bidimensional que consta de dos **números Double.**</span><span class="sxs-lookup"><span data-stu-id="c4552-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4552-1303">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4552-1303">Attributes</span></span></th>
<th><span data-ttu-id="c4552-1304">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4552-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1305">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1305">Value</span></span></td>
<td><span data-ttu-id="c4552-1306"><strong>Cadena</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1306"><strong>String</strong>.</span></span> <span data-ttu-id="c4552-1307">Representación de texto de ambos números vectoriales separados por un espacio.</span><span class="sxs-lookup"><span data-stu-id="c4552-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1308">X</span><span class="sxs-lookup"><span data-stu-id="c4552-1308">X</span></span></td>
<td><span data-ttu-id="c4552-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1310">Componente X de este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1311">esté</span><span class="sxs-lookup"><span data-stu-id="c4552-1311">Y</span></span></td>
<td><span data-ttu-id="c4552-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1313">Componente Y de este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1314">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-1314">Type</span></span></td>
<td><span data-ttu-id="c4552-1315"><strong>DvvectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="c4552-1316">Unidades esperadas para este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1316">Expected units for this vector.</span></span> <span data-ttu-id="c4552-1317">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-1318">Medida</span><span class="sxs-lookup"><span data-stu-id="c4552-1318">Measure</span></span></li>
<li><span data-ttu-id="c4552-1319">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1319">Length</span></span></li>
<li><span data-ttu-id="c4552-1320">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="c4552-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="c4552-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="c4552-1321">Fraction</span></span></li>
<li><span data-ttu-id="c4552-1322">Entero de porcentaje de número</span><span class="sxs-lookup"><span data-stu-id="c4552-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4552-1323">**Tipo de datos IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="c4552-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="c4552-1324">Especifica un vector tridimensional que consta de tres **números Double.**</span><span class="sxs-lookup"><span data-stu-id="c4552-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4552-1325">Valor</span><span class="sxs-lookup"><span data-stu-id="c4552-1325">Value</span></span></td>
<td><span data-ttu-id="c4552-1326"><strong>Cadena</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1326"><strong>String</strong>.</span></span> <span data-ttu-id="c4552-1327">Representación de texto de tres números vectoriales separados por un espacio.</span><span class="sxs-lookup"><span data-stu-id="c4552-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1328">X</span><span class="sxs-lookup"><span data-stu-id="c4552-1328">X</span></span></td>
<td><span data-ttu-id="c4552-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1330">Componente X de este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1331">esté</span><span class="sxs-lookup"><span data-stu-id="c4552-1331">Y</span></span></td>
<td><span data-ttu-id="c4552-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1333">Componente Y de este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4552-1334">Z</span><span class="sxs-lookup"><span data-stu-id="c4552-1334">Z</span></span></td>
<td><span data-ttu-id="c4552-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="c4552-1336">Componente Z de este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4552-1337">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4552-1337">Type</span></span></td>
<td><span data-ttu-id="c4552-1338"><strong>DvvectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4552-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="c4552-1339">Unidades esperadas para este vector.</span><span class="sxs-lookup"><span data-stu-id="c4552-1339">Expected units for this vector.</span></span> <span data-ttu-id="c4552-1340">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c4552-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="c4552-1341">Medida</span><span class="sxs-lookup"><span data-stu-id="c4552-1341">Measure</span></span></li>
<li><span data-ttu-id="c4552-1342">Length</span><span class="sxs-lookup"><span data-stu-id="c4552-1342">Length</span></span></li>
<li><span data-ttu-id="c4552-1343">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="c4552-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="c4552-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="c4552-1344">Fraction</span></span></li>
<li><span data-ttu-id="c4552-1345">Número</span><span class="sxs-lookup"><span data-stu-id="c4552-1345">Number</span></span></li>
<li><span data-ttu-id="c4552-1346">Porcentaje</span><span class="sxs-lookup"><span data-stu-id="c4552-1346">Percentage</span></span></li>
<li><span data-ttu-id="c4552-1347">Entero</span><span class="sxs-lookup"><span data-stu-id="c4552-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4552-1348">**Tipo de datos length**</span><span class="sxs-lookup"><span data-stu-id="c4552-1348">**Length data type**</span></span>

<span data-ttu-id="c4552-1349">Número de punto flotante con un intervalo de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="c4552-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="c4552-1350">**Tipo de datos de medida**</span><span class="sxs-lookup"><span data-stu-id="c4552-1350">**Measure data type**</span></span>

<span data-ttu-id="c4552-1351">Número de punto flotante de infinito a infinito.</span><span class="sxs-lookup"><span data-stu-id="c4552-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="c4552-1352">**Tipo de datos String**</span><span class="sxs-lookup"><span data-stu-id="c4552-1352">**String data type**</span></span>

<span data-ttu-id="c4552-1353">Datos de caracteres de cualquier longitud.</span><span class="sxs-lookup"><span data-stu-id="c4552-1353">Character data of any length.</span></span>

<span data-ttu-id="c4552-1354">**CkBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="c4552-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="c4552-1355">Modo de representación para blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="c4552-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="c4552-1356">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="c4552-1356">Possible values are:</span></span>

-   <span data-ttu-id="c4552-1357">**Color**</span><span class="sxs-lookup"><span data-stu-id="c4552-1357">**Color**</span></span>
-   <span data-ttu-id="c4552-1358">**Automático**</span><span class="sxs-lookup"><span data-stu-id="c4552-1358">**Auto**</span></span>
-   <span data-ttu-id="c4552-1359">**Grises**</span><span class="sxs-lookup"><span data-stu-id="c4552-1359">**GrayScale**</span></span>
-   <span data-ttu-id="c4552-1360">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="c4552-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="c4552-1361">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="c4552-1361">**InverseGray**</span></span>
-   <span data-ttu-id="c4552-1362">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="c4552-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="c4552-1363">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="c4552-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="c4552-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="c4552-1364">**HighContrast**</span></span>
-   <span data-ttu-id="c4552-1365">**Negro**</span><span class="sxs-lookup"><span data-stu-id="c4552-1365">**Black**</span></span>
-   <span data-ttu-id="c4552-1366">**Blanco**</span><span class="sxs-lookup"><span data-stu-id="c4552-1366">**White**</span></span>
-   <span data-ttu-id="c4552-1367">**Desdrawn**</span><span class="sxs-lookup"><span data-stu-id="c4552-1367">**Undrawn**</span></span>

<span data-ttu-id="c4552-1368">**Tipo de datos Desconexión**</span><span class="sxs-lookup"><span data-stu-id="c4552-1368">**VgFraction data type**</span></span>

<span data-ttu-id="c4552-1369">Número de punto flotante con intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c4552-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="c4552-1370">Las fracciones también se pueden especificar como porcentaje; Por ejemplo, "50 %".</span><span class="sxs-lookup"><span data-stu-id="c4552-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="c4552-1371">**Tipo de datos DerTriState**</span><span class="sxs-lookup"><span data-stu-id="c4552-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="c4552-1372">Enumeración usada para valores que pueden ser uno de tres estados:</span><span class="sxs-lookup"><span data-stu-id="c4552-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="c4552-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c4552-1373">**TRUE**</span></span>
-   <span data-ttu-id="c4552-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c4552-1374">**FALSE**</span></span>
-   <span data-ttu-id="c4552-1375">**COMBINACIÓN**</span><span class="sxs-lookup"><span data-stu-id="c4552-1375">**MIXED**</span></span>