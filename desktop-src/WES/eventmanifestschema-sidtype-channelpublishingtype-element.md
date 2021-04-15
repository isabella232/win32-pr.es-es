---
title: Elemento SID (ChannelPublishingType)
description: Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- elemento SID EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695958"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="5fb88-104">Elemento SID (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="5fb88-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="5fb88-105">Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal.</span><span class="sxs-lookup"><span data-stu-id="5fb88-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="5fb88-106">El elemento **SID** se define mediante el tipo complejo de [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5fb88-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb88-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fb88-107">Requirements</span></span>



| <span data-ttu-id="5fb88-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fb88-108">Requirement</span></span> | <span data-ttu-id="5fb88-109">Value</span><span class="sxs-lookup"><span data-stu-id="5fb88-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5fb88-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fb88-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5fb88-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5fb88-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5fb88-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fb88-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5fb88-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5fb88-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fb88-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fb88-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fb88-115">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="5fb88-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="5fb88-116">**publicación (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="5fb88-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





