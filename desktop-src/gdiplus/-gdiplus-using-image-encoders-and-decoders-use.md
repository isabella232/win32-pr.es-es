---
description: Windows GDI+ proporciona la clase Image y la clase Bitmap para almacenar imágenes en memoria y manipular imágenes en memoria.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Usar codificadores y descodificadores de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154213"
---
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="98ca6-103">Usar codificadores y descodificadores de imágenes</span><span class="sxs-lookup"><span data-stu-id="98ca6-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="98ca6-104">Windows GDI+ proporciona la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y la clase [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para almacenar imágenes en memoria y manipular imágenes en memoria.</span><span class="sxs-lookup"><span data-stu-id="98ca6-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="98ca6-105">GDI+ escribe imágenes en archivos de disco con la ayuda de codificadores de imágenes y carga imágenes de archivos de disco con la ayuda de los descodificadores de imágenes.</span><span class="sxs-lookup"><span data-stu-id="98ca6-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="98ca6-106">Un codificador traduce los datos de una **imagen** o un objeto de **mapa de bits** a un formato de archivo de disco designado.</span><span class="sxs-lookup"><span data-stu-id="98ca6-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="98ca6-107">Un descodificador traduce los datos de un archivo de disco al formato requerido por los objetos de **imagen** y de **mapa de bits** .</span><span class="sxs-lookup"><span data-stu-id="98ca6-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="98ca6-108">GDI+ tiene codificadores y descodificadores integrados que admiten los siguientes tipos de archivo:</span><span class="sxs-lookup"><span data-stu-id="98ca6-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="98ca6-109">BMP</span><span class="sxs-lookup"><span data-stu-id="98ca6-109">BMP</span></span>
-   <span data-ttu-id="98ca6-110">GIF</span><span class="sxs-lookup"><span data-stu-id="98ca6-110">GIF</span></span>
-   <span data-ttu-id="98ca6-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="98ca6-111">JPEG</span></span>
-   <span data-ttu-id="98ca6-112">PNG</span><span class="sxs-lookup"><span data-stu-id="98ca6-112">PNG</span></span>
-   <span data-ttu-id="98ca6-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="98ca6-113">TIFF</span></span>

<span data-ttu-id="98ca6-114">GDI+ también tiene descodificadores integrados que admiten los siguientes tipos de archivo:</span><span class="sxs-lookup"><span data-stu-id="98ca6-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="98ca6-115">WMF</span><span class="sxs-lookup"><span data-stu-id="98ca6-115">WMF</span></span>
-   <span data-ttu-id="98ca6-116">EMF</span><span class="sxs-lookup"><span data-stu-id="98ca6-116">EMF</span></span>
-   <span data-ttu-id="98ca6-117">ICON</span><span class="sxs-lookup"><span data-stu-id="98ca6-117">ICON</span></span>

<span data-ttu-id="98ca6-118">En los temas siguientes se describen con más detalle los codificadores y descodificadores:</span><span class="sxs-lookup"><span data-stu-id="98ca6-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="98ca6-119">Enumerar los codificadores instalados</span><span class="sxs-lookup"><span data-stu-id="98ca6-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="98ca6-120">Enumerar descodificadores instalados</span><span class="sxs-lookup"><span data-stu-id="98ca6-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="98ca6-121">Recuperar el identificador de clase para un codificador</span><span class="sxs-lookup"><span data-stu-id="98ca6-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="98ca6-122">Determinar los parámetros admitidos por un codificador</span><span class="sxs-lookup"><span data-stu-id="98ca6-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="98ca6-123">Convertir una imagen BMP en una imagen PNG</span><span class="sxs-lookup"><span data-stu-id="98ca6-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="98ca6-124">Establecer el nivel de compresión JPEG</span><span class="sxs-lookup"><span data-stu-id="98ca6-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="98ca6-125">Transformar una imagen JPEG sin pérdida de información</span><span class="sxs-lookup"><span data-stu-id="98ca6-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="98ca6-126">Creación y almacenamiento de una imagen de trama múltiple</span><span class="sxs-lookup"><span data-stu-id="98ca6-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="98ca6-127">Copiar fotogramas individuales de una imagen de Multiple-Frame</span><span class="sxs-lookup"><span data-stu-id="98ca6-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



