---
description: Especifica el ancho de banda del vínculo para el origen de red, en bits por segundo.
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: Propiedad MFNETSOURCE_CONNECTIONBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b852b3eb8dbfe5d3abc85e2223e868c5be708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543203"
---
# <a name="mfnetsource_connectionbandwidth-property"></a><span data-ttu-id="31b60-103">\_Propiedad CONNECTIONBANDWIDTH de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="31b60-103">MFNETSOURCE\_CONNECTIONBANDWIDTH property</span></span>

<span data-ttu-id="31b60-104">Especifica el ancho de banda del vínculo para el origen de red, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="31b60-104">Specifies the link bandwidth for the network source, in bits per second.</span></span>



<span data-ttu-id="31b60-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="31b60-105">Data type</span></span>

<span data-ttu-id="31b60-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="31b60-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="31b60-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="31b60-107">PROPVARIANT member</span></span>

<span data-ttu-id="31b60-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="31b60-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="31b60-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="31b60-109">VT\_I4</span></span>

<span data-ttu-id="31b60-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="31b60-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="31b60-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31b60-111">Remarks</span></span>

<span data-ttu-id="31b60-112">La constante **MFNETSOURCE \_ CONNECTIONBANDWIDTH** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="31b60-112">The constant **MFNETSOURCE\_CONNECTIONBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="31b60-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="31b60-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="31b60-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="31b60-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="31b60-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="31b60-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="31b60-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="31b60-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31b60-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31b60-117">Requirements</span></span>



| <span data-ttu-id="31b60-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b60-118">Requirement</span></span> | <span data-ttu-id="31b60-119">Value</span><span class="sxs-lookup"><span data-stu-id="31b60-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31b60-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31b60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31b60-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="31b60-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="31b60-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31b60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31b60-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31b60-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="31b60-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31b60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b60-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b60-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b60-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="31b60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b60-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31b60-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="31b60-128">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="31b60-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="31b60-129">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31b60-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




