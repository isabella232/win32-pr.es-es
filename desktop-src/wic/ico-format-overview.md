---
description: En este tema se proporciona información sobre el códec ICO nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Introducción al formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444476"
---
# <a name="ico-format-overview"></a><span data-ttu-id="8bd4c-103">Introducción al formato ICO</span><span class="sxs-lookup"><span data-stu-id="8bd4c-103">ICO Format Overview</span></span>

<span data-ttu-id="8bd4c-104">En este tema se proporciona información sobre el códec ICO nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="8bd4c-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="8bd4c-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="8bd4c-105">Codec Identity</span></span>

<span data-ttu-id="8bd4c-106">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="8bd4c-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="8bd4c-107">Componente</span><span class="sxs-lookup"><span data-stu-id="8bd4c-107">Component</span></span>            | <span data-ttu-id="8bd4c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bd4c-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="8bd4c-109">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="8bd4c-109">Formal Name(s)</span></span>         | <span data-ttu-id="8bd4c-110">Formato de icono (ICO)</span><span class="sxs-lookup"><span data-stu-id="8bd4c-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="8bd4c-111">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="8bd4c-111">File Name Extension(s)</span></span> | <span data-ttu-id="8bd4c-112">Ico</span><span class="sxs-lookup"><span data-stu-id="8bd4c-112">ico</span></span>               |
| <span data-ttu-id="8bd4c-113">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="8bd4c-113">MIME type</span></span>              | <span data-ttu-id="8bd4c-114">image/ico</span><span class="sxs-lookup"><span data-stu-id="8bd4c-114">image/ico</span></span>         |
| <span data-ttu-id="8bd4c-115">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="8bd4c-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="8bd4c-116">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec ICO nativos.</span><span class="sxs-lookup"><span data-stu-id="8bd4c-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="8bd4c-117">Componente</span><span class="sxs-lookup"><span data-stu-id="8bd4c-117">Component</span></span>        | <span data-ttu-id="8bd4c-118">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="8bd4c-118">Friendly Name</span></span>            | <span data-ttu-id="8bd4c-119">GUID</span><span class="sxs-lookup"><span data-stu-id="8bd4c-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="8bd4c-120">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="8bd4c-120">Container Format</span></span> | <span data-ttu-id="8bd4c-121">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="8bd4c-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="8bd4c-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="8bd4c-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="8bd4c-123">Descodificador</span><span class="sxs-lookup"><span data-stu-id="8bd4c-123">Decoder</span></span>          | <span data-ttu-id="8bd4c-124">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="8bd4c-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="8bd4c-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="8bd4c-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="8bd4c-126">Codificador</span><span class="sxs-lookup"><span data-stu-id="8bd4c-126">Encoder</span></span>          | <span data-ttu-id="8bd4c-127">NO DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="8bd4c-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="8bd4c-128">NO DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="8bd4c-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="8bd4c-129">Encoding</span><span class="sxs-lookup"><span data-stu-id="8bd4c-129">Encoding</span></span>

<span data-ttu-id="8bd4c-130">WIC no proporciona un codificador de imágenes ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="8bd4c-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="8bd4c-131">Descodificación</span><span class="sxs-lookup"><span data-stu-id="8bd4c-131">Decoding</span></span>

<span data-ttu-id="8bd4c-132">La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="8bd4c-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8bd4c-133">Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="8bd4c-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8bd4c-134">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="8bd4c-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



