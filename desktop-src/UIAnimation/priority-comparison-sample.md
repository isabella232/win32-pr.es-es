---
title: Ejemplo de comparación de prioridades
description: Muestra cómo usar la animación de Windows con su propia comparación de prioridad mediante Direct2D para la representación.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "104149149"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="45fd3-103">Ejemplo de comparación de prioridades</span><span class="sxs-lookup"><span data-stu-id="45fd3-103">Priority Comparison Sample</span></span>

<span data-ttu-id="45fd3-104">Muestra cómo usar la animación de Windows con su propia comparación de prioridad mediante Direct2D para la representación.</span><span class="sxs-lookup"><span data-stu-id="45fd3-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="45fd3-105">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="45fd3-105">Downloading the Sample</span></span>

<span data-ttu-id="45fd3-106">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="45fd3-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="45fd3-107">Location</span><span class="sxs-lookup"><span data-stu-id="45fd3-107">Location</span></span>                               | <span data-ttu-id="45fd3-108">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="45fd3-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fd3-109">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="45fd3-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="45fd3-110">Kit de desarrollo de software de Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="45fd3-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="45fd3-111">Galería de códigos</span><span class="sxs-lookup"><span data-stu-id="45fd3-111">Code Gallery</span></span>                           | [<span data-ttu-id="45fd3-112">Código de ejemplo del administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="45fd3-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="45fd3-113">Después de haber descargado e instalado el Windows SDK, encontrará los ejemplos en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="45fd3-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="45fd3-114">Por ejemplo, si usa la ruta de instalación predeterminada para el Windows SDK para Windows 7, los ejemplos se instalan en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="45fd3-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="45fd3-115">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="45fd3-115">Building the Sample</span></span>

<span data-ttu-id="45fd3-116">Use uno de los métodos siguientes para compilar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45fd3-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="45fd3-117">**Para generar el ejemplo en el símbolo del sistema**</span><span class="sxs-lookup"><span data-stu-id="45fd3-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="45fd3-118">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="45fd3-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="45fd3-119">Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="45fd3-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="45fd3-120">Ejecute el siguiente comando: **msbuild PriorityComparison. sln**</span><span class="sxs-lookup"><span data-stu-id="45fd3-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="45fd3-121">**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**</span><span class="sxs-lookup"><span data-stu-id="45fd3-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="45fd3-122">Abra el explorador de Windows y navegue hasta el directorio del proyecto PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="45fd3-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="45fd3-123">Haga doble clic en el icono del archivo PriorityComparison. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="45fd3-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="45fd3-124">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="45fd3-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="45fd3-125">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="45fd3-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="45fd3-126">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="45fd3-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="45fd3-127">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="45fd3-127">Running the Sample</span></span>

<span data-ttu-id="45fd3-128">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="45fd3-128">To run the sample:</span></span>

1.  <span data-ttu-id="45fd3-129">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="45fd3-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="45fd3-130">Ejecute **PriorityComparison.exe** en el símbolo del sistema o haga doble clic en el icono de PriorityComparison.exe en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="45fd3-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="45fd3-131">Las imágenes de ejemplo se cargan desde la biblioteca de imágenes.</span><span class="sxs-lookup"><span data-stu-id="45fd3-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="45fd3-132">Cambie el tamaño de la ventana o presione la barra espaciadora y las imágenes se moverán al centro.</span><span class="sxs-lookup"><span data-stu-id="45fd3-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="45fd3-133">Use las teclas de flecha izquierda y derecha para seleccionar distintas imágenes (cuanto más rápido se presiona la tecla más rápido cambiará la selección).</span><span class="sxs-lookup"><span data-stu-id="45fd3-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="45fd3-134">Use las teclas de flecha arriba y abajo para crear una onda a través de las imágenes (cuanto más rápido se presiona la tecla, más rápida es la onda).</span><span class="sxs-lookup"><span data-stu-id="45fd3-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 




