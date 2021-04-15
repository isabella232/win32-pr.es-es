---
description: Obtiene las características del origen multimedia del lector de origen.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361941"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="d9d93-103">\_Atributo de \_ \_ características MEDIASOURCE del lector de origen MF \_</span><span class="sxs-lookup"><span data-stu-id="d9d93-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="d9d93-104">Obtiene las características del origen multimedia del lector de [origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="d9d93-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="d9d93-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d9d93-105">Data type</span></span>

<span data-ttu-id="d9d93-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d9d93-106">**UINT32**</span></span>

<span data-ttu-id="d9d93-107">El valor es **una operación OR bit a bit** de marcas de la enumeración de [**\_ características de MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="d9d93-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d93-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9d93-108">Remarks</span></span>

<span data-ttu-id="d9d93-109">Para obtener este atributo, llame al método [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) en el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="d9d93-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="d9d93-110">Establezca el parámetro *dwStreamIndex* en el parámetro del **\_ lector de código fuente \_ \_ MF** y el parámetro *guidAttribute* en las \_ características de MediaSource del lector de código fuente MF \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d9d93-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="d9d93-111">El tipo **PROPVARIANT** para este atributo es **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="d9d93-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="d9d93-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d9d93-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d9d93-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9d93-113">Requirements</span></span>



| <span data-ttu-id="d9d93-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9d93-114">Requirement</span></span> | <span data-ttu-id="d9d93-115">Value</span><span class="sxs-lookup"><span data-stu-id="d9d93-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d93-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9d93-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d93-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d9d93-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d9d93-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9d93-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d93-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d9d93-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d9d93-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9d93-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9d93-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9d93-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d93-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9d93-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d93-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9d93-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9d93-124">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="d9d93-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




