---
description: Especifica el número máximo de muestras PCM adicionales que podrían devolverse al final de después de descodificar un archivo.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Propiedad MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715879"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="f4360-103">\_Propiedad MaxNumPCMSamplesWithPaddedSilence del descodificador de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="f4360-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="f4360-104">Especifica el número máximo de muestras PCM adicionales que podrían devolverse al final de después de descodificar un archivo.</span><span class="sxs-lookup"><span data-stu-id="f4360-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f4360-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f4360-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f4360-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f4360-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f4360-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f4360-107">Data Type</span></span>

<span data-ttu-id="f4360-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f4360-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f4360-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f4360-109">Default Value</span></span>

<span data-ttu-id="f4360-110">2048</span><span class="sxs-lookup"><span data-stu-id="f4360-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="f4360-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4360-111">Remarks</span></span>

<span data-ttu-id="f4360-112">Esta propiedad se puede utilizar para calcular el silencio artificial que se inserta entre las canciones a medida que se introducen en el descodificador una tras otra.</span><span class="sxs-lookup"><span data-stu-id="f4360-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="f4360-113">En el caso de los descodificadores de Windows Media Audio 10 Professional y Windows Media Audio 9 sin pérdida de, esta propiedad siempre es igual a 0.</span><span class="sxs-lookup"><span data-stu-id="f4360-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4360-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4360-114">Requirements</span></span>



| <span data-ttu-id="f4360-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4360-115">Requirement</span></span> | <span data-ttu-id="f4360-116">Value</span><span class="sxs-lookup"><span data-stu-id="f4360-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4360-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4360-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f4360-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f4360-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f4360-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4360-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f4360-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4360-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4360-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4360-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4360-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4360-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4360-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4360-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4360-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4360-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
