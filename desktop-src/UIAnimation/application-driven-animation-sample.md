---
title: Ejemplo de animación Application-Driven
description: Muestra la animación de Windows en la configuración controlada por aplicaciones mediante Direct2D para animar el color de fondo de una ventana y sincronizar con la frecuencia de actualización.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "105685688"
---
# <a name="application-driven-animation-sample"></a><span data-ttu-id="c8d8f-103">Ejemplo de animación Application-Driven</span><span class="sxs-lookup"><span data-stu-id="c8d8f-103">Application-Driven Animation Sample</span></span>

<span data-ttu-id="c8d8f-104">Muestra la animación de Windows en la configuración controlada por aplicaciones mediante Direct2D para animar el color de fondo de una ventana y sincronizar con la frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-104">Shows Windows Animation in the application-driven configuration by using Direct2D to animate the background color of a window and syncing to the refresh rate.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c8d8f-105">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8d8f-105">Downloading the Sample</span></span>

<span data-ttu-id="c8d8f-106">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c8d8f-107">Location</span><span class="sxs-lookup"><span data-stu-id="c8d8f-107">Location</span></span>                               | <span data-ttu-id="c8d8f-108">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="c8d8f-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d8f-109">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="c8d8f-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="c8d8f-110">Kit de desarrollo de software de Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="c8d8f-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="c8d8f-111">Galería de códigos</span><span class="sxs-lookup"><span data-stu-id="c8d8f-111">Code Gallery</span></span>                           | [<span data-ttu-id="c8d8f-112">Código de ejemplo del administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="c8d8f-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="c8d8f-113">Después de haber descargado e instalado el Windows SDK, encontrará los ejemplos en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="c8d8f-114">Por ejemplo, si usa la ruta de instalación predeterminada para el Windows SDK para Windows 7, los ejemplos se instalan en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c8d8f-115">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8d8f-115">Building the Sample</span></span>

<span data-ttu-id="c8d8f-116">Use uno de los métodos siguientes para compilar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="c8d8f-117">**Para generar el ejemplo en el símbolo del sistema**</span><span class="sxs-lookup"><span data-stu-id="c8d8f-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="c8d8f-118">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto AppDriven.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-118">Open the Command Prompt window and navigate to the AppDriven project directory.</span></span> <span data-ttu-id="c8d8f-119">Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ AppDriven.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\AppDriven.</span></span>

2.  <span data-ttu-id="c8d8f-120">Ejecute el siguiente comando: **msbuild AppDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="c8d8f-120">Run the following command: **msbuild AppDriven.sln**</span></span>

<span data-ttu-id="c8d8f-121">**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**</span><span class="sxs-lookup"><span data-stu-id="c8d8f-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="c8d8f-122">Abra el explorador de Windows y navegue hasta el directorio del proyecto AppDriven.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-122">Open Windows Explorer and navigate to the AppDriven project directory.</span></span>

2.  <span data-ttu-id="c8d8f-123">Haga doble clic en el icono del archivo AppDriven. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-123">Double-click the icon for the AppDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="c8d8f-124">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c8d8f-125">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="c8d8f-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="c8d8f-126">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c8d8f-127">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8d8f-127">Running the Sample</span></span>

<span data-ttu-id="c8d8f-128">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c8d8f-128">To run the sample:</span></span>

1.  <span data-ttu-id="c8d8f-129">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="c8d8f-130">Ejecute **AppDriven.exe** en el símbolo del sistema o haga doble clic en el icono de AppDriven.exe en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-130">Run **AppDriven.exe** at the command prompt, or double-click the icon for AppDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="c8d8f-131">Haga clic en cualquier parte del área cliente y el color de fondo de la ventana cambiará a un color aleatorio.</span><span class="sxs-lookup"><span data-stu-id="c8d8f-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




