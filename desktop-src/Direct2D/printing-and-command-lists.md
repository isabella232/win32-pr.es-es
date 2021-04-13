---
title: Impresión y listas de comandos
description: El control de impresión de Direct2D \ 32; es un componente nuevo en el módulo de Direct2D en Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420837"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="222af-103">Impresión y listas de comandos</span><span class="sxs-lookup"><span data-stu-id="222af-103">Printing and command lists</span></span>

<span data-ttu-id="222af-104">El [](./direct2d-portal.md) [**control de impresión**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) de direct2d es un nuevo componente del módulo de direct2d en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="222af-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="222af-105">Este componente permite a las aplicaciones de Direct2D volver a usar las llamadas de dibujo de Direct2D (en términos de cambios de estado y primitivas de representación) para proporcionar resultados de impresión similares a lo que se ve en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="222af-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="222af-106">La interfaz [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) representa un trabajo de impresión virtual: puede crear un control de impresión de [direct2d](./direct2d-portal.md) para iniciar un nuevo trabajo de impresión, pasar el contenido de direct2d para cada página que desee imprimir y, a continuación, cerrar el control de impresión para completar un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="222af-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="222af-107">Un control de impresión se asigna a uno y exactamente un trabajo de impresión, y no se puede volver a usar.</span><span class="sxs-lookup"><span data-stu-id="222af-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="222af-108">El control de impresión de [direct2d](./direct2d-portal.md) convierte y optimiza el contenido pasado en direct2d para el subsistema de impresión, que funciona con las impresoras reales para proporcionar la copia impresa real.</span><span class="sxs-lookup"><span data-stu-id="222af-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="222af-109">Todos los detalles específicos de la impresión se ocultan de las aplicaciones de Direct2D, lo que significa que las aplicaciones de Direct2D pueden imprimir sin saber qué dispositivos están dibujando o cómo se traducen los dibujos a la impresión.</span><span class="sxs-lookup"><span data-stu-id="222af-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="222af-110">Para imprimir con [Direct2D](./direct2d-portal.md), debe preparar una lista de comandos de direct2d para cada página que desee imprimir y, a continuación, pasar esa lista de comandos al control de impresión de direct2d.</span><span class="sxs-lookup"><span data-stu-id="222af-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="222af-111">Para preparar esa lista de comandos de Direct2D, solo tiene que crear y establecer una lista de comandos como destino de dibujo del contexto de dispositivo actual y, a continuación, dibujar en ese contexto de dispositivo, exactamente igual que si se dibuja en un destino de mapa de bits para su presentación.</span><span class="sxs-lookup"><span data-stu-id="222af-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="222af-112">Consulte [dispositivos y contextos de dispositivo](devices-and-device-contexts.md) para obtener más información sobre los dispositivos y los destinos.</span><span class="sxs-lookup"><span data-stu-id="222af-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="222af-113">En este diagrama se muestra la interacción entre la aplicación, el contexto de dispositivo, el destino de mapa de bits, el destino de la lista de comandos y el control de impresión.</span><span class="sxs-lookup"><span data-stu-id="222af-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="222af-114">Los componentes de impresora y Sub-System de impresión de Windows están en gris porque están totalmente ocultos en las aplicaciones de [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="222af-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![un diagrama que muestra cómo interactúan commandlist e Printing con una aplicación y direct2d.](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="222af-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="222af-116">Example</span></span>

<span data-ttu-id="222af-117">El proceso completo de imprimir contenido de Direct2D incluye los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="222af-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="222af-118">Cree un control de impresión para iniciar un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="222af-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="222af-119">Agregue una página al control de impresión pasando una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="222af-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="222af-120">Repita el paso 2 para cada página del resto del documento.</span><span class="sxs-lookup"><span data-stu-id="222af-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="222af-121">Cierre el control de impresión para completar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="222af-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="222af-122">Este es un ejemplo de código que muestra el proceso.</span><span class="sxs-lookup"><span data-stu-id="222af-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="222af-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="222af-123">Related topics</span></span>

[<span data-ttu-id="222af-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="222af-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="222af-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="222af-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="222af-126">Mejorar el rendimiento de las aplicaciones y la impresión en Direct2D</span><span class="sxs-lookup"><span data-stu-id="222af-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)