---
description: Especifica el ancho de banda del par de paquetes y el ancho de banda en tiempo de ejecución detectado por el origen de red.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Propiedad MFNETSOURCE_PPBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720470"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="ef789-103">\_Propiedad PPBANDWIDTH de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="ef789-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="ef789-104">Especifica el ancho de banda del par de paquetes y el ancho de banda en tiempo de ejecución detectado por el origen de red.</span><span class="sxs-lookup"><span data-stu-id="ef789-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="ef789-105">El valor de la propiedad es una matriz de dos valores:</span><span class="sxs-lookup"><span data-stu-id="ef789-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="ef789-106">Ancho de banda de pares de paquetes, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ef789-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="ef789-107">Ancho de banda en tiempo de ejecución, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ef789-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="ef789-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ef789-108">Data type</span></span>

<span data-ttu-id="ef789-109">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="ef789-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ef789-110">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="ef789-110">PROPVARIANT member</span></span>

<span data-ttu-id="ef789-111">Matriz de valores **ULong** (**caul**)</span><span class="sxs-lookup"><span data-stu-id="ef789-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="ef789-112">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ef789-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="ef789-113">**caul**</span><span class="sxs-lookup"><span data-stu-id="ef789-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="ef789-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef789-114">Remarks</span></span>

<span data-ttu-id="ef789-115">La constante **MFNETSOURCE \_ PPBANDWIDTH** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ef789-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="ef789-116">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="ef789-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="ef789-117">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ef789-117">This property is read-only.</span></span> <span data-ttu-id="ef789-118">Para recuperar esta propiedad, consulte el origen de red para la interfaz **IPropertyStore** y llame a **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="ef789-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef789-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef789-119">Requirements</span></span>



| <span data-ttu-id="ef789-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef789-120">Requirement</span></span> | <span data-ttu-id="ef789-121">Value</span><span class="sxs-lookup"><span data-stu-id="ef789-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef789-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef789-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef789-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef789-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ef789-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef789-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef789-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef789-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef789-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef789-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef789-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef789-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef789-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef789-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef789-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef789-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ef789-130">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="ef789-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="ef789-131">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef789-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




