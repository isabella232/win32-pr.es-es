---
description: Datos de formato adicionales para una secuencia binaria en un archivo de formato de sistema avanzado (ASF).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716355"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="f4b69-103">Atributo de formato de MF \_ MT \_ arbitrario \_</span><span class="sxs-lookup"><span data-stu-id="f4b69-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="f4b69-104">Datos de formato adicionales para una secuencia binaria en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f4b69-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4b69-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f4b69-105">Data type</span></span>

<span data-ttu-id="f4b69-106">**BYTES\[\]**</span><span class="sxs-lookup"><span data-stu-id="f4b69-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="f4b69-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="f4b69-107">Get/set</span></span>

<span data-ttu-id="f4b69-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="f4b69-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="f4b69-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="f4b69-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b69-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4b69-110">Remarks</span></span>

<span data-ttu-id="f4b69-111">Las aplicaciones pueden usar secuencias binarias para contener tipos de datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="f4b69-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="f4b69-112">El origen de medios ASF trata el valor de este atributo como un BLOB opaco.</span><span class="sxs-lookup"><span data-stu-id="f4b69-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="f4b69-113">El miembro **formatType** de la estructura de [**\_ \_ encabezado arbitraria de MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) define el diseño de los datos de formato.</span><span class="sxs-lookup"><span data-stu-id="f4b69-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="f4b69-114">Esta estructura corresponde al campo de datos de formato de los datos específicos del tipo en el objeto de propiedades de la secuencia, en archivos donde el tipo de secuencia es un **\_ \_ medio binario ASF**.</span><span class="sxs-lookup"><span data-stu-id="f4b69-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="f4b69-115">Para obtener más información, consulte la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="f4b69-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="f4b69-116">En el SDK de Windows Media Format, las secuencias binarias se denominan *flujos arbitrarios* o *flujos de datos arbitrarios*.</span><span class="sxs-lookup"><span data-stu-id="f4b69-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="f4b69-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f4b69-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b69-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4b69-118">Requirements</span></span>



| <span data-ttu-id="f4b69-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4b69-119">Requirement</span></span> | <span data-ttu-id="f4b69-120">Value</span><span class="sxs-lookup"><span data-stu-id="f4b69-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b69-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4b69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b69-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4b69-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4b69-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4b69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b69-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4b69-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f4b69-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4b69-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4b69-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4b69-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4b69-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4b69-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4b69-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4b69-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4b69-129">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="f4b69-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4b69-130">\_ \_ encabezado arbitrario MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="f4b69-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




