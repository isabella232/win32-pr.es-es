---
description: Especifica si están habilitados todos los protocolos de descarga.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: Propiedad MFNETSOURCE_ENABLE_DOWNLOAD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1b57d8ab984f7c198d1c1b43455f2d0d5dda68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082241"
---
# <a name="mfnetsource_enable_download-property"></a><span data-ttu-id="61dc9-103">MFNETSOURCE \_ Habilitar la \_ propiedad de descarga</span><span class="sxs-lookup"><span data-stu-id="61dc9-103">MFNETSOURCE\_ENABLE\_DOWNLOAD property</span></span>

<span data-ttu-id="61dc9-104">Especifica si están habilitados todos los protocolos de descarga.</span><span class="sxs-lookup"><span data-stu-id="61dc9-104">Specifies whether all download protocols are enabled.</span></span>



<span data-ttu-id="61dc9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="61dc9-105">Data type</span></span>

<span data-ttu-id="61dc9-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="61dc9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="61dc9-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="61dc9-107">PROPVARIANT member</span></span>

<span data-ttu-id="61dc9-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="61dc9-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="61dc9-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="61dc9-109">VT\_I4</span></span>

<span data-ttu-id="61dc9-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="61dc9-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="61dc9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61dc9-111">Remarks</span></span>

<span data-ttu-id="61dc9-112">La constante **MFNETSOURCE \_ enable \_ download** define el GUID de esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="61dc9-112">The constant **MFNETSOURCE\_ENABLE\_DOWNLOAD** defines the GUID for this property key.</span></span> <span data-ttu-id="61dc9-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="61dc9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="61dc9-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="61dc9-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="61dc9-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="61dc9-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61dc9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61dc9-116">Requirements</span></span>



| <span data-ttu-id="61dc9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="61dc9-117">Requirement</span></span> | <span data-ttu-id="61dc9-118">Value</span><span class="sxs-lookup"><span data-stu-id="61dc9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61dc9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61dc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="61dc9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="61dc9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="61dc9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61dc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="61dc9-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="61dc9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="61dc9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61dc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61dc9-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61dc9-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61dc9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="61dc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61dc9-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61dc9-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="61dc9-127">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61dc9-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="61dc9-128">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="61dc9-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




