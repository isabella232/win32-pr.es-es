---
description: Especifica si están habilitados todos los protocolos de streaming.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: Propiedad MFNETSOURCE_ENABLE_STREAMING (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543195"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="e2b66-103">MFNETSOURCE \_ Habilitar la \_ propiedad de transmisión por secuencias</span><span class="sxs-lookup"><span data-stu-id="e2b66-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="e2b66-104">Especifica si están habilitados todos los protocolos de streaming.</span><span class="sxs-lookup"><span data-stu-id="e2b66-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="e2b66-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e2b66-105">Data type</span></span>

<span data-ttu-id="e2b66-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e2b66-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e2b66-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e2b66-107">PROPVARIANT member</span></span>

<span data-ttu-id="e2b66-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="e2b66-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="e2b66-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e2b66-109">VT\_I4</span></span>

<span data-ttu-id="e2b66-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e2b66-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e2b66-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2b66-111">Remarks</span></span>

<span data-ttu-id="e2b66-112">La constante **MFNETSOURCE \_ enable \_ streaming** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2b66-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="e2b66-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="e2b66-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e2b66-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="e2b66-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e2b66-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e2b66-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2b66-116">Requirements</span></span>



| <span data-ttu-id="e2b66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b66-117">Requirement</span></span> | <span data-ttu-id="e2b66-118">Value</span><span class="sxs-lookup"><span data-stu-id="e2b66-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b66-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2b66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b66-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2b66-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2b66-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2b66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b66-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2b66-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2b66-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2b66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b66-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b66-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b66-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2b66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b66-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2b66-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e2b66-127">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2b66-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e2b66-128">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="e2b66-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




