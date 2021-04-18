---
description: Especifica si un objeto subyacente de nodos topología es un Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: MF_TOPONODE_DECRYPTOR atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707171"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="489d2-103">\_Atributo de \_ descifrador MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="489d2-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="489d2-104">Especifica si el objeto subyacente de un nodo topología es un Decrypter.</span><span class="sxs-lookup"><span data-stu-id="489d2-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="489d2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="489d2-105">Data type</span></span>

<span data-ttu-id="489d2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="489d2-106">**UINT32**</span></span>

<span data-ttu-id="489d2-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="489d2-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="489d2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="489d2-108">Remarks</span></span>

<span data-ttu-id="489d2-109">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="489d2-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="489d2-110">Si el valor de este atributo es distinto de cero, el objeto subyacente del nodo es un Decrypter.</span><span class="sxs-lookup"><span data-stu-id="489d2-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="489d2-111">Normalmente, las aplicaciones no usan este atributo directamente.</span><span class="sxs-lookup"><span data-stu-id="489d2-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="489d2-112">La sesión multimedia establece este atributo cuando crea un nodo para un Decrypter, obtenido del método [**IMFInputTrustAuthority:: GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .</span><span class="sxs-lookup"><span data-stu-id="489d2-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="489d2-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="489d2-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="489d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="489d2-114">Requirements</span></span>



| <span data-ttu-id="489d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="489d2-115">Requirement</span></span> | <span data-ttu-id="489d2-116">Value</span><span class="sxs-lookup"><span data-stu-id="489d2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="489d2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="489d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="489d2-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="489d2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="489d2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="489d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="489d2-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="489d2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="489d2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="489d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="489d2-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="489d2-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489d2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="489d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489d2-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="489d2-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="489d2-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="489d2-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="489d2-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="489d2-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="489d2-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="489d2-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="489d2-128">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="489d2-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




