---
description: El valor de la primera parte del campo &\# 0034; CS (User-Agent) &\# 0034; que usa el origen de red para el registro.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: Propiedad MFNETSOURCE_BROWSERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543206"
---
# <a name="mfnetsource_browseruseragent-property"></a><span data-ttu-id="6324d-103">\_Propiedad BROWSERUSERAGENT de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="6324d-103">MFNETSOURCE\_BROWSERUSERAGENT property</span></span>

<span data-ttu-id="6324d-104">El valor de la primera parte del campo "CS (User-Agent)" que utiliza el origen de red para el registro.</span><span class="sxs-lookup"><span data-stu-id="6324d-104">The value of the first portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="6324d-105">Las aplicaciones pueden establecer esta propiedad en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="6324d-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="6324d-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6324d-106">Data type</span></span>

<span data-ttu-id="6324d-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6324d-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6324d-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6324d-108">PROPVARIANT member</span></span>

<span data-ttu-id="6324d-109">Cadena de caracteres anchos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="6324d-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="6324d-110">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="6324d-110">VT\_LPWSTR</span></span>

<span data-ttu-id="6324d-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="6324d-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6324d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6324d-112">Remarks</span></span>

<span data-ttu-id="6324d-113">La constante **MFNETSOURCE \_ BROWSERUSERAGENT** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6324d-113">The constant **MFNETSOURCE\_BROWSERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="6324d-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="6324d-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6324d-115">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="6324d-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="6324d-116">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="6324d-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="6324d-117">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6324d-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6324d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6324d-118">Requirements</span></span>



| <span data-ttu-id="6324d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6324d-119">Requirement</span></span> | <span data-ttu-id="6324d-120">Value</span><span class="sxs-lookup"><span data-stu-id="6324d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6324d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6324d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6324d-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6324d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6324d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6324d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6324d-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6324d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6324d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6324d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6324d-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6324d-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6324d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6324d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6324d-128">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="6324d-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="6324d-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6324d-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6324d-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6324d-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6324d-131">**MFNETSOURCE \_ PLAYERUSERAGENT**</span><span class="sxs-lookup"><span data-stu-id="6324d-131">**MFNETSOURCE\_PLAYERUSERAGENT**</span></span>](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




