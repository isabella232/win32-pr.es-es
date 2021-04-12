---
title: Agregando el cerrar BUTTONELEMENT
description: Agregando el cerrar BUTTONELEMENT
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- crear máscaras, elemento BUTTONELEMENT
- Aspectos de Windows Media Player, elemento BUTTONELEMENT
- máscaras, elemento BUTTONELEMENT
- archivos de definición de máscara, elemento BUTTONELEMENT
- BUTTONELEMENT (elemento)
- elementos, BUTTONELEMENT
- crear máscaras, cerrar botones
- Aspectos de Windows Media Player, botones de cierre
- máscaras, botones de cierre
- archivos de definición de máscara, botones de cierre
- Botones cerrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268870"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="a44db-114">Agregando el cerrar BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="a44db-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="a44db-115">El botón Cerrar es similar en concepto al botón reproducir, pero tiene códigos y colores distintos.</span><span class="sxs-lookup"><span data-stu-id="a44db-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="a44db-116">Coloque el código **BUTTONELEMENT** de cierre después del corchete angular de cierre de la ejecución de **ButtonElement**.</span><span class="sxs-lookup"><span data-stu-id="a44db-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="a44db-117">Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón Cerrar:</span><span class="sxs-lookup"><span data-stu-id="a44db-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="a44db-118">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="a44db-118">**mappingColor**</span></span>

<span data-ttu-id="a44db-119">Este es el valor de color de la región en el archivo de imagen de asignación que creó antes.</span><span class="sxs-lookup"><span data-stu-id="a44db-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="a44db-120">En este caso, es el color rojo sólido.</span><span class="sxs-lookup"><span data-stu-id="a44db-120">In this case it is the solid red color.</span></span> <span data-ttu-id="a44db-121">Este atributo es necesario para cualquier **BUTTONELEMENT**.</span><span class="sxs-lookup"><span data-stu-id="a44db-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="a44db-122">Al definir este color, está indicando a Windows Media Player que asocie esta área de color con el código XML de este botón.</span><span class="sxs-lookup"><span data-stu-id="a44db-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="a44db-123">**Información sobre herramientas**</span><span class="sxs-lookup"><span data-stu-id="a44db-123">**upToolTip**</span></span>

<span data-ttu-id="a44db-124">Define el texto que se mostrará cuando el usuario mantenga el mouse sobre el botón.</span><span class="sxs-lookup"><span data-stu-id="a44db-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="a44db-125">Es lo mismo que el botón reproducir, salvo que tiene la etiqueta "cerrar".</span><span class="sxs-lookup"><span data-stu-id="a44db-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="a44db-126">**AlHacerClic**</span><span class="sxs-lookup"><span data-stu-id="a44db-126">**onClick**</span></span>

<span data-ttu-id="a44db-127">Define el evento que se produce cuando se hace clic con el mouse en el botón.</span><span class="sxs-lookup"><span data-stu-id="a44db-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="a44db-128">El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función de JScript en un archivo de texto externo cargado por el atributo **loadScript** de una **vista**.</span><span class="sxs-lookup"><span data-stu-id="a44db-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="a44db-129">En este caso, el código JScript llama al método **Close** del elemento **View** mediante la **vista** de atributos global, que cierra la vista y cierra Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a44db-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a44db-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a44db-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a44db-131">**Crear el archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="a44db-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




