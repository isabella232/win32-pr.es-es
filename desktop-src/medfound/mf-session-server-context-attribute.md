---
description: Permite que dos instancias de la sesión multimedia compartan el mismo proceso de la ruta de acceso a medios protegidos (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: MF_SESSION_SERVER_CONTEXT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156804"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="22d9f-103">\_Atributo de \_ contexto de servidor de sesión MF \_</span><span class="sxs-lookup"><span data-stu-id="22d9f-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="22d9f-104">Permite que dos instancias de la sesión multimedia compartan el mismo proceso de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="22d9f-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="22d9f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="22d9f-105">Data type</span></span>

<span data-ttu-id="22d9f-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="22d9f-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="22d9f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22d9f-107">Remarks</span></span>

<span data-ttu-id="22d9f-108">Utilice este atributo si desea crear la sesión de medios de PMP en un proceso de PMP existente.</span><span class="sxs-lookup"><span data-stu-id="22d9f-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="22d9f-109">El valor del atributo es un puntero a la interfaz [_ *IMFPMPServer* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="22d9f-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="22d9f-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="22d9f-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="22d9f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22d9f-111">Requirements</span></span>



| <span data-ttu-id="22d9f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="22d9f-112">Requirement</span></span> | <span data-ttu-id="22d9f-113">Value</span><span class="sxs-lookup"><span data-stu-id="22d9f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22d9f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22d9f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="22d9f-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22d9f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="22d9f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22d9f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="22d9f-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="22d9f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="22d9f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22d9f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="22d9f-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22d9f-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d9f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="22d9f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d9f-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="22d9f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="22d9f-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="22d9f-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="22d9f-123">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="22d9f-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="22d9f-124">Atributos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="22d9f-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




