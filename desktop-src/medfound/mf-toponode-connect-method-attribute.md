---
description: Especifica cómo el cargador de topología conecta este nodo de topología y si este nodo es opcional.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: MF_TOPONODE_CONNECT_METHOD atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278649"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="6204f-103">\_Atributo de \_ método de conexión MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="6204f-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="6204f-104">Especifica cómo el cargador de topología conecta este nodo de topología y si este nodo es opcional.</span><span class="sxs-lookup"><span data-stu-id="6204f-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="6204f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6204f-105">Data type</span></span>

<span data-ttu-id="6204f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6204f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6204f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6204f-107">Remarks</span></span>

<span data-ttu-id="6204f-108">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="6204f-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="6204f-109">El valor del atributo es una **operación OR bit a bit** de las marcas de la enumeración del [**\_ \_ método de conexión MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) .</span><span class="sxs-lookup"><span data-stu-id="6204f-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="6204f-110">Si no se establece este atributo, el valor predeterminado es **MF \_ Connect \_ permitir \_ descodificador**.</span><span class="sxs-lookup"><span data-stu-id="6204f-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="6204f-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6204f-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6204f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6204f-112">Requirements</span></span>



| <span data-ttu-id="6204f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6204f-113">Requirement</span></span> | <span data-ttu-id="6204f-114">Value</span><span class="sxs-lookup"><span data-stu-id="6204f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6204f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6204f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6204f-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6204f-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6204f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6204f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6204f-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6204f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6204f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6204f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6204f-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6204f-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6204f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6204f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6204f-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6204f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6204f-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6204f-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6204f-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6204f-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6204f-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="6204f-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="6204f-126">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="6204f-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




