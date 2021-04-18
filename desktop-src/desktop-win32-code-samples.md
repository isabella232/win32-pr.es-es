---
title: Ejemplos de código Win32 de escritorio
description: Acerca de los ejemplos repositorios para Win32 y cómo buscar en ellos.
ms.topic: article
ms.date: 03/19/2021
ms.openlocfilehash: 5a4083697d444f36b31c553a2d6159d4370565d4
ms.sourcegitcommit: 46e75903326c49a6c5cc576ee2b4f67f64a6d5ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105721569"
---
# <a name="desktop-win32-code-samples"></a><span data-ttu-id="d6a4b-103">Ejemplos de código Win32 de escritorio</span><span class="sxs-lookup"><span data-stu-id="d6a4b-103">Desktop Win32 code samples</span></span>

<span data-ttu-id="d6a4b-104">Vea también [ejemplos de código](https://developer.microsoft.com/windows/samples/).</span><span class="sxs-lookup"><span data-stu-id="d6a4b-104">Also see [Code samples](https://developer.microsoft.com/windows/samples/).</span></span>

## <a name="find-a-sample-for-the-api-youre-interested-in"></a><span data-ttu-id="d6a4b-105">Busque un ejemplo de la API que le interese</span><span class="sxs-lookup"><span data-stu-id="d6a4b-105">Find a sample for the API you're interested in</span></span>

<span data-ttu-id="d6a4b-106">Puede usar Microsoft Visual Studio para buscar el código fuente de un repositorio completo y ver si se muestra el uso de una API de Windows determinada.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-106">You can use Microsoft Visual Studio to search an entire repo's source code to see whether the usage of a particular Windows API is being demonstrated.</span></span>

* <span data-ttu-id="d6a4b-107">Clone cualquiera de las repositorios enumeradas en las secciones siguientes (o descargue el archivo ZIP) en el sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-107">Clone any of the repos listed in the sections below (or download the ZIP) to your local file system.</span></span>
* <span data-ttu-id="d6a4b-108">A continuación, **Busque en archivos** en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-108">Then **Find in Files** in Visual Studio.</span></span> <span data-ttu-id="d6a4b-109">Establezca **Buscar en** la carpeta clonada o descargada en y busque el nombre de la API que le interesa.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-109">Set **Look in** to the folder you cloned or downloaded into, and search for the name of the API you're interested in.</span></span> <span data-ttu-id="d6a4b-110">La comprobación de **coincidencia de mayúsculas y minúsculas** proporciona mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-110">Checking **Match case** gives best results.</span></span>
* <span data-ttu-id="d6a4b-111">Tenga cuidado al comprobar la **palabra completa de coincidencia** si se puede llamar a la API en varios formatos &mdash; , por ejemplo, **CreateMutex**, **CreateMutexA** y **CreateMutexW**.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-111">Be careful of checking **Match whole word** if the API can be called in various forms&mdash;for example, **CreateMutex**, **CreateMutexA**, and **CreateMutexW**.</span></span> <span data-ttu-id="d6a4b-112">En ese caso, busque **CreateMutex** con **palabra completa coincidir** desactivada.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-112">In that case, search for **CreateMutex** with **Match whole word** unchecked.</span></span>

> [!NOTE]
> <span data-ttu-id="d6a4b-113">Puede instalar [Visual Studio](https://visualstudio.microsoft.com/downloads/) sin gastos.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-113">You can install [Visual Studio](https://visualstudio.microsoft.com/downloads/) without expense.</span></span> <span data-ttu-id="d6a4b-114">Hay disponible una edición Community &mdash;es gratuita para estudiantes, colaboradores de código abierto y particulares—.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-114">A Community edition is available&mdash;it's free for students, open-source contributors, and individuals.</span></span> <span data-ttu-id="d6a4b-115">Por supuesto, puede hacer lo mismo con cualquier repositorio de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-115">Of course you can do the same thing with any samples repo.</span></span>

## <a name="the-windows-classic-samples-repo"></a><span data-ttu-id="d6a4b-116">Repositorio de ejemplos de Windows clásico</span><span class="sxs-lookup"><span data-stu-id="d6a4b-116">The Windows classic samples repo</span></span>

<span data-ttu-id="d6a4b-117">El repositorio principal que contiene aplicaciones de ejemplo de Windows con la API de Win32 es el repositorio de [ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples) .</span><span class="sxs-lookup"><span data-stu-id="d6a4b-117">The main repo containing sample Windows apps using the Win32 API is the [Windows classic samples](https://github.com/Microsoft/Windows-classic-samples) repo.</span></span>

## <a name="directx-samples"></a><span data-ttu-id="d6a4b-118">Ejemplos de DirectX</span><span class="sxs-lookup"><span data-stu-id="d6a4b-118">DirectX samples</span></span>

<span data-ttu-id="d6a4b-119">Consulte el repositorio [DirectX-Graphics-samples](https://github.com/Microsoft/DirectX-Graphics-Samples) para gráficos de DirectX 12 que muestran cómo crear aplicaciones de uso intensivo de gráficos para Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d6a4b-119">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="d6a4b-120">Vea también [ejemplos de DirectX](/windows/uwp/gaming/directx-samples).</span><span class="sxs-lookup"><span data-stu-id="d6a4b-120">Also see [DirectX samples](/windows/uwp/gaming/directx-samples).</span></span>

## <a name="older-samples"></a><span data-ttu-id="d6a4b-121">Ejemplos más antiguos</span><span class="sxs-lookup"><span data-stu-id="d6a4b-121">Older samples</span></span>

<span data-ttu-id="d6a4b-122">Puede encontrar algunas aplicaciones anteriores de Win32 de ejemplo en el repositorio de ejemplos de Microsoft de la [Galería de código de MSDN](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) .</span><span class="sxs-lookup"><span data-stu-id="d6a4b-122">You can find some older Win32 sample apps in the [MSDN Code Gallery Microsoft samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) repo.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6a4b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6a4b-123">See also</span></span>

* [<span data-ttu-id="d6a4b-124">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="d6a4b-124">Code samples</span></span>](https://developer.microsoft.com/windows/samples/)
* [<span data-ttu-id="d6a4b-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d6a4b-125">Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="d6a4b-126">Ejemplos de Windows clásico</span><span class="sxs-lookup"><span data-stu-id="d6a4b-126">Windows classic samples</span></span>](https://github.com/Microsoft/Windows-classic-samples)
* [<span data-ttu-id="d6a4b-127">DirectX-Graphics-Samples</span><span class="sxs-lookup"><span data-stu-id="d6a4b-127">DirectX-Graphics-Samples</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples)
* [<span data-ttu-id="d6a4b-128">Ejemplos de DirectX</span><span class="sxs-lookup"><span data-stu-id="d6a4b-128">DirectX samples</span></span>](/windows/uwp/gaming/directx-samples)
* [<span data-ttu-id="d6a4b-129">Galería de código de MSDN ejemplos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="d6a4b-129">MSDN Code Gallery Microsoft samples</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft)
