---
description: Proporciona información sobre el códec DDS nativo disponible a través del Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Introducción al formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444956"
---
# <a name="dds-format-overview"></a><span data-ttu-id="bde4e-103">Introducción al formato DDS</span><span class="sxs-lookup"><span data-stu-id="bde4e-103">DDS Format Overview</span></span>

<span data-ttu-id="bde4e-104">En este tema se proporciona información sobre el códec DDS nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="bde4e-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="bde4e-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="bde4e-105">Codec Identity</span></span>

<span data-ttu-id="bde4e-106">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="bde4e-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="bde4e-107">Componente</span><span class="sxs-lookup"><span data-stu-id="bde4e-107">Component</span></span>              | <span data-ttu-id="bde4e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bde4e-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="bde4e-109">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="bde4e-109">Formal Name(s)</span></span>         | <span data-ttu-id="bde4e-110">DirectDraw Surface</span><span class="sxs-lookup"><span data-stu-id="bde4e-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="bde4e-111">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="bde4e-111">File Name Extension(s)</span></span> | <span data-ttu-id="bde4e-112">Dds</span><span class="sxs-lookup"><span data-stu-id="bde4e-112">dds</span></span>                |
| <span data-ttu-id="bde4e-113">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="bde4e-113">MIME type</span></span>              | <span data-ttu-id="bde4e-114">image/vnd-ms.dds</span><span class="sxs-lookup"><span data-stu-id="bde4e-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="bde4e-115">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec DDS nativos.</span><span class="sxs-lookup"><span data-stu-id="bde4e-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="bde4e-116">Componente</span><span class="sxs-lookup"><span data-stu-id="bde4e-116">Component</span></span>        | <span data-ttu-id="bde4e-117">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="bde4e-117">Friendly Name</span></span>            | <span data-ttu-id="bde4e-118">GUID</span><span class="sxs-lookup"><span data-stu-id="bde4e-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="bde4e-119">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="bde4e-119">Container Format</span></span> | <span data-ttu-id="bde4e-120">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="bde4e-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="bde4e-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="bde4e-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="bde4e-122">Descodificador</span><span class="sxs-lookup"><span data-stu-id="bde4e-122">Decoder</span></span>          | <span data-ttu-id="bde4e-123">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="bde4e-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="bde4e-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="bde4e-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="bde4e-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="bde4e-125">Encoder</span></span>          | <span data-ttu-id="bde4e-126">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="bde4e-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="bde4e-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="bde4e-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="bde4e-128">Compatibilidad con el formato de píxel</span><span class="sxs-lookup"><span data-stu-id="bde4e-128">Pixel Format Support</span></span>

<span data-ttu-id="bde4e-129">Tenga en cuenta que el formato DDS admite cualquier valor [**VÁLIDO \_ DE DXGI FORMAT.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="bde4e-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="bde4e-130">Sin embargo, el códec WIC DDS solo admite la codificación y la codificación de archivos que contienen los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="bde4e-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="bde4e-131">DXGI \_ FORMAT \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="bde4e-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="bde4e-132">DXGI \_ FORMAT \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="bde4e-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="bde4e-133">DXGI \_ FORMAT \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="bde4e-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="bde4e-134">Encoding</span><span class="sxs-lookup"><span data-stu-id="bde4e-134">Encoding</span></span>

<span data-ttu-id="bde4e-135">Las API de codificación de WIC están diseñadas para ser independientes del códec y, por tanto, la codificación de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="bde4e-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bde4e-136">Para más información sobre la codificación de imágenes mediante la API de WIC, consulte Información general [sobre codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="bde4e-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="bde4e-137">El formato de archivo DDS tiene requisitos únicos que surgen de su compatibilidad con conceptos como mapas mip y matrices de textura.</span><span class="sxs-lookup"><span data-stu-id="bde4e-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="bde4e-138">Para controlar completamente la codificación de imágenes DDS, debe usar la interfaz [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para establecer parámetros de codificación específicos de DDS.</span><span class="sxs-lookup"><span data-stu-id="bde4e-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="bde4e-139">Descodificación</span><span class="sxs-lookup"><span data-stu-id="bde4e-139">Decoding</span></span>

<span data-ttu-id="bde4e-140">Las API de decodificación de WIC están diseñadas para ser independientes del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="bde4e-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bde4e-141">Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="bde4e-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="bde4e-142">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="bde4e-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="bde4e-143">Bloquear el acceso a datos comprimidos</span><span class="sxs-lookup"><span data-stu-id="bde4e-143">Block compressed data access</span></span>

<span data-ttu-id="bde4e-144">Además de admitir las interfaces de códec WIC estándar, el descodificador DDS proporciona acceso directo a los datos comprimidos en bloque nativo mediante las interfaces específicas de DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="bde4e-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="bde4e-145">Para usar estas interfaces, llame a QueryInterface fuera de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bde4e-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
