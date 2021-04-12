---
description: Especifica el idioma de una secuencia.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: MF_SD_LANGUAGE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278346"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="123d0-103">\_Atributo de \_ idioma MF SD</span><span class="sxs-lookup"><span data-stu-id="123d0-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="123d0-104">Especifica el idioma de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="123d0-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="123d0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="123d0-105">Data type</span></span>

<span data-ttu-id="123d0-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="123d0-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="123d0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="123d0-107">Remarks</span></span>

<span data-ttu-id="123d0-108">El valor de este atributo es una etiqueta de lenguaje compatible con RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="123d0-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="123d0-109">Este atributo se aplica a los descriptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="123d0-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="123d0-110">Un origen multimedia (o cualquier objeto que crea un descriptor de secuencia) puede establecer este atributo si la secuencia tiene un idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="123d0-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="123d0-111">Las aplicaciones pueden consultar este atributo para obtener el lenguaje.</span><span class="sxs-lookup"><span data-stu-id="123d0-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="123d0-112">Si no se establece el atributo, la secuencia no tiene un idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="123d0-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="123d0-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="123d0-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="123d0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="123d0-114">Requirements</span></span>



| <span data-ttu-id="123d0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="123d0-115">Requirement</span></span> | <span data-ttu-id="123d0-116">Value</span><span class="sxs-lookup"><span data-stu-id="123d0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="123d0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123d0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="123d0-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="123d0-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="123d0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123d0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="123d0-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="123d0-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="123d0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="123d0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="123d0-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="123d0-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="123d0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="123d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123d0-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="123d0-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="123d0-125">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="123d0-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="123d0-126">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="123d0-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="123d0-127">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="123d0-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="123d0-128">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="123d0-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




