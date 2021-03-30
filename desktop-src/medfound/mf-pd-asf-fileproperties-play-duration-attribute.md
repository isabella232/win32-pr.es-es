---
description: Especifica el tiempo necesario para reproducir un archivo de formato de sistema avanzado (ASF), en unidades de 100-nanosegundos.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002407"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="1c06b-103">MF \_ PD \_ ASF \_ FILEPROPERTIES de \_ reproducción de atributo de \_ duración</span><span class="sxs-lookup"><span data-stu-id="1c06b-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="1c06b-104">Especifica el tiempo necesario para reproducir un archivo de formato de sistema avanzado (ASF), en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="1c06b-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="1c06b-105">Este valor incluye el tiempo de prelanzamiento.</span><span class="sxs-lookup"><span data-stu-id="1c06b-105">This value includes the preroll time.</span></span> <span data-ttu-id="1c06b-106">Para recuperar la duración real de la reproducción, obtenga el valor del atributo de [**\_ \_ duración MF PD**](mf-pd-duration-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1c06b-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="1c06b-107">Sin embargo, si el valor de preroll es mayor que la duración de la reproducción, el valor de la **\_ \_ duración de MF PD** es cero.</span><span class="sxs-lookup"><span data-stu-id="1c06b-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c06b-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1c06b-108">Data type</span></span>

<span data-ttu-id="1c06b-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1c06b-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c06b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c06b-110">Remarks</span></span>

<span data-ttu-id="1c06b-111">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="1c06b-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="1c06b-112">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="1c06b-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="1c06b-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c06b-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="1c06b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c06b-114">Requirements</span></span>



| <span data-ttu-id="1c06b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c06b-115">Requirement</span></span> | <span data-ttu-id="1c06b-116">Value</span><span class="sxs-lookup"><span data-stu-id="1c06b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c06b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c06b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c06b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1c06b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1c06b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c06b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c06b-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c06b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c06b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c06b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c06b-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c06b-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c06b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c06b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c06b-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c06b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c06b-125">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="1c06b-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="1c06b-126">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="1c06b-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="1c06b-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1c06b-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1c06b-128">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="1c06b-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c06b-129">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="1c06b-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="1c06b-130">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="1c06b-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




