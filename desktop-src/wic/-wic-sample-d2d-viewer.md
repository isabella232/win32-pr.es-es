---
description: En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar un archivo de imagen y Direct2D para representar la imagen en la pantalla.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visor de imágenes WIC con el ejemplo de Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105653295"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="fa0bc-103">Visor de imágenes WIC con el ejemplo de Direct2D</span><span class="sxs-lookup"><span data-stu-id="fa0bc-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="fa0bc-104">En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar un archivo de imagen y Direct2D para representar la imagen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0bc-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa0bc-105">Requirements</span></span>

<span data-ttu-id="fa0bc-106">Este ejemplo tiene los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="fa0bc-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa0bc-107">Requirement</span></span> | <span data-ttu-id="fa0bc-108">Value</span><span class="sxs-lookup"><span data-stu-id="fa0bc-108">Value</span></span> |
|-|-|
| <span data-ttu-id="fa0bc-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa0bc-109">Minimum supported client</span></span> | <span data-ttu-id="fa0bc-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa0bc-110">Windows Vista</span></span> |
| <span data-ttu-id="fa0bc-111">Windows SDK mínimo</span><span class="sxs-lookup"><span data-stu-id="fa0bc-111">Minimum Windows SDK</span></span> | <span data-ttu-id="fa0bc-112">[Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa0bc-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="fa0bc-113">Descarga del ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa0bc-113">Downloading the sample</span></span>

<span data-ttu-id="fa0bc-114">Este ejemplo está disponible en el [visor de WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span><span class="sxs-lookup"><span data-stu-id="fa0bc-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="fa0bc-115">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa0bc-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="fa0bc-116">Usar Visual Studio (método preferido)</span><span class="sxs-lookup"><span data-stu-id="fa0bc-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="fa0bc-117">Abra el Explorador de Windows y vaya al directorio.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="fa0bc-118">Haga doble clic en el icono del archivo. sln (solución) para abrir el archivo en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="fa0bc-119">En el menú **Compilar**, seleccione **Compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="fa0bc-120">La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="fa0bc-121">Uso del símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="fa0bc-121">Using the command prompt</span></span>

<span data-ttu-id="fa0bc-122">Para compilar el ejemplo mediante un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="fa0bc-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="fa0bc-123">Abra una ventana del símbolo del sistema y navegue hasta el directorio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fa0bc-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="fa0bc-124">Escriba `msbuild WICViewerD2D.sln`</span><span class="sxs-lookup"><span data-stu-id="fa0bc-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="fa0bc-125">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa0bc-125">Running the sample</span></span>

<span data-ttu-id="fa0bc-126">Una vez iniciada la aplicación, cargue un archivo de imagen con el comando **abrir** del menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="fa0bc-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa0bc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa0bc-127">See also</span></span>

[<span data-ttu-id="fa0bc-128">Códec de procesamiento de imágenes de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="fa0bc-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="fa0bc-129">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="fa0bc-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="fa0bc-130">Referencia</span><span class="sxs-lookup"><span data-stu-id="fa0bc-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="fa0bc-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="fa0bc-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="fa0bc-132">Ejemplos y ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="fa0bc-132">Samples and code examples</span></span>](-wic-samples.md)
