---
title: Ejemplo de interpolador personalizado
description: Muestra cómo usar la animación de Windows con su propio interpolador personalizado, con Direct2D usado para la representación.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "104149150"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="37c66-103">Ejemplo de interpolador personalizado</span><span class="sxs-lookup"><span data-stu-id="37c66-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="37c66-104">Muestra cómo usar la animación de Windows con su propio interpolador personalizado, con Direct2D usado para la representación.</span><span class="sxs-lookup"><span data-stu-id="37c66-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="37c66-105">Las imágenes de ejemplo se cargan desde la biblioteca de imágenes.</span><span class="sxs-lookup"><span data-stu-id="37c66-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="37c66-106">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37c66-106">Downloading the Sample</span></span>

<span data-ttu-id="37c66-107">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="37c66-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="37c66-108">Location</span><span class="sxs-lookup"><span data-stu-id="37c66-108">Location</span></span>                               | <span data-ttu-id="37c66-109">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="37c66-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c66-110">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="37c66-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="37c66-111">Kit de desarrollo de software de Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="37c66-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="37c66-112">Galería de códigos</span><span class="sxs-lookup"><span data-stu-id="37c66-112">Code Gallery</span></span>                           | [<span data-ttu-id="37c66-113">Código de ejemplo del administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="37c66-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="37c66-114">Después de haber descargado e instalado el Windows SDK, encontrará los ejemplos en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="37c66-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="37c66-115">Por ejemplo, si usa la ruta de instalación predeterminada para el Windows SDK para Windows 7, los ejemplos se instalan en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="37c66-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="37c66-116">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37c66-116">Building the Sample</span></span>

<span data-ttu-id="37c66-117">Use uno de los métodos siguientes para compilar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="37c66-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="37c66-118">**Para generar el ejemplo en el símbolo del sistema**</span><span class="sxs-lookup"><span data-stu-id="37c66-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="37c66-119">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="37c66-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="37c66-120">Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ CustomInterpolator</span><span class="sxs-lookup"><span data-stu-id="37c66-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="37c66-121">Ejecute el siguiente comando: **msbuild CustomInterpolator. sln**</span><span class="sxs-lookup"><span data-stu-id="37c66-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="37c66-122">**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**</span><span class="sxs-lookup"><span data-stu-id="37c66-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="37c66-123">Abra el explorador de Windows y navegue hasta el directorio del proyecto CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="37c66-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="37c66-124">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="37c66-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="37c66-125">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="37c66-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="37c66-126">Haga doble clic en el icono del archivo CustomInterpolator. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37c66-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="37c66-127">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="37c66-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="37c66-128">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37c66-128">Running the Sample</span></span>

<span data-ttu-id="37c66-129">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="37c66-129">To run the sample:</span></span>

1.  <span data-ttu-id="37c66-130">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="37c66-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="37c66-131">Ejecute **CustomInterpolator.exe** en el símbolo del sistema o haga doble clic en el icono de CustomInterpolator.exe en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="37c66-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="37c66-132">Cambie el tamaño de la ventana o presione la barra espaciadora, y las imágenes se organizarán de forma aleatoria en el centro del área cliente.</span><span class="sxs-lookup"><span data-stu-id="37c66-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="37c66-133">Presione la flecha arriba o abajo para que las imágenes se aceleren hacia la parte superior o inferior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="37c66-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 




