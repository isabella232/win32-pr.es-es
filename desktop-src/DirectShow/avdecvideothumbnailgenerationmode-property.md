---
description: Habilita o deshabilita el modo de generación de miniaturas en un descodificador de vídeo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propiedad AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997997"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="bc850-103">Propiedad AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="bc850-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="bc850-104">Habilita o deshabilita el modo de generación de miniaturas en un descodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bc850-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="bc850-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bc850-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bc850-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bc850-106">Data type</span></span>

<span data-ttu-id="bc850-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="bc850-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bc850-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="bc850-108">Property GUID</span></span>

<span data-ttu-id="bc850-109">**CODECAPI \_ AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="bc850-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="bc850-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc850-110">Remarks</span></span>

<span data-ttu-id="bc850-111">Si el valor es **Variant \_ true**, el descodificador usa una configuración optimizada para generar imágenes en miniatura rápidamente.</span><span class="sxs-lookup"><span data-stu-id="bc850-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="bc850-112">(Por ejemplo, puede omitir los fotogramas B o P). De lo contrario, si el valor es **Variant \_ false**, el descodificador usa su configuración de descodificación normal.</span><span class="sxs-lookup"><span data-stu-id="bc850-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc850-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc850-113">Requirements</span></span>



| <span data-ttu-id="bc850-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc850-114">Requirement</span></span> | <span data-ttu-id="bc850-115">Value</span><span class="sxs-lookup"><span data-stu-id="bc850-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc850-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc850-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc850-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="bc850-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bc850-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc850-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc850-119">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="bc850-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bc850-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc850-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc850-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc850-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc850-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc850-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc850-123">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="bc850-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bc850-124">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="bc850-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




