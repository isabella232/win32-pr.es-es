---
description: Especifica las partes de contenido que el códec de voz debe codificar como música.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Propiedad MFPKEY_WMAVOICE_ENC_EDL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812631"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="db112-103">MFPKEY \_ WMAVOICE \_ enc \_ EDL (propiedad)</span><span class="sxs-lookup"><span data-stu-id="db112-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="db112-104">Especifica las partes de contenido que el códec de voz debe codificar como música.</span><span class="sxs-lookup"><span data-stu-id="db112-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="db112-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="db112-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="db112-106">g \_ wszWMACVoiceBuffer</span><span class="sxs-lookup"><span data-stu-id="db112-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="db112-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="db112-107">Data Type</span></span>

<span data-ttu-id="db112-108">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="db112-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="db112-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="db112-109">Default Value</span></span>

<span data-ttu-id="db112-110">Ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="db112-110">No default value.</span></span> <span data-ttu-id="db112-111">Si no se establece esta propiedad, el códec usará el valor de la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) para determinar cómo codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="db112-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="db112-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db112-112">Remarks</span></span>

<span data-ttu-id="db112-113">Puede usar esta propiedad si el modo automático del códec no da resultados satisfactorios.</span><span class="sxs-lookup"><span data-stu-id="db112-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="db112-114">Este valor es una cadena delimitada por comas que contiene al menos cuatro enteros.</span><span class="sxs-lookup"><span data-stu-id="db112-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="db112-115">El primer entero es el número de versión; Use siempre 1 para este valor.</span><span class="sxs-lookup"><span data-stu-id="db112-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="db112-116">El segundo entero es el número de secciones que se deben codificar como música.</span><span class="sxs-lookup"><span data-stu-id="db112-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="db112-117">Después del segundo entero hay un número de pares de valores que representan rangos en milisegundos, un par para cada sección de contenido que debe codificarse como música.</span><span class="sxs-lookup"><span data-stu-id="db112-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="db112-118">Por ejemplo, "1, 2100200500600" informa al codificador que use la versión 1 con 2 secciones de música.</span><span class="sxs-lookup"><span data-stu-id="db112-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="db112-119">La primera sección de música comienza en 100 ms y termina en 200 ms.</span><span class="sxs-lookup"><span data-stu-id="db112-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="db112-120">La segunda sección Music comienza en 500 ms y termina en 600 ms.</span><span class="sxs-lookup"><span data-stu-id="db112-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="db112-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db112-121">Requirements</span></span>



| <span data-ttu-id="db112-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="db112-122">Requirement</span></span> | <span data-ttu-id="db112-123">Value</span><span class="sxs-lookup"><span data-stu-id="db112-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db112-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db112-124">Minimum supported client</span></span><br/> | <span data-ttu-id="db112-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="db112-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db112-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db112-126">Minimum supported server</span></span><br/> | <span data-ttu-id="db112-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db112-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db112-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db112-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="db112-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db112-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db112-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="db112-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db112-131">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db112-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




