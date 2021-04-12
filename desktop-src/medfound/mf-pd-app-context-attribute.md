---
description: Contiene un puntero al descriptor de presentación de la ruta de acceso a medios protegidos (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: MF_PD_APP_CONTEXT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278347"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="7a54d-103">Atributo de contexto de la \_ aplicación MF PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a54d-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="7a54d-104">Contiene un puntero al descriptor de presentación de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="7a54d-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="7a54d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7a54d-105">Data type</span></span>

<span data-ttu-id="7a54d-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="7a54d-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="7a54d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a54d-107">Remarks</span></span>

<span data-ttu-id="7a54d-108">El proxy de origen de medios, que se crea en el proceso de PMP, usa este atributo para almacenar el descriptor de presentación remoto en el descriptor de presentación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a54d-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="7a54d-109">El valor de este atributo es un puntero a la interfaz [_ *IMFPresentationDescriptor* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7a54d-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="7a54d-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7a54d-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a54d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a54d-111">Requirements</span></span>



| <span data-ttu-id="7a54d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a54d-112">Requirement</span></span> | <span data-ttu-id="7a54d-113">Value</span><span class="sxs-lookup"><span data-stu-id="7a54d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a54d-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a54d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7a54d-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7a54d-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7a54d-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a54d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7a54d-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a54d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a54d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a54d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a54d-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a54d-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a54d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a54d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a54d-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7a54d-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7a54d-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="7a54d-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="7a54d-123">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="7a54d-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="7a54d-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="7a54d-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




