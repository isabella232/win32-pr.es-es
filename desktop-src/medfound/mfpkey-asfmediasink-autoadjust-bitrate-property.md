---
description: Especifica si el receptor de medios ASF ajusta automáticamente la velocidad de bits.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Propiedad MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697974"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="8e1f4-103">\_ \_ Propiedad autoajuste de \_ velocidad de bits de MFPKEY ASFMEDIASINK</span><span class="sxs-lookup"><span data-stu-id="8e1f4-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="8e1f4-104">Especifica si el receptor de medios ASF ajusta automáticamente la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="8e1f4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8e1f4-105">Data type</span></span>

<span data-ttu-id="8e1f4-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8e1f4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8e1f4-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8e1f4-107">PROPVARIANT member</span></span>

<span data-ttu-id="8e1f4-108">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="8e1f4-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="8e1f4-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="8e1f4-109">VT\_BOOL</span></span>

<span data-ttu-id="8e1f4-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="8e1f4-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8e1f4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e1f4-111">Remarks</span></span>

<span data-ttu-id="8e1f4-112">Si el valor de esta propiedad es VARIANT \_ true, el receptor de medios ASF ajusta automáticamente la velocidad de bits del contenido ASF en respuesta a las características de las secuencias que se multiplexan.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="8e1f4-113">Esta propiedad afecta a cómo se comporta el receptor de medios ASF cuando una secuencia desborda los parámetros del "cubo de fugas" del receptor:</span><span class="sxs-lookup"><span data-stu-id="8e1f4-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="8e1f4-114">Value</span><span class="sxs-lookup"><span data-stu-id="8e1f4-114">Value</span></span>              | <span data-ttu-id="8e1f4-115">Comportamiento</span><span class="sxs-lookup"><span data-stu-id="8e1f4-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1f4-116">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="8e1f4-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="8e1f4-117">El receptor de medios ASF ajusta automáticamente la velocidad de bits del contenido ASF en respuesta a las características de las secuencias que se multiplexan.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="8e1f4-118">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="8e1f4-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="8e1f4-119">El receptor de medios ASF usa el valor de velocidad de bits de transmisión proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="8e1f4-120">El valor predeterminado es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="8e1f4-121">Establezca esta propiedad al configurar el receptor de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="8e1f4-122">El uso depende de la función a la que llame para crear el receptor de medios ASF:</span><span class="sxs-lookup"><span data-stu-id="8e1f4-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="8e1f4-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Consulte el puntero [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="8e1f4-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="8e1f4-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el parámetro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="8e1f4-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="8e1f4-125">Establecer esta propiedad en VARIANT \_ true hace que el receptor de medios ASF establezca la marca de **\_ velocidad de \_ \_ bits de autoajuste del multiplexor de MFASF** en el multiplexor ASF.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="8e1f4-126">Vea [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span><span class="sxs-lookup"><span data-stu-id="8e1f4-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="8e1f4-127">Para obtener más información sobre el concepto de depósito con fugas, vea el tema sobre el modelo de búfer de depósitos con fugas en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1f4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1f4-128">Requirements</span></span>



| <span data-ttu-id="8e1f4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1f4-129">Requirement</span></span> | <span data-ttu-id="8e1f4-130">Value</span><span class="sxs-lookup"><span data-stu-id="8e1f4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1f4-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1f4-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e1f4-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e1f4-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1f4-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e1f4-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e1f4-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e1f4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e1f4-136"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1f4-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1f4-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e1f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1f4-138">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e1f4-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8e1f4-139">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="8e1f4-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="8e1f4-140">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="8e1f4-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




