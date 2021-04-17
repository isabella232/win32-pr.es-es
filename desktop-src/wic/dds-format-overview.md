---
description: Proporciona información sobre el códec DDS nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Información general sobre el formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697224"
---
# <a name="dds-format-overview"></a><span data-ttu-id="2f297-103">Información general sobre el formato DDS</span><span class="sxs-lookup"><span data-stu-id="2f297-103">DDS Format Overview</span></span>

<span data-ttu-id="2f297-104">En este tema se proporciona información sobre el códec DDS nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="2f297-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="2f297-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="2f297-105">Codec Identity</span></span>

<span data-ttu-id="2f297-106">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="2f297-106">The following table provides codec identification information.</span></span>



|                        |                    |
|------------------------|--------------------|
| <span data-ttu-id="2f297-107">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="2f297-107">Formal Name(s)</span></span>         | <span data-ttu-id="2f297-108">Superficie de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="2f297-108">DirectDraw Surface</span></span> |
| <span data-ttu-id="2f297-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="2f297-109">File Name Extension(s)</span></span> | <span data-ttu-id="2f297-110">DDS</span><span class="sxs-lookup"><span data-stu-id="2f297-110">dds</span></span>                |
| <span data-ttu-id="2f297-111">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="2f297-111">MIME type</span></span>              | <span data-ttu-id="2f297-112">Image/vnd-ms. DDS</span><span class="sxs-lookup"><span data-stu-id="2f297-112">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="2f297-113">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec DDS nativo.</span><span class="sxs-lookup"><span data-stu-id="2f297-113">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="2f297-114">Componente</span><span class="sxs-lookup"><span data-stu-id="2f297-114">Component</span></span>        | <span data-ttu-id="2f297-115">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="2f297-115">Friendly Name</span></span>            | <span data-ttu-id="2f297-116">GUID</span><span class="sxs-lookup"><span data-stu-id="2f297-116">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="2f297-117">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="2f297-117">Container Format</span></span> | <span data-ttu-id="2f297-118">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="2f297-118">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="2f297-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="2f297-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="2f297-120">Descodificador</span><span class="sxs-lookup"><span data-stu-id="2f297-120">Decoder</span></span>          | <span data-ttu-id="2f297-121">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="2f297-121">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="2f297-122">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="2f297-122">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="2f297-123">Codificador</span><span class="sxs-lookup"><span data-stu-id="2f297-123">Encoder</span></span>          | <span data-ttu-id="2f297-124">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="2f297-124">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="2f297-125">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="2f297-125">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="2f297-126">Compatibilidad con formato de píxeles</span><span class="sxs-lookup"><span data-stu-id="2f297-126">Pixel Format Support</span></span>

<span data-ttu-id="2f297-127">Tenga en cuenta que el formato DDS admite cualquier valor de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) válido.</span><span class="sxs-lookup"><span data-stu-id="2f297-127">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="2f297-128">Sin embargo, el códec DDS de WIC solo admite la descodificación y la codificación de archivos que contienen los formatos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f297-128">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="2f297-129">Formato de DXGI \_ \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2f297-129">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="2f297-130">Formato de DXGI \_ \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2f297-130">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="2f297-131">Formato de DXGI \_ \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2f297-131">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="2f297-132">Encoding</span><span class="sxs-lookup"><span data-stu-id="2f297-132">Encoding</span></span>

<span data-ttu-id="2f297-133">Las API de codificación WIC están diseñadas para ser independientes del códec y, por lo tanto, la codificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="2f297-133">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2f297-134">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="2f297-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="2f297-135">El formato de archivo DDS tiene requisitos únicos que surgen de su compatibilidad con conceptos como mapas de y matrices de texturas.</span><span class="sxs-lookup"><span data-stu-id="2f297-135">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="2f297-136">Para ejercer el control completo sobre la codificación de imagen DDS, debe usar la interfaz [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para establecer los parámetros de codificación específicos de DDS.</span><span class="sxs-lookup"><span data-stu-id="2f297-136">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="2f297-137">Descodificación</span><span class="sxs-lookup"><span data-stu-id="2f297-137">Decoding</span></span>

<span data-ttu-id="2f297-138">Las API de descodificación de WIC están diseñadas para ser independientes del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="2f297-138">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2f297-139">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="2f297-139">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="2f297-140">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="2f297-140">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="2f297-141">Bloquear el acceso a datos comprimidos</span><span class="sxs-lookup"><span data-stu-id="2f297-141">Block compressed data access</span></span>

<span data-ttu-id="2f297-142">Además de admitir las interfaces de códecs WIC estándar, el descodificador DDS proporciona acceso directo a los datos comprimidos de bloque nativo mediante las interfaces específicas de DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) y [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="2f297-142">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="2f297-143">Para utilizar estas interfaces, llame a QueryInterface fuera de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2f297-143">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
