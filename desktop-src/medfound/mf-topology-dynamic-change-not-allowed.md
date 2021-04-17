---
description: Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497356"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="44b68-103">\_Atributo de cambio dinámico de topología MF \_ \_ \_ no \_ permitido</span><span class="sxs-lookup"><span data-stu-id="44b68-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="44b68-104">Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="44b68-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="44b68-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="44b68-105">Data type</span></span>

<span data-ttu-id="44b68-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="44b68-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="44b68-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="44b68-107">Get/set</span></span>

<span data-ttu-id="44b68-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="44b68-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="44b68-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="44b68-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="44b68-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="44b68-110">Applies to</span></span>

[<span data-ttu-id="44b68-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="44b68-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="44b68-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44b68-112">Remarks</span></span>

<span data-ttu-id="44b68-113">Este atributo controla el modo en que la sesión multimedia responde si el formato de una secuencia cambia durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="44b68-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="44b68-114">Si el formato cambia y el \_ atributo el cambio dinámico de la topología MF \_ \_ \_ no \_ se permite es **false**, la sesión multimedia podría insertar nuevos nodos en la topología para que coincida con el nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="44b68-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="44b68-115">Por ejemplo, si cambia el tamaño del vídeo, es posible que la sesión multimedia agregue una Media Foundation transformación (MFT) que cambie el tamaño del vídeo.</span><span class="sxs-lookup"><span data-stu-id="44b68-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="44b68-116">De lo contrario, si el atributo es **true**, la sesión multimedia no modificará la topología.</span><span class="sxs-lookup"><span data-stu-id="44b68-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="44b68-117">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="44b68-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="44b68-118">El valor recomendado es **false**.</span><span class="sxs-lookup"><span data-stu-id="44b68-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="44b68-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="44b68-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="44b68-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44b68-120">Requirements</span></span>



| <span data-ttu-id="44b68-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b68-121">Requirement</span></span> | <span data-ttu-id="44b68-122">Value</span><span class="sxs-lookup"><span data-stu-id="44b68-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44b68-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44b68-123">Minimum supported client</span></span><br/> | <span data-ttu-id="44b68-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="44b68-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44b68-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44b68-125">Minimum supported server</span></span><br/> | <span data-ttu-id="44b68-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44b68-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="44b68-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44b68-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="44b68-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b68-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b68-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="44b68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b68-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44b68-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44b68-131">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="44b68-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




