---
description: Especifica el modo del códec de voz.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Propiedad MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696686"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="4f0c0-103">MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode propiedad</span><span class="sxs-lookup"><span data-stu-id="4f0c0-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="4f0c0-104">Especifica el modo del códec de voz.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4f0c0-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4f0c0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4f0c0-106">g \_ wszWMACMusicSpeechClassMode</span><span class="sxs-lookup"><span data-stu-id="4f0c0-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="4f0c0-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4f0c0-107">Data Type</span></span>

<span data-ttu-id="4f0c0-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4f0c0-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4f0c0-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4f0c0-109">Default Value</span></span>

<span data-ttu-id="4f0c0-110">1</span><span class="sxs-lookup"><span data-stu-id="4f0c0-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="4f0c0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f0c0-111">Remarks</span></span>

<span data-ttu-id="4f0c0-112">Un valor de 1 informa al códec de que el contenido es de solo voz, un valor de 2 tiene el códec determina el modo automáticamente y cualquier otro valor informa al códec de que use el modo de música.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="4f0c0-113">Si el modo automático no está codificando voz mixta y música correctamente, puede especificar la codificación para secciones individuales del archivo mediante la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4f0c0-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0c0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f0c0-114">Requirements</span></span>



| <span data-ttu-id="4f0c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f0c0-115">Requirement</span></span> | <span data-ttu-id="4f0c0-116">Value</span><span class="sxs-lookup"><span data-stu-id="4f0c0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0c0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f0c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0c0-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4f0c0-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4f0c0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f0c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0c0-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f0c0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f0c0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f0c0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f0c0-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f0c0-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0c0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f0c0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0c0-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f0c0-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




