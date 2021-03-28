---
description: 'Los métodos Image:: Save y métodos Image:: SaveAdd de la clase Image reciben un objeto EncoderParameters que contiene una matriz de objetos EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes del codificador de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276404"
---
# <a name="image-encoder-constants"></a><span data-ttu-id="5eb37-103">Constantes del codificador de imágenes</span><span class="sxs-lookup"><span data-stu-id="5eb37-103">Image Encoder Constants</span></span>

<span data-ttu-id="5eb37-104">Los [métodos Image:: Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) y [métodos Image:: SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) reciben un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que contiene una matriz de objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="5eb37-104">The [Image::Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) and [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class receive an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that contains an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="5eb37-105">Cada objeto **EncoderParameter** tiene un miembro de datos GUID que especifica la categoría de parámetro.</span><span class="sxs-lookup"><span data-stu-id="5eb37-105">Each **EncoderParameter** object has a GUID data member that specifies the parameter category.</span></span> <span data-ttu-id="5eb37-106">Las siguientes constantes, definidas en Gdiplusimaging. h, representan los GUID que especifican las distintas categorías de parámetros.</span><span class="sxs-lookup"><span data-stu-id="5eb37-106">The following constants, defined in Gdiplusimaging.h, represent GUIDs that specify the various parameter categories.</span></span>

-   <span data-ttu-id="5eb37-107">EncoderChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="5eb37-107">EncoderChrominanceTable</span></span>
-   <span data-ttu-id="5eb37-108">EncoderColorDepth</span><span class="sxs-lookup"><span data-stu-id="5eb37-108">EncoderColorDepth</span></span>
-   <span data-ttu-id="5eb37-109">EncoderColorSpace</span><span class="sxs-lookup"><span data-stu-id="5eb37-109">EncoderColorSpace</span></span>
-   <span data-ttu-id="5eb37-110">EncoderCompression</span><span class="sxs-lookup"><span data-stu-id="5eb37-110">EncoderCompression</span></span>
-   <span data-ttu-id="5eb37-111">EncoderLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="5eb37-111">EncoderLuminanceTable</span></span>
-   <span data-ttu-id="5eb37-112">EncoderQuality</span><span class="sxs-lookup"><span data-stu-id="5eb37-112">EncoderQuality</span></span>
-   <span data-ttu-id="5eb37-113">EncoderRenderMethod</span><span class="sxs-lookup"><span data-stu-id="5eb37-113">EncoderRenderMethod</span></span>
-   <span data-ttu-id="5eb37-114">EncoderSaveFlag</span><span class="sxs-lookup"><span data-stu-id="5eb37-114">EncoderSaveFlag</span></span>
-   <span data-ttu-id="5eb37-115">EncoderScanMethod</span><span class="sxs-lookup"><span data-stu-id="5eb37-115">EncoderScanMethod</span></span>
-   <span data-ttu-id="5eb37-116">EncoderTransformation</span><span class="sxs-lookup"><span data-stu-id="5eb37-116">EncoderTransformation</span></span>
-   <span data-ttu-id="5eb37-117">EncoderVersion</span><span class="sxs-lookup"><span data-stu-id="5eb37-117">EncoderVersion</span></span>
-   <span data-ttu-id="5eb37-118">EncoderImageItems</span><span class="sxs-lookup"><span data-stu-id="5eb37-118">EncoderImageItems</span></span>
-   <span data-ttu-id="5eb37-119">EncoderSaveAsCMYK</span><span class="sxs-lookup"><span data-stu-id="5eb37-119">EncoderSaveAsCMYK</span></span>

 

 
