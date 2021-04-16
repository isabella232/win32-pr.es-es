---
description: Especifica el protocolo de control utilizado por el origen de red.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: Propiedad MFNETSOURCE_PROTOCOL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541331"
---
# <a name="mfnetsource_protocol-property"></a><span data-ttu-id="d8522-103">\_Propiedad del protocolo MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="d8522-103">MFNETSOURCE\_PROTOCOL property</span></span>

<span data-ttu-id="d8522-104">Especifica el protocolo de control utilizado por el origen de red.</span><span class="sxs-lookup"><span data-stu-id="d8522-104">Specifies the control protocol used by the network source.</span></span> <span data-ttu-id="d8522-105">El valor de esta propiedad es un miembro de la enumeración del [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="d8522-105">The value of this property is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>



<span data-ttu-id="d8522-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d8522-106">Data type</span></span>

<span data-ttu-id="d8522-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d8522-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d8522-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d8522-108">PROPVARIANT member</span></span>

<span data-ttu-id="d8522-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="d8522-109">**LONG**</span></span>

<span data-ttu-id="d8522-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d8522-110">VT\_I4</span></span>

<span data-ttu-id="d8522-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="d8522-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d8522-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8522-112">Remarks</span></span>

<span data-ttu-id="d8522-113">El **\_ Protocolo MFNETSOURCE** constante define el GUID de esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d8522-113">The constant **MFNETSOURCE\_PROTOCOL** defines the GUID for this property key.</span></span> <span data-ttu-id="d8522-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="d8522-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d8522-115">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8522-115">This property is read-only.</span></span> <span data-ttu-id="d8522-116">Para recuperar esta propiedad, consulte el origen de red para la interfaz **IPropertyStore** y llame a **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="d8522-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8522-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8522-117">Requirements</span></span>



| <span data-ttu-id="d8522-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8522-118">Requirement</span></span> | <span data-ttu-id="d8522-119">Value</span><span class="sxs-lookup"><span data-stu-id="d8522-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8522-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8522-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8522-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d8522-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d8522-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8522-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8522-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8522-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d8522-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8522-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8522-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8522-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8522-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8522-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8522-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8522-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d8522-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8522-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="d8522-129">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="d8522-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




