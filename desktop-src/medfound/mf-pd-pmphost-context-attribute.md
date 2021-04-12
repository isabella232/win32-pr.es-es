---
description: Contiene un puntero al objeto de proxy para el descriptor de presentación de aplicaciones.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: MF_PD_PMPHOST_CONTEXT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423972"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="5262c-103">\_Atributo de contexto MF PD \_ PMPHOST \_</span><span class="sxs-lookup"><span data-stu-id="5262c-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="5262c-104">Contiene un puntero al objeto de proxy para el descriptor de presentación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5262c-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="5262c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5262c-105">Data type</span></span>

<span data-ttu-id="5262c-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="5262c-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="5262c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5262c-107">Remarks</span></span>

<span data-ttu-id="5262c-108">El host de la ruta de acceso a medios protegidos (PMP) usa este atributo para almacenar el descriptor de presentación de la aplicación en el descriptor de presentación remoto.</span><span class="sxs-lookup"><span data-stu-id="5262c-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="5262c-109">El valor del atributo es un puntero a la interfaz [_ *IMFRemoteProxy* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .</span><span class="sxs-lookup"><span data-stu-id="5262c-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="5262c-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5262c-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5262c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5262c-111">Requirements</span></span>



| <span data-ttu-id="5262c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5262c-112">Requirement</span></span> | <span data-ttu-id="5262c-113">Value</span><span class="sxs-lookup"><span data-stu-id="5262c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5262c-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5262c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5262c-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5262c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5262c-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5262c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5262c-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5262c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5262c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5262c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5262c-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5262c-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5262c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5262c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5262c-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5262c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5262c-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="5262c-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="5262c-123">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="5262c-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="5262c-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5262c-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5262c-125">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="5262c-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




