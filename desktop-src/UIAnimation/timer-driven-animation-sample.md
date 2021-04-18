---
title: Ejemplo de animación Timer-Driven
description: Muestra cómo usar la animación de Windows con el temporizador de animación, mientras que usa GDI+ para animar el color de fondo de una ventana.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "104358790"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="a22f0-103">Ejemplo de animación Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="a22f0-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="a22f0-104">Muestra cómo usar la animación de Windows con el temporizador de animación, mientras que usa GDI+ para animar el color de fondo de una ventana.</span><span class="sxs-lookup"><span data-stu-id="a22f0-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a22f0-105">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a22f0-105">Downloading the Sample</span></span>

<span data-ttu-id="a22f0-106">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="a22f0-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="a22f0-107">Location</span><span class="sxs-lookup"><span data-stu-id="a22f0-107">Location</span></span>                               | <span data-ttu-id="a22f0-108">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="a22f0-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22f0-109">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="a22f0-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="a22f0-110">Kit de desarrollo de software de Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="a22f0-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="a22f0-111">Galería de códigos</span><span class="sxs-lookup"><span data-stu-id="a22f0-111">Code Gallery</span></span>                           | [<span data-ttu-id="a22f0-112">Código de ejemplo del administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="a22f0-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="a22f0-113">Después de haber descargado e instalado el Windows SDK, encontrará los ejemplos en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="a22f0-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="a22f0-114">Por ejemplo, si usa la ruta de instalación predeterminada para el Windows SDK para Windows 7, los ejemplos se instalan en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="a22f0-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="a22f0-115">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a22f0-115">Building the Sample</span></span>

<span data-ttu-id="a22f0-116">Use uno de los métodos siguientes para compilar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a22f0-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="a22f0-117">**Para generar el ejemplo en el símbolo del sistema**</span><span class="sxs-lookup"><span data-stu-id="a22f0-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="a22f0-118">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="a22f0-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="a22f0-119">Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="a22f0-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="a22f0-120">Ejecute el siguiente comando: **msbuild TimerDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="a22f0-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="a22f0-121">**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**</span><span class="sxs-lookup"><span data-stu-id="a22f0-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="a22f0-122">Abra el explorador de Windows y navegue hasta el directorio del proyecto TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="a22f0-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="a22f0-123">Haga doble clic en el icono del archivo TimerDriven. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a22f0-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="a22f0-124">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a22f0-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="a22f0-125">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="a22f0-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="a22f0-126">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="a22f0-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a22f0-127">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a22f0-127">Running the Sample</span></span>

<span data-ttu-id="a22f0-128">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a22f0-128">To run the sample:</span></span>

1.  <span data-ttu-id="a22f0-129">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="a22f0-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="a22f0-130">Ejecute **TimerDriven.exe** en el símbolo del sistema o haga doble clic en el icono de TimerDriven.exe en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="a22f0-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="a22f0-131">Haga clic en cualquier parte del área cliente y el color de fondo de la ventana cambiará a un color aleatorio.</span><span class="sxs-lookup"><span data-stu-id="a22f0-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




