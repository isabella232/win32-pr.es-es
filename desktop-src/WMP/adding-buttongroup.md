---
title: Agregar BUTTONGROUP
description: Agregar BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- crear máscaras, elemento BUTTONGROUP
- Aspectos de Windows Media Player, elemento BUTTONGROUP
- aspectos, elemento BUTTONGROUP
- archivos de definición de máscara, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- elementos, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356873"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="9574d-109">Agregar BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="9574d-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="9574d-110">En este ejemplo se usa el elemento **BUTTONGROUP** para la codificación en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="9574d-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="9574d-111">**BUTTONGROUP** crea una manera fácil de procesar eventos del mouse sin tener que calcular ubicaciones exactas en la pantalla y utiliza el color en lugar de las coordenadas x e y.</span><span class="sxs-lookup"><span data-stu-id="9574d-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="9574d-112">En primer lugar, debe agregar las etiquetas **BUTTONGROUP** al archivo de definición de máscara que creó.</span><span class="sxs-lookup"><span data-stu-id="9574d-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="9574d-113">Colóquelos después de los atributos de la etiqueta de **tema** .</span><span class="sxs-lookup"><span data-stu-id="9574d-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="9574d-114">Deje unas cuantas líneas en blanco por encima de la etiqueta **BUTTONGROUP** de cierre para los botones que va a agregar a continuación.</span><span class="sxs-lookup"><span data-stu-id="9574d-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="9574d-115">Los atributos siguientes se usan para definir **BUTTONGROUP**:</span><span class="sxs-lookup"><span data-stu-id="9574d-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="9574d-116">**mappingImage**</span><span class="sxs-lookup"><span data-stu-id="9574d-116">**mappingImage**</span></span>

<span data-ttu-id="9574d-117">Este es el nombre de archivo del archivo de imagen de asignación que creó antes, el que tiene los círculos rojo y verde.</span><span class="sxs-lookup"><span data-stu-id="9574d-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="9574d-118">Este atributo es necesario para cualquier **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="9574d-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="9574d-119">**hoverImage**</span><span class="sxs-lookup"><span data-stu-id="9574d-119">**hoverImage**</span></span>

<span data-ttu-id="9574d-120">Este es el nombre de archivo del archivo de imagen emergente que ha creado antes, el que tiene los dos botones amarillos que leen "Play" y "CLOSE".</span><span class="sxs-lookup"><span data-stu-id="9574d-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="9574d-121">Esto no es necesario, pero una imagen de mantener el mouse ayuda a proporcionar comentarios al usuario.</span><span class="sxs-lookup"><span data-stu-id="9574d-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9574d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9574d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9574d-123">**Crear el archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="9574d-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




