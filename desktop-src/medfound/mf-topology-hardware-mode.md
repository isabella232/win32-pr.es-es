---
description: Especifica si se van a cargar transformaciones de Microsoft Media Foundation basadas en hardware (MFTs) en la topología.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705401"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="6bcf6-103">Atributo de modo de hardware de \_ topología MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bcf6-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="6bcf6-104">Especifica si se van a cargar transformaciones de Microsoft Media Foundation basadas en hardware (MFTs) en la topología.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="6bcf6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6bcf6-105">Data type</span></span>

<span data-ttu-id="6bcf6-106">**[**MFTOPOLOGY \_ \_Modo de hardware**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="6bcf6-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6bcf6-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="6bcf6-107">Get/set</span></span>

<span data-ttu-id="6bcf6-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6bcf6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6bcf6-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6bcf6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6bcf6-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="6bcf6-110">Applies to</span></span>

[<span data-ttu-id="6bcf6-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="6bcf6-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="6bcf6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bcf6-112">Remarks</span></span>

<span data-ttu-id="6bcf6-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-113">This attribute is optional.</span></span> <span data-ttu-id="6bcf6-114">Establezca el atributo antes de resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="6bcf6-115">Value</span><span class="sxs-lookup"><span data-stu-id="6bcf6-115">Value</span></span>                                  | <span data-ttu-id="6bcf6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bcf6-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcf6-117">**MFTOPOLOGY \_ HWMODE \_ uso de \_ hardware**</span><span class="sxs-lookup"><span data-stu-id="6bcf6-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="6bcf6-118">El cargador de topología cargará los MFTs basados en hardware, como los descodificadores de hardware, si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="6bcf6-119">El cargador de topología recurre automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no puede conectarse por algún motivo.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="6bcf6-120">**MFTOPOLOGY \_ HWMODE \_ \_ solo software**</span><span class="sxs-lookup"><span data-stu-id="6bcf6-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="6bcf6-121">El cargador de topología solo cargará software MFTs, incluidos los descodificadores de software.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="6bcf6-122">El valor predeterminado es **MFTOPOLOGY \_ HWMODE \_ software \_ Only**, por compatibilidad con las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="6bcf6-123">El valor recomendado es **MFTOPOLOGY \_ HWMODE \_ use \_ hardware**.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="6bcf6-124">Si el cargador de topología inserta un MFT de hardware en la topología, establece el atributo de [ \_ atributo de \_ \_ dirección URL \_ de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en el nodo de la topología.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="6bcf6-125">Para comprobar si existe un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="6bcf6-126">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6bcf6-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bcf6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bcf6-127">Requirements</span></span>



| <span data-ttu-id="6bcf6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bcf6-128">Requirement</span></span> | <span data-ttu-id="6bcf6-129">Value</span><span class="sxs-lookup"><span data-stu-id="6bcf6-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcf6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bcf6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6bcf6-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bcf6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6bcf6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bcf6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6bcf6-133">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bcf6-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6bcf6-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bcf6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bcf6-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bcf6-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bcf6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bcf6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcf6-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6bcf6-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6bcf6-138">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="6bcf6-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




