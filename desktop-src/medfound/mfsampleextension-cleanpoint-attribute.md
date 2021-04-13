---
description: Indica si un ejemplo es un punto de acceso aleatorio.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: MFSampleExtension_CleanPoint atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543955"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="4934f-103">\_Atributo CleanPoint de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="4934f-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="4934f-104">Indica si un ejemplo es un punto de acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="4934f-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="4934f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4934f-105">Data type</span></span>

<span data-ttu-id="4934f-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4934f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4934f-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="4934f-107">Get/set</span></span>

<span data-ttu-id="4934f-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4934f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4934f-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4934f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4934f-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4934f-110">Applies to</span></span>

[<span data-ttu-id="4934f-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="4934f-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="4934f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4934f-112">Remarks</span></span>

<span data-ttu-id="4934f-113">Este atributo se aplica a los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="4934f-113">This attribute applies to samples.</span></span> <span data-ttu-id="4934f-114">Si el atributo es **true**, el ejemplo es un punto de acceso aleatorio y la descodificación puede empezar a partir de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4934f-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="4934f-115">De lo contrario, el ejemplo no es un punto de acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="4934f-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="4934f-116">Si no se establece este atributo, el valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="4934f-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="4934f-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4934f-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="4934f-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4934f-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="4934f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4934f-119">Requirements</span></span>



| <span data-ttu-id="4934f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4934f-120">Requirement</span></span> | <span data-ttu-id="4934f-121">Value</span><span class="sxs-lookup"><span data-stu-id="4934f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4934f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4934f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4934f-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="4934f-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4934f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4934f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4934f-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="4934f-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4934f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4934f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4934f-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4934f-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4934f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4934f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4934f-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4934f-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4934f-130">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4934f-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="4934f-131">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="4934f-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




