---
description: Especifica una lista de velocidades de bits y las ventanas de búfer correspondientes para un archivo de formato de sistema avanzado (VBR) de velocidad de bits variable (VBR).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716422"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="08341-103">\_Atributo de \_ \_ pares de \_ \_ cubos de los metadatos de MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="08341-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="08341-104">Especifica una lista de velocidades de bits y las ventanas de búfer correspondientes para un archivo de formato de sistema avanzado (VBR) de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="08341-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="08341-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="08341-105">Data type</span></span>

<span data-ttu-id="08341-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="08341-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="08341-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08341-107">Remarks</span></span>

<span data-ttu-id="08341-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="08341-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="08341-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo que se aplica al descriptor de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="08341-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="08341-110">El valor del atributo tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="08341-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="08341-111">La estructura de **\_ par de \_ depósitos \_ con fugas de WM** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="08341-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="08341-112">Para cada velocidad de bits, el miembro **msBufferWindow** indica la cantidad de contenido que se almacena en búfer antes de que se inicie la reproducción, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="08341-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="08341-113">El tamaño del búfer en bytes es igual a **msBufferWinow** x **dwBitrate** /8000.</span><span class="sxs-lookup"><span data-stu-id="08341-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="08341-114">Este atributo corresponde al atributo **ASFLeakyBucketPairs** en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="08341-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08341-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08341-115">Requirements</span></span>



| <span data-ttu-id="08341-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="08341-116">Requirement</span></span> | <span data-ttu-id="08341-117">Value</span><span class="sxs-lookup"><span data-stu-id="08341-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08341-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08341-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08341-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08341-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08341-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08341-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08341-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="08341-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="08341-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08341-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08341-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="08341-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08341-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="08341-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08341-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08341-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08341-126">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="08341-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="08341-127">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="08341-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="08341-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="08341-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="08341-129">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="08341-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="08341-130">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="08341-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="08341-131">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="08341-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




