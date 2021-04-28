---
description: 'Elemento profileList (LANPolicy): contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.'
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento profileList (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090783"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="de59d-103">elemento profileList (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="de59d-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="de59d-104">El elemento profileList (LANPolicy) contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.</span><span class="sxs-lookup"><span data-stu-id="de59d-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="de59d-105">Los perfiles deben basarse en el esquema de [ \_ perfil de LAN](lan-profileschema-schema.md), con un elemento raíz de [**LANProfile**](lan-profileschema-lanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="de59d-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="de59d-106">Se omitirán los perfiles basados en cualquier otro esquema.</span><span class="sxs-lookup"><span data-stu-id="de59d-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="de59d-107">Cuando [**enableAutoConfig se**](lan-policyschema-enableautoconfig-globalflags-element.md) establece en FALSE, este elemento no debe estar presente en un perfil de directiva LAN.</span><span class="sxs-lookup"><span data-stu-id="de59d-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="de59d-108">Cuando **enableAutoConfig se** establece en TRUE, se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de59d-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="de59d-109">El **elemento profileList** se define mediante el [**elemento LANPolicy.**](lan-policyschema-lanpolicy-element.md)</span><span class="sxs-lookup"><span data-stu-id="de59d-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="de59d-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de59d-110">Remarks</span></span>

<span data-ttu-id="de59d-111">Este elemento debe contener exactamente un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="de59d-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="de59d-112">Si se especifica más de un perfil en la directiva, solo se aplicará la primera red.</span><span class="sxs-lookup"><span data-stu-id="de59d-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="de59d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de59d-113">Requirements</span></span>



| <span data-ttu-id="de59d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de59d-114">Requirement</span></span> | <span data-ttu-id="de59d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="de59d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de59d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de59d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de59d-117">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="de59d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de59d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de59d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de59d-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="de59d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de59d-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de59d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="de59d-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="de59d-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="de59d-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="de59d-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="de59d-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="de59d-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="de59d-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="de59d-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




