---
title: Cambio de la propiedad del complemento DSP de audio de ejemplo
description: Cambio de la propiedad del complemento DSP de audio de ejemplo
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, propiedades de audio
- Complementos DSP, propiedades de audio
- Complementos DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777719"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="d18f0-108">Cambio de la propiedad del complemento DSP de audio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d18f0-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="d18f0-109">Probablemente querrá cambiar la propiedad que el Asistente para complementos de Windows Media Player crea de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d18f0-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="d18f0-110">En la siguiente lista se detallan los elementos que pueden requerir un cambio:</span><span class="sxs-lookup"><span data-stu-id="d18f0-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="d18f0-111">**El recurso de cuadro de diálogo.**</span><span class="sxs-lookup"><span data-stu-id="d18f0-111">**The dialog resource.**</span></span> <span data-ttu-id="d18f0-112">Haga clic en la pestaña **ResourceView** en la ventana área de trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d18f0-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="d18f0-113">Expanda la lista de carpetas para abrir la carpeta del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d18f0-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="d18f0-114">Haga doble clic en el recurso de cuadro de diálogo para abrir el editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="d18f0-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="d18f0-115">Puede realizar cambios en el cuadro de diálogo de la página de propiedades para satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="d18f0-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="d18f0-116">Por ejemplo, puede cambiar el texto de la etiqueta o reemplazar el control de edición por una casilla.</span><span class="sxs-lookup"><span data-stu-id="d18f0-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="d18f0-117">**Código del objeto de página de propiedades.**</span><span class="sxs-lookup"><span data-stu-id="d18f0-117">**The property page object code.**</span></span> <span data-ttu-id="d18f0-118">La implementación predeterminada usa una variable de tipo Double para almacenar el factor de escala.</span><span class="sxs-lookup"><span data-stu-id="d18f0-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="d18f0-119">Podría requerir un tipo de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="d18f0-119">You might require a different type of data.</span></span> <span data-ttu-id="d18f0-120">Esto también requeriría cambiar el código que conserva los datos en el registro y Lee los datos del registro (incluido el código que lee del registro en *CProjectName*::**FinalConstruct**).</span><span class="sxs-lookup"><span data-stu-id="d18f0-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="d18f0-121">**Variable miembro que almacena el valor de propiedad.**</span><span class="sxs-lookup"><span data-stu-id="d18f0-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="d18f0-122">Esta variable se denomina "m \_ fScaleFactor" y se declara como tipo Double.</span><span class="sxs-lookup"><span data-stu-id="d18f0-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="d18f0-123">Puede que desee cambiar el nombre y el tipo de esta variable en todo el proyecto.</span><span class="sxs-lookup"><span data-stu-id="d18f0-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="d18f0-124">**Los métodos GET y put de propiedad.**</span><span class="sxs-lookup"><span data-stu-id="d18f0-124">**The property get and property put methods.**</span></span> <span data-ttu-id="d18f0-125">Es posible que desee cambiar los nombres, los parámetros y las implementaciones de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d18f0-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="d18f0-126">No olvide también reflejar los cambios en otros lugares del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d18f0-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="d18f0-127">Por ejemplo, el método de **aplicación** de la página de propiedades llama a *CProjectName*::**Put \_ Scale**.</span><span class="sxs-lookup"><span data-stu-id="d18f0-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d18f0-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d18f0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d18f0-129">**Implementar un complemento de DSP de audio**</span><span class="sxs-lookup"><span data-stu-id="d18f0-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




