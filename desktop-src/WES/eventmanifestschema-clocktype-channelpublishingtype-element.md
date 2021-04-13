---
title: Elemento clockType (ChannelPublishingType)
description: Resolución del reloj que se va a usar al registrar la marca de tiempo para cada evento.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- elemento clockType EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421998"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="b117a-104">Elemento clockType (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="b117a-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="b117a-105">Resolución del reloj que se va a usar al registrar la marca de tiempo para cada evento.</span><span class="sxs-lookup"><span data-stu-id="b117a-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b117a-106">El elemento **clockType** se define mediante el tipo complejo de [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b117a-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b117a-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b117a-107">Requirements</span></span>



| <span data-ttu-id="b117a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="b117a-108">Requirement</span></span> | <span data-ttu-id="b117a-109">Value</span><span class="sxs-lookup"><span data-stu-id="b117a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b117a-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b117a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b117a-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b117a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b117a-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b117a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b117a-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b117a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b117a-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="b117a-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="b117a-115">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="b117a-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="b117a-116">**publicación (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="b117a-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





