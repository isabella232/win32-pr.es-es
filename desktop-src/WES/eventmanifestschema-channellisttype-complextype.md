---
title: Tipo complejo de ChannelListType
description: Define una lista de canales en los que los proveedores pueden registrar eventos. | Tipo complejo de ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- ChannelListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698164"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="9996d-105">Tipo complejo de ChannelListType</span><span class="sxs-lookup"><span data-stu-id="9996d-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="9996d-106">Define una lista de canales en los que los proveedores pueden registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="9996d-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9996d-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9996d-107">Child elements</span></span>



| <span data-ttu-id="9996d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9996d-108">Element</span></span>                                                                            | <span data-ttu-id="9996d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9996d-109">Type</span></span>                                                                           | <span data-ttu-id="9996d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9996d-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9996d-111">**MiCanal**</span><span class="sxs-lookup"><span data-stu-id="9996d-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="9996d-112">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="9996d-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="9996d-113">Define un canal en el que se pueden registrar los eventos.</span><span class="sxs-lookup"><span data-stu-id="9996d-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="9996d-114">**importChannel**</span><span class="sxs-lookup"><span data-stu-id="9996d-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="9996d-115">**ImportChannelType**</span><span class="sxs-lookup"><span data-stu-id="9996d-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="9996d-116">Identifica un canal definido por otro proveedor o en un manifiesto que contiene una sección de metadatos.</span><span class="sxs-lookup"><span data-stu-id="9996d-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9996d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9996d-117">Remarks</span></span>

<span data-ttu-id="9996d-118">Puede especificar hasta ocho canales (cualquier combinación de canales o canales importados que defina).</span><span class="sxs-lookup"><span data-stu-id="9996d-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="9996d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9996d-119">Requirements</span></span>



| <span data-ttu-id="9996d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9996d-120">Requirement</span></span> | <span data-ttu-id="9996d-121">Value</span><span class="sxs-lookup"><span data-stu-id="9996d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9996d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9996d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9996d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9996d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9996d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9996d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9996d-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9996d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





