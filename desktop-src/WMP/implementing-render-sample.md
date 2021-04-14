---
title: Implementación del ejemplo de representación
description: Implementación del ejemplo de representación
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualizaciones, muestra brillante
- visualizaciones personalizadas, ejemplo de resplandor
- Guía de programación, visualizaciones
- ejemplos, visualización de resplandor
- Ejemplo de visualización brillante
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, ejemplo Glow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533717"
---
# <a name="implementing-render-sample"></a><span data-ttu-id="a865d-111">Implementación del ejemplo de representación</span><span class="sxs-lookup"><span data-stu-id="a865d-111">Implementing Render Sample</span></span>

<span data-ttu-id="a865d-112">El código siguiente se usa para implementar la función de **representación** :</span><span class="sxs-lookup"><span data-stu-id="a865d-112">The following code is used to implement the **Render** function:</span></span>


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



<span data-ttu-id="a865d-113">A continuación se muestra una explicación del código:</span><span class="sxs-lookup"><span data-stu-id="a865d-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="a865d-114">Una variable denominada *ColorDelFondo* se usa para el color del resplandor y se declara con **COLORREF**.</span><span class="sxs-lookup"><span data-stu-id="a865d-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="a865d-115">Todos los colores deben usar el tipo de datos **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="a865d-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="a865d-116">Se utiliza una variable denominada *allevel* para la instantánea de nivel de onda de audio.</span><span class="sxs-lookup"><span data-stu-id="a865d-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="a865d-117">Este valor dependerá del nivel de energía real en el momento de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="a865d-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="a865d-118">La instrucción **Switch** se establece mediante el valor preestablecido que el usuario ha elegido en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a865d-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="a865d-119">La *opción establecerá el color deseado* (rojo, verde o azul).</span><span class="sxs-lookup"><span data-stu-id="a865d-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="a865d-120">Sin embargo, el color exacto lo determinará el nivel de energía de audio.</span><span class="sxs-lookup"><span data-stu-id="a865d-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="a865d-121">Por ejemplo, si se elige el valor preestablecido rojo, el color será un rojo sólido, pero será más claro o más oscuro en función de la forma de onda de audio en el momento de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="a865d-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="a865d-122">Asegúrese de usar la macro **RBG** para crear el color.</span><span class="sxs-lookup"><span data-stu-id="a865d-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="a865d-123">Se crea un pincel denominado *hNewBrush*, que se usa para rellenar el rectángulo *PRC* proporcionado por Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a865d-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="a865d-124">La superficie de dibujo es el contexto de dispositivo *HDC* proporcionado por Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a865d-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="a865d-125">El pincel se elimina mediante **DeleteObject**.</span><span class="sxs-lookup"><span data-stu-id="a865d-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="a865d-126">Asegúrese de eliminar siempre los lápices o pinceles que cree.</span><span class="sxs-lookup"><span data-stu-id="a865d-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="a865d-127">Una vez finalizado el código de **representación** , Windows Media Player mostrará los gráficos de *HDC* en una ventana determinada por la máscara que se está usando.</span><span class="sxs-lookup"><span data-stu-id="a865d-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a865d-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a865d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a865d-129">**El ejemplo de resplandor**</span><span class="sxs-lookup"><span data-stu-id="a865d-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




