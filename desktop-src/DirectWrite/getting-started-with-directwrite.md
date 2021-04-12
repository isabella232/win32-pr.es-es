---
title: Tutorial Introducción con DirectWrite
description: En este documento se muestra cómo usar DirectWrite y Direct2D para crear texto simple que contenga un solo formato y, a continuación, texto que contenga varios formatos.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, tutorial
- DirectWrite, tutorial de introducción
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, interfaz IDWriteTextLayout
- Interfaz IDWriteTextLayout
- DirectWrite, interfaz IDWriteTypography
- Interfaz IDWriteTypography
- DirectWrite, interfaz IDWriteTextFormat
- Interfaz IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359216"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="ab6c1-113">Tutorial: Introducción con DirectWrite</span><span class="sxs-lookup"><span data-stu-id="ab6c1-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="ab6c1-114">En este documento se muestra cómo usar [DirectWrite](direct-write-portal.md) y [Direct2D](rendering-by-using-direct2d.md) para crear texto simple que contenga un solo formato y, a continuación, texto que contenga varios formatos.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="ab6c1-115">Este tutorial contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="ab6c1-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="ab6c1-116">Código fuente</span><span class="sxs-lookup"><span data-stu-id="ab6c1-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="ab6c1-117">Dibujo de texto simple</span><span class="sxs-lookup"><span data-stu-id="ab6c1-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="ab6c1-118">Parte 1: declarar recursos de DirectWrite y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="ab6c1-119">Parte 2: creación de recursos independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="ab6c1-120">Parte 3: crear recursos de Device-Dependent.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="ab6c1-121">Parte 4: dibujar texto mediante el método DrawText de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="ab6c1-122">Parte 5: representar el contenido de la ventana mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="ab6c1-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="ab6c1-123">Dibujar texto con varios formatos.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="ab6c1-124">Parte 1: creación de una interfaz IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="ab6c1-125">Parte 2: aplicar formato con IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="ab6c1-126">Parte 3: agregar características tipográficas con IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="ab6c1-127">Parte 4: dibujar texto con el método DrawTextLayout de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="ab6c1-128">Código fuente</span><span class="sxs-lookup"><span data-stu-id="ab6c1-128">Source Code</span></span>

<span data-ttu-id="ab6c1-129">El código fuente que se muestra en esta información general se toma del [ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="ab6c1-130">Cada parte se implementa en una clase independiente (SimpleText y MultiformattedText) y se muestra en una ventana secundaria independiente.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="ab6c1-131">Cada clase representa una ventana de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="ab6c1-132">Además del método *WndProc* , cada clase contiene los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="ab6c1-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="ab6c1-133">Función</span><span class="sxs-lookup"><span data-stu-id="ab6c1-133">Function</span></span>                              | <span data-ttu-id="ab6c1-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab6c1-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6c1-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="ab6c1-136">Crea recursos independientes del dispositivo, por lo que se pueden volver a usar en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="ab6c1-137">**DiscardDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="ab6c1-138">Libera los recursos independientes del dispositivo una vez que ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="ab6c1-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="ab6c1-140">Crea recursos, como pinceles y destinos de representación, que están vinculados a un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="ab6c1-141">**DiscardDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="ab6c1-142">Libera los recursos dependientes del dispositivo una vez que ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="ab6c1-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="ab6c1-144">Usa [Direct2D](../direct2d/direct2d-portal.md) para representar en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="ab6c1-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-145">**DrawText**</span></span>                          | <span data-ttu-id="ab6c1-146">Dibuja la cadena de texto mediante [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="ab6c1-147">**OnResize**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-147">**OnResize**</span></span>                          | <span data-ttu-id="ab6c1-148">Cambia el tamaño del destino de representación de [Direct2D](../direct2d/direct2d-portal.md) cuando se cambia el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="ab6c1-149">Puede usar el ejemplo proporcionado, o bien usar las instrucciones siguientes para agregar [DirectWrite](direct-write-portal.md) y [Direct2D](rendering-by-using-direct2d.md) a su propia aplicación de Win32.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="ab6c1-150">Para obtener más información sobre el ejemplo y los archivos de proyecto asociados, vea el [ejemplo DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="ab6c1-151">Dibujo de texto simple</span><span class="sxs-lookup"><span data-stu-id="ab6c1-151">Drawing Simple Text</span></span>

<span data-ttu-id="ab6c1-152">En esta sección se muestra cómo usar [DirectWrite](direct-write-portal.md) y [Direct2D](../direct2d/direct2d-portal.md) para representar texto simple que tiene un solo formato, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

![captura de pantalla de "Hello World Using directwrite!"](images/simplecropped.png)

<span data-ttu-id="ab6c1-155">Dibujar texto simple en la pantalla requiere cuatro componentes:</span><span class="sxs-lookup"><span data-stu-id="ab6c1-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="ab6c1-156">Cadena de caracteres que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-156">A character string to render.</span></span>
-   <span data-ttu-id="ab6c1-157">Instancia de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="ab6c1-158">Dimensiones del área que va a contener el texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="ab6c1-159">Objeto que puede representar el texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-159">An object that can render the text.</span></span> <span data-ttu-id="ab6c1-160">En este tutorial.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-160">In this tutorial.</span></span> <span data-ttu-id="ab6c1-161">se usa un destino de representación de [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="ab6c1-162">La interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) describe el nombre, el tamaño, el peso, el estilo y la extensión de la familia de fuentes que se usan para dar formato al texto, y describe la información de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="ab6c1-163">**IDWriteTextFormat** también define los métodos para establecer y obtener las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="ab6c1-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="ab6c1-164">Espaciado de línea.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-164">The line spacing.</span></span>
-   <span data-ttu-id="ab6c1-165">Alineación del texto con respecto a los bordes izquierdo y derecho del cuadro de diseño.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="ab6c1-166">Alineación de párrafo relativa a la parte superior e inferior del cuadro de diseño.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="ab6c1-167">Dirección de lectura.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-167">The reading direction.</span></span>
-   <span data-ttu-id="ab6c1-168">Granularidad de recorte de texto para el texto que desborda el cuadro de diseño.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="ab6c1-169">La tabulación incremental.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="ab6c1-170">Dirección del flujo de párrafo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-170">The paragraph flow direction.</span></span>

<span data-ttu-id="ab6c1-171">La interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) es necesaria para dibujar texto que use los dos procesos descritos en este documento.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="ab6c1-172">Para poder crear un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o cualquier otro objeto [DirectWrite](direct-write-portal.md) , se necesita una instancia de [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="ab6c1-173">Se usa un **IDWriteFactory** para crear instancias de **IDWriteTextFormat** y otros objetos de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="ab6c1-174">Para obtener una instancia de generador, utilice la función [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="ab6c1-175">Parte 1: declarar recursos de DirectWrite y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="ab6c1-176">En esta parte, se declaran los objetos que usará más adelante para crear y mostrar texto como miembros de datos privados de la clase.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="ab6c1-177">Todas las interfaces, funciones y tipos de archivos de [DirectWrite](direct-write-portal.md) se declaran en el archivo de encabezado *dwrite. h* y los de [Direct2D](../direct2d/direct2d-portal.md) se declaran en *d2d1. h*; Si aún no lo ha hecho, incluya estos encabezados en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="ab6c1-178">En el archivo de encabezado de clase (SimpleText. h), declare punteros a las interfaces [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) como miembros privados.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="ab6c1-179">Declare los miembros para que contengan la cadena de texto que se va a representar y la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="ab6c1-180">Declare punteros a las interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)y [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para representar el texto con [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="ab6c1-181">Parte 2: creación de recursos independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="ab6c1-182">[Direct2D](rendering-by-using-direct2d.md) proporciona dos tipos de recursos: recursos dependientes del dispositivo y recursos independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="ab6c1-183">Los recursos dependientes del dispositivo se asocian a un dispositivo de representación y ya no funcionan si se quita ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="ab6c1-184">Por otro lado, los recursos independientes del dispositivo pueden durar el ámbito de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="ab6c1-185">Los recursos de [DirectWrite](direct-write-portal.md) son independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="ab6c1-186">En esta sección, creará los recursos independientes del dispositivo que usa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="ab6c1-187">Estos recursos se deben liberar con una llamada al método **Release** de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="ab6c1-188">Algunos de los recursos que se usan solo deben crearse una vez y no están vinculados a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="ab6c1-189">La inicialización de estos recursos se coloca en el método *SimpleText:: CreateDeviceIndependentResources* , al que se llama al inicializar la clase.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="ab6c1-190">Dentro del método *SimpleText:: CreateDeviceIndependentResources* en el archivo de implementación de clase (SimpleText. cpp), llame a la función [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) para crear una interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , que es la interfaz de fábrica raíz para todos los objetos de [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="ab6c1-191">Use el mismo generador para crear instancias de otros recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="ab6c1-192">Llame a la función [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para crear una interfaz [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , que es la interfaz de fábrica raíz para todos los objetos [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="ab6c1-193">Use el mismo generador para crear instancias de otros recursos de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  <span data-ttu-id="ab6c1-194">Inicialice la cadena de texto y almacene su longitud.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="ab6c1-195">Cree un objeto de interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) mediante el método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="ab6c1-196">**IDWriteTextFormat** especifica la fuente, el peso, el estiramiento, el estilo y la configuración regional que se utilizará para representar la cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  <span data-ttu-id="ab6c1-197">Centre el texto horizontal y verticalmente mediante una llamada a los métodos [**IDWriteTextFormat:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) y [**IDWriteTextFormat:: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

<span data-ttu-id="ab6c1-198">En esta parte, ha inicializado los recursos independientes del dispositivo que usa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="ab6c1-199">En la siguiente parte, se inicializan los recursos dependientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="ab6c1-200">Parte 3: crear recursos de Device-Dependent.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="ab6c1-201">En esta parte, creará un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) y un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para representar el texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="ab6c1-202">Un destino de representación es un objeto de Direct2D que crea recursos de dibujo y representa comandos de dibujo en un dispositivo de representación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="ab6c1-203">Un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) es un destino de representación que se representa en un **hWnd**.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="ab6c1-204">Uno de los recursos de dibujo que puede crear un destino de representación es un pincel para dibujar contornos, rellenos y texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="ab6c1-205">Un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="ab6c1-206">Las interfaces [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) y [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) se enlazan a un dispositivo de representación cuando se crean y se deben liberar y volver a crear si el dispositivo deja de ser válido.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="ab6c1-207">Dentro del método SimpleText:: CreateDeviceResources, compruebe si el puntero de destino de representación es **null**.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="ab6c1-208">Si es así, recupere el tamaño del área de representación y cree un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) de ese tamaño.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="ab6c1-209">Use **ID2D1HwndRenderTarget** para crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  <span data-ttu-id="ab6c1-210">En el método SimpleText::D iscardDeviceResources, libere el pincel y el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="ab6c1-211">Ahora que ha creado un destino de representación y un pincel, puede usarlos para representar el texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="ab6c1-212">Parte 4: dibujar texto mediante el método DrawText de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="ab6c1-213">En el método SimpleText::D rawText de la clase, defina el área del diseño de texto recuperando las dimensiones del área de representación y cree un rectángulo de [Direct2D](../direct2d/direct2d-portal.md) que tenga las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="ab6c1-214">Use el método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y el objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para representar texto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="ab6c1-215">El método **ID2D1RenderTarget::D rawtext** toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab6c1-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="ab6c1-216">Cadena que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-216">A string to render.</span></span>
    -   <span data-ttu-id="ab6c1-217">Puntero a una interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="ab6c1-218">Rectángulo de diseño de [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="ab6c1-219">Puntero a una interfaz que expone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="ab6c1-220">Parte 5: representar el contenido de la ventana mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="ab6c1-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="ab6c1-221">Para representar el contenido de la ventana mediante [Direct2D](../direct2d/direct2d-portal.md) cuando se recibe un mensaje de dibujo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab6c1-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="ab6c1-222">Cree los recursos dependientes del dispositivo mediante una llamada al método SimpleText:: CreateDeviceResources implementado en la parte 3.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="ab6c1-223">Llame al método [**ID2D1HwndRenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="ab6c1-224">Borre el destino de representación llamando al método [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="ab6c1-225">Llame al método SimpleText::D rawText, implementado en la parte 4.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="ab6c1-226">Llame al método [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="ab6c1-227">Si es necesario, descarte los recursos dependientes del dispositivo para que se puedan volver a crear cuando se vuelva a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



<span data-ttu-id="ab6c1-228">La clase SimpleText se implementa en SimpleText. h y SimpleText. cpp.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="ab6c1-229">Dibujar texto con varios formatos.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="ab6c1-230">En esta sección se muestra cómo usar [DirectWrite](direct-write-portal.md) y [Direct2D](../direct2d/direct2d-portal.md) para representar texto con varios formatos, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

![captura de pantalla de "Hello World Using directwrite!", con algunas partes en diferentes estilos, tamaños y formatos](images/multiformattedcropped.png)

<span data-ttu-id="ab6c1-232">El código de esta sección se implementa como la clase MultiformattedText en el [ejemplo DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="ab6c1-233">Se basa en los pasos de la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="ab6c1-234">Para crear texto con formato múltiple, se usa la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) además de la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) presentada en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="ab6c1-235">La interfaz **IDWriteTextLayout** describe el formato y el diseño de un bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="ab6c1-236">Además del formato predeterminado especificado por un objeto **IDWriteTextFormat** , el formato de los intervalos de texto específicos se puede cambiar mediante **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="ab6c1-237">Esto incluye el nombre de la familia de fuentes, el tamaño, el peso, el estilo, el ancho, el tachado y el subrayado.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="ab6c1-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) también proporciona métodos de prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="ab6c1-239">Las métricas de pruebas de posicionamiento devueltas por estos métodos son relativas al cuadro de diseño especificado cuando el objeto de interfaz **IDWriteTextLayout** se crea mediante el método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) de la interfaz [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="ab6c1-240">La interfaz [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) se usa para agregar características tipográficas de [OpenType](../intl/opentype-font-format.md) opcionales a un diseño de texto, como los caracteres floreados y los conjuntos de texto de estilo alternativos.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="ab6c1-241">Las características tipográficas se pueden agregar a un intervalo de texto específico dentro de un diseño de texto mediante una llamada al método [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) de la interfaz **IDWriteTypography** .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="ab6c1-242">Este método recibe una estructura de [**\_ \_ características de fuente DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) como un parámetro que contiene una constante de enumeración de etiquetas  de la **\_ \_ característica \_ de fuente DWRITE** y un parámetro de ejecución UINT32.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="ab6c1-243">Puede encontrar una lista de las características de OpenType registradas en el [registro de etiquetas de diseño OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) en Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="ab6c1-244">Para las constantes de enumeración de DirectWrite equivalentes, vea etiqueta de la **\_ característica de fuente \_ \_ DWRITE**.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="ab6c1-245">Parte 1: creación de una interfaz IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="ab6c1-246">Declare un puntero a una interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase MultiformattedText.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="ab6c1-247">Al final del método MultiformattedText:: CreateDeviceIndependentResources, cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="ab6c1-248">La interfaz **IDWriteTextLayout** proporciona características de formato adicionales, como la capacidad de aplicar distintos formatos a partes seleccionadas del texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="ab6c1-249">Parte 2: aplicar formato con IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="ab6c1-250">El formato, como el tamaño de fuente, el peso y el subrayado, se puede aplicar a las subcadenas del texto que se va a mostrar mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="ab6c1-251">Establezca el tamaño de fuente para la subcadena "di" de "DirectWrite" en 100 mediante la declaración de un [**\_ \_ intervalo de texto de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) y una llamada al método [**IDWriteTextLayout:: SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="ab6c1-252">Subraye la subcadena "DirectWrite" llamando al método [**IDWriteTextLayout:: SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="ab6c1-253">Establezca el espesor de la fuente en negrita para la subcadena "DirectWrite" llamando al método [**IDWriteTextLayout:: SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="ab6c1-254">Parte 3: agregar características tipográficas con IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="ab6c1-255">Declare y cree un objeto de interfaz [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) llamando al método [**IDWriteFactory:: CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="ab6c1-256">Agregue una característica de fuente declarando un objeto de [**\_ \_ característica de fuente DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) que tenga el estilo de estilo 7 especificado y llamando al método [**IDWriteTypography:: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="ab6c1-257">Establezca el diseño del texto para usar la tipografía sobre toda la cadena declarando una variable de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) y llamando al método [**IDWriteTextLayout:: SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) y pasando el intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="ab6c1-258">Establezca el nuevo ancho y alto para el objeto de diseño de texto en el método MultiformattedText:: OnResize.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="ab6c1-259">Parte 4: dibujar texto con el método DrawTextLayout de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="ab6c1-260">Para dibujar el texto con la configuración de diseño de texto especificada por el objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , cambie el código del método MultiformattedText::D rawtext para usar [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="ab6c1-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="ab6c1-261">Delcare una variable de [**D2D1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) y establézcala en el punto superior izquierdo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="ab6c1-262">Dibuje el texto en la pantalla llamando al método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) del destino de representación de [Direct2D](../direct2d/direct2d-portal.md) y pasando el puntero [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="ab6c1-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="ab6c1-263">La clase MultiformattedText se implementa en MultiformattedText. h y MultiformattedText. cpp.</span><span class="sxs-lookup"><span data-stu-id="ab6c1-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 