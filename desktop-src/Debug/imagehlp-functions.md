---
description: A continuación se indican las funciones ImageHlp.
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Funciones ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e921707474f68e288f67e84dda9e361922bca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000717"
---
# <a name="imagehlp-functions"></a><span data-ttu-id="3786d-103">Funciones ImageHlp</span><span class="sxs-lookup"><span data-stu-id="3786d-103">ImageHlp Functions</span></span>

<span data-ttu-id="3786d-104">A continuación se indican las funciones ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="3786d-104">The following are the ImageHlp functions.</span></span>

## <a name="image-access"></a><span data-ttu-id="3786d-105">Acceso a imágenes</span><span class="sxs-lookup"><span data-stu-id="3786d-105">Image Access</span></span>

<span data-ttu-id="3786d-106">Las funciones de acceso a la imagen obtienen acceso a los datos de una imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="3786d-106">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="3786d-107">Las funciones proporcionan acceso de alto nivel a la base de imágenes y acceso muy específico a las partes más comunes de los datos de una imagen.</span><span class="sxs-lookup"><span data-stu-id="3786d-107">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="3786d-108">**GetImageConfigInformation**</span><span class="sxs-lookup"><span data-stu-id="3786d-108">**GetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[<span data-ttu-id="3786d-109">**GetImageUnusedHeaderBytes**</span><span class="sxs-lookup"><span data-stu-id="3786d-109">**GetImageUnusedHeaderBytes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[<span data-ttu-id="3786d-110">**ImageLoad**</span><span class="sxs-lookup"><span data-stu-id="3786d-110">**ImageLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[<span data-ttu-id="3786d-111">**ImageUnload**</span><span class="sxs-lookup"><span data-stu-id="3786d-111">**ImageUnload**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[<span data-ttu-id="3786d-112">**MapAndLoad**</span><span class="sxs-lookup"><span data-stu-id="3786d-112">**MapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[<span data-ttu-id="3786d-113">**SetImageConfigInformation**</span><span class="sxs-lookup"><span data-stu-id="3786d-113">**SetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[<span data-ttu-id="3786d-114">**UnMapAndLoad**</span><span class="sxs-lookup"><span data-stu-id="3786d-114">**UnMapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a><span data-ttu-id="3786d-115">Integridad de la imagen</span><span class="sxs-lookup"><span data-stu-id="3786d-115">Image Integrity</span></span>

<span data-ttu-id="3786d-116">Las funciones de integridad de la imagen administran el conjunto de certificados en un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="3786d-116">The image integrity functions manage the set of certificates in an image file.</span></span>

<dl>

[<span data-ttu-id="3786d-117">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="3786d-117">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[<span data-ttu-id="3786d-118">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="3786d-118">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[<span data-ttu-id="3786d-119">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="3786d-119">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[<span data-ttu-id="3786d-120">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="3786d-120">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[<span data-ttu-id="3786d-121">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="3786d-121">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[<span data-ttu-id="3786d-122">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="3786d-122">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[<span data-ttu-id="3786d-123">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="3786d-123">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a><span data-ttu-id="3786d-124">Modificación de imagen</span><span class="sxs-lookup"><span data-stu-id="3786d-124">Image Modification</span></span>

<span data-ttu-id="3786d-125">Las funciones de modificación de imágenes permiten cambiar la imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="3786d-125">The image modification functions allow you to change the executable image.</span></span>

<dl>

[<span data-ttu-id="3786d-126">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="3786d-126">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[<span data-ttu-id="3786d-127">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="3786d-127">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[<span data-ttu-id="3786d-128">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="3786d-128">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[<span data-ttu-id="3786d-129">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="3786d-129">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[<span data-ttu-id="3786d-130">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="3786d-130">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[<span data-ttu-id="3786d-131">**ReBaseImage64**</span><span class="sxs-lookup"><span data-stu-id="3786d-131">**ReBaseImage64**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[<span data-ttu-id="3786d-132">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="3786d-132">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[<span data-ttu-id="3786d-133">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="3786d-133">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[<span data-ttu-id="3786d-134">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="3786d-134">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[<span data-ttu-id="3786d-135">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="3786d-135">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[<span data-ttu-id="3786d-136">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="3786d-136">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



