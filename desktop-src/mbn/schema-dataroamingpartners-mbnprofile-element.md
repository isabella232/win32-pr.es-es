---
description: Especifica la lista de proveedores de red preferidos en el momento de la itinerancia.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Elemento DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659817"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="2229a-103">Elemento DataRoamingPartners (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="2229a-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="2229a-104">El elemento **DataRoamingPartners (MBNProfile)** especifica la lista de proveedores de red preferidos en el momento de la itinerancia.</span><span class="sxs-lookup"><span data-stu-id="2229a-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="2229a-105">El servicio de banda ancha móvil usa este elemento para seleccionar la red preferida que se proporciona en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="2229a-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="2229a-106">El elemento tiene el siguiente elemento secundario que se debe definir al menos una vez, pero se puede definir varias veces.</span><span class="sxs-lookup"><span data-stu-id="2229a-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="2229a-107">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="2229a-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="2229a-108">Este elemento puede tener un máximo de una repetición.</span><span class="sxs-lookup"><span data-stu-id="2229a-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="2229a-109">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="2229a-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2229a-110">El elemento **DataRoamingPartners** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2229a-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2229a-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2229a-111">Child elements</span></span>



| <span data-ttu-id="2229a-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="2229a-112">Element</span></span>                                                         | <span data-ttu-id="2229a-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="2229a-113">Type</span></span>                                                    | <span data-ttu-id="2229a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2229a-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="2229a-115">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="2229a-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="2229a-116">**providerType**</span><span class="sxs-lookup"><span data-stu-id="2229a-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="2229a-117">Nombre y identificador de proveedor de una red de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="2229a-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2229a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2229a-118">Requirements</span></span>



| <span data-ttu-id="2229a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2229a-119">Requirement</span></span> | <span data-ttu-id="2229a-120">Value</span><span class="sxs-lookup"><span data-stu-id="2229a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2229a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2229a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2229a-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="2229a-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2229a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2229a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2229a-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2229a-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="2229a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2229a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2229a-126">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="2229a-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2229a-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="2229a-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="2229a-128">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="2229a-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2229a-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="2229a-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




