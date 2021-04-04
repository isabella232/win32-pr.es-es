---
description: Especifica si el codificador utiliza la codificación de velocidad de bits variable (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Propiedad MFPKEY_VBRENABLED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908746"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="f5f4e-103">\_Propiedad VBRENABLED de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="f5f4e-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="f5f4e-104">Especifica si el codificador utiliza la codificación de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="f5f4e-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="f5f4e-105">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f5f4e-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f5f4e-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f5f4e-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="f5f4e-107">**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**</span><span class="sxs-lookup"><span data-stu-id="f5f4e-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="f5f4e-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f5f4e-108">Data Type</span></span>

<span data-ttu-id="f5f4e-109">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f5f4e-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="f5f4e-110">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f5f4e-110">Default Value</span></span>

<span data-ttu-id="f5f4e-111">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="f5f4e-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f4e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5f4e-112">Remarks</span></span>

<span data-ttu-id="f5f4e-113">Este valor debe establecerse en **Variant \_ true** para cualquiera de las demás propiedades de VBR que va a usar el códec.</span><span class="sxs-lookup"><span data-stu-id="f5f4e-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="f5f4e-114">Después de establecer este valor en **Variant \_ true** en el codificador de audio, los tipos de salida que se recuperan mediante el método [**IMediaObject:: GETOUTPUTTYPE**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) son tipos de VBR.</span><span class="sxs-lookup"><span data-stu-id="f5f4e-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f4e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5f4e-115">Requirements</span></span>



| <span data-ttu-id="f5f4e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f4e-116">Requirement</span></span> | <span data-ttu-id="f5f4e-117">Value</span><span class="sxs-lookup"><span data-stu-id="f5f4e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f4e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5f4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f4e-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f5f4e-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5f4e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5f4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f4e-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5f4e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5f4e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5f4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f4e-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f4e-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f4e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5f4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f4e-125">**MFPKEY \_ restricción de \_ VBRQUALITY enumerada \_**</span><span class="sxs-lookup"><span data-stu-id="f5f4e-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="f5f4e-126">**MFPKEY \_ deseado \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="f5f4e-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="f5f4e-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5f4e-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
