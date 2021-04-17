---
description: Contiene el nombre del idioma de intercambio de medios accesibles (SAMI) sincronizado que se define para la secuencia.
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: MF_SD_SAMI_LANGUAGE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717002"
---
# <a name="mf_sd_sami_language-attribute"></a><span data-ttu-id="f5a98-103">MF \_ SD \_ ( \_ atributo de lenguaje Sami)</span><span class="sxs-lookup"><span data-stu-id="f5a98-103">MF\_SD\_SAMI\_LANGUAGE attribute</span></span>

<span data-ttu-id="f5a98-104">Contiene el nombre del idioma de intercambio de medios accesibles (SAMI) sincronizado que se define para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f5a98-104">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span>

<span data-ttu-id="f5a98-105">Este atributo está presente en los descriptores de flujo devueltos desde el origen de medios SAMI.</span><span class="sxs-lookup"><span data-stu-id="f5a98-105">This attribute is present in the stream descriptors returned from the SAMI media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5a98-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f5a98-106">Data type</span></span>

<span data-ttu-id="f5a98-107">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="f5a98-107">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a98-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5a98-108">Remarks</span></span>

<span data-ttu-id="f5a98-109">El nombre de lenguaje SAMI se especifica en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="f5a98-109">The SAMI language name is specified in the SAMI file.</span></span>

<span data-ttu-id="f5a98-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f5a98-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a98-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5a98-111">Requirements</span></span>



| <span data-ttu-id="f5a98-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a98-112">Requirement</span></span> | <span data-ttu-id="f5a98-113">Value</span><span class="sxs-lookup"><span data-stu-id="f5a98-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a98-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5a98-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a98-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5a98-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5a98-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5a98-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a98-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5a98-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5a98-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5a98-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a98-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a98-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a98-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5a98-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a98-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5a98-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5a98-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="f5a98-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="f5a98-123">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="f5a98-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="f5a98-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f5a98-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="f5a98-125">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="f5a98-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5a98-126">**IMFSAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="f5a98-126">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




