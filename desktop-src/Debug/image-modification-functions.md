---
description: Las funciones de modificación de imágenes permiten cambiar la imagen ejecutable.
ms.assetid: 195959cb-e1ab-4c76-b7f9-f20522feac8c
title: Funciones de modificación de imagen de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6be83457738d1237865940463f438d3b73afa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807070"
---
# <a name="imagehlp-image-modification-functions"></a><span data-ttu-id="4fcf3-103">Funciones de modificación de imagen de ImageHlp</span><span class="sxs-lookup"><span data-stu-id="4fcf3-103">ImageHlp Image Modification Functions</span></span>

<span data-ttu-id="4fcf3-104">Las funciones de modificación de imágenes permiten cambiar la imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-104">The image modification functions allow you to change the executable image.</span></span> <span data-ttu-id="4fcf3-105">Son principalmente para su uso por parte de las herramientas de desarrollo y los programas de instalación.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-105">They are mostly for use by development tools and install programs.</span></span> <span data-ttu-id="4fcf3-106">Se pueden usar para enlazar una imagen, calcular su suma de comprobación (que es importante para garantizar la integridad de la imagen), cambiar su dirección de carga y generar archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-106">They can be used to bind an image, compute its checksum (which is important for ensuring image integrity), change its load address, and produce symbol files.</span></span>

<span data-ttu-id="4fcf3-107">A continuación se muestran las funciones de modificación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-107">The following are the image modification functions.</span></span>

-   [<span data-ttu-id="4fcf3-108">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-108">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)
-   [<span data-ttu-id="4fcf3-109">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-109">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)
-   [<span data-ttu-id="4fcf3-110">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-110">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)
-   [<span data-ttu-id="4fcf3-111">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-111">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)
-   [<span data-ttu-id="4fcf3-112">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-112">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)
-   [<span data-ttu-id="4fcf3-113">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-113">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)
-   [<span data-ttu-id="4fcf3-114">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-114">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)
-   [<span data-ttu-id="4fcf3-115">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-115">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)
-   [<span data-ttu-id="4fcf3-116">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-116">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)
-   [<span data-ttu-id="4fcf3-117">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-117">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)

 

 



