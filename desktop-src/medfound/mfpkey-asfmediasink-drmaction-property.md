---
description: Especifica cómo el receptor de medios ASF debe aplicar DRM de Windows Media.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Propiedad MFPKEY_ASFMEDIASINK_DRMACTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820327"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="3004e-103">\_ \_ Propiedad DRMACTION de MFPKEY ASFMEDIASINK</span><span class="sxs-lookup"><span data-stu-id="3004e-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="3004e-104">Especifica cómo el receptor de medios ASF debe aplicar DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3004e-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="3004e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3004e-105">Data type</span></span>

<span data-ttu-id="3004e-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="3004e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3004e-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3004e-107">PROPVARIANT member</span></span>

<span data-ttu-id="3004e-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="3004e-108">**ULONG**</span></span>

<span data-ttu-id="3004e-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="3004e-109">VT\_UI4</span></span>

<span data-ttu-id="3004e-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="3004e-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3004e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3004e-111">Remarks</span></span>

<span data-ttu-id="3004e-112">El valor de esta propiedad es un miembro de la enumeración [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .</span><span class="sxs-lookup"><span data-stu-id="3004e-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="3004e-113">Puede utilizar este atributo para configurar el receptor de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="3004e-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="3004e-114">El uso depende de la función a la que llame para crear el receptor de medios ASF:</span><span class="sxs-lookup"><span data-stu-id="3004e-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="3004e-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Consulte el puntero [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="3004e-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="3004e-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el parámetro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="3004e-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3004e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3004e-117">Requirements</span></span>



| <span data-ttu-id="3004e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3004e-118">Requirement</span></span> | <span data-ttu-id="3004e-119">Value</span><span class="sxs-lookup"><span data-stu-id="3004e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3004e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3004e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3004e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3004e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3004e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3004e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3004e-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3004e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3004e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3004e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3004e-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3004e-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3004e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3004e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3004e-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3004e-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
