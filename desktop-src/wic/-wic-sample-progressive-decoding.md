---
description: En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar una imagen codificada con niveles progresivos.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Ejemplo de descodificación progresiva de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718593"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="e2955-103">Ejemplo de descodificación progresiva de WIC</span><span class="sxs-lookup"><span data-stu-id="e2955-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="e2955-104">En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar una imagen codificada con niveles progresivos.</span><span class="sxs-lookup"><span data-stu-id="e2955-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="e2955-105">En este ejemplo se usa Direct2D para representar los distintos niveles progresivos en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e2955-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2955-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2955-106">Requirements</span></span>

<span data-ttu-id="e2955-107">Este ejemplo tiene los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="e2955-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="e2955-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2955-108">Requirement</span></span> | <span data-ttu-id="e2955-109">Value</span><span class="sxs-lookup"><span data-stu-id="e2955-109">Value</span></span> |
|-|
| <span data-ttu-id="e2955-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2955-110">Minimum supported client</span></span> | <span data-ttu-id="e2955-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2955-111">Windows 7</span></span> |
| <span data-ttu-id="e2955-112">Windows SDK mínimo</span><span class="sxs-lookup"><span data-stu-id="e2955-112">Minimum Windows SDK</span></span> | <span data-ttu-id="e2955-113">[Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2955-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="e2955-114">Descarga del ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2955-114">Downloading the sample</span></span>

<span data-ttu-id="e2955-115">Este ejemplo está disponible en la [codificación progresiva de WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span><span class="sxs-lookup"><span data-stu-id="e2955-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="e2955-116">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2955-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="e2955-117">Usar Visual Studio (método preferido)</span><span class="sxs-lookup"><span data-stu-id="e2955-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="e2955-118">Abra el Explorador de Windows y vaya al directorio.</span><span class="sxs-lookup"><span data-stu-id="e2955-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="e2955-119">Haga doble clic en el icono del archivo. sln (solución) para abrir el archivo en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e2955-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="e2955-120">En el menú Compilar, seleccione Compilar solución.</span><span class="sxs-lookup"><span data-stu-id="e2955-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="e2955-121">La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e2955-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="e2955-122">Uso del símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="e2955-122">Using the command prompt</span></span>

<span data-ttu-id="e2955-123">Para compilar el ejemplo mediante el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2955-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="e2955-124">Abra el símbolo del sistema y navegue hasta el directorio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e2955-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="e2955-125">Escriba `msbuild WICProgressiveDecoding.sln`</span><span class="sxs-lookup"><span data-stu-id="e2955-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e2955-126">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2955-126">Running the sample</span></span>

<span data-ttu-id="e2955-127">Una vez iniciada la aplicación, cargue un archivo de imagen a través del menú archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="e2955-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="e2955-128">Al cargar, el nivel progresivo predeterminado se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="e2955-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="e2955-129">Puede desplazarse a distintos niveles progresivos, ya sea a través del menú o de la tecla arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="e2955-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="e2955-130">El texto de nivel progresivo actual se muestra en la barra de estado de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="e2955-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="e2955-131">Se admite el cambio de tamaño de las ventanas.</span><span class="sxs-lookup"><span data-stu-id="e2955-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="e2955-132">La descodificación progresiva solo está disponible para las imágenes que se han codificado progresivamente.</span><span class="sxs-lookup"><span data-stu-id="e2955-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="e2955-133">La imagen proporcionada con este ejemplo se ha codificado progresivamente.</span><span class="sxs-lookup"><span data-stu-id="e2955-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2955-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2955-134">See also</span></span>

[<span data-ttu-id="e2955-135">Códec de procesamiento de imágenes de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="e2955-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="e2955-136">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="e2955-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="e2955-137">Referencia</span><span class="sxs-lookup"><span data-stu-id="e2955-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="e2955-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="e2955-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="e2955-139">Ejemplos y ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="e2955-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="e2955-140">Información general sobre descodificación progresiva</span><span class="sxs-lookup"><span data-stu-id="e2955-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
