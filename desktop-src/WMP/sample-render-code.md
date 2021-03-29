---
title: Código de representación de ejemplo
description: Código de representación de ejemplo
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizaciones, código de ejemplo
- visualizaciones personalizadas, código de ejemplo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, código de ejemplo
- ejemplos, función Render para visualizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075964"
---
# <a name="sample-render-code"></a><span data-ttu-id="b918e-109">Código de representación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b918e-109">Sample Render Code</span></span>

<span data-ttu-id="b918e-110">Este es un código de ejemplo que usa la función **Render** para dibujar una línea a través de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b918e-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="b918e-111">El alto de la línea se define mediante el valor de la forma de onda.</span><span class="sxs-lookup"><span data-stu-id="b918e-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="b918e-112">La función de **representación** es donde tiene lugar el trabajo principal del código.</span><span class="sxs-lookup"><span data-stu-id="b918e-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="b918e-113">Cada vez que Windows Media Player toma una instantánea del audio, llamará a esta función y el código se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="b918e-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="b918e-114">Este código realiza las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="b918e-114">This code performs the following tasks.</span></span> <span data-ttu-id="b918e-115">Consulte el SDK de la plataforma Microsoft Windows para Windows de 32 bits para obtener más detalles sobre funciones específicas.</span><span class="sxs-lookup"><span data-stu-id="b918e-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="b918e-116">Crear objetos</span><span class="sxs-lookup"><span data-stu-id="b918e-116">Creating Objects</span></span>

<span data-ttu-id="b918e-117">Normalmente, se usarán las funciones de dibujo que se incorporan a la interfaz gráfica de visualización de Microsoft Windows (GDI).</span><span class="sxs-lookup"><span data-stu-id="b918e-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="b918e-118">Debe crear lápices para dibujar líneas y pinceles para rellenar áreas.</span><span class="sxs-lookup"><span data-stu-id="b918e-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="b918e-119">Se crea un pincel negro sólido para rellenar el fondo.</span><span class="sxs-lookup"><span data-stu-id="b918e-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="b918e-120">Se crea un lápiz sólido para dibujar una línea.</span><span class="sxs-lookup"><span data-stu-id="b918e-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="b918e-121">El color será el color de primer plano tal como lo define la máscara que va a mostrar la visualización.</span><span class="sxs-lookup"><span data-stu-id="b918e-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="b918e-122">Agregar el objeto al controlador de dominio</span><span class="sxs-lookup"><span data-stu-id="b918e-122">Adding the Object to the DC</span></span>

<span data-ttu-id="b918e-123">Debe agregar el lápiz al contexto de dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="b918e-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="b918e-124">El controlador de dominio es la parte de la memoria en la que se almacenan todos los datos y objetos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="b918e-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="b918e-125">Esencialmente, el controlador de dominio es el administrador de tráfico de Windows que realiza un seguimiento de todo el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b918e-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="b918e-126">Debe *convertir* el objeto Pen que creó y almacenarlo como un lápiz antiguo.</span><span class="sxs-lookup"><span data-stu-id="b918e-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="b918e-127">Use esta técnica de codificación para todos los lápices nuevos.</span><span class="sxs-lookup"><span data-stu-id="b918e-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="b918e-128">Esta técnica es necesaria para la programación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b918e-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="b918e-129">Rellenar el fondo</span><span class="sxs-lookup"><span data-stu-id="b918e-129">Filling in the Background</span></span>

<span data-ttu-id="b918e-130">Ahora está listo para dibujar.</span><span class="sxs-lookup"><span data-stu-id="b918e-130">You now are ready to draw.</span></span> <span data-ttu-id="b918e-131">La función **FillRect** llenará el rectángulo de la ventana, tal como se define en los parámetros de la función de **representación** .</span><span class="sxs-lookup"><span data-stu-id="b918e-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="b918e-132">El rectángulo se rellena con un pincel negro.</span><span class="sxs-lookup"><span data-stu-id="b918e-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="b918e-133">Obtención de datos de audio</span><span class="sxs-lookup"><span data-stu-id="b918e-133">Getting Audio Data</span></span>

<span data-ttu-id="b918e-134">A continuación, el código obtiene algunos datos de audio de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b918e-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="b918e-135">Mediante el uso de la matriz de forma de onda, puede obtener el valor actual de la energía de audio en el momento en que se tomó la instantánea.</span><span class="sxs-lookup"><span data-stu-id="b918e-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="b918e-136">En este caso, va a tomar los datos de audio del canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="b918e-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="b918e-137">El primer valor de la matriz es el primer 1024th de la instantánea de la alimentación de audio.</span><span class="sxs-lookup"><span data-stu-id="b918e-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="b918e-138">Esta información se usará para mostrar una línea cuyo alto coincida con la instantánea de la alimentación de audio.</span><span class="sxs-lookup"><span data-stu-id="b918e-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="b918e-139">Dibujar la línea</span><span class="sxs-lookup"><span data-stu-id="b918e-139">Draw the Line</span></span>

<span data-ttu-id="b918e-140">La línea se dibuja de izquierda a derecha mediante las funciones GDI **MoveToEx** y **lineTo** .</span><span class="sxs-lookup"><span data-stu-id="b918e-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="b918e-141">En primer lugar, mueva el lápiz al punto inicial.</span><span class="sxs-lookup"><span data-stu-id="b918e-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="b918e-142">En este caso, x e y se usan para definir los valores de izquierda a derecha y de arriba a abajo que el usuario verá en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b918e-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="b918e-143">X se define mediante el rectángulo PRC y, en concreto, por el valor de PRC->izquierda.</span><span class="sxs-lookup"><span data-stu-id="b918e-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="b918e-144">Y se define como el valor de los datos de la forma de onda en ese momento.</span><span class="sxs-lookup"><span data-stu-id="b918e-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="b918e-145">A continuación, dibuje una línea en el otro lado de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b918e-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="b918e-146">El punto al que se dibuja la línea es de nuevo un valor x, y.</span><span class="sxs-lookup"><span data-stu-id="b918e-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="b918e-147">X se define mediante el rectángulo PRC, pero esta vez por PRC->a la derecha.</span><span class="sxs-lookup"><span data-stu-id="b918e-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="b918e-148">Y sigue estando definido por los datos de la forma de onda y es el mismo que el punto desde el que se inició, porque está dibujando una línea recta de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="b918e-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="b918e-149">Limpie todo</span><span class="sxs-lookup"><span data-stu-id="b918e-149">Clean up Everything</span></span>

<span data-ttu-id="b918e-150">Debe eliminar los objetos que cree.</span><span class="sxs-lookup"><span data-stu-id="b918e-150">You must delete the objects you create.</span></span> <span data-ttu-id="b918e-151">En concreto, debe eliminar todos los pinceles y lápices que cree.</span><span class="sxs-lookup"><span data-stu-id="b918e-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="b918e-152">Es recomendable eliminar lápices y pinceles cuando termine de utilizarlos.</span><span class="sxs-lookup"><span data-stu-id="b918e-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="b918e-153">Si no Los elimina antes de finalizar la implementación de la función de **representación** , la visualización se bloqueará en un minuto o menos.</span><span class="sxs-lookup"><span data-stu-id="b918e-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="b918e-154">Debe mantener un recuento de los lápices y pinceles y destruir cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="b918e-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="b918e-155">Tenga especial cuidado de no crear lápices dentro de un bucle de código.</span><span class="sxs-lookup"><span data-stu-id="b918e-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="b918e-156">Use la técnica de codificación que se proporciona en el ejemplo para destruir los lápices y los pinceles.</span><span class="sxs-lookup"><span data-stu-id="b918e-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="b918e-157">**Importante** Destruya sus lápices y pinceles.</span><span class="sxs-lookup"><span data-stu-id="b918e-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="b918e-158">Cuando haya terminado de limpiar, asegúrese de volver a ser \_ correcto para que Windows Media Player sepa que ha terminado de dibujar.</span><span class="sxs-lookup"><span data-stu-id="b918e-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="b918e-159">Una vez que termine, el dibujo se transferirá a la ventana, se tomará otra instantánea, la **representación** le pedirá que vuelva a dibujar el código, etc.</span><span class="sxs-lookup"><span data-stu-id="b918e-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b918e-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b918e-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b918e-161">**Implementación de render**</span><span class="sxs-lookup"><span data-stu-id="b918e-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




