---
title: Ejemplo de diseño de cuadrícula
description: Muestra cómo usar la animación de Windows, utilizando Direct2D para animar una cuadrícula de imágenes.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "103789418"
---
# <a name="grid-layout-sample"></a><span data-ttu-id="c2970-103">Ejemplo de diseño de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="c2970-103">Grid Layout Sample</span></span>

<span data-ttu-id="c2970-104">Muestra cómo usar la animación de Windows, utilizando Direct2D para animar una cuadrícula de imágenes.</span><span class="sxs-lookup"><span data-stu-id="c2970-104">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c2970-105">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2970-105">Downloading the Sample</span></span>

<span data-ttu-id="c2970-106">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="c2970-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c2970-107">Location</span><span class="sxs-lookup"><span data-stu-id="c2970-107">Location</span></span>                               | <span data-ttu-id="c2970-108">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="c2970-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2970-109">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="c2970-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="c2970-110">Kit de desarrollo de software de Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="c2970-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="c2970-111">Galería de códigos</span><span class="sxs-lookup"><span data-stu-id="c2970-111">Code Gallery</span></span>                           | [<span data-ttu-id="c2970-112">Código de ejemplo del administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="c2970-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="c2970-113">Después de haber descargado e instalado el Windows SDK, encontrará los ejemplos en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="c2970-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="c2970-114">Por ejemplo, si usa la ruta de instalación predeterminada para el Windows SDK para Windows 7, los ejemplos se instalan en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="c2970-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c2970-115">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2970-115">Building the Sample</span></span>

<span data-ttu-id="c2970-116">Use uno de los métodos siguientes para compilar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c2970-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="c2970-117">**Para generar el ejemplo en el símbolo del sistema**</span><span class="sxs-lookup"><span data-stu-id="c2970-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="c2970-118">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto GridLayout.</span><span class="sxs-lookup"><span data-stu-id="c2970-118">Open the Command Prompt window and navigate to the GridLayout project directory.</span></span> <span data-ttu-id="c2970-119">Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ GridLayout</span><span class="sxs-lookup"><span data-stu-id="c2970-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\GridLayout</span></span>

2.  <span data-ttu-id="c2970-120">Ejecute el siguiente comando: **msbuild GridLayout. sln**</span><span class="sxs-lookup"><span data-stu-id="c2970-120">Run the following command: **msbuild GridLayout.sln**</span></span>

<span data-ttu-id="c2970-121">**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**</span><span class="sxs-lookup"><span data-stu-id="c2970-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="c2970-122">Abra el explorador de Windows y navegue hasta el directorio del proyecto GridLayout.</span><span class="sxs-lookup"><span data-stu-id="c2970-122">Open Windows Explorer and navigate to the GridLayout project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="c2970-123">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c2970-123">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c2970-124">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="c2970-124">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="c2970-125">Haga doble clic en el icono del archivo GridLayout. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c2970-125">Double-click the icon for the GridLayout.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="c2970-126">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="c2970-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c2970-127">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2970-127">Running the Sample</span></span>

<span data-ttu-id="c2970-128">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c2970-128">To run the sample:</span></span>

1.  <span data-ttu-id="c2970-129">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2970-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="c2970-130">Ejecute **GridLayout.exe** en el símbolo del sistema o haga doble clic en el icono de GridLayout.exe en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2970-130">Run **GridLayout.exe** at the command prompt, or double-click the icon for GridLayout.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="c2970-131">Las imágenes de ejemplo se cargan desde la biblioteca de imágenes.</span><span class="sxs-lookup"><span data-stu-id="c2970-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="c2970-132">Cambie el tamaño de la ventana y las imágenes se organizarán en una cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="c2970-132">Resize the window and the images will arrange themselves into a grid.</span></span>

 

 




