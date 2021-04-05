---
description: Datos específicos del tipo de una secuencia binaria en un archivo de formato de sistema avanzado (ASF).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082345"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="019d2-103">\_Atributo de \_ encabezado arbitrario MF MT \_</span><span class="sxs-lookup"><span data-stu-id="019d2-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="019d2-104">Datos específicos del tipo de una secuencia binaria en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="019d2-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="019d2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="019d2-105">Data type</span></span>

<span data-ttu-id="019d2-106">**[**MT \_ \_Encabezado arbitrario**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** almacenado como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="019d2-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="019d2-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="019d2-107">Get/set</span></span>

<span data-ttu-id="019d2-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="019d2-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="019d2-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="019d2-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="019d2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="019d2-110">Remarks</span></span>

<span data-ttu-id="019d2-111">Los archivos ASF pueden contener secuencias con datos binarios.</span><span class="sxs-lookup"><span data-stu-id="019d2-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="019d2-112">El \_ \_ \_ atributo de encabezado arbitrario MF MT en el tipo de medio contiene una estructura de [**\_ \_ encabezado arbitrario MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) que describe la secuencia.</span><span class="sxs-lookup"><span data-stu-id="019d2-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="019d2-113">Además del \_ \_ atributo de encabezado arbitrario MF MT \_ , el tipo de medio de una secuencia binaria ASF contiene los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="019d2-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="019d2-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="019d2-114">Attribute</span></span>                                                 | <span data-ttu-id="019d2-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="019d2-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="019d2-116">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="019d2-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="019d2-117">El valor del atributo es **MFMediaType \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="019d2-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="019d2-118">\_ \_ formato arbitrario MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="019d2-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="019d2-119">Contiene datos de formato adicionales.</span><span class="sxs-lookup"><span data-stu-id="019d2-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="019d2-120">En el SDK de Windows Media Format, las secuencias binarias se denominan *flujos arbitrarios* o *flujos de datos arbitrarios*.</span><span class="sxs-lookup"><span data-stu-id="019d2-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="019d2-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="019d2-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="019d2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="019d2-122">Requirements</span></span>



| <span data-ttu-id="019d2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="019d2-123">Requirement</span></span> | <span data-ttu-id="019d2-124">Value</span><span class="sxs-lookup"><span data-stu-id="019d2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="019d2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="019d2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="019d2-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="019d2-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="019d2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="019d2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="019d2-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="019d2-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="019d2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="019d2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="019d2-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="019d2-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="019d2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="019d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="019d2-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="019d2-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="019d2-133">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="019d2-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




