---
description: El número de veces que el origen de red ha intentado volver a conectarse a la red.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Propiedad MFNETSOURCE_AUTORECONNECTPROGRESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715367"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="c32ce-103">\_Propiedad AUTORECONNECTPROGRESS de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="c32ce-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="c32ce-104">El número de veces que el origen de red ha intentado volver a conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="c32ce-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="c32ce-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c32ce-105">Data type</span></span>

<span data-ttu-id="c32ce-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c32ce-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c32ce-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c32ce-107">PROPVARIANT member</span></span>

<span data-ttu-id="c32ce-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="c32ce-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="c32ce-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c32ce-109">VT\_I4</span></span>

<span data-ttu-id="c32ce-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="c32ce-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c32ce-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c32ce-111">Remarks</span></span>

<span data-ttu-id="c32ce-112">La constante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c32ce-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="c32ce-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="c32ce-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c32ce-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c32ce-114">This property is read-only.</span></span> <span data-ttu-id="c32ce-115">Para recuperar esta propiedad, consulte el origen de red para la interfaz **IPropertyStore** y llame a **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="c32ce-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c32ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c32ce-116">Requirements</span></span>



| <span data-ttu-id="c32ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32ce-117">Requirement</span></span> | <span data-ttu-id="c32ce-118">Value</span><span class="sxs-lookup"><span data-stu-id="c32ce-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c32ce-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c32ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c32ce-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c32ce-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c32ce-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c32ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c32ce-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c32ce-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c32ce-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c32ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c32ce-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c32ce-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32ce-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c32ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32ce-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c32ce-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c32ce-127">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="c32ce-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="c32ce-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c32ce-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




