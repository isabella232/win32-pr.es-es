---
description: Hora de envío base del receptor de medios ASF, en milisegundos.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: Propiedad MFPKEY_ASFMEDIASINK_BASE_SENDTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697973"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="82bcf-103">\_ \_ Propiedad SENDTIME base de MFPKEY ASFMEDIASINK \_</span><span class="sxs-lookup"><span data-stu-id="82bcf-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="82bcf-104">Hora de envío base del receptor de medios ASF, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="82bcf-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="82bcf-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="82bcf-105">Data type</span></span>

<span data-ttu-id="82bcf-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="82bcf-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="82bcf-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="82bcf-107">PROPVARIANT member</span></span>

<span data-ttu-id="82bcf-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="82bcf-108">**ULONG**</span></span>

<span data-ttu-id="82bcf-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="82bcf-109">VT\_UI4</span></span>

<span data-ttu-id="82bcf-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="82bcf-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="82bcf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82bcf-111">Remarks</span></span>

<span data-ttu-id="82bcf-112">La hora de envío es la hora a la que se envía un paquete ASF a través de la red.</span><span class="sxs-lookup"><span data-stu-id="82bcf-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="82bcf-113">No se corresponde directamente con el tiempo de presentación de los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="82bcf-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="82bcf-114">Puede utilizar esta propiedad para configurar el receptor de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="82bcf-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="82bcf-115">El uso depende de la función a la que llame para crear el receptor de medios ASF:</span><span class="sxs-lookup"><span data-stu-id="82bcf-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="82bcf-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Consulte el puntero [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="82bcf-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="82bcf-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el parámetro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="82bcf-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="82bcf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82bcf-118">Requirements</span></span>



| <span data-ttu-id="82bcf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="82bcf-119">Requirement</span></span> | <span data-ttu-id="82bcf-120">Value</span><span class="sxs-lookup"><span data-stu-id="82bcf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82bcf-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82bcf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82bcf-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82bcf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82bcf-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82bcf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82bcf-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="82bcf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="82bcf-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82bcf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="82bcf-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82bcf-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82bcf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="82bcf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bcf-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82bcf-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




