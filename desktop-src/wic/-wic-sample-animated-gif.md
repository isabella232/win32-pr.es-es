---
description: En este ejemplo se muestra la descodificación de varios marcos en un archivo GIF, la lectura de los metadatos adecuados para cada fotograma, la composición de Marcos y la representación de la animación con Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Ejemplo de GIF animado de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105653296"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="2083b-103">Ejemplo de GIF animado de WIC</span><span class="sxs-lookup"><span data-stu-id="2083b-103">WIC animated GIF sample</span></span>

<span data-ttu-id="2083b-104">En este ejemplo se muestra la descodificación de varios marcos en un archivo GIF, la lectura de los metadatos adecuados para cada fotograma, la composición de Marcos y la representación de la animación con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2083b-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="2083b-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2083b-105">Requirements</span></span>

<span data-ttu-id="2083b-106">Este ejemplo tiene los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="2083b-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="2083b-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="2083b-107">Requirement</span></span> | <span data-ttu-id="2083b-108">Value</span><span class="sxs-lookup"><span data-stu-id="2083b-108">Value</span></span> |
|-|-|
| <span data-ttu-id="2083b-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2083b-109">Minimum supported client</span></span> | <span data-ttu-id="2083b-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2083b-110">Windows 7</span></span> |
| <span data-ttu-id="2083b-111">Windows SDK mínimo</span><span class="sxs-lookup"><span data-stu-id="2083b-111">Minimum Windows SDK</span></span> | <span data-ttu-id="2083b-112">[Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7</span><span class="sxs-lookup"><span data-stu-id="2083b-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="2083b-113">Descarga del ejemplo</span><span class="sxs-lookup"><span data-stu-id="2083b-113">Downloading the sample</span></span>

<span data-ttu-id="2083b-114">Este ejemplo está disponible en [GIF animado de WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span><span class="sxs-lookup"><span data-stu-id="2083b-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="2083b-115">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2083b-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="2083b-116">Usar Visual Studio (método preferido)</span><span class="sxs-lookup"><span data-stu-id="2083b-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="2083b-117">Abra el Explorador de Windows y vaya al directorio.</span><span class="sxs-lookup"><span data-stu-id="2083b-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="2083b-118">Haga doble clic en el icono del archivo. sln (solución) para abrir el archivo en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2083b-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="2083b-119">En el menú **Compilar**, seleccione **Compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="2083b-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="2083b-120">La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2083b-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="2083b-121">Uso del símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="2083b-121">Using the command prompt</span></span>

<span data-ttu-id="2083b-122">Para generar el ejemplo mediante un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="2083b-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="2083b-123">Abra el símbolo del sistema y navegue hasta el directorio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2083b-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="2083b-124">Escriba `msbuild WICAnimatedGif.sln`</span><span class="sxs-lookup"><span data-stu-id="2083b-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2083b-125">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="2083b-125">Running the sample</span></span>

<span data-ttu-id="2083b-126">Una vez iniciada la aplicación, cargue un archivo de imagen con el comando **abrir** del menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="2083b-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="2083b-127">Se admite el cambio de tamaño de las ventanas.</span><span class="sxs-lookup"><span data-stu-id="2083b-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="2083b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2083b-128">See also</span></span>

[<span data-ttu-id="2083b-129">Códec de procesamiento de imágenes de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="2083b-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="2083b-130">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="2083b-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="2083b-131">Referencia</span><span class="sxs-lookup"><span data-stu-id="2083b-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="2083b-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="2083b-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="2083b-133">Ejemplos y ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="2083b-133">Samples and code examples</span></span>](-wic-samples.md)
