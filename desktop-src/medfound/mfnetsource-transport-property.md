---
description: Especifica el protocolo de transporte utilizado por el origen de red.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: Propiedad MFNETSOURCE_TRANSPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908244"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="9fd8c-103">\_Propiedad de transporte MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="9fd8c-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="9fd8c-104">Especifica el protocolo de transporte utilizado por el origen de red.</span><span class="sxs-lookup"><span data-stu-id="9fd8c-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="9fd8c-105">El valor de esta propiedad es un miembro de la enumeración de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="9fd8c-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="9fd8c-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9fd8c-106">Data type</span></span>

<span data-ttu-id="9fd8c-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9fd8c-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9fd8c-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9fd8c-108">PROPVARIANT member</span></span>

<span data-ttu-id="9fd8c-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="9fd8c-109">**LONG**</span></span>

<span data-ttu-id="9fd8c-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9fd8c-110">VT\_I4</span></span>

<span data-ttu-id="9fd8c-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="9fd8c-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9fd8c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fd8c-112">Remarks</span></span>

<span data-ttu-id="9fd8c-113">El **\_ transporte constante MFNETSOURCE** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9fd8c-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="9fd8c-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="9fd8c-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="9fd8c-115">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9fd8c-115">This property is read-only.</span></span> <span data-ttu-id="9fd8c-116">Para recuperar esta propiedad, consulte el origen de red para la interfaz **IPropertyStore** y llame a **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="9fd8c-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd8c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fd8c-117">Requirements</span></span>



| <span data-ttu-id="9fd8c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd8c-118">Requirement</span></span> | <span data-ttu-id="9fd8c-119">Value</span><span class="sxs-lookup"><span data-stu-id="9fd8c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd8c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fd8c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd8c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fd8c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9fd8c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fd8c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd8c-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fd8c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9fd8c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fd8c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd8c-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd8c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd8c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fd8c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd8c-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fd8c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9fd8c-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fd8c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="9fd8c-129">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="9fd8c-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




