---
description: Especifica si el transporte del Protocolo de datagramas de usuario (UDP) está habilitado en el origen de red.
ms.assetid: d46a59e6-8abc-484b-aecc-edf57ffff512
title: Propiedad MFNETSOURCE_ENABLE_UDP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326cbd375a7d7e22ea2afc121dd4af9086e60c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001260"
---
# <a name="mfnetsource_enable_udp-property"></a><span data-ttu-id="760aa-103">MFNETSOURCE \_ habilitar \_ propiedad de UDP</span><span class="sxs-lookup"><span data-stu-id="760aa-103">MFNETSOURCE\_ENABLE\_UDP property</span></span>

<span data-ttu-id="760aa-104">Especifica si el transporte del Protocolo de datagramas de usuario (UDP) está habilitado en el origen de red.</span><span class="sxs-lookup"><span data-stu-id="760aa-104">Specifies whether User Datagram Protocol (UDP) transport is enabled in the network source.</span></span>



<span data-ttu-id="760aa-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="760aa-105">Data type</span></span>

<span data-ttu-id="760aa-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="760aa-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="760aa-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="760aa-107">PROPVARIANT member</span></span>

<span data-ttu-id="760aa-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="760aa-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="760aa-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="760aa-109">VT\_I4</span></span>

<span data-ttu-id="760aa-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="760aa-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="760aa-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="760aa-111">Remarks</span></span>

<span data-ttu-id="760aa-112">La constante **MFNETSOURCE \_ enable \_ UDP** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="760aa-112">The constant **MFNETSOURCE\_ENABLE\_UDP** defines the GUID for this property key.</span></span> <span data-ttu-id="760aa-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="760aa-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="760aa-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="760aa-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="760aa-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="760aa-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="760aa-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="760aa-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="760aa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="760aa-117">Requirements</span></span>



| <span data-ttu-id="760aa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="760aa-118">Requirement</span></span> | <span data-ttu-id="760aa-119">Value</span><span class="sxs-lookup"><span data-stu-id="760aa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="760aa-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="760aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="760aa-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="760aa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="760aa-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="760aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="760aa-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="760aa-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="760aa-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="760aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="760aa-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="760aa-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="760aa-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="760aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760aa-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="760aa-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="760aa-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="760aa-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="760aa-129">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="760aa-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




